---
title: Conception d’animation
description: Conception d’animation
ms.assetid: 8812e4cc-9062-4c65-81ef-229bd29534cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7d6cf86cfe115ec209fb305f0ae017951bd7f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939845"
---
# <a name="animation-design"></a><span data-ttu-id="ff76c-103">Conception d’animation</span><span class="sxs-lookup"><span data-stu-id="ff76c-103">Animation Design</span></span>

<span data-ttu-id="ff76c-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ff76c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

### <a name="image-design"></a><span data-ttu-id="ff76c-105">Conception d’image</span><span class="sxs-lookup"><span data-stu-id="ff76c-105">Image Design</span></span>

<span data-ttu-id="ff76c-106">Utilisez la palette de Microsoft Office lors de la conception de vos caractères pour réduire les problèmes potentiels de réalisation de la palette.</span><span class="sxs-lookup"><span data-stu-id="ff76c-106">Use the Microsoft Office Palette when designing your characters to minimize any potential palette realization issues.</span></span> <span data-ttu-id="ff76c-107">Évitez de sélectionner une couleur de transparence similaire aux couleurs que vous utilisez dans votre document.</span><span class="sxs-lookup"><span data-stu-id="ff76c-107">Avoid selecting a transparency color that is similar to the colors that you use in your document.</span></span>

### <a name="sounds"></a><span data-ttu-id="ff76c-108">Sons</span><span class="sxs-lookup"><span data-stu-id="ff76c-108">Sounds</span></span>

<span data-ttu-id="ff76c-109">Microsoft agent vous permet de lire des sons dans vos animations.</span><span class="sxs-lookup"><span data-stu-id="ff76c-109">Microsoft Agent enables you to play sounds in your animations.</span></span> <span data-ttu-id="ff76c-110">Nous vous recommandons de ne pas inclure de sons pour vos animations **inactives** .</span><span class="sxs-lookup"><span data-stu-id="ff76c-110">We recommend you do not include sounds for your **Idle** animations.</span></span> <span data-ttu-id="ff76c-111">Ainsi, il n’y aura pas de délai au milieu de l’animation, si l’agent doit charger la DLL multimédia système.</span><span class="sxs-lookup"><span data-stu-id="ff76c-111">This is so there won't be a delay in the middle of the animation, if Agent has to load the system multimedia DLL.</span></span>

### <a name="frame-size"></a><span data-ttu-id="ff76c-112">Taille de trame</span><span class="sxs-lookup"><span data-stu-id="ff76c-112">Frame Size</span></span>

<span data-ttu-id="ff76c-113">Les compagnons Office standard sont 123 x 93 pixels.</span><span class="sxs-lookup"><span data-stu-id="ff76c-113">Typical Office Assistants are 123 x 93 pixels.</span></span> <span data-ttu-id="ff76c-114">Bien que vous puissiez créer des caractères d’autres tailles, ceux-ci seront mis à l’échelle à 123 x 93 dans la Galerie de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="ff76c-114">While you can create characters of other sizes, they will be scaled to 123 x 93 in the Assistant Gallery.</span></span>

### <a name="frame-transition"></a><span data-ttu-id="ff76c-115">Transition de frame</span><span class="sxs-lookup"><span data-stu-id="ff76c-115">Frame Transition</span></span>

<span data-ttu-id="ff76c-116">Toutes les animations, à l’exception de **adieu**, **Greetings**, **Show** et **Hide** , doivent commencer et se terminer par l’animation RestPose.</span><span class="sxs-lookup"><span data-stu-id="ff76c-116">All animations except for **Goodbye**, **Greeting**, **Show** and **Hide** should begin and end with the RestPose animation.</span></span> <span data-ttu-id="ff76c-117">Microsoft Office ne lise pas les animations de **retour** explicites, vous ne devez pas les définir.</span><span class="sxs-lookup"><span data-stu-id="ff76c-117">Microsoft Office does not play explicit **Return** animations, so you should not define them.</span></span> <span data-ttu-id="ff76c-118">Toutes les animations doivent également avoir une branche de sortie.</span><span class="sxs-lookup"><span data-stu-id="ff76c-118">All animations should also have Exit Branching.</span></span> <span data-ttu-id="ff76c-119">La création de branche de sortie nous permet de mettre en place et de terminer l’animation en cours avant d’appeler l’animation suivante.</span><span class="sxs-lookup"><span data-stu-id="ff76c-119">Exit branching enables us to 'hurry up and finish' the current animation before we call the next animation.</span></span> <span data-ttu-id="ff76c-120">Si vous ne fournissez pas de branchement de sortie, la transition entre les animations peut être saccadée.</span><span class="sxs-lookup"><span data-stu-id="ff76c-120">If you don't supply Exit Branching, the transition between animations may be jerky.</span></span>

