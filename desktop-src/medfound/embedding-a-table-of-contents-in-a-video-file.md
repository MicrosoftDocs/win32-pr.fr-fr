---
description: Incorporation d’une table des matières dans un fichier vidéo
ms.assetid: 1546388a-7868-4411-be20-34d28becbe76
title: Incorporation d’une table des matières dans un fichier vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8303082e454dde181de336ee0f64ff9d583312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111779"
---
# <a name="embedding-a-table-of-contents-in-a-video-file"></a><span data-ttu-id="a2337-103">Incorporation d’une table des matières dans un fichier vidéo</span><span class="sxs-lookup"><span data-stu-id="a2337-103">Embedding a Table of Contents in a Video File</span></span>

<span data-ttu-id="a2337-104">Cette rubrique montre comment créer une table des matières et l’incorporer dans un fichier vidéo.</span><span class="sxs-lookup"><span data-stu-id="a2337-104">This topic demonstrates how to create a table of contents (TOC) and embed it in a video file.</span></span> <span data-ttu-id="a2337-105">Pour que l’exemple de code reste concis, la table des matières est très simple ; il ne contient qu’une seule entrée, et l’entrée est remplie avec un minimum d’informations.</span><span class="sxs-lookup"><span data-stu-id="a2337-105">To keep the example code short, the table of contents is very simple; it contains only one entry, and the entry is populated with a minimum of information.</span></span>

<span data-ttu-id="a2337-106">Pour créer une table des matières et l’incorporer dans un fichier, vous devez créer les quatre objets suivants en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="a2337-106">To create a table of contents and embed it in a file, you must create the following four objects by calling **CoCreateInstance**.</span></span>

-   <span data-ttu-id="a2337-107">Entrée de la table des matières</span><span class="sxs-lookup"><span data-stu-id="a2337-107">TOC Entry</span></span>
-   <span data-ttu-id="a2337-108">Liste des entrées de la table des matières</span><span class="sxs-lookup"><span data-stu-id="a2337-108">TOC Entry List</span></span>
-   <span data-ttu-id="a2337-109">Table des matières</span><span class="sxs-lookup"><span data-stu-id="a2337-109">TOC</span></span>
-   <span data-ttu-id="a2337-110">Analyseur de table des matières</span><span class="sxs-lookup"><span data-stu-id="a2337-110">TOC Parser</span></span>

<span data-ttu-id="a2337-111">Les identificateurs de classe pour les objets sont fournis dans les [identificateurs de classe pour l’analyseur de table des matières](class-identifiers-for-toc-parser.md).</span><span class="sxs-lookup"><span data-stu-id="a2337-111">Class identifiers for the objects are given in [Class Identifiers for Table of Contents Parser](class-identifiers-for-toc-parser.md).</span></span>

<span data-ttu-id="a2337-112">Tout d’abord, renseignez l’entrée de la table des matières avec des informations qui décrivent une partie du fichier vidéo.</span><span class="sxs-lookup"><span data-stu-id="a2337-112">First populate the TOC entry with information that describes one portion of the video file.</span></span> <span data-ttu-id="a2337-113">Ajoutez l’entrée TOC à la liste entrée de la table des matières, puis ajoutez la liste des entrées de la table des matières à la table des matières.</span><span class="sxs-lookup"><span data-stu-id="a2337-113">Add the TOC entry to the TOC entry list, and then add the TOC entry list to the TOC.</span></span> <span data-ttu-id="a2337-114">Enfin, ajoutez la table des matières à l’analyseur de table des matières, qui fournit la fonctionnalité d’incorporation de la table des matières dans le fichier vidéo.</span><span class="sxs-lookup"><span data-stu-id="a2337-114">Finally, add the TOC to the TOC parser, which provides the functionality for embedding the TOC in the video file.</span></span> <span data-ttu-id="a2337-115">La liste suivante présente les étapes plus en détail.</span><span class="sxs-lookup"><span data-stu-id="a2337-115">The following list gives the steps in more detail.</span></span>

