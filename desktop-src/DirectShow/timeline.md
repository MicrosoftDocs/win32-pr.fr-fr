---
description: Durée
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: Durée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d1f802f12df6ca3469b8283bd4fe8b27e22412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539762"
---
# <a name="timeline"></a><span data-ttu-id="661f3-103">Durée</span><span class="sxs-lookup"><span data-stu-id="661f3-103">Timeline</span></span>

> [!Note]  
> <span data-ttu-id="661f3-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="661f3-104">\[Deprecated.</span></span> <span data-ttu-id="661f3-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="661f3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="661f3-106">L’objet Timeline gère tous les objets d’un projet de montage vidéo.</span><span class="sxs-lookup"><span data-stu-id="661f3-106">The timeline object manages all of the objects in a video editing project.</span></span> <span data-ttu-id="661f3-107">Pour créer cet objet, appelez **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="661f3-107">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="661f3-108">L’identificateur de classe est CLSID \_ AMTimeline.</span><span class="sxs-lookup"><span data-stu-id="661f3-108">The class identifier is CLSID\_AMTimeline.</span></span>

<span data-ttu-id="661f3-109">Pour lire des fichiers Windows Media™, l’application doit fournir un certificat logiciel, également appelé clé.</span><span class="sxs-lookup"><span data-stu-id="661f3-109">To read Windows Media™ files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="661f3-110">Inscrivez l’application en tant que fournisseur de clé via l’interface **IObjectWithSite** de la chronologie.</span><span class="sxs-lookup"><span data-stu-id="661f3-110">Register the application as a key provider through the timeline's **IObjectWithSite** interface.</span></span> <span data-ttu-id="661f3-111">Pour plus d’informations, consultez [déverrouillage du kit de développement logiciel (SDK) de format Windows Media](unlocking-the-windows-media-format-sdk.md).</span><span class="sxs-lookup"><span data-stu-id="661f3-111">For more information, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="661f3-112">L’objet Timeline expose les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="661f3-112">The timeline object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="661f3-113">**IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="661f3-113">**IAMSetErrorLog**</span></span>](iamseterrorlog.md)
-   [<span data-ttu-id="661f3-114">**IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="661f3-114">**IAMTimeline**</span></span>](iamtimeline.md)
-   <span data-ttu-id="661f3-115">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="661f3-115">**IObjectWithSite**</span></span>
-   <span data-ttu-id="661f3-116">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="661f3-116">**IPersistStream**</span></span>

## <a name="related-topics"></a><span data-ttu-id="661f3-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="661f3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="661f3-118">Modèle de chronologie</span><span class="sxs-lookup"><span data-stu-id="661f3-118">The Timeline Model</span></span>](the-timeline-model.md)
</dt> <dt>

[<span data-ttu-id="661f3-119">Construction d’une chronologie</span><span class="sxs-lookup"><span data-stu-id="661f3-119">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



