---
title: IPaper enregistrer
description: Le principal objectif de cet exemple de code est de savoir comment le colivre peut charger et enregistrer ses données papier dans des fichiers composés. Les implémentations de la méthode IPaper, Load et Save sont décrites en détail.
ms.assetid: 62154658-ff47-425f-94da-ee2806de5318
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ea49f194e64ab3f0cfd78569b1e6ff9ddee577
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106545733"
---
# <a name="ipapersave"></a><span data-ttu-id="484fe-104">IPaper :: enregistrer</span><span class="sxs-lookup"><span data-stu-id="484fe-104">IPaper::Save</span></span>

<span data-ttu-id="484fe-105">Le principal objectif de cet exemple de code est de savoir comment le colivre peut charger et enregistrer ses données papier dans des fichiers composés.</span><span class="sxs-lookup"><span data-stu-id="484fe-105">The principal focus in this sample code is how COPaper can load and save its paper data in compound files.</span></span> <span data-ttu-id="484fe-106">Les implémentations de la méthode [**IPaper**](ipaper-methods.md), [**Load**](ipaper--load.md)et **Save** sont décrites en détail.</span><span class="sxs-lookup"><span data-stu-id="484fe-106">The [**IPaper**](ipaper-methods.md), [**Load**](ipaper--load.md), and **Save** method implementations are discussed in detail.</span></span>

<span data-ttu-id="484fe-107">Voici la méthode **IPaper :: Save** de Paper. cpp.</span><span class="sxs-lookup"><span data-stu-id="484fe-107">The following is the **IPaper::Save** method from Paper.cpp.</span></span>


```C++
STDMETHODIMP COPaper::CImpIPaper::Save(
                 SHORT nLockKey,
                 IStorage* pIStorage)
  {
    HRESULT hr = E_FAIL;
    IStream* pIStream;
    ULONG ulToWrite, ulWritten;

    if (OwnThis())
    {
      if (m_bLocked && m_cLockKey == nLockKey && NULL != pIStorage)
      {
        // Use the COM service to mark this compound file as one 
        // that is handled by our server component, DllPaper.
        WriteClassStg(pIStorage, CLSID_DllPaper);

        // Use the COM Service to write user-readable clipboard 
        // format into the compound file.
        WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, 
                            TEXT(CLIPBDFMT_STR));

        // Create the stream to be used for the actual paper data.
        // Call it "PAPERDATA".
        hr = pIStorage->CreateStream(
               STREAM_PAPERDATA_USTR,
        STGM_CREATE | STGM_WRITE | STGM_DIRECT | STGM_SHARE_EXCLUSIVE,
               0,
               0,
               &pIStream);
        if (SUCCEEDED(hr))
        {
          // Obtained a stream. Write data to it.
          // First, write PAPER_PROPERTIES structure.
          m_PaperProperties.lInkArraySize = m_lInkDataEnd+1;
          m_PaperProperties.crWinColor = m_crWinColor;
          m_PaperProperties.WinRect.right = m_WinRect.right;
          m_PaperProperties.WinRect.bottom = m_WinRect.bottom;
          ulToWrite = sizeof(PAPER_PROPERTIES);
          hr = pIStream->Write(&m_Paper_Properties, ulToWrite, 
                               &ulWritten);
          if (SUCCEEDED(hr) && ulToWrite != ulWritten)
            hr = STG_E_CANTSAVE;
          if (SUCCEEDED(hr))
          {
            // Now, write the complete array of Ink Data.
            ulToWrite = m_PaperProperties.lInkArraySize * 
                                                     sizeof(INKDATA);
            hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
            if (SUCCEEDED(hr) && ulToWrite != ulWritten)
              hr = STG_E_CANTSAVE;
          }

          // Release the stream.
          pIStream->Release();
        }
      }

      UnOwnThis();
    }

    // Notify all other connected clients that Paper is now saved.
    if (SUCCEEDED(hr))
      m_pBackObj->NotifySinks(PAPER_EVENT_SAVED, 0, 0, 0, 0);

    return hr;
  }
```



