---
description: Énumération des appareils et des filtres
ms.assetid: 334bba2a-7477-4115-9ce0-d4495c1fc290
title: Énumération des appareils et des filtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69997a4af4f3160f0b338bc9c595adea83a5354
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846601"
---
# <a name="enumerating-devices-and-filters"></a><span data-ttu-id="96b6a-103">Énumération des appareils et des filtres</span><span class="sxs-lookup"><span data-stu-id="96b6a-103">Enumerating Devices and Filters</span></span>

<span data-ttu-id="96b6a-104">Parfois, une application doit localiser un filtre particulier sur le système de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="96b6a-104">Sometimes an application needs to locate a particular filter on the user's system.</span></span> <span data-ttu-id="96b6a-105">Par exemple, une application de capture vidéo peut afficher une liste des périphériques de capture disponibles.</span><span class="sxs-lookup"><span data-stu-id="96b6a-105">For example, a video capture application might display a list of available capture devices.</span></span> <span data-ttu-id="96b6a-106">Étant donné que DirectShow utilise une architecture basée sur des composants, vous ne pouvez pas savoir au moment de la conception quels filtres sont installés sur le système de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="96b6a-106">Because DirectShow uses a component-based architecture, you cannot know at design time which filters are installed on the user's system.</span></span> <span data-ttu-id="96b6a-107">Cela est particulièrement vrai pour les filtres qui représentent des périphériques matériels.</span><span class="sxs-lookup"><span data-stu-id="96b6a-107">This is particularly true for filters that represent hardware devices.</span></span> <span data-ttu-id="96b6a-108">DirectShow fournit deux composants qui localisent les filtres enregistrés :</span><span class="sxs-lookup"><span data-stu-id="96b6a-108">DirectShow provides two components that locate registered filters:</span></span>

-   <span data-ttu-id="96b6a-109">L' [énumérateur de périphérique système](system-device-enumerator.md) recherche les filtres par catégorie.</span><span class="sxs-lookup"><span data-stu-id="96b6a-109">The [System Device Enumerator](system-device-enumerator.md) finds filters by their category.</span></span>
-   <span data-ttu-id="96b6a-110">Le [Mappeur de filtre](filter-mapper.md) recherche les filtres en fonction des critères de recherche fournis par l’application.</span><span class="sxs-lookup"><span data-stu-id="96b6a-110">The [Filter Mapper](filter-mapper.md) finds filters according to search criteria supplied by the application.</span></span>

<span data-ttu-id="96b6a-111">Les énumérateurs abordés dans cette section suivent le formulaire standard utilisé par les interfaces d’énumération COM.</span><span class="sxs-lookup"><span data-stu-id="96b6a-111">The enumerators discussed in this section follow the standard form used by COM enumeration interfaces.</span></span> <span data-ttu-id="96b6a-112">Pour plus d’informations, consultez la rubrique « IEnumXXXX » dans le kit de développement logiciel (SDK) de la plate-forme Microsoft.</span><span class="sxs-lookup"><span data-stu-id="96b6a-112">For more information, see the "IEnumXXXX" topic in the Microsoft Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="96b6a-113">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="96b6a-113">This section contains the following topics:</span></span>

-   [<span data-ttu-id="96b6a-114">Utilisation de l’énumérateur de périphérique système</span><span class="sxs-lookup"><span data-stu-id="96b6a-114">Using the System Device Enumerator</span></span>](using-the-system-device-enumerator.md)
-   [<span data-ttu-id="96b6a-115">Utilisation du mappeur de filtre</span><span class="sxs-lookup"><span data-stu-id="96b6a-115">Using the Filter Mapper</span></span>](using-the-filter-mapper.md)

## <a name="related-topics"></a><span data-ttu-id="96b6a-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="96b6a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96b6a-117">Tâches de base de DirectShow</span><span class="sxs-lookup"><span data-stu-id="96b6a-117">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



