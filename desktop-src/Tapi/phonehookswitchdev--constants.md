---
description: Les \_ constantes d’indicateur de bit PHONEHOOKSWITCHDEV décrivent différents périphériques d’e/s audio, chacun avec son propre hookswitch contrôlable à partir de l’ordinateur.
ms.assetid: b3272a75-87b0-4afc-b2e2-2d65e4b49300
title: Constantes PHONEHOOKSWITCHDEV_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a6727bf8103c35402bebc048de4ed9286650be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544373"
---
# <a name="phonehookswitchdev_-constants"></a><span data-ttu-id="fc799-103">\_Constantes PHONEHOOKSWITCHDEV</span><span class="sxs-lookup"><span data-stu-id="fc799-103">PHONEHOOKSWITCHDEV\_ Constants</span></span>

<span data-ttu-id="fc799-104">Les constantes d’indicateur de bit **PHONEHOOKSWITCHDEV \_** décrivent différents périphériques d’e/s audio, chacun avec son propre hookswitch contrôlable à partir de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fc799-104">The **PHONEHOOKSWITCHDEV\_** bit-flag constants describe various audio I/O devices each with its own hookswitch controllable from the computer.</span></span>

<dl> <dt>

<span data-ttu-id="fc799-105"><span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**\_téléphone PHONEHOOKSWITCHDEV**</span><span class="sxs-lookup"><span data-stu-id="fc799-105"><span id="PHONEHOOKSWITCHDEV_HANDSET"></span><span id="phonehookswitchdev_handset"></span>**PHONEHOOKSWITCHDEV\_HANDSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc799-106">Il s’agit d’un téléphone auriculaire standard et embout.</span><span class="sxs-lookup"><span data-stu-id="fc799-106">This is a standard ear- and mouthpiece phone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc799-107"><span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**\_casque PHONEHOOKSWITCHDEV**</span><span class="sxs-lookup"><span data-stu-id="fc799-107"><span id="PHONEHOOKSWITCHDEV_HEADSET"></span><span id="phonehookswitchdev_headset"></span>**PHONEHOOKSWITCHDEV\_HEADSET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc799-108">Il s’agit d’un casque connecté à l’ensemble téléphonique.</span><span class="sxs-lookup"><span data-stu-id="fc799-108">This is a headset connected to the phone set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc799-109"><span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**PHONEHOOKSWITCHDEV \_ Speaker**</span><span class="sxs-lookup"><span data-stu-id="fc799-109"><span id="PHONEHOOKSWITCHDEV_SPEAKER"></span><span id="phonehookswitchdev_speaker"></span>**PHONEHOOKSWITCHDEV\_SPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fc799-110">Il s’agit d’un haut-parleur et d’un microphone intégrés.</span><span class="sxs-lookup"><span data-stu-id="fc799-110">This is a built-in loudspeaker and microphone.</span></span> <span data-ttu-id="fc799-111">Il peut également s’agir d’un orateur complémentaire connecté en externe au jeu de téléphones.</span><span class="sxs-lookup"><span data-stu-id="fc799-111">This could also be an externally connected adjunct speaker to the telephone set.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc799-112">Notes</span><span class="sxs-lookup"><span data-stu-id="fc799-112">Remarks</span></span>

<span data-ttu-id="fc799-113">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="fc799-113">No extensibility.</span></span> <span data-ttu-id="fc799-114">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="fc799-114">All 32 bits are reserved.</span></span>

<span data-ttu-id="fc799-115">Ces constantes sont utilisées dans la structure de données [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) pour indiquer les fonctionnalités de l’appareil hookswitch d’un appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="fc799-115">These constants are used in the [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) data structure to indicate the hookswitch device capabilities of a phone device.</span></span> <span data-ttu-id="fc799-116">La structure [**PHONESTATUS**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) signale l’état des appareils hookswitch du téléphone.</span><span class="sxs-lookup"><span data-stu-id="fc799-116">The [**PHONESTATUS**](/windows/desktop/api/Tapi/ns-tapi-phonestatus) structure reports the state of the phone's hookswitch devices.</span></span> <span data-ttu-id="fc799-117">La fonction [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) et [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) l’utilisent en tant que paramètre pour sélectionner le périphérique d’e/s du téléphone.</span><span class="sxs-lookup"><span data-stu-id="fc799-117">The function [**phoneSetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonesethookswitch) and [**phoneGetHookSwitch**](/windows/desktop/api/Tapi/nf-tapi-phonegethookswitch) use it as a parameter to select the phone's I/O device.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc799-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc799-118">Requirements</span></span>



| <span data-ttu-id="fc799-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc799-119">Requirement</span></span> | <span data-ttu-id="fc799-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc799-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fc799-121">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="fc799-121">TAPI version</span></span><br/> | <span data-ttu-id="fc799-122">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fc799-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="fc799-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc799-123">Header</span></span><br/>       | <dl> <span data-ttu-id="fc799-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc799-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




