---
description: Contient la période de signal de sortie effective pour un contrôleur de modulation d’impulsions (PWM).
ms.assetid: 280F564F-FF7F-4121-B726-9F9AF9E98EB7
title: Structure de PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: f63057299a8ef37ed1b38151958d2e0061ad2727
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748341"
---
# <a name="pwm_controller_get_actual_period_output-structure"></a><span data-ttu-id="f64eb-103">Structure de sortie de la récupération de la \_ \_ \_ \_ période réelle \_ du contrôleur PWM</span><span class="sxs-lookup"><span data-stu-id="f64eb-103">PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD\_OUTPUT structure</span></span>

<span data-ttu-id="f64eb-104">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="f64eb-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f64eb-105">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="f64eb-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f64eb-106">Contient la période de signal de sortie effective pour un contrôleur de modulation d’impulsions (PWM).</span><span class="sxs-lookup"><span data-stu-id="f64eb-106">Contains the effective output signal period for a Pulse Width Modulation (PWM) controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="f64eb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f64eb-107">Syntax</span></span>


```C++
typedef struct _PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT {
  PWM_PERIOD ActualPeriod;
} PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="f64eb-108">Membres</span><span class="sxs-lookup"><span data-stu-id="f64eb-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f64eb-109">**ActualPeriod**</span><span class="sxs-lookup"><span data-stu-id="f64eb-109">**ActualPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="f64eb-110">La période de signal de sortie effective telle qu’elle sera mesurée sur les canaux de sortie du contrôleur.</span><span class="sxs-lookup"><span data-stu-id="f64eb-110">The effective output signal period as it would be measured on the output channels of the controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f64eb-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f64eb-111">Requirements</span></span>



| <span data-ttu-id="f64eb-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f64eb-112">Requirement</span></span> | <span data-ttu-id="f64eb-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="f64eb-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f64eb-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f64eb-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f64eb-115">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f64eb-115">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f64eb-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f64eb-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f64eb-117">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f64eb-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f64eb-118">Version KMDF minimale</span><span class="sxs-lookup"><span data-stu-id="f64eb-118">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="f64eb-119">1,19</span><span class="sxs-lookup"><span data-stu-id="f64eb-119">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="f64eb-120">Version UMDF minimale</span><span class="sxs-lookup"><span data-stu-id="f64eb-120">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="f64eb-121">2.19</span><span class="sxs-lookup"><span data-stu-id="f64eb-121">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="f64eb-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="f64eb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f64eb-123"><dt>PWM. h (include PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f64eb-123"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f64eb-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f64eb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f64eb-125">**\_récupération de \_ la \_ \_ période réelle \_ par le contrôleur PWM IOCTL**</span><span class="sxs-lookup"><span data-stu-id="f64eb-125">**IOCTL\_PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD**)
</dt> </dl>

 

 




