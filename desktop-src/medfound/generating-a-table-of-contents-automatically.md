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
# <a name="generating-a-table-of-contents-automatically"></a><span data-ttu-id="8b78e-103">Génération automatique d’une table des matières</span><span class="sxs-lookup"><span data-stu-id="8b78e-103">Generating a Table of Contents Automatically</span></span>

<span data-ttu-id="8b78e-104">Cette rubrique montre comment utiliser le composant [**Générateur de table des matières**](/previous-versions/ee264297(v=vs.85)) (TM Generator) pour générer automatiquement une table des matières pour un fichier vidéo.</span><span class="sxs-lookup"><span data-stu-id="8b78e-104">This topic demonstrates how to use [**Table of Contents Generator**](/previous-versions/ee264297(v=vs.85)) (TOC Generator) component to automatically generate a table of contents for a video file.</span></span>

<span data-ttu-id="8b78e-105">Le générateur de table des matières est un objet de média DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="8b78e-105">TOC Generator is a DirectX Media Object (DMO).</span></span> <span data-ttu-id="8b78e-106">Pour utiliser le générateur de table des matières DMO, créez un graphique de filtre DirectX contenant un fichier vidéo comme source.</span><span class="sxs-lookup"><span data-stu-id="8b78e-106">To use the TOC Generator DMO, build a DirectX filter graph that has a video file as its source.</span></span> <span data-ttu-id="8b78e-107">Insérez le générateur de table des matières DMO dans le graphique de filtre, puis exécutez le graphique.</span><span class="sxs-lookup"><span data-stu-id="8b78e-107">Insert the TOC Generator DMO into the filter graph, and run the graph.</span></span> <span data-ttu-id="8b78e-108">Vous pouvez ensuite obtenir la table des matières générée automatiquement à partir du générateur de table des matières DMO.</span><span class="sxs-lookup"><span data-stu-id="8b78e-108">You can then obtain the automatically generated table of contents from the TOC Generator DMO.</span></span>

<span data-ttu-id="8b78e-109">La procédure suivante décrit les étapes plus en détail.</span><span class="sxs-lookup"><span data-stu-id="8b78e-109">The following procedure gives the steps in more detail.</span></span>