<span data-ttu-id="484fe-108">Dans cette relation de client et de serveur, le colivre ne crée pas le fichier composé utilisé pour stocker les données de papier.</span><span class="sxs-lookup"><span data-stu-id="484fe-108">In this client and server relationship, COPaper does not create the compound file used to store paper data.</span></span> <span data-ttu-id="484fe-109">Pour les méthodes d' **enregistrement** et de [**chargement**](ipaper--load.md) , le client transmet un pointeur d’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pour un fichier composé existant.</span><span class="sxs-lookup"><span data-stu-id="484fe-109">For both the **Save** and [**Load**](ipaper--load.md) methods, the client passes an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface pointer for an existing compound file.</span></span> <span data-ttu-id="484fe-110">Il utilise ensuite l' **IStorage** pour écrire et lire des données dans ce fichier composé.</span><span class="sxs-lookup"><span data-stu-id="484fe-110">It then uses the **IStorage** to write and read data in that compound file.</span></span> <span data-ttu-id="484fe-111">Dans **IPaper :: Save** ci-dessus, plusieurs types de données sont stockés.</span><span class="sxs-lookup"><span data-stu-id="484fe-111">In **IPaper::Save** above, several types of data are stored.</span></span>

<span data-ttu-id="484fe-112">Le CLSID de DllPaper, CLSID \_ DllPaper, est sérialisé et stocké dans un flux spécial contrôlé par com au sein de l’objet de stockage appelé « \\ 001CompObj ».</span><span class="sxs-lookup"><span data-stu-id="484fe-112">The CLSID for DllPaper, CLSID\_DllPaper, is serialized and stored in a special COM-controlled stream within the storage object called "\\001CompObj".</span></span> <span data-ttu-id="484fe-113">La fonction de service [**WriteClassStg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) effectue ce stockage.</span><span class="sxs-lookup"><span data-stu-id="484fe-113">The [**WriteClassStg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) service function performs this storage.</span></span> <span data-ttu-id="484fe-114">Ces données de CLSID stockées peuvent être utilisées pour associer le contenu de stockage au composant DllPaper qui a été créé et peut l’interpréter.</span><span class="sxs-lookup"><span data-stu-id="484fe-114">This stored CLSID data can be used to associate the storage content with the DllPaper component that created and can interpret it.</span></span> <span data-ttu-id="484fe-115">Dans cet exemple, le stockage racine est passé par **StoClien** et, par conséquent, le fichier composé entier est associé au composant DllPaper.</span><span class="sxs-lookup"><span data-stu-id="484fe-115">In this sample, the root storage is passed by **StoClien**, and thus the entire compound file is associated with the DllPaper component.</span></span> <span data-ttu-id="484fe-116">Ces données CLSID peuvent être récupérées ultérieurement à l’aide d’un appel à la fonction de service [**ReadClassStg**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) .</span><span class="sxs-lookup"><span data-stu-id="484fe-116">This CLSID data can be retrieved later with a call to the [**ReadClassStg**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) service function.</span></span>

<span data-ttu-id="484fe-117">Étant donné que DllPaper traite les données modifiables, il est également approprié d’enregistrer un format de presse-papiers dans le stockage.</span><span class="sxs-lookup"><span data-stu-id="484fe-117">Because DllPaper deals with editable data, it is also appropriate to record a clipboard format in the storage.</span></span> <span data-ttu-id="484fe-118">La fonction de service [**WriteFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) est appelée pour stocker une désignation de format de presse-papiers et un nom lisible par l’utilisateur pour le format.</span><span class="sxs-lookup"><span data-stu-id="484fe-118">The [**WriteFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) service function is called to store both a clipboard format designation and a user-readable name for the format.</span></span> <span data-ttu-id="484fe-119">Le nom lisible par l’utilisateur est destiné à l’affichage de l’interface graphique dans les listes de sélection.</span><span class="sxs-lookup"><span data-stu-id="484fe-119">The user-readable name is meant for GUI display in selection lists.</span></span> <span data-ttu-id="484fe-120">Le nom passé ci-dessus utilise une macro, CLIPBDFMT \_ Str, qui est définie comme « DllPaper 1,0 » dans Paper. h.</span><span class="sxs-lookup"><span data-stu-id="484fe-120">The name passed above uses a macro, CLIPBDFMT\_STR, which is defined as "DllPaper 1.0" in Paper.h.</span></span> <span data-ttu-id="484fe-121">Ces données stockées dans le presse-papiers peuvent être récupérées ultérieurement à l’aide d’un appel à la fonction de service [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg).</span><span class="sxs-lookup"><span data-stu-id="484fe-121">This stored clipboard data can be retrieved later with a call to the service function [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg).</span></span> <span data-ttu-id="484fe-122">Cette fonction retourne une valeur de chaîne allouée à l’aide de l’allocateur de mémoire de tâche.</span><span class="sxs-lookup"><span data-stu-id="484fe-122">This function returns a string value that is allocated using the task memory allocator.</span></span> <span data-ttu-id="484fe-123">L’appelant est responsable de la libération de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="484fe-123">The caller is responsible for freeing the string.</span></span>

<span data-ttu-id="484fe-124">**Save** Next crée un flux dans le stockage pour les données du livre blanc.</span><span class="sxs-lookup"><span data-stu-id="484fe-124">**Save** next creates a stream in the storage for the COPaper paper data.</span></span> <span data-ttu-id="484fe-125">Le flux est appelé « PAPERDATA » et est passé à l’aide de la \_ macro PAPERDATA de flux \_ USTR.</span><span class="sxs-lookup"><span data-stu-id="484fe-125">The stream is called "PAPERDATA" and is passed using the STREAM\_PAPERDATA\_USTR macro.</span></span> <span data-ttu-id="484fe-126">La méthode [**IStorage :: CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) requiert que cette chaîne soit au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="484fe-126">The [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) method requires that this string be in Unicode.</span></span> <span data-ttu-id="484fe-127">Étant donné que la chaîne est fixe au moment de la compilation, la macro est définie en tant que Unicode dans Paper. h.</span><span class="sxs-lookup"><span data-stu-id="484fe-127">Because the string is fixed at compile time, the macro is defined as Unicode in Paper.h.</span></span>

``` syntax
#define STREAM_PAPERDATA_USTR L"PAPERDATA"
```

<span data-ttu-id="484fe-128">Le’L’avant la chaîne, indiquant LONG, y parvient.</span><span class="sxs-lookup"><span data-stu-id="484fe-128">The 'L' before the string, indicating LONG, achieves this.</span></span>

