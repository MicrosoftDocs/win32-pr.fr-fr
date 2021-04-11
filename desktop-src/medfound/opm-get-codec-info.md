---
description: Obtient la valeur mérite d’un codec matériel.
ms.assetid: 51987a79-78bf-41b2-8349-8c2725dd89d6
title: OPM_GET_CODEC_INFO (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf310ae3dafee7823119b2d5d5bd2c6b61fe822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201866"
---
# <a name="opm_get_codec_info"></a><span data-ttu-id="a3268-103">\_informations sur l’extraction de \_ codec OPM \_</span><span class="sxs-lookup"><span data-stu-id="a3268-103">OPM\_GET\_CODEC\_INFO</span></span>

<span data-ttu-id="a3268-104">Obtient la valeur mérite d’un codec matériel.</span><span class="sxs-lookup"><span data-stu-id="a3268-104">Gets the merit value of a hardware codec.</span></span>



| <span data-ttu-id="a3268-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3268-105">Requirement</span></span> | <span data-ttu-id="a3268-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3268-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3268-107">GUID de la demande</span><span class="sxs-lookup"><span data-stu-id="a3268-107">Request GUID</span></span> | <span data-ttu-id="a3268-108">**\_informations sur l’extraction de \_ codec OPM \_**</span><span class="sxs-lookup"><span data-stu-id="a3268-108">**OPM\_GET\_CODEC\_INFO**</span></span>                                                                 |
| <span data-ttu-id="a3268-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="a3268-109">Input data</span></span>   | <span data-ttu-id="a3268-110">Une structure de [**\_ \_ \_ \_ paramètres d’extraction de codec OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)</span><span class="sxs-lookup"><span data-stu-id="a3268-110">An [**OPM\_GET\_CODEC\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) structure</span></span>   |
| <span data-ttu-id="a3268-111">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="a3268-111">Return data</span></span>  | <span data-ttu-id="a3268-112">Structure d’informations de l' [**\_ extraction de \_ codec \_ \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information)</span><span class="sxs-lookup"><span data-stu-id="a3268-112">An [**OPM\_GET\_CODEC\_INFO\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a3268-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a3268-113">Remarks</span></span>

<span data-ttu-id="a3268-114">Bien que cette commande utilise l’interface de [sortie Protection Manager](output-protection-manager.md) (OPM), elle s’applique uniquement aux encodeurs et aux décodeurs matériels.</span><span class="sxs-lookup"><span data-stu-id="a3268-114">Although this command uses the [Output Protection Manager](output-protection-manager.md) (OPM) interface, it applies only to hardware encoders and decoders.</span></span> <span data-ttu-id="a3268-115">Elle ne s’applique pas aux périphériques de sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="a3268-115">It does not apply to video output devices.</span></span>

<span data-ttu-id="a3268-116">En règle générale, vous ne devez pas utiliser cette commande directement.</span><span class="sxs-lookup"><span data-stu-id="a3268-116">Generally, you should not use this command directly.</span></span> <span data-ttu-id="a3268-117">Pour obtenir la valeur mérite d’un codec matériel, appelez la fonction [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) .</span><span class="sxs-lookup"><span data-stu-id="a3268-117">To get the merit value for a hardware codec, call the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function.</span></span> <span data-ttu-id="a3268-118">Cette fonction effectue tous les appels OPM nécessaires à l’envoi de la commande d' **\_ extraction d' \_ \_ informations de codec OPM** .</span><span class="sxs-lookup"><span data-stu-id="a3268-118">This function performs all of the OPM calls needed to send the **OPM\_GET\_CODEC\_INFO** command.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3268-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3268-119">Requirements</span></span>



| <span data-ttu-id="a3268-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3268-120">Requirement</span></span> | <span data-ttu-id="a3268-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3268-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a3268-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3268-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a3268-123">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3268-123">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a3268-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3268-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a3268-125">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a3268-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a3268-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3268-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3268-127"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3268-127"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3268-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3268-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3268-129">Demandes d’État OPM</span><span class="sxs-lookup"><span data-stu-id="a3268-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> <dt>

[<span data-ttu-id="a3268-130">Gestionnaire de protection de sortie</span><span class="sxs-lookup"><span data-stu-id="a3268-130">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> <dt>

[<span data-ttu-id="a3268-131">**IOPMVideoOutput :: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="a3268-131">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> </dl>

 

 




