---
title: Load, méthode-CPapFile
description: Une fois ces opérations réussies, l’interface IStorage obtenue est libérée. Cela ferme le fichier et indique que le fichier n’est pas ouvert pendant d’autres opérations du client. Il sera rouvert à la demande.
ms.assetid: 40f79adb-87f3-4b0e-9cfe-927a4bc9ada5
keywords:
- Load, méthode-CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe70be7241fe1e1eaeb779317e11a76fb479f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840889"
---
# <a name="load-method---cpapfile"></a><span data-ttu-id="c4e1a-106">Load, méthode-CPapFile</span><span class="sxs-lookup"><span data-stu-id="c4e1a-106">Load Method - CPapFile</span></span>

<span data-ttu-id="c4e1a-107">Une fois ces opérations réussies, l’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) obtenue est libérée.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-107">When these operations are successful, the obtained [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface is released.</span></span> <span data-ttu-id="c4e1a-108">Cela ferme le fichier et indique que le fichier n’est pas ouvert pendant d’autres opérations du client.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-108">This closes the file and indicates that the file is not held open during other client operations.</span></span> <span data-ttu-id="c4e1a-109">Il sera rouvert à la demande.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-109">It will be reopened when required.</span></span>

<span data-ttu-id="c4e1a-110">Cet exemple est la méthode de  **chargement** **CPapFile** à partir de Papfile. cpp.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-110">This example is the **CPapFile** **Load** method from Papfile.cpp.</span></span>


```C++
HRESULT CPapFile::Load(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If null file name passed then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Verify that the file is using the APPUTIL function.
    if (FileExist(pszFile))
    {
      // Use the COM service to verify that the file is actually a 
      // valid compound file.
      hr = StgIsStorageFile(pszFile);
      if (SUCCEEDED(hr))
      {
        // Use the COM service to open the compound file and
        // obtain an IStorage interface.
        hr = StgOpenStorage(
               pszFile,
               NULL,
               STGM_DIRECT | STGM_READ | STGM_SHARE_EXCLUSIVE,
               NULL,
               0,
               &m_pIStorage);
        if (SUCCEEDED(hr))
        {
          // An IStorage interface has been obtained. Now, request 
          // the COPaper object on the server side to load into  
          // itself the file's paper data using IStorage for our 
          // client-provided compound file.
          hr = m_pIPaper->Load(nLockKey, m_pIStorage);
          if (SUCCEEDED(hr))
          {
            // The paper data was loaded and a current compound
            // file name exists. Copy it for later use in a saves 
            // and loads.
            if (bNewFile)
              StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
          }

          // The Storage object is not required now. Do not hold the 
          // file open. Re-obtain the IStorage again later, when 
          // required (and thus re-open the compound file) for
          // another save or load.
          RELEASE_INTERFACE(m_pIStorage);
        }
      }
    }

    return (hr);
  }
  
```



### <a name="remarks"></a><span data-ttu-id="c4e1a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c4e1a-111">Remarks</span></span>

<span data-ttu-id="c4e1a-112">Comme avec la méthode [**Save**](save-method---cpapfile.md) , si la **valeur null** est transmise pour le paramètre *pszFileName* , le contenu stocké du membre **m \_ szCurFileName** est utilisé pour le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-112">As with the [**Save**](save-method---cpapfile.md) method, if **NULL** is passed for the *pszFileName* parameter, the stored content of member **m\_szCurFileName** is used for the file name.</span></span> <span data-ttu-id="c4e1a-113">Étant donné qu’un fichier existant peut être ouvert, la fonction APPUTIL **FileExist** est d’abord utilisée pour vérifier que le fichier existe.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-113">Because an existing file may be opened, the APPUTIL **FileExist** function is first used to verify that the file exists.</span></span> <span data-ttu-id="c4e1a-114">S’il existe, la fonction de service [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) standard est appelée pour vérifier le format du fichier afin de déterminer s’il s’agit d’un fichier composé valide.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-114">If it exists, the standard [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) service function is called to verify the format of the file to determine if it is a valid compound file.</span></span>

<span data-ttu-id="c4e1a-115">Si le fichier est valide, la fonction de service [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) standard est appelée pour ouvrir le fichier et retourner un pointeur vers une interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pour celui-ci.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-115">If the file is valid, the standard [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) service function is called to open the file and return a pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface for it.</span></span>