<span data-ttu-id="484fe-129">La méthode [**CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) crée et ouvre un flux dans le stockage spécifié.</span><span class="sxs-lookup"><span data-stu-id="484fe-129">The [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) method creates and opens a stream within the specified storage.</span></span> <span data-ttu-id="484fe-130">Un pointeur d’interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) pour le nouveau flux est passé dans une variable de pointeur d’interface appelant.</span><span class="sxs-lookup"><span data-stu-id="484fe-130">An [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface pointer for the new stream is passed in a caller interface pointer variable.</span></span> <span data-ttu-id="484fe-131">AddRef est appelé sur ce pointeur d’interface dans **CreateStream,**, et l’appelant doit libérer ce pointeur après l’avoir utilisé.</span><span class="sxs-lookup"><span data-stu-id="484fe-131">AddRef is called on this interface pointer within **CreateStream**, and the caller must release this pointer after using it.</span></span> <span data-ttu-id="484fe-132">La méthode **CreateStream,** reçoit de nombreux indicateurs de mode d’accès, comme suit.</span><span class="sxs-lookup"><span data-stu-id="484fe-132">The **CreateStream** method is passed numerous access mode flags, as follows.</span></span>

<span data-ttu-id="484fe-133">STGM \_ Create \| STGM \_ Write \| STGM \_ direct \| STGM \_ share \_ exclusive</span><span class="sxs-lookup"><span data-stu-id="484fe-133">STGM\_CREATE \| STGM\_WRITE \| STGM\_DIRECT \| STGM\_SHARE\_EXCLUSIVE</span></span>

<span data-ttu-id="484fe-134">[**STGM \_ CRÉER**](stgm-constants.md) crée un flux ou remplace un nouveau flux existant du même nom.</span><span class="sxs-lookup"><span data-stu-id="484fe-134">[**STGM\_CREATE**](stgm-constants.md) creates a new stream or overwrites an existing one of the same name.</span></span> <span data-ttu-id="484fe-135">[**STGM \_ WRITE**](stgm-constants.md) ouvre le flux avec l’autorisation Write.</span><span class="sxs-lookup"><span data-stu-id="484fe-135">[**STGM\_WRITE**](stgm-constants.md) opens the stream with write permission.</span></span> <span data-ttu-id="484fe-136">[**STGM \_ DIRECT**](stgm-constants.md) ouvre le flux pour l’accès direct, par opposition à l’accès transactionnel.</span><span class="sxs-lookup"><span data-stu-id="484fe-136">[**STGM\_DIRECT**](stgm-constants.md) opens the stream for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="484fe-137">[**STGM \_ PARTAGER \_ exclusive**](stgm-constants.md) ouvre le fichier pour une utilisation exclusive, non partagée par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="484fe-137">[**STGM\_SHARE\_EXCLUSIVE**](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="484fe-138">Une fois le flux PAPERDATA correctement créé, l’interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) est utilisée pour écrire dans le flux.</span><span class="sxs-lookup"><span data-stu-id="484fe-138">After the PAPERDATA stream is successfully created, the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface is used to write into the stream.</span></span> <span data-ttu-id="484fe-139">La méthode **IStream :: Write** est utilisée pour stocker le contenu de la structure de \_ Propriétés Paper.</span><span class="sxs-lookup"><span data-stu-id="484fe-139">The **IStream::Write** method is used to first store the content of the PAPER\_PROPERTIES structure.</span></span> <span data-ttu-id="484fe-140">Il s’agit essentiellement d’un en-tête de propriétés au début du flux.</span><span class="sxs-lookup"><span data-stu-id="484fe-140">This is essentially a properties header at the front of the stream.</span></span> <span data-ttu-id="484fe-141">Étant donné que le numéro de version est la première chose dans le fichier, il peut être lu indépendamment pour déterminer comment traiter les données qui suivent.</span><span class="sxs-lookup"><span data-stu-id="484fe-141">Because the version number is the first thing in the file, it can be read independently to determine how to deal with the data that follows.</span></span> <span data-ttu-id="484fe-142">Si la quantité de données réellement écrites n’est pas égale à la quantité demandée, la méthode Save est abandonnée et retourne STG \_ E \_ CANTSAVE.</span><span class="sxs-lookup"><span data-stu-id="484fe-142">If the amount of data actually written does not equal the amount requested, the Save method is aborted, and it returns STG\_E\_CANTSAVE.</span></span>

<span data-ttu-id="484fe-143">L’enregistrement de la totalité du tableau de données manuscrites dans le flux est simple.</span><span class="sxs-lookup"><span data-stu-id="484fe-143">Saving the entire array of ink data into the stream is simple.</span></span>


```C++
// Now write the complete array of Ink Data.
  ulToWrite = m_PaperProperties.lInkArraySize * sizeof(INKDATA);
  hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
  if (SUCCEEDED(hr) && ulToWrite != ulWritten)
    hr = STG_E_CANTSAVE;
```



<span data-ttu-id="484fe-144">Étant donné que la méthode [**IStream :: Write**](/windows/desktop/api/Objidl/nn-objidl-istream) opère sur un tableau d’octets, le nombre d’octets de données d’encre stockées dans le tableau est calculé et l’opération d’écriture commence au début du tableau.</span><span class="sxs-lookup"><span data-stu-id="484fe-144">Because the [**IStream::Write**](/windows/desktop/api/Objidl/nn-objidl-istream) method operates on a byte array, the number of bytes of stored ink data in the array is calculated and the write operation begins at the start of the array.</span></span> <span data-ttu-id="484fe-145">Si la quantité de données réellement écrites n’est pas égale à la quantité demandée, la méthode **Save** retourne STG \_ E \_ CANTSAVE.</span><span class="sxs-lookup"><span data-stu-id="484fe-145">If the amount of data actually written does not equal the amount requested, the **Save** method returns STG\_E\_CANTSAVE.</span></span>

<span data-ttu-id="484fe-146">Une fois le flux écrit, la méthode **IPaper :: Save** libère le pointeur [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) qu’il utilisait.</span><span class="sxs-lookup"><span data-stu-id="484fe-146">After the stream is written, the **IPaper::Save** method releases the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) pointer it was using.</span></span>

<span data-ttu-id="484fe-147">La méthode **Save** appelle également le client [**IPaperSink**](ipapersink-methods.md) (dans la méthode Internal NotifySinks) pour notifier au client que l’opération d’enregistrement est terminée.</span><span class="sxs-lookup"><span data-stu-id="484fe-147">The **Save** method also calls the client [**IPaperSink**](ipapersink-methods.md) (in the COPaper internal NotifySinks method) to notify the client that the save operation is complete.</span></span> <span data-ttu-id="484fe-148">À ce stade, la méthode **Save** retourne au client appelant, qui libère généralement le pointeur [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="484fe-148">At this point the **Save** method returns to the calling client, which will typically release the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pointer.</span></span>

 

 




