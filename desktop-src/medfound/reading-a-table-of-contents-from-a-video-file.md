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
# <a name="reading-a-table-of-contents-from-a-video-file"></a>Lecture d’une table des matières à partir d’un fichier vidéo

Cette rubrique montre comment lire une table des matières qui a déjà été incorporée dans un fichier vidéo.

Commencez en appelant [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer un objet d’analyse de table des matières et obtenir une interface [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) . Obtenez ensuite les interfaces suivantes en appelant des méthodes.

-   [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc)
-   [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist)
-   [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry)

Utilisez les méthodes de [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) pour inspecter une entrée individuelle dans la table des matières. Par exemple, vous pouvez inspecter le titre, l’heure de début et l’heure de fin de l’entrée.

La liste suivante présente les étapes plus en détail.

1.  Appelez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer un objet d’analyse de table des matières et obtenir une interface [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) sur celui-ci.
2.  Appelez [**ITocParser :: init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) pour initialiser l’analyseur TOC et l’associer à un fichier vidéo.
3.  Obtenez une interface [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) en appelant [**ITocParser :: GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex).
4.  Obtenez une interface [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) en appelant [**IToc :: GetEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getentrylistbyindex).
5.  Obtenez une interface [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) en appelant [**ITocEntryList :: GetEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrybyindex).
6.  Allouez une structure de [**\_ \_ descripteur d’entrée TOC**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) .
7.  Remplissez la structure du [**\_ \_ descripteur d’entrée TOC**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) en appelant [**ITocEntry :: GetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptor).

Le code suivant illustre les étapes de la liste précédente.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Incorporation d’une table des matières dans un fichier vidéo](embedding-a-table-of-contents-in-a-video-file.md)
</dt> <dt>

[Objets de l’analyseur de table des matières](toc-parser-objects.md)
</dt> <dt>

[Guide de programmation de l’analyseur de table des matières](toc-parser-programming-guide.md)
</dt> </dl>

 

 