<span data-ttu-id="c4e1a-116">Le premier paramètre est le nom du fichier composé à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-116">The first parameter is the name of the compound file to open.</span></span> <span data-ttu-id="c4e1a-117">Comme avec l’appel [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) , cette chaîne est attendue dans le formulaire Unicode, et au cours de la compilation ANSI, une macro apputil est utilisée pour garantir que le paramètre ANSI est converti au format Unicode attendu.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-117">As with the [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) call, this string is expected in the Unicode form, and during ANSI compilation an APPUTIL macro is used to ensure the ANSI parameter is converted to the expected Unicode.</span></span>

<span data-ttu-id="c4e1a-118">Le deuxième paramètre de stockage prioritaire a la **valeur null**, ce qui signifie qu’il n’est pas utilisé dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-118">The second priority storage parameter is **NULL**, indicating it is not used in this sample.</span></span>

<span data-ttu-id="c4e1a-119">Les indicateurs du mode d’accès sont passés comme troisième paramètre pour spécifier les modes d’accès autorisés sur le fichier ouvert.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-119">The access mode flags are passed as the third parameter to specify what access modes are permitted on the opened file.</span></span> <span data-ttu-id="c4e1a-120">[**STGM \_ LIRE**](stgm-constants.md) ouvre le fichier avec l’autorisation lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-120">[**STGM\_READ**](stgm-constants.md) opens the file with read-only permission.</span></span> <span data-ttu-id="c4e1a-121">[**STGM \_ DIRECT**](stgm-constants.md) ouvre le fichier pour un accès direct, par opposition à l’accès transactionnel.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-121">[**STGM\_DIRECT**](stgm-constants.md) opens the file for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="c4e1a-122">[**STGM \_ PARTAGER \_ exclusive**](stgm-constants.md) ouvre le fichier pour une utilisation exclusive, non partagée par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-122">[**STGM\_SHARE\_EXCLUSIVE**](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="c4e1a-123">Quatrième élément d’exclusion de la **valeur null**, indiquant qu’il n’est pas utilisé dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-123">The fourth element exclusion parameter in **NULL**, indicating it is not used in this sample.</span></span>

<span data-ttu-id="c4e1a-124">Le cinquième paramètre est réservé pour une utilisation ultérieure et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-124">The fifth parameter is reserved for future use and must be zero.</span></span>

<span data-ttu-id="c4e1a-125">L’adresse de la variable pointeur **m \_ pIStorage** est passée comme sixième paramètre.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-125">The address of pointer variable **m\_pIStorage** is passed as the sixth parameter.</span></span> <span data-ttu-id="c4e1a-126">Lorsque l’appel est retourné avec succès, **m \_ pIStorage** contient un pointeur vers une interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="c4e1a-126">When the call successfully returns, **m\_pIStorage** contains a pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="c4e1a-127">Il s’agit de l’interface utilisée pour les opérations suivantes sur le fichier ouvert.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-127">This is the interface that is used for any subsequent operations on the opened file.</span></span>

<span data-ttu-id="c4e1a-128">Dans ce cas, l’opération importante consiste à faire en sorte que l’objet du codocument charge ses données de dessin à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-128">The important operation in this case is to have the COPaper object load its drawing data from the file.</span></span> <span data-ttu-id="c4e1a-129">Pour ce faire, vous utilisez la méthode **Load** de l’interface [**IPaper**](ipaper-methods.md) du codocument.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-129">This is done above using the **Load** method of COPaper's [**IPaper**](ipaper-methods.md) interface.</span></span> <span data-ttu-id="c4e1a-130">Si le « coarticle » parvient à charger ses données à l’aide de la [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) fournie, le nom du fichier composé est copié dans **m \_ szCurFileName** comme nouveau nom de fichier actuel.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-130">If COPaper succeeds in loading its data using the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) provided, the name of the compound file is copied into **m\_szCurFileName** as the new current file name.</span></span>

<span data-ttu-id="c4e1a-131">Lorsque ces opérations sont terminées avec succès, l’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) obtenue est libérée.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-131">When these operations are successfully completed, the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface that was obtained is released.</span></span> <span data-ttu-id="c4e1a-132">Cela ferme le fichier et signifie que le fichier n’est pas ouvert pendant d’autres opérations du client.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-132">This closes the file and means that the file is not held open during other client operations.</span></span> <span data-ttu-id="c4e1a-133">Il sera rouvert à la demande.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-133">It will be reopened when required.</span></span>

 

 




