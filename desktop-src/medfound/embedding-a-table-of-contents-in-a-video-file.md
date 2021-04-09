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
# <a name="embedding-a-table-of-contents-in-a-video-file"></a>Incorporation d’une table des matières dans un fichier vidéo

Cette rubrique montre comment créer une table des matières et l’incorporer dans un fichier vidéo. Pour que l’exemple de code reste concis, la table des matières est très simple ; il ne contient qu’une seule entrée, et l’entrée est remplie avec un minimum d’informations.

Pour créer une table des matières et l’incorporer dans un fichier, vous devez créer les quatre objets suivants en appelant **CoCreateInstance**.

-   Entrée de la table des matières
-   Liste des entrées de la table des matières
-   Table des matières
-   Analyseur de table des matières

Les identificateurs de classe pour les objets sont fournis dans les [identificateurs de classe pour l’analyseur de table des matières](class-identifiers-for-toc-parser.md).

Tout d’abord, renseignez l’entrée de la table des matières avec des informations qui décrivent une partie du fichier vidéo. Ajoutez l’entrée TOC à la liste entrée de la table des matières, puis ajoutez la liste des entrées de la table des matières à la table des matières. Enfin, ajoutez la table des matières à l’analyseur de table des matières, qui fournit la fonctionnalité d’incorporation de la table des matières dans le fichier vidéo. La liste suivante présente les étapes plus en détail.

1.  Créez un objet entrée de la table des matières et obtenez une interface [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) sur celui-ci.
2.  Remplir une structure de [**\_ \_ descripteur d’entrée TOC**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) et la passer à [**ITocEntry :: SetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor).
3.  Créez un objet de liste d’entrée de table des matières et obtenez une interface [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) sur celui-ci.
4.  Ajoutez l’objet entrée de la table des matières que vous avez créé à l’étape 1 à l’objet de liste entrée de table des matières en appelant [**ITocEntryList :: AddEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex).
5.  Créez un objet TOC et obtenez une interface [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) sur celui-ci.
6.  Ajoutez l’objet de liste d’entrées de la table des matières que vous avez créé à l’étape 3 à l’objet TOC en appelant [**IToc :: AddEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex).
7.  Créez un objet d’analyse de table des matières et obtenez une interface [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) sur celui-ci.
8.  Appelez [**ITocParser :: init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) pour initialiser l’objet de l’analyseur de la table des matières et l’associer à un fichier vidéo.
9.  Ajoutez l’objet TOC que vous avez créé à l’étape 5 à l’objet analyseur de la table des matières en appelant [**ITocParser :: AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc).
10. Incorporez la table des matières dans le fichier vidéo en appelant [**ITocParser :: Commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit).

Le code suivant illustre les étapes indiquées dans la liste précédente.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture d’une table des matières à partir d’un fichier vidéo](reading-a-table-of-contents-from-a-video-file.md)
</dt> <dt>

[Objets de l’analyseur de table des matières](toc-parser-objects.md)
</dt> <dt>

[Guide de programmation de l’analyseur de table des matières](toc-parser-programming-guide.md)
</dt> </dl>

 

 



