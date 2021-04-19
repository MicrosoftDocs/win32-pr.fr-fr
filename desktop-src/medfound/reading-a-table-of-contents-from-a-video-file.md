---
description: Lecture d’une table des matières à partir d’un fichier vidéo
ms.assetid: 10c4f4ca-cb30-453c-b18d-0470bfecc14e
title: Lecture d’une table des matières à partir d’un fichier vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d75d1101b2ad0a2ecd57dcf53acbe6a6e7d435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536989"
---
# <a name="reading-a-table-of-contents-from-a-video-file"></a><span data-ttu-id="85b10-103">Lecture d’une table des matières à partir d’un fichier vidéo</span><span class="sxs-lookup"><span data-stu-id="85b10-103">Reading a Table of Contents from a Video File</span></span>

<span data-ttu-id="85b10-104">Cette rubrique montre comment lire une table des matières qui a déjà été incorporée dans un fichier vidéo.</span><span class="sxs-lookup"><span data-stu-id="85b10-104">This topic demonstrates how to read a table of contents that has already been embedded in a video file.</span></span>

<span data-ttu-id="85b10-105">Commencez en appelant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer un objet d’analyse de table des matières et obtenir une interface [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) .</span><span class="sxs-lookup"><span data-stu-id="85b10-105">Start by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a TOC Parser object and obtain an [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface.</span></span> <span data-ttu-id="85b10-106">Obtenez ensuite les interfaces suivantes en appelant des méthodes.</span><span class="sxs-lookup"><span data-stu-id="85b10-106">Then obtain the following interfaces by calling methods.</span></span>

-   [<span data-ttu-id="85b10-107">**IToc**</span><span class="sxs-lookup"><span data-stu-id="85b10-107">**IToc**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc)
-   [<span data-ttu-id="85b10-108">**ITocEntryList**</span><span class="sxs-lookup"><span data-stu-id="85b10-108">**ITocEntryList**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist)
-   [<span data-ttu-id="85b10-109">**ITocEntry**</span><span class="sxs-lookup"><span data-stu-id="85b10-109">**ITocEntry**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry)

<span data-ttu-id="85b10-110">Utilisez les méthodes de [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) pour inspecter une entrée individuelle dans la table des matières.</span><span class="sxs-lookup"><span data-stu-id="85b10-110">Use the methods of [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) to inspect an individual entry in the table of contents.</span></span> <span data-ttu-id="85b10-111">Par exemple, vous pouvez inspecter le titre, l’heure de début et l’heure de fin de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="85b10-111">For example, you can inspect the title, the start time, and the end time of the entry.</span></span>

<span data-ttu-id="85b10-112">La liste suivante présente les étapes plus en détail.</span><span class="sxs-lookup"><span data-stu-id="85b10-112">The following list gives the steps in more detail.</span></span>

1.  <span data-ttu-id="85b10-113">Appelez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer un objet d’analyse de table des matières et obtenir une interface [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="85b10-113">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a TOC Parser object and obtain an [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface on it.</span></span>
2.  <span data-ttu-id="85b10-114">Appelez [**ITocParser :: init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) pour initialiser l’analyseur TOC et l’associer à un fichier vidéo.</span><span class="sxs-lookup"><span data-stu-id="85b10-114">Call [**ITocParser::Init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) to initialize the TOC parser and associate it with a video file.</span></span>
3.  <span data-ttu-id="85b10-115">Obtenez une interface [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) en appelant [**ITocParser :: GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex).</span><span class="sxs-lookup"><span data-stu-id="85b10-115">Obtain an [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) interface by calling [**ITocParser::GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex).</span></span>
4.  <span data-ttu-id="85b10-116">Obtenez une interface [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) en appelant [**IToc :: GetEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getentrylistbyindex).</span><span class="sxs-lookup"><span data-stu-id="85b10-116">Obtain an [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) interface by calling [**IToc::GetEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getentrylistbyindex).</span></span>
5.  <span data-ttu-id="85b10-117">Obtenez une interface [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) en appelant [**ITocEntryList :: GetEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrybyindex).</span><span class="sxs-lookup"><span data-stu-id="85b10-117">Obtain an [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) interface by calling [**ITocEntryList::GetEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrybyindex).</span></span>
6.  <span data-ttu-id="85b10-118">Allouez une structure de [**\_ \_ descripteur d’entrée TOC**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="85b10-118">Allocate a [**TOC\_ENTRY\_DESCRIPTOR**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) structure.</span></span>
7.  <span data-ttu-id="85b10-119">Remplissez la structure du [**\_ \_ descripteur d’entrée TOC**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) en appelant [**ITocEntry :: GetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptor).</span><span class="sxs-lookup"><span data-stu-id="85b10-119">Populate the [**TOC\_ENTRY\_DESCRIPTOR**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) structure by calling [**ITocEntry::GetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptor).</span></span>

<span data-ttu-id="85b10-120">Le code suivant illustre les étapes de la liste précédente.</span><span class="sxs-lookup"><span data-stu-id="85b10-120">The following code demonstrates the steps in the preceding list.</span></span>


```C++
#include <stdio.h>
#include <wmcodecdsp.h>

HRESULT ShowEntryInfo(ITocEntry* pEntry);

void main()
{
   HRESULT hr = CoInitialize(NULL);
   
   if(SUCCEEDED(hr))
   {    
      ITocParser* pTocParser = NULL;

      hr = CoCreateInstance(CLSID_CTocParser, NULL, CLSCTX_INPROC_SERVER, 
         IID_ITocParser, (VOID**)&pTocParser);  
      
      if(SUCCEEDED(hr))
      {  
         hr = pTocParser->Init(L"\\\\?\\c:\\experiment\\seattle.wmv");

         if(SUCCEEDED(hr))
         {
            IToc* pToc = NULL;
            hr = pTocParser->GetTocByIndex(TOC_POS_TOPLEVELOBJECT, 0, &pToc);

            if(SUCCEEDED(hr))
            {
               ITocEntryList* pEntryList = NULL;
               hr = pToc->GetEntryListByIndex(0, &pEntryList);

               if(SUCCEEDED(hr))
               {
                  ITocEntry* pEntry = NULL;
                  hr = pEntryList->GetEntryByIndex(0, &pEntry);

                  if(SUCCEEDED(hr))
                  {
                     hr = ShowEntryInfo(pEntry);
                     pEntry->Release();
                     pEntry = NULL;
                  }

                  pEntryList->Release();
                  pEntryList = NULL;
               }

               pToc->Release();
               pToc = NULL;
            }
         }

         pTocParser->Release();
         pTocParser = NULL;  
      }
                   
      CoUninitialize();
   }
}

HRESULT ShowEntryInfo(ITocEntry* pEntry)
{
   HRESULT hr = E_FAIL;

   TOC_ENTRY_DESCRIPTOR entryDesc = {0};
   hr = pEntry->GetDescriptor(&entryDesc);

   if(SUCCEEDED(hr))
   {
      printf_s("qwStartTime: %x\n", entryDesc.qwStartTime);
      printf_s("qwEndTime: %x\n", entryDesc.qwEndTime);
      printf_s("qwStartStartPacketOffset: %x\n", entryDesc.qwStartPacketOffset);
      printf_s("qwEndPacketOffset: %x\n", entryDesc.qwEndPacketOffset);
      printf_s("qwRepresentativeFrameTime: %x\n", entryDesc.qwRepresentativeFrameTime);
   }

   return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="85b10-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="85b10-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85b10-122">Incorporation d’une table des matières dans un fichier vidéo</span><span class="sxs-lookup"><span data-stu-id="85b10-122">Embedding a Table of Contents in a Video File</span></span>](embedding-a-table-of-contents-in-a-video-file.md)
</dt> <dt>

[<span data-ttu-id="85b10-123">Objets de l’analyseur de table des matières</span><span class="sxs-lookup"><span data-stu-id="85b10-123">Table of Contents Parser Objects</span></span>](toc-parser-objects.md)
</dt> <dt>

[<span data-ttu-id="85b10-124">Guide de programmation de l’analyseur de table des matières</span><span class="sxs-lookup"><span data-stu-id="85b10-124">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 
