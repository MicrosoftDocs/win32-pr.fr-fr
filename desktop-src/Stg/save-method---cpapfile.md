---
title: Save, méthode-CPapFile
description: Lorsque CPapFile est initialisé, il peut être utilisé pour enregistrer les données de dessin actuelles contenues dans l’objet du colivre.
ms.assetid: ceac32e5-7d47-480b-b1cd-5a17ac04dd0c
keywords:
- Save, méthode-CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3166b649f28cb1a8ddc37e9efc53465a6cb5d3e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940342"
---
# <a name="save-method---cpapfile"></a><span data-ttu-id="0f72c-104">Save, méthode-CPapFile</span><span class="sxs-lookup"><span data-stu-id="0f72c-104">Save Method - CPapFile</span></span>

<span data-ttu-id="0f72c-105">Lorsque **CPapFile** est initialisé, il peut être utilisé pour enregistrer les données de dessin actuelles contenues dans l’objet du colivre.</span><span class="sxs-lookup"><span data-stu-id="0f72c-105">When **CPapFile** is initialized, it can be used to save the current drawing data held in the COPaper object.</span></span>

## <a name="save-method-papfilecpp"></a><span data-ttu-id="0f72c-106">Méthode Save (PAPFILE. COTISATIONS</span><span class="sxs-lookup"><span data-stu-id="0f72c-106">Save Method (PAPFILE.CPP)</span></span>

<span data-ttu-id="0f72c-107">Cet exemple est la méthode **CPapFile** [**Save**](ipaper--save.md) de Papfile. cpp.</span><span class="sxs-lookup"><span data-stu-id="0f72c-107">This example is the **CPapFile** [**Save**](ipaper--save.md) method from Papfile.cpp.</span></span>


```C++
HRESULT CPapFile::Save(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If a null file name is passed, then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Use the COM service to reopen, or create, the compound file.
    hr = StgCreateDocfile(
        pszFile,
    STGM_CREATE | STGM_DIRECT | STGM_READWRITE | STGM_SHARE_EXCLUSIVE,
        0,
        &m_pIStorage);
    if (SUCCEEDED(hr))
    {
      // Obtained the IStorage. The compound file is open.
      // Instruct the COPaper object on the server side to save its
      // paper data into the compound file using the IStorage of our
      // client-provided compound file.
      hr = m_pIPaper->Save(nLockKey, m_pIStorage);
      if (SUCCEEDED(hr))
      {
        // The paper data was saved and obtained a new current 
        // compound file name. Copy it for later use in saves 
        // and loads.
        if (bNewFile)
          StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
      }

      // Storage complete. Do not hold the file open.
      // Re-obtain the IStorage again later (and thus re-open
      // the compound file) when required for another save or load.
      RELEASE_INTERFACE(m_pIStorage);
    }

    return (hr);
  }
  
```



<span data-ttu-id="0f72c-108">Si la **valeur null** est transmise pour le paramètre *pszFileName* , le contenu stocké du membre **m \_ szCurFileName** est utilisé pour le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="0f72c-108">If **NULL** is passed for the *pszFileName* parameter, the stored content of member **m\_szCurFileName** is used for the file name.</span></span> <span data-ttu-id="0f72c-109">Le *nLockKey* est la clé de verrouillage du client obtenue dans un appel précédent à la méthode de [**verrouillage**](ipaper-methods.md) du copapier dans l’interface **IPaper** .</span><span class="sxs-lookup"><span data-stu-id="0f72c-109">The *nLockKey* is the client lock key obtained in a previous call to the COPaper [**Lock**](ipaper-methods.md) method in the **IPaper** interface.</span></span>

<span data-ttu-id="0f72c-110">La fonction de service [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) standard com est appelée pour créer le fichier composé dans lequel les données de dessin seront enregistrées.</span><span class="sxs-lookup"><span data-stu-id="0f72c-110">The COM standard [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) service function is called to create the compound file in which the drawing data will be saved.</span></span>