### <a name="character-properties"></a><span data-ttu-id="ff76c-121">Propriétés des caractères</span><span class="sxs-lookup"><span data-stu-id="ff76c-121">Character Properties</span></span>

<span data-ttu-id="ff76c-122">Microsoft agent vous permet de définir les propriétés [**Name**](name-property.md), [**Description**](description-property.md) et [**ExtraData**](extradata-property.md) du caractère.</span><span class="sxs-lookup"><span data-stu-id="ff76c-122">Microsoft Agent enables you to set the character's [**Name**](name-property.md), [**Description**](description-property.md) and [**ExtraData**](extradata-property.md) properties.</span></span> <span data-ttu-id="ff76c-123">Microsoft Office utilise le champ **ExtraData** pour contenir une ou plusieurs expressions d’introduction et expressions de rappel.</span><span class="sxs-lookup"><span data-stu-id="ff76c-123">Microsoft Office uses the **ExtraData** field to hold to one or more Introduction Phrases and Reminder Phrases.</span></span> <span data-ttu-id="ff76c-124">Microsoft Office choisit les autres expressions de présentation à placer dans la bulle de reconnaissance vocale dans la Galerie de l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="ff76c-124">Microsoft Office picks from the other Introduction Phrases to put in the speech balloon in the Assistant Gallery.</span></span> <span data-ttu-id="ff76c-125">Nous utilisons les phrases de rappel lorsque vous recevez un rappel d’Outlook.</span><span class="sxs-lookup"><span data-stu-id="ff76c-125">We use the Reminder Phrases when you receive a reminder from Outlook.</span></span>

<span data-ttu-id="ff76c-126">Le champ [**ExtraData**](extradata-property.md) est mis en forme comme suit :</span><span class="sxs-lookup"><span data-stu-id="ff76c-126">The [**ExtraData**](extradata-property.md) field is formatted as follows:</span></span>

<span data-ttu-id="ff76c-127">IntroPhrase1~~IntroPhrase2~~IntroPhrase3 ^ ^ ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3</span><span class="sxs-lookup"><span data-stu-id="ff76c-127">IntroPhrase1~~IntroPhrase2~~IntroPhrase3^^ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3</span></span>

<span data-ttu-id="ff76c-128">Les expressions Intro sont séparées par une paire de caractères tildes (~), suivis de phrases de rappel.</span><span class="sxs-lookup"><span data-stu-id="ff76c-128">Intro Phrases are separated by a pair of tilde characters (~), followed by Reminder Phrases.</span></span> <span data-ttu-id="ff76c-129">Ces expressions de rappel sont également séparées par une paire de caractères tilde.</span><span class="sxs-lookup"><span data-stu-id="ff76c-129">These Reminder Phrases are also separated by a pair of tilde characters.</span></span> <span data-ttu-id="ff76c-130">Les deux ensembles d’expressions sont séparés par deux caractères de signe insertion (^^).</span><span class="sxs-lookup"><span data-stu-id="ff76c-130">The two sets of phrases are separated by two caret characters (^^).</span></span> <span data-ttu-id="ff76c-131">Il n’existe pas de limite au nombre de chaque type d’expression, sauf qu’il doit y en avoir au moins un.</span><span class="sxs-lookup"><span data-stu-id="ff76c-131">There is no limit to the number of each kind of phrase, except that there must be at least one of each.</span></span>

 

 




