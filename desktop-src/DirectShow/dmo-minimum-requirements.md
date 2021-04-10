---
description: Configuration minimale requise pour DMO
ms.assetid: cd342f0f-a3dc-4623-a18f-c45071795ef4
title: Configuration minimale requise pour DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c26267f50619062fb8396f93b7578db4d3d8c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950243"
---
# <a name="dmo-minimum-requirements"></a><span data-ttu-id="1ae75-103">Configuration minimale requise pour DMO</span><span class="sxs-lookup"><span data-stu-id="1ae75-103">DMO Minimum Requirements</span></span>

<span data-ttu-id="1ae75-104">Chaque DMO doit respecter la configuration minimale suivante :</span><span class="sxs-lookup"><span data-stu-id="1ae75-104">Every DMO should meet the following minimum requirements:</span></span>

-   <span data-ttu-id="1ae75-105">Il doit prendre en charge l’agrégation.</span><span class="sxs-lookup"><span data-stu-id="1ae75-105">It must support aggregation.</span></span>
-   <span data-ttu-id="1ae75-106">Elle doit exposer l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .</span><span class="sxs-lookup"><span data-stu-id="1ae75-106">It must expose the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface.</span></span>
-   <span data-ttu-id="1ae75-107">Le modèle de thread doit être’both'.</span><span class="sxs-lookup"><span data-stu-id="1ae75-107">The threading model must be 'both'.</span></span> <span data-ttu-id="1ae75-108">DMOs doit fonctionner correctement dans un environnement à threads libres.</span><span class="sxs-lookup"><span data-stu-id="1ae75-108">DMOs must function correctly in a free-threaded environment.</span></span>

<span data-ttu-id="1ae75-109">L’effet audio DMOs doit prendre en charge l’interface [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) , pour une utilisation dans DirectMusic et DirectSound.</span><span class="sxs-lookup"><span data-stu-id="1ae75-109">Audio effect DMOs should support the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) interface, for use in DirectMusic and DirectSound.</span></span>

<span data-ttu-id="1ae75-110">Les interfaces suivantes sont documentées ailleurs, mais sont utiles pour de nombreux DMOs.</span><span class="sxs-lookup"><span data-stu-id="1ae75-110">The following interfaces are documented elsewhere, but are useful for many DMOs.</span></span> <span data-ttu-id="1ae75-111">Toutefois, elles ne sont pas requises.</span><span class="sxs-lookup"><span data-stu-id="1ae75-111">They are not required, however.</span></span>

-   <span data-ttu-id="1ae75-112">**ISpecifyPropertyPages**, **IPropertyPage**: ces interfaces permettent à DMO de fournir une page de propriétés, pour permettre à l’utilisateur de définir des propriétés.</span><span class="sxs-lookup"><span data-stu-id="1ae75-112">**ISpecifyPropertyPages**, **IPropertyPage**: These interfaces enable a DMO to provide a property page, for the user to set properties.</span></span>
-   <span data-ttu-id="1ae75-113">**IPersistStream**: cette interface permet à DMO d’enregistrer son état dans un stockage persistant.</span><span class="sxs-lookup"><span data-stu-id="1ae75-113">**IPersistStream**: This interface enables the DMO to save its state to persistent storage.</span></span>
-   <span data-ttu-id="1ae75-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression): ces interfaces permettent à un client de configurer les paramètres de compression et de format de sortie d’un encodeur.</span><span class="sxs-lookup"><span data-stu-id="1ae75-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression): These interfaces enable a client to configure an encoder's output format and compression settings.</span></span> <span data-ttu-id="1ae75-115">(Ces deux interfaces font partie de l’API DirectShow, mais elles sont également recommandées pour DMOs.)</span><span class="sxs-lookup"><span data-stu-id="1ae75-115">(These two interfaces are part of the DirectShow API, but are also recommended for DMOs.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ae75-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ae75-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ae75-117">Écriture d’un DMO</span><span class="sxs-lookup"><span data-stu-id="1ae75-117">Writing a DMO</span></span>](writing-a-dmo.md)
</dt> </dl>

 

 