<span data-ttu-id="0f72c-111">Le nom du fichier composé à créer est passé en tant que premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="0f72c-111">The name of the compound file to create is passed as the first parameter.</span></span> <span data-ttu-id="0f72c-112">Cela est attendu par [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) comme une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="0f72c-112">This is expected by [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) as a Unicode string.</span></span> <span data-ttu-id="0f72c-113">Quand **StoClien** est compilé pour des chaînes ANSI (Unicode n’est pas défini, qui est la valeur par défaut dans le Makefile), cet appel réduit en fait un appel à une fonction apputil interne, **\_ StgCreateDocFile**.</span><span class="sxs-lookup"><span data-stu-id="0f72c-113">When **StoClien** is compiled for ANSI strings (UNICODE is not defined, which is the default in the makefile), this call actually reduces to a call to an internal APPUTIL function, **A\_StgCreateDocfile**.</span></span> <span data-ttu-id="0f72c-114">Cette fonction effectue la conversion appropriée du paramètre ANSI pszFile en une version Unicode avant d’appeler **StgCreateDocFile**.</span><span class="sxs-lookup"><span data-stu-id="0f72c-114">This function performs the proper conversion of the ANSI pszFile parameter to a Unicode version before calling **StgCreateDocfile**.</span></span> <span data-ttu-id="0f72c-115">Pour plus d’informations, consultez apputil. h et Stoserve.htm.</span><span class="sxs-lookup"><span data-stu-id="0f72c-115">For more information, see Apputil.h and Stoserve.htm.</span></span>

<span data-ttu-id="0f72c-116">Les indicateurs du mode d’accès sont passés comme deuxième paramètre et déterminent les modes d’accès autorisés sur le nouveau fichier.</span><span class="sxs-lookup"><span data-stu-id="0f72c-116">The access mode flags are passed as the second parameter and determine which access modes are permitted on the new file.</span></span> <span data-ttu-id="0f72c-117">L’indicateur [STGM \_ Create](stgm-constants.md) Access mode crée un nouveau fichier composé ou remplace un fichier existant du même nom.</span><span class="sxs-lookup"><span data-stu-id="0f72c-117">The [STGM\_CREATE](stgm-constants.md) access mode flag creates a new compound file or overwrites an existing one of the same name.</span></span> <span data-ttu-id="0f72c-118">[STGM \_ READWRITE](stgm-constants.md) ouvre le fichier avec l’autorisation de lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="0f72c-118">[STGM\_READWRITE](stgm-constants.md) opens the file with read-write permission.</span></span> <span data-ttu-id="0f72c-119">[STGM \_ DIRECT](stgm-constants.md) ouvre le fichier pour un accès direct, par opposition à l’accès transactionnel.</span><span class="sxs-lookup"><span data-stu-id="0f72c-119">[STGM\_DIRECT](stgm-constants.md) opens the file for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="0f72c-120">[STGM \_ PARTAGER \_ exclusive](stgm-constants.md) ouvre le fichier pour une utilisation exclusive, non partagée par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="0f72c-120">[STGM\_SHARE\_EXCLUSIVE](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="0f72c-121">Le troisième paramètre est réservé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="0f72c-121">The third parameter is reserved and must be zero.</span></span>

<span data-ttu-id="0f72c-122">L’adresse de la variable pointeur **m \_ pIStorage** est transmise à [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) en tant que quatrième paramètre.</span><span class="sxs-lookup"><span data-stu-id="0f72c-122">The address of pointer variable **m\_pIStorage** is passed to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) as the fourth parameter.</span></span> <span data-ttu-id="0f72c-123">Lorsque l’appel est retourné avec succès, **m \_ pIStorage** contient un pointeur d’interface vers une interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="0f72c-123">When the call successfully returns, **m\_pIStorage** contains an interface pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="0f72c-124">Il s’agit de l’interface utilisée pour les opérations suivantes sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="0f72c-124">This is the interface that is used for any subsequent operations on the file.</span></span>

<span data-ttu-id="0f72c-125">Dans ce cas, l’opération importante consiste à faire en sorte que l’objet du colivre stocke ses données de dessin dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="0f72c-125">The important operation in this case is to have the COPaper object store its drawing data in the file.</span></span> <span data-ttu-id="0f72c-126">Pour ce faire, vous utilisez la méthode [**Save**](ipaper--save.md) de l’interface [**IPaper**](ipaper-methods.md) du colivre.</span><span class="sxs-lookup"><span data-stu-id="0f72c-126">This is done above using the [**Save**](ipaper--save.md) method of the COPaper [**IPaper**](ipaper-methods.md) interface.</span></span> <span data-ttu-id="0f72c-127">Si l’enregistrement de ses données dans l’objet de stockage fourni par le colivre fonctionne, le nom du fichier composé est copié dans **m \_ szCurFileName** comme nouveau nom de fichier actuel.</span><span class="sxs-lookup"><span data-stu-id="0f72c-127">If COPaper succeeds in saving its data in the storage object provided, the name of the compound file is copied into **m\_szCurFileName** as the new current file name.</span></span>

 

 




