---
description: Définit le niveau de protection HDCP pour la lecture des DVD, en suivant les règles du système de brouillage du contenu DVD (CSS).
ms.assetid: 8d9ecb9b-8528-4b23-ab2f-234ba2cb7ed0
title: OPM_SET_PROTECTION_LEVEL_ACCORDING_TO_CSS_DVD (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971d288367bdc5c59e11bdfd5b86fb233755c95e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114378"
---
# <a name="opm_set_protection_level_according_to_css_dvd"></a><span data-ttu-id="3415a-103">\_ \_ niveau de protection de l’ensemble OPM \_ selon le \_ \_ \_ \_ DVD CSS</span><span class="sxs-lookup"><span data-stu-id="3415a-103">OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD</span></span>

<span data-ttu-id="3415a-104">Définit le niveau de protection HDCP pour la lecture des DVD, en suivant les règles du système de brouillage du contenu DVD (CSS).</span><span class="sxs-lookup"><span data-stu-id="3415a-104">Sets the HDCP protection level for DVD playback, following DVD Content Scramble System (CSS) rules.</span></span>



| <span data-ttu-id="3415a-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3415a-105">Requirement</span></span> | <span data-ttu-id="3415a-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="3415a-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3415a-107">GUID de la commande</span><span class="sxs-lookup"><span data-stu-id="3415a-107">Command GUID</span></span> | <span data-ttu-id="3415a-108">\_ \_ niveau de protection de l’ensemble OPM \_ selon le \_ \_ \_ \_ DVD CSS</span><span class="sxs-lookup"><span data-stu-id="3415a-108">OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD</span></span>                                                |
| <span data-ttu-id="3415a-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="3415a-109">Input data</span></span>   | <span data-ttu-id="3415a-110">Structure [**des \_ \_ paramètres de \_ niveau \_ de protection de l’ensemble OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)</span><span class="sxs-lookup"><span data-stu-id="3415a-110">An [**OPM\_SET\_PROTECTION\_LEVEL\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3415a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3415a-111">Remarks</span></span>

<span data-ttu-id="3415a-112">Cette commande permet de définir High-Bandwidth protection du contenu numérique (HDCP) lors de la diffusion de DVD standard.</span><span class="sxs-lookup"><span data-stu-id="3415a-112">This command is used to set High-Bandwidth Digital Content Protection (HDCP) when playing standard DVDs.</span></span> <span data-ttu-id="3415a-113">Contrairement à la commande de [**\_ \_ \_ niveau de protection Set de OPM**](opm-set-protection-level.md) , si HDCP ne peut pas être défini pour une raison quelconque, cette commande n’arrête pas la lecture.</span><span class="sxs-lookup"><span data-stu-id="3415a-113">Unlike the [**OPM\_SET\_PROTECTION\_LEVEL**](opm-set-protection-level.md) command, if HDCP cannot be set for some reason, this command does not stop playback.</span></span> <span data-ttu-id="3415a-114">(Les règles CSS de DVD contiennent un « meilleur effort » pour les joueurs.) Dans le cas contraire, cette commande est identique à la commande de **\_ \_ \_ niveau de protection Set OPM** .</span><span class="sxs-lookup"><span data-stu-id="3415a-114">(DVD CSS rules contain a "best effort" provision for players.) Otherwise, this command is identical to the **OPM\_SET\_PROTECTION\_LEVEL** command.</span></span>

## <a name="requirements"></a><span data-ttu-id="3415a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3415a-115">Requirements</span></span>



| <span data-ttu-id="3415a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3415a-116">Requirement</span></span> | <span data-ttu-id="3415a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3415a-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3415a-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3415a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3415a-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3415a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3415a-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3415a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3415a-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3415a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3415a-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="3415a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3415a-123"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3415a-123"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3415a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3415a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3415a-125">**IOPMVideoOutput :: configure**</span><span class="sxs-lookup"><span data-stu-id="3415a-125">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="3415a-126">Commandes OPM</span><span class="sxs-lookup"><span data-stu-id="3415a-126">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




