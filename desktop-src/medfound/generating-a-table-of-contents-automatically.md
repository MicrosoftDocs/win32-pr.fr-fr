---
description: Génération automatique d’une table des matières
ms.assetid: 3acb9c12-0158-4b89-87c4-4abd35ae8c2f
title: Génération automatique d’une table des matières
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22adc4d48ad7f4b1d89a446eb28c25d6011804a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538635"
---
# <a name="generating-a-table-of-contents-automatically"></a>Génération automatique d’une table des matières

Cette rubrique montre comment utiliser le composant [**Générateur de table des matières**](/previous-versions/ee264297(v=vs.85)) (TM Generator) pour générer automatiquement une table des matières pour un fichier vidéo.

Le générateur de table des matières est un objet de média DirectX (DMO). Pour utiliser le générateur de table des matières DMO, créez un graphique de filtre DirectX contenant un fichier vidéo comme source. Insérez le générateur de table des matières DMO dans le graphique de filtre, puis exécutez le graphique. Vous pouvez ensuite obtenir la table des matières générée automatiquement à partir du générateur de table des matières DMO.

La procédure suivante décrit les étapes plus en détail.

1.  Appelez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer un objet de graphique de filtre (**CLSID \_ FilterGraph**) et obtenir une interface [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .
2.  Appelez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer un objet de filtre de wrapper DMO (**CLSID \_ DMOWrapperFilter**) et obtenir une interface [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter) .
3.  Transmettez le **CLSID \_ CTocGeneratorDmo** à la méthode [**init**](/previous-versions/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init) de votre filtre de wrappers DMO. Cela crée un générateur de tables des matières DMO et l’enveloppe dans votre filtre de wrappers DMO.
4.  Appelez la méthode [**AddFilter**](/windows/win32/api/strmif/nf-strmif-ifiltergraph-addfilter) de votre interface [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) pour ajouter le générateur de table de matières encapsulé DMO au graphique de filtre.
    > [!Note]  
    > [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) hérite de [**IFilterGraph**](/windows/win32/api/strmif/nn-strmif-ifiltergraph).

     

5.  Appelez la méthode [**AddSourceFilter**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-addsourcefilter) de votre interface [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) pour créer un filtre de ressource et l’ajouter au graphique.
6.  Énumérer les codes confidentiels sur le filtre de wrapper DMO et le filtre source. Cela implique d’obtenir des interfaces [**IEnumPins**](/windows/win32/api/strmif/nn-strmif-ienumpins) et des interfaces [**IPIN**](/windows/win32/api/strmif/nn-strmif-ipin) .
7.  Connectez le filtre source et le filtre de wrapper en appelant la méthode [**Connect**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-connect) de votre interface [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .
8.  Complétez le graphique en appelant la méthode [**Render**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-render) de votre interface [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .
9.  Exécutez le graphique ([**IMediaControl :: Run**](/windows/win32/api/control/nf-control-imediacontrol-run)) et attendez qu’il se termine ([**IMediaEvent :: WaitForCompletion**](/windows/win32/api/control/nf-control-imediaevent-waitforcompletion)).
10. Obtenez une interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) sur votre Wrapper de filtre DMO et obtenez la valeur de la propriété [**MFPKEY \_ TOCGENERATOR \_ TOCREADY**](/previous-versions/ee264297(v=vs.85)) . Répétez cette opération si nécessaire jusqu’à ce que la table des matières soit prête.
11. Utilisez votre interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pour récupérer la valeur de la propriété [**MFPKEY \_ TOCGENERATOR \_ TOCOBJECT**](/previous-versions/ee264297(v=vs.85)) . Cette propriété est une interface [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) qui représente la table des matières générée automatiquement.

Le code suivant illustre la procédure de génération automatique d’une table des matières. Le code utilise trois fonctions d’assistance ([**BuildGraph**](buildgraph-method-for-generating-a-table-of-contents.md), [**RunGraphAndWait**](rungraphandwait-method-for-generating-a-table-of-contents.md)et [**GetToc**](gettoc-method-for-generating-a-table-of-contents.md)) qui sont affichées sur d’autres pages de cette documentation.


```C++
#include <dshow.h>
#include <dmodshow.h>
#include <wmcodecdsp.h>
#include <dmoreg.h>
#include <propsys.h>
#include <propidl.h>
#include <initguid.h>

HRESULT GetToc(IDMOWrapperFilter* pWrap, IToc** ppToc);
HRESULT RunGraphAndWait(IGraphBuilder* pGraph);
HRESULT BuildGraph(IGraphBuilder* pGraph, IDMOWrapperFilter* pWrap);

WCHAR g_sourceFile[] = L"c:\\experiment\\Seattle.wmv";

void main()
{
   HRESULT hr = E_FAIL;
   hr = CoInitialize(NULL);

   if(SUCCEEDED(hr))
   {
      IGraphBuilder* pBuilder = NULL;
      hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
         IID_IGraphBuilder, (VOID**)&pBuilder);

      if(SUCCEEDED(hr))
      {
         IDMOWrapperFilter* pWrap = NULL;
         hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, CLSCTX_INPROC, 
            IID_IDMOWrapperFilter, (VOID**)&pWrap);

         if(SUCCEEDED(hr))
         {
            hr = pWrap->Init(CLSID_CTocGeneratorDmo, DMOCATEGORY_VIDEO_EFFECT); 

            if(SUCCEEDED(hr))
            {
               hr = BuildGraph(pBuilder, pWrap);

               if(SUCCEEDED(hr))
               {
                  hr = RunGraphAndWait(pBuilder);

                  if(SUCCEEDED(hr))
                  {
                     IToc* pToc = NULL;
                     hr = GetToc(pWrap, &pToc);

                     if(SUCCEEDED(hr))
                     {
                        // Inspect the table of contents by calling IToc methods.

                        pToc->Release();
                        pToc = NULL;
                     }
                  }
               }
            }

            pWrap->Release();
            pWrap = NULL;
         }

         pBuilder->Release();
         pBuilder = NULL;
      }

      CoUninitialize();
   }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonction BuildGraph pour générer une table des matières](buildgraph-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[Fonction GetToc pour générer une table des matières](gettoc-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[Fonction RunGraphAndWait pour générer une table des matières](rungraphandwait-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[Guide de programmation de l’analyseur de table des matières](toc-parser-programming-guide.md)
</dt> </dl>

 

 
