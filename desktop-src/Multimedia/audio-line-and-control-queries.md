---
title: Requêtes audio et de contrôle
description: Requêtes audio et de contrôle
ms.assetid: f0954fc7-9961-410a-a638-a7025fb2616a
keywords:
- audio multimédia, contrôles de mixage
- audio, contrôles de mixage
- mixages audio, lignes audio
- lignes audio
- mixages audio, contrôles
- mélangeurs, contrôles
- mixages, lignes audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec581f2ddb54b06de8fa1a1b1356d9b80422ad5c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725085"
---
# <a name="audio-line-and-control-queries"></a><span data-ttu-id="a6f39-110">Requêtes audio et de contrôle</span><span class="sxs-lookup"><span data-stu-id="a6f39-110">Audio Line and Control Queries</span></span>

<span data-ttu-id="a6f39-111">Les services de mixage fournissent des fonctions permettant de déterminer les informations sur les lignes audio, les contrôles de ligne audio et les détails de contrôle.</span><span class="sxs-lookup"><span data-stu-id="a6f39-111">The mixer services provide functions for determining information about audio lines, audio-line controls, and control details.</span></span> <span data-ttu-id="a6f39-112">Les services fournissent également des fonctions permettant de définir les détails du contrôle.</span><span class="sxs-lookup"><span data-stu-id="a6f39-112">The services also provide functions for setting control details.</span></span>

<span data-ttu-id="a6f39-113">Vous pouvez utiliser la fonction [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) pour récupérer des informations sur une ligne audio spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a6f39-113">You can use the [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) function to retrieve information about a specified audio line.</span></span> <span data-ttu-id="a6f39-114">Cette fonction remplit la structure [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) pour une ligne audio source, une ligne audio de destination ou un identificateur de ligne spécifiés.</span><span class="sxs-lookup"><span data-stu-id="a6f39-114">This function fills the [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) structure for a specified source audio line, destination audio line, or line identifier.</span></span> <span data-ttu-id="a6f39-115">La structure comprend le numéro de ligne de destination, le nombre de canaux dans la ligne audio, ainsi qu’un nom abrégé et un nom long pour la ligne audio.</span><span class="sxs-lookup"><span data-stu-id="a6f39-115">The structure includes the destination line number, the number of channels in the audio line, as well as a short and a long name for the audio line.</span></span>

<span data-ttu-id="a6f39-116">La fonction [**mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) récupère des informations générales sur un ou plusieurs contrôles associés à une ligne audio.</span><span class="sxs-lookup"><span data-stu-id="a6f39-116">The [**mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) function retrieves general information about one or more controls associated with an audio line.</span></span> <span data-ttu-id="a6f39-117">Cette fonction remplit la structure [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) avec des informations sur le ou les contrôles spécifiés.</span><span class="sxs-lookup"><span data-stu-id="a6f39-117">This function fills the [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) structure with information about the specified control or controls.</span></span> <span data-ttu-id="a6f39-118">Vous pouvez utiliser **mixerGetLineControls** pour récupérer des propriétés de contrôle pour l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="a6f39-118">You can use **mixerGetLineControls** to retrieve control properties for one of the following:</span></span>

-   <span data-ttu-id="a6f39-119">Tous les contrôles pour une ligne source spécifiée</span><span class="sxs-lookup"><span data-stu-id="a6f39-119">All controls for a specified source line</span></span>
-   <span data-ttu-id="a6f39-120">Contrôle spécifié pour une ligne source spécifiée</span><span class="sxs-lookup"><span data-stu-id="a6f39-120">A specified control for a specified source line</span></span>
-   <span data-ttu-id="a6f39-121">Premier contrôle d’une classe spécifique pour une ligne source spécifiée</span><span class="sxs-lookup"><span data-stu-id="a6f39-121">The first control of a specific class for a specified source line</span></span>

<span data-ttu-id="a6f39-122">La fonction [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) récupère les propriétés d’un contrôle unique associé à une ligne audio.</span><span class="sxs-lookup"><span data-stu-id="a6f39-122">The [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) function retrieves properties of a single control associated with an audio line.</span></span> <span data-ttu-id="a6f39-123">Cette fonction remplit la structure [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) avec les valeurs actuelles d’un contrôle.</span><span class="sxs-lookup"><span data-stu-id="a6f39-123">This function fills the [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) structure with the current values for a control.</span></span>

<span data-ttu-id="a6f39-124">La fonction [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) utilise le contenu de la structure **MIXERCONTROLDETAILS** pour définir les propriétés du contrôle spécifié.</span><span class="sxs-lookup"><span data-stu-id="a6f39-124">The [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) function uses the contents of the **MIXERCONTROLDETAILS** structure to set the properties of the specified control.</span></span> <span data-ttu-id="a6f39-125">Vous devez vous assurer que tous les membres de cette structure sont remplis avant d’appeler **mixerSetControlDetails**.</span><span class="sxs-lookup"><span data-stu-id="a6f39-125">You must ensure that all members of this structure are filled before you call **mixerSetControlDetails**.</span></span>

 

 