---
description: Les \_ constantes d’indicateur de bit PHONEHOOKSWITCHMODE décrivent les composants de microphone et de haut-parleur d’un appareil hookswitch.
ms.assetid: 532bf089-d5ca-4a04-847d-69e48990ff5c
title: Constantes PHONEHOOKSWITCHMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8028cb531d5b38185edf75ae58e4c3c855398f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521780"
---
# <a name="phonehookswitchmode_-constants"></a><span data-ttu-id="f7369-103">\_Constantes PHONEHOOKSWITCHMODE</span><span class="sxs-lookup"><span data-stu-id="f7369-103">PHONEHOOKSWITCHMODE\_ Constants</span></span>

<span data-ttu-id="f7369-104">Les constantes d’indicateur de bit **PHONEHOOKSWITCHMODE \_** décrivent les composants de microphone et de haut-parleur d’un appareil hookswitch.</span><span class="sxs-lookup"><span data-stu-id="f7369-104">The **PHONEHOOKSWITCHMODE\_** bit-flag constants describe the microphone and speaker components of a hookswitch device.</span></span>

<dl> <dt>

<span data-ttu-id="f7369-105"><span id="PHONEHOOKSWITCHMODE_MIC"></span><span id="phonehookswitchmode_mic"></span>**\_MIC PHONEHOOKSWITCHMODE**</span><span class="sxs-lookup"><span data-stu-id="f7369-105"><span id="PHONEHOOKSWITCHMODE_MIC"></span><span id="phonehookswitchmode_mic"></span>**PHONEHOOKSWITCHMODE\_MIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f7369-106">Le microphone de l’appareil est actif, le haut-parleur est muet.</span><span class="sxs-lookup"><span data-stu-id="f7369-106">The device's microphone is active, the speaker is mute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7369-107"><span id="PHONEHOOKSWITCHMODE_MICSPEAKER"></span><span id="phonehookswitchmode_micspeaker"></span>**PHONEHOOKSWITCHMODE \_ MICSPEAKER**</span><span class="sxs-lookup"><span data-stu-id="f7369-107"><span id="PHONEHOOKSWITCHMODE_MICSPEAKER"></span><span id="phonehookswitchmode_micspeaker"></span>**PHONEHOOKSWITCHMODE\_MICSPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f7369-108">Le microphone et le haut-parleur de l’appareil sont tous deux actifs.</span><span class="sxs-lookup"><span data-stu-id="f7369-108">The device's microphone and speaker are both active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7369-109"><span id="PHONEHOOKSWITCHMODE_ONHOOK"></span><span id="phonehookswitchmode_onhook"></span>**PHONEHOOKSWITCHMODE \_ ONHOOK**</span><span class="sxs-lookup"><span data-stu-id="f7369-109"><span id="PHONEHOOKSWITCHMODE_ONHOOK"></span><span id="phonehookswitchmode_onhook"></span>**PHONEHOOKSWITCHMODE\_ONHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f7369-110">Le microphone et le haut-parleur de l’appareil sont tous deux OnHook.</span><span class="sxs-lookup"><span data-stu-id="f7369-110">The device's microphone and speaker are both onhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7369-111"><span id="PHONEHOOKSWITCHMODE_SPEAKER"></span><span id="phonehookswitchmode_speaker"></span>**PHONEHOOKSWITCHMODE \_ Speaker**</span><span class="sxs-lookup"><span data-stu-id="f7369-111"><span id="PHONEHOOKSWITCHMODE_SPEAKER"></span><span id="phonehookswitchmode_speaker"></span>**PHONEHOOKSWITCHMODE\_SPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f7369-112">Le haut-parleur de l’appareil est actif, le microphone est muet.</span><span class="sxs-lookup"><span data-stu-id="f7369-112">The device's speaker is active, the microphone is mute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7369-113"><span id="PHONEHOOKSWITCHMODE_UNKNOWN"></span><span id="phonehookswitchmode_unknown"></span>**PHONEHOOKSWITCHMODE \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="f7369-113"><span id="PHONEHOOKSWITCHMODE_UNKNOWN"></span><span id="phonehookswitchmode_unknown"></span>**PHONEHOOKSWITCHMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f7369-114">Le mode hookswitch de l’appareil est actuellement inconnu.</span><span class="sxs-lookup"><span data-stu-id="f7369-114">The device's hookswitch mode is currently unknown.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7369-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f7369-115">Remarks</span></span>

<span data-ttu-id="f7369-116">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="f7369-116">No extensibility.</span></span> <span data-ttu-id="f7369-117">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="f7369-117">All 32 bits are reserved.</span></span>

<span data-ttu-id="f7369-118">Ces constantes sont utilisées pour fournir un niveau individuel de contrôle sur les composants de microphone et de haut-parleur d’un appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="f7369-118">These constants are used to provide an individual level of control over the microphone and speaker components of a phone device.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7369-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7369-119">Requirements</span></span>



| <span data-ttu-id="f7369-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7369-120">Requirement</span></span> | <span data-ttu-id="f7369-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7369-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f7369-122">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="f7369-122">TAPI version</span></span><br/> | <span data-ttu-id="f7369-123">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f7369-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f7369-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7369-124">Header</span></span><br/>       | <dl> <span data-ttu-id="f7369-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7369-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