1.  <span data-ttu-id="8b78e-110">Appelez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer un objet de graphique de filtre (**CLSID \_ FilterGraph**) et obtenir une interface [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .</span><span class="sxs-lookup"><span data-stu-id="8b78e-110">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a Filter Graph object (**CLSID\_FilterGraph**) and obtain an [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
2.  <span data-ttu-id="8b78e-111">Appelez [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer un objet de filtre de wrapper DMO (**CLSID \_ DMOWrapperFilter**) et obtenir une interface [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter) .</span><span class="sxs-lookup"><span data-stu-id="8b78e-111">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a DMO Wrapper Filter object (**CLSID\_DMOWrapperFilter**) and obtain an [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter) interface.</span></span>
3.  <span data-ttu-id="8b78e-112">Transmettez le **CLSID \_ CTocGeneratorDmo** à la méthode [**init**](/previous-versions/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init) de votre filtre de wrappers DMO.</span><span class="sxs-lookup"><span data-stu-id="8b78e-112">Pass **CLSID\_CTocGeneratorDmo** to the [**Init**](/previous-versions/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init) method of your DMO wrapper filter.</span></span> <span data-ttu-id="8b78e-113">Cela crée un générateur de tables des matières DMO et l’enveloppe dans votre filtre de wrappers DMO.</span><span class="sxs-lookup"><span data-stu-id="8b78e-113">This creates a TOC Generator DMO and wraps it in your DMO wrapper filter.</span></span>
4.  <span data-ttu-id="8b78e-114">Appelez la méthode [**AddFilter**](/windows/win32/api/strmif/nf-strmif-ifiltergraph-addfilter) de votre interface [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) pour ajouter le générateur de table de matières encapsulé DMO au graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="8b78e-114">Call the [**AddFilter**](/windows/win32/api/strmif/nf-strmif-ifiltergraph-addfilter) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface to add the wrapped TOC Generator DMO to the filter graph.</span></span>
    > [!Note]  
    > <span data-ttu-id="8b78e-115">[**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) hérite de [**IFilterGraph**](/windows/win32/api/strmif/nn-strmif-ifiltergraph).</span><span class="sxs-lookup"><span data-stu-id="8b78e-115">[**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) inherits from [**IFilterGraph**](/windows/win32/api/strmif/nn-strmif-ifiltergraph).</span></span>

     

5.  <span data-ttu-id="8b78e-116">Appelez la méthode [**AddSourceFilter**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-addsourcefilter) de votre interface [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) pour créer un filtre de ressource et l’ajouter au graphique.</span><span class="sxs-lookup"><span data-stu-id="8b78e-116">Call the [**AddSourceFilter**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-addsourcefilter) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface to create a souce filter and add it to the graph.</span></span>
6.  <span data-ttu-id="8b78e-117">Énumérer les codes confidentiels sur le filtre de wrapper DMO et le filtre source.</span><span class="sxs-lookup"><span data-stu-id="8b78e-117">Enumerate pins on the DMO wrapper filter and the source filter.</span></span> <span data-ttu-id="8b78e-118">Cela implique d’obtenir des interfaces [**IEnumPins**](/windows/win32/api/strmif/nn-strmif-ienumpins) et des interfaces [**IPIN**](/windows/win32/api/strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="8b78e-118">This involves obtaining [**IEnumPins**](/windows/win32/api/strmif/nn-strmif-ienumpins) interfaces and [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) interfaces.</span></span>
7.  <span data-ttu-id="8b78e-119">Connectez le filtre source et le filtre de wrapper en appelant la méthode [**Connect**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-connect) de votre interface [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .</span><span class="sxs-lookup"><span data-stu-id="8b78e-119">Connect the source filter and the wrapper filter by calling the [**Connect**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-connect) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
8.  <span data-ttu-id="8b78e-120">Complétez le graphique en appelant la méthode [**Render**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-render) de votre interface [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .</span><span class="sxs-lookup"><span data-stu-id="8b78e-120">Complete the graph by calling the [**Render**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-render) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
9.  <span data-ttu-id="8b78e-121">Exécutez le graphique ([**IMediaControl :: Run**](/windows/win32/api/control/nf-control-imediacontrol-run)) et attendez qu’il se termine ([**IMediaEvent :: WaitForCompletion**](/windows/win32/api/control/nf-control-imediaevent-waitforcompletion)).</span><span class="sxs-lookup"><span data-stu-id="8b78e-121">Run the graph ([**IMediaControl::Run**](/windows/win32/api/control/nf-control-imediacontrol-run)), and wait for it to complete ([**IMediaEvent::WaitForCompletion**](/windows/win32/api/control/nf-control-imediaevent-waitforcompletion)).</span></span>
10. <span data-ttu-id="8b78e-122">Obtenez une interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) sur votre Wrapper de filtre DMO et obtenez la valeur de la propriété [**MFPKEY \_ TOCGENERATOR \_ TOCREADY**](/previous-versions/ee264297(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8b78e-122">Obtain an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface on your DMO filter wrapper, and get the value of the [**MFPKEY\_TOCGENERATOR\_TOCREADY**](/previous-versions/ee264297(v=vs.85)) property.</span></span> <span data-ttu-id="8b78e-123">Répétez cette opération si nécessaire jusqu’à ce que la table des matières soit prête.</span><span class="sxs-lookup"><span data-stu-id="8b78e-123">Repeat if necessary until the table of contents is ready.</span></span>
11. <span data-ttu-id="8b78e-124">Utilisez votre interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pour récupérer la valeur de la propriété [**MFPKEY \_ TOCGENERATOR \_ TOCOBJECT**](/previous-versions/ee264297(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8b78e-124">Use your [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface to get the value of the [**MFPKEY\_TOCGENERATOR\_TOCOBJECT**](/previous-versions/ee264297(v=vs.85)) property.</span></span> <span data-ttu-id="8b78e-125">Cette propriété est une interface [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) qui représente la table des matières générée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="8b78e-125">This property is an [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) interface that represents the automatically generated table of contents.</span></span>

<span data-ttu-id="8b78e-126">Le code suivant illustre la procédure de génération automatique d’une table des matières.</span><span class="sxs-lookup"><span data-stu-id="8b78e-126">The following code demonstrates the procedure for generating a table of contents automatically.</span></span> <span data-ttu-id="8b78e-127">Le code utilise trois fonctions d’assistance ([**BuildGraph**](buildgraph-method-for-generating-a-table-of-contents.md), [**RunGraphAndWait**](rungraphandwait-method-for-generating-a-table-of-contents.md)et [**GetToc**](gettoc-method-for-generating-a-table-of-contents.md)) qui sont affichées sur d’autres pages de cette documentation.</span><span class="sxs-lookup"><span data-stu-id="8b78e-127">The code uses three helper functions ([**BuildGraph**](buildgraph-method-for-generating-a-table-of-contents.md), [**RunGraphAndWait**](rungraphandwait-method-for-generating-a-table-of-contents.md), and [**GetToc**](gettoc-method-for-generating-a-table-of-contents.md)) that are shown on other pages of this documentation.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8b78e-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8b78e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b78e-129">Fonction BuildGraph pour générer une table des matières</span><span class="sxs-lookup"><span data-stu-id="8b78e-129">BuildGraph Function for Generating a Table of Contents</span></span>](buildgraph-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="8b78e-130">Fonction GetToc pour générer une table des matières</span><span class="sxs-lookup"><span data-stu-id="8b78e-130">GetToc Function for Generating a Table of Contents</span></span>](gettoc-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="8b78e-131">Fonction RunGraphAndWait pour générer une table des matières</span><span class="sxs-lookup"><span data-stu-id="8b78e-131">RunGraphAndWait Function for Generating a Table of Contents</span></span>](rungraphandwait-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="8b78e-132">Guide de programmation de l’analyseur de table des matières</span><span class="sxs-lookup"><span data-stu-id="8b78e-132">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 