1.  <span data-ttu-id="a2337-116">Créez un objet entrée de la table des matières et obtenez une interface [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="a2337-116">Create a TOC Entry object and obtain an [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) interface on it.</span></span>
2.  <span data-ttu-id="a2337-117">Remplir une structure de [**\_ \_ descripteur d’entrée TOC**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) et la passer à [**ITocEntry :: SetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor).</span><span class="sxs-lookup"><span data-stu-id="a2337-117">Populate a [**TOC\_ENTRY\_DESCRIPTOR**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) structure and pass it to [**ITocEntry::SetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor).</span></span>
3.  <span data-ttu-id="a2337-118">Créez un objet de liste d’entrée de table des matières et obtenez une interface [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="a2337-118">Create a TOC Entry List object and obtain an [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) interface on it.</span></span>
4.  <span data-ttu-id="a2337-119">Ajoutez l’objet entrée de la table des matières que vous avez créé à l’étape 1 à l’objet de liste entrée de table des matières en appelant [**ITocEntryList :: AddEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex).</span><span class="sxs-lookup"><span data-stu-id="a2337-119">Add the TOC Entry object you created in step 1 to the TOC Entry List object by calling [**ITocEntryList::AddEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex).</span></span>
5.  <span data-ttu-id="a2337-120">Créez un objet TOC et obtenez une interface [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="a2337-120">Create a TOC object and obtain an [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) interface on it.</span></span>
6.  <span data-ttu-id="a2337-121">Ajoutez l’objet de liste d’entrées de la table des matières que vous avez créé à l’étape 3 à l’objet TOC en appelant [**IToc :: AddEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex).</span><span class="sxs-lookup"><span data-stu-id="a2337-121">Add the TOC Entry List object you created in step 3 to the TOC object by calling [**IToc::AddEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex).</span></span>
7.  <span data-ttu-id="a2337-122">Créez un objet d’analyse de table des matières et obtenez une interface [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="a2337-122">Create a TOC Parser object and obtain an [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface on it.</span></span>
8.  <span data-ttu-id="a2337-123">Appelez [**ITocParser :: init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) pour initialiser l’objet de l’analyseur de la table des matières et l’associer à un fichier vidéo.</span><span class="sxs-lookup"><span data-stu-id="a2337-123">Call [**ITocParser::Init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) to initialize the TOC Parser object and associate it with a video file.</span></span>
9.  <span data-ttu-id="a2337-124">Ajoutez l’objet TOC que vous avez créé à l’étape 5 à l’objet analyseur de la table des matières en appelant [**ITocParser :: AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc).</span><span class="sxs-lookup"><span data-stu-id="a2337-124">Add the TOC object you created in step 5 to the TOC Parser object by calling [**ITocParser::AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc).</span></span>
10. <span data-ttu-id="a2337-125">Incorporez la table des matières dans le fichier vidéo en appelant [**ITocParser :: Commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit).</span><span class="sxs-lookup"><span data-stu-id="a2337-125">Embed the table of contents in the video file by calling [**ITocParser::Commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit).</span></span>

<span data-ttu-id="a2337-126">Le code suivant illustre les étapes indiquées dans la liste précédente.</span><span class="sxs-lookup"><span data-stu-id="a2337-126">The following code demonstrates the steps given in the preceding list.</span></span>


```C++
#include <wmcodecdsp.h>
HRESULT InitTocParserAndCommit(IToc* pToc);

void main()
{
   HRESULT hr = CoInitialize(NULL);
   
   if(SUCCEEDED(hr))
   {    
      ITocEntry* pEntry = NULL;
      hr = CoCreateInstance(CLSID_CTocEntry, NULL, 
         CLSCTX_INPROC_SERVER, IID_ITocEntry, (VOID**)&pEntry); 

      if(SUCCEEDED(hr))
      {
         TOC_ENTRY_DESCRIPTOR tocDesc = {0};
         tocDesc.qwStartTime = 4; 
         tocDesc.qwEndTime = 8;
         pEntry->SetDescriptor(&tocDesc); // HRESULT ignored for simplicity.    
    
         ITocEntryList* pEntryList = NULL;
         hr = CoCreateInstance(CLSID_CTocEntryList, NULL, 
            CLSCTX_INPROC_SERVER, IID_ITocEntryList, (VOID**)&pEntryList);

         if(SUCCEEDED(hr))
         {
            pEntryList->AddEntryByIndex(0, pEntry); // HRESULT ignored.
      
            IToc* pToc = NULL;
            hr = CoCreateInstance(CLSID_CToc, NULL, 
               CLSCTX_INPROC_SERVER, IID_IToc, (VOID**)&pToc);

            if(SUCCEEDED(hr))
            {
               pToc->AddEntryListByIndex(0, pEntryList); // HRESULT ignored.
               hr = InitTocParserAndCommit(pToc);
            }
         }
      }
     
      CoUninitialize();
   }
}

HRESULT InitTocParserAndCommit(IToc* pToc)
{
   ITocParser* pTocParser = NULL;
   HRESULT hr = CoCreateInstance(CLSID_CTocParser, NULL, 
      CLSCTX_INPROC_SERVER, IID_ITocParser, (VOID**)&pTocParser);

   if(SUCCEEDED(hr))
   {
      hr = pTocParser->Init(L"\\\\?\\c:\\experiment\\seattle.wmv");

      if(SUCCEEDED(hr))
      {
         DWORD tocIndex = 0;
         hr = pTocParser->AddToc(TOC_POS_TOPLEVELOBJECT, pToc, &tocIndex);

         if(SUCCEEDED(hr))
         {
            hr = pTocParser->Commit();
         }
      }

      pTocParser->Release();
      pTocParser = NULL;
   }

   return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="a2337-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a2337-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2337-128">Lecture d’une table des matières à partir d’un fichier vidéo</span><span class="sxs-lookup"><span data-stu-id="a2337-128">Reading a Table of Contents From a Video File</span></span>](reading-a-table-of-contents-from-a-video-file.md)
</dt> <dt>

[<span data-ttu-id="a2337-129">Objets de l’analyseur de table des matières</span><span class="sxs-lookup"><span data-stu-id="a2337-129">Table of Contents Parser Objects</span></span>](toc-parser-objects.md)
</dt> <dt>

[<span data-ttu-id="a2337-130">Guide de programmation de l’analyseur de table des matières</span><span class="sxs-lookup"><span data-stu-id="a2337-130">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 



