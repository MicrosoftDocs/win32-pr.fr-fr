---
description: WMI implémente une technique qui permet de stocker plusieurs versions localisées de la même classe dans le référentiel.
ms.assetid: 01e1cee5-d882-45b6-ac93-68533c2c6c9d
ms.tgt_platform: multiple
title: Localisation des informations de classe WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9f1a7e34c3ba230655ebba4c070981a8dab901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320334"
---
# <a name="localizing-wmi-class-information"></a><span data-ttu-id="0a0ab-103">Localisation des informations de classe WMI</span><span class="sxs-lookup"><span data-stu-id="0a0ab-103">Localizing WMI Class Information</span></span>

<span data-ttu-id="0a0ab-104">WMI implémente une technique qui permet de stocker plusieurs versions localisées de la même classe dans le référentiel.</span><span class="sxs-lookup"><span data-stu-id="0a0ab-104">WMI implements a technique that allows multiple localized versions of the same class to be stored in the repository.</span></span>

<span data-ttu-id="0a0ab-105">La définition de classe est divisée en versions suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a0ab-105">The class definition is separated into the following versions:</span></span>

-   <span data-ttu-id="0a0ab-106">Version indépendante du langage qui contient uniquement une définition de classe de base.</span><span class="sxs-lookup"><span data-stu-id="0a0ab-106">A language-neutral version that contains only a basic class definition.</span></span>
-   <span data-ttu-id="0a0ab-107">Version spécifique à un langage qui contient des informations localisées, telles que des descriptions de propriété spécifiques à des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="0a0ab-107">A language-specific version that contains localized information, such as property descriptions that are specific to a locale.</span></span>

<span data-ttu-id="0a0ab-108">Les définitions de classe spécifiques à une langue sont stockées dans un espace de noms enfant sous l’espace de noms qui contient une définition de classe de base indépendante du langage.</span><span class="sxs-lookup"><span data-stu-id="0a0ab-108">The language-specific class definitions are stored in a child namespace beneath the namespace that contains a language-neutral basic class definition.</span></span>

<span data-ttu-id="0a0ab-109">Lorsque vous demandez une définition de classe localisée pour des paramètres régionaux spécifiques, WMI combine la définition de la classe de base et les informations de classe localisées pour former une classe localisée complète.</span><span class="sxs-lookup"><span data-stu-id="0a0ab-109">When you request a localized class definition for a specific locale, WMI combines the basic class definition and the localized class information to form a complete localized class.</span></span> <span data-ttu-id="0a0ab-110">Vous pouvez obtenir une version localisée d’une classe WMI en spécifiant des paramètres régionaux lorsque vous vous connectez à WMI et en définissant un indicateur qui indique que vous souhaitez des informations localisées.</span><span class="sxs-lookup"><span data-stu-id="0a0ab-110">You can get a localized version of a WMI class by specifying a locale when you connect to WMI and setting a flag that indicates that you want localized information.</span></span> <span data-ttu-id="0a0ab-111">WMI fusionne ensuite les informations à partir des versions indépendantes du langage et des versions spécifiques à la langue de la définition de classe pour former une classe localisée.</span><span class="sxs-lookup"><span data-stu-id="0a0ab-111">WMI then merges the information from the language-neutral and the language-specific versions of the class definition to form a localized class.</span></span>

<span data-ttu-id="0a0ab-112">Les classes WMI qui contiennent des informations localisées sont marquées avec le qualificateur d' **Amendement** et sont appelées classes modifiées ; une classe prend en charge les informations localisées si elle possède ce qualificateur.</span><span class="sxs-lookup"><span data-stu-id="0a0ab-112">WMI classes that contain localized information are marked with the **Amendment** qualifier and are called amended classes; a class supports localized information if it has this qualifier.</span></span> <span data-ttu-id="0a0ab-113">Vous pouvez déterminer les paramètres régionaux pour lesquels la classe a été localisée en recherchant un autre qualificateur appelé [**paramètres régionaux**](swbemobjectpath-locale.md).</span><span class="sxs-lookup"><span data-stu-id="0a0ab-113">You can determine which locale the class has been localized for by checking for another qualifier called [**Locale**](swbemobjectpath-locale.md).</span></span> <span data-ttu-id="0a0ab-114">Le qualificateur de paramètres régionaux contient un identificateur de localisation (LCID Windows) qui identifie des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="0a0ab-114">The locale qualifier contains a localization identifier (Windows LCID) that identifies a locale.</span></span> <span data-ttu-id="0a0ab-115">Par exemple, les paramètres régionaux pour l’anglais américain sont 0x40C.</span><span class="sxs-lookup"><span data-stu-id="0a0ab-115">For example, the locale for American English is 0x409.</span></span> <span data-ttu-id="0a0ab-116">Si un qualificateur dans une classe modifiée contient des informations localisées, il contient la version de qualificateur **modifiée** .</span><span class="sxs-lookup"><span data-stu-id="0a0ab-116">If a qualifier in an amended class contains localized information, it contains the **amended** qualifier flavor.</span></span>

<span data-ttu-id="0a0ab-117">La localisation WMI comprend les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a0ab-117">WMI localization includes the following tasks:</span></span>

-   [<span data-ttu-id="0a0ab-118">Création de définitions de classes localisées</span><span class="sxs-lookup"><span data-stu-id="0a0ab-118">Creating localized class definitions</span></span>](creating-localized-class-definitions.md)
-   [<span data-ttu-id="0a0ab-119">Compilation des fichiers MOF localisés</span><span class="sxs-lookup"><span data-stu-id="0a0ab-119">Compiling localized MOF files</span></span>](compiling-localized-mof-files.md)
-   [<span data-ttu-id="0a0ab-120">Localiser des valeurs de propriété</span><span class="sxs-lookup"><span data-stu-id="0a0ab-120">Localizing property values</span></span>](localizing-property-values.md)
-   [<span data-ttu-id="0a0ab-121">Récupération des classes modifiées</span><span class="sxs-lookup"><span data-stu-id="0a0ab-121">Retrieving amended classes</span></span>](retrieving-amended-classes.md)

<span data-ttu-id="0a0ab-122">Pour plus d’informations, consultez [Considérations sur les classes modifiées](amended-class-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="0a0ab-122">For more information, see [Amended Class Considerations](amended-class-considerations.md).</span></span>

 

 



