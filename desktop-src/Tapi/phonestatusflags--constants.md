---
description: Les \_ constantes d’indicateur de bit PHONESTATUSFLAGS décrivent une variété d’informations sur l’état des appareils téléphoniques.
ms.assetid: e94da591-49ab-4932-8621-0a62b8a55dd6
title: Constantes PHONESTATUSFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969c2553274037797bdf9abea3e8bdbc1cd8d018
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532978"
---
# <a name="phonestatusflags_-constants"></a><span data-ttu-id="d1ca5-103">\_Constantes PHONESTATUSFLAGS</span><span class="sxs-lookup"><span data-stu-id="d1ca5-103">PHONESTATUSFLAGS\_ Constants</span></span>

<span data-ttu-id="d1ca5-104">Les constantes d’indicateur de bit **PHONESTATUSFLAGS \_** décrivent une variété d’informations sur l’état des appareils téléphoniques.</span><span class="sxs-lookup"><span data-stu-id="d1ca5-104">The **PHONESTATUSFLAGS\_** bit-flag constants describe a variety of phone device status information.</span></span>

<dl> <dt>

<span data-ttu-id="d1ca5-105"><span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**PHONESTATUSFLAGS \_ connecté**</span><span class="sxs-lookup"><span data-stu-id="d1ca5-105"><span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**PHONESTATUSFLAGS\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d1ca5-106">Spécifie si le téléphone est actuellement connecté à l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="d1ca5-106">Specifies whether the phone is currently connected to TAPI.</span></span> <span data-ttu-id="d1ca5-107">**True** si connecté ; sinon, **false** .</span><span class="sxs-lookup"><span data-stu-id="d1ca5-107">**TRUE** if connected, **FALSE** otherwise.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d1ca5-108"><span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**PHONESTATUSFLAGS \_ suspendu**</span><span class="sxs-lookup"><span data-stu-id="d1ca5-108"><span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**PHONESTATUSFLAGS\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d1ca5-109">Spécifie si la manipulation de l’appareil téléphonique par l’interface TAPI est suspendue.</span><span class="sxs-lookup"><span data-stu-id="d1ca5-109">Specifies whether TAPI's manipulation of the phone device is suspended.</span></span> <span data-ttu-id="d1ca5-110">**True** si l’interruption est suspendue ; sinon, **false** .</span><span class="sxs-lookup"><span data-stu-id="d1ca5-110">**TRUE** if suspended, **FALSE** otherwise.</span></span> <span data-ttu-id="d1ca5-111">L’utilisation d’un appareil téléphonique par une application peut être temporairement suspendue quand le commutateur souhaite manipuler le téléphone de manière à ne pas tolérer les interférences de l’application.</span><span class="sxs-lookup"><span data-stu-id="d1ca5-111">An application's use of a phone device can be temporarily suspended when the switch wants to manipulate the phone in a way that cannot tolerate interference from the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1ca5-112">Notes</span><span class="sxs-lookup"><span data-stu-id="d1ca5-112">Remarks</span></span>

<span data-ttu-id="d1ca5-113">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="d1ca5-113">No extensibility.</span></span> <span data-ttu-id="d1ca5-114">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="d1ca5-114">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1ca5-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1ca5-115">Requirements</span></span>



| <span data-ttu-id="d1ca5-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1ca5-116">Requirement</span></span> | <span data-ttu-id="d1ca5-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1ca5-117">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d1ca5-118">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="d1ca5-118">TAPI version</span></span><br/> | <span data-ttu-id="d1ca5-119">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="d1ca5-119">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="d1ca5-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1ca5-120">Header</span></span><br/>       | <dl> <span data-ttu-id="d1ca5-121"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1ca5-121"><dt>Tapi.h</dt></span></span> </dl> |



 

 




