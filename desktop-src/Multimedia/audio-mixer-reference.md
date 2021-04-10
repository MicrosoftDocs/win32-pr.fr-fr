---
title: Référence du mélangeur audio
description: Référence du mélangeur audio
ms.assetid: 9d8751b1-9c0b-4238-a961-27c09a869bb3
keywords:
- audio multimédia, mixages audio
- audio, mixages audio
- audio multimédia, référence du mélangeur
- audio, référence du mélangeur
- mixages audio, référence
- mixageions, référence
- référence pour les mixages audio, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1d86f305714d72631b56495753417699b1a146
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104199201"
---
# <a name="audio-mixer-reference"></a><span data-ttu-id="38289-110">Référence du mélangeur audio</span><span class="sxs-lookup"><span data-stu-id="38289-110">Audio Mixer Reference</span></span>

<span data-ttu-id="38289-111">Cette section décrit les fonctions, les structures et les messages associés aux mixages audio.</span><span class="sxs-lookup"><span data-stu-id="38289-111">This section describes the functions, structures, and messages associated with audio mixers.</span></span> <span data-ttu-id="38289-112">Ces éléments sont regroupés comme suit.</span><span class="sxs-lookup"><span data-stu-id="38289-112">These elements are grouped as follows.</span></span>

## <a name="querying-devices"></a><span data-ttu-id="38289-113">Interrogation des appareils</span><span class="sxs-lookup"><span data-stu-id="38289-113">Querying Devices</span></span>

-   [<span data-ttu-id="38289-114">**MIXERCAPS**</span><span class="sxs-lookup"><span data-stu-id="38289-114">**MIXERCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps)
-   [<span data-ttu-id="38289-115">**mixerGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="38289-115">**mixerGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps)
-   [<span data-ttu-id="38289-116">**mixerGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="38289-116">**mixerGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs)

## <a name="opening-and-closing"></a><span data-ttu-id="38289-117">Ouverture et fermeture</span><span class="sxs-lookup"><span data-stu-id="38289-117">Opening and Closing</span></span>

-   [<span data-ttu-id="38289-118">**mixerClose**</span><span class="sxs-lookup"><span data-stu-id="38289-118">**mixerClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose)
-   [<span data-ttu-id="38289-119">**mixerOpen**</span><span class="sxs-lookup"><span data-stu-id="38289-119">**mixerOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)

## <a name="retrieving-mixer-identifiers"></a><span data-ttu-id="38289-120">Récupération des identificateurs de mixage</span><span class="sxs-lookup"><span data-stu-id="38289-120">Retrieving Mixer Identifiers</span></span>

-   [<span data-ttu-id="38289-121">**mixerGetID**</span><span class="sxs-lookup"><span data-stu-id="38289-121">**mixerGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid)

## <a name="retrieving-line-controls"></a><span data-ttu-id="38289-122">Récupération de contrôles Line</span><span class="sxs-lookup"><span data-stu-id="38289-122">Retrieving Line Controls</span></span>

-   [<span data-ttu-id="38289-123">**MIXERCONTROL**</span><span class="sxs-lookup"><span data-stu-id="38289-123">**MIXERCONTROL**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercontrol)
-   [<span data-ttu-id="38289-124">**mixerGetLineControls**</span><span class="sxs-lookup"><span data-stu-id="38289-124">**mixerGetLineControls**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols)
-   [<span data-ttu-id="38289-125">**MIXERLINECONTROLS**</span><span class="sxs-lookup"><span data-stu-id="38289-125">**MIXERLINECONTROLS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols)

## <a name="changing-control-attributes"></a><span data-ttu-id="38289-126">Modification des attributs de contrôle</span><span class="sxs-lookup"><span data-stu-id="38289-126">Changing Control Attributes</span></span>

-   [<span data-ttu-id="38289-127">**MIXERCONTROLDETAILS**</span><span class="sxs-lookup"><span data-stu-id="38289-127">**MIXERCONTROLDETAILS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta)
-   <span data-ttu-id="38289-128">[**MIXERCONTROLDETAILS \_ booléen**](/previous-versions//dd757295(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38289-128">[**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85))</span></span>
-   <span data-ttu-id="38289-129">[**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38289-129">[**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85))</span></span>
-   <span data-ttu-id="38289-130">[**MIXERCONTROLDETAILS \_ signé**](/previous-versions//dd757297(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38289-130">[**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85))</span></span>
-   <span data-ttu-id="38289-131">[**MIXERCONTROLDETAILS \_ non signé**](/previous-versions//dd757298(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38289-131">[**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85))</span></span>
-   [<span data-ttu-id="38289-132">**mixerGetControlDetails**</span><span class="sxs-lookup"><span data-stu-id="38289-132">**mixerGetControlDetails**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails)
-   [<span data-ttu-id="38289-133">**mixerSetControlDetails**</span><span class="sxs-lookup"><span data-stu-id="38289-133">**mixerSetControlDetails**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails)

## <a name="retrieving-line-information"></a><span data-ttu-id="38289-134">Récupération des informations de ligne</span><span class="sxs-lookup"><span data-stu-id="38289-134">Retrieving Line Information</span></span>

-   [<span data-ttu-id="38289-135">**mixerGetLineInfo**</span><span class="sxs-lookup"><span data-stu-id="38289-135">**mixerGetLineInfo**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo)
-   [<span data-ttu-id="38289-136">**MIXERLINE**</span><span class="sxs-lookup"><span data-stu-id="38289-136">**MIXERLINE**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixerline)
-   [<span data-ttu-id="38289-137">**\_modification du \_ contrôle \_ MIXM mm**</span><span class="sxs-lookup"><span data-stu-id="38289-137">**MM\_MIXM\_CONTROL\_CHANGE**</span></span>](mm-mixm-control-change.md)
-   [<span data-ttu-id="38289-138">**MM \_ \_ modification de ligne MIXM \_**</span><span class="sxs-lookup"><span data-stu-id="38289-138">**MM\_MIXM\_LINE\_CHANGE**</span></span>](mm-mixm-line-change.md)

## <a name="sending-user-defined-messages"></a><span data-ttu-id="38289-139">Envoi de messages de User-Defined</span><span class="sxs-lookup"><span data-stu-id="38289-139">Sending User-Defined Messages</span></span>

-   [<span data-ttu-id="38289-140">**mixerMessage**</span><span class="sxs-lookup"><span data-stu-id="38289-140">**mixerMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixermessage)

## <a name="related-topics"></a><span data-ttu-id="38289-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="38289-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38289-142">Référence du mélangeur audio</span><span class="sxs-lookup"><span data-stu-id="38289-142">Audio Mixer Reference</span></span>](audio-mixer-reference.md)
</dt> </dl>

 

 