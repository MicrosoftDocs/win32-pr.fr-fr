---
description: Contient un pourcentage de cycle de responsabilité souhaité pour un pin ou un canal dans un contrôleur de modulation d’impulsions en largeur (PWM).
ms.assetid: CA699703-2D9B-4841-99AD-9C27FF428394
title: Structure de PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 98811ace7ce8fce760e10757b8bf012cc2b9b27d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392935"
---
# <a name="pwm_pin_set_active_duty_cycle_percentage_input-structure"></a><span data-ttu-id="08cdd-103">\_ \_ \_ \_ \_ \_ Structure d’entrée en pourcentage du cycle de vie \_ de l’épinglage activé</span><span class="sxs-lookup"><span data-stu-id="08cdd-103">PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_INPUT structure</span></span>

<span data-ttu-id="08cdd-104">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="08cdd-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="08cdd-105">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="08cdd-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="08cdd-106">Contient un pourcentage de cycle de responsabilité souhaité pour un pin ou un canal dans un contrôleur de modulation d’impulsions en largeur (PWM).</span><span class="sxs-lookup"><span data-stu-id="08cdd-106">Contains a desired duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="08cdd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08cdd-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT;
```



## <a name="members"></a><span data-ttu-id="08cdd-108">Membres</span><span class="sxs-lookup"><span data-stu-id="08cdd-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="08cdd-109">**Percentage**</span><span class="sxs-lookup"><span data-stu-id="08cdd-109">**Percentage**</span></span>
</dt> <dd>

<span data-ttu-id="08cdd-110">Cycle de vie de signal PWM souhaité, en tant que \_ pourcentage PWM, qui est une valeur ULONGLONG.</span><span class="sxs-lookup"><span data-stu-id="08cdd-110">The desired PWM signal duty cycle, as a PWM\_PERCENTAGE, which is a ULONGLONG value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08cdd-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08cdd-111">Requirements</span></span>



| <span data-ttu-id="08cdd-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08cdd-112">Requirement</span></span> | <span data-ttu-id="08cdd-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="08cdd-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08cdd-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08cdd-114">Minimum supported client</span></span><br/> | <span data-ttu-id="08cdd-115">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08cdd-115">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="08cdd-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08cdd-116">Minimum supported server</span></span><br/> | <span data-ttu-id="08cdd-117">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08cdd-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="08cdd-118">Version KMDF minimale</span><span class="sxs-lookup"><span data-stu-id="08cdd-118">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="08cdd-119">1,19</span><span class="sxs-lookup"><span data-stu-id="08cdd-119">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="08cdd-120">Version UMDF minimale</span><span class="sxs-lookup"><span data-stu-id="08cdd-120">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="08cdd-121">2.19</span><span class="sxs-lookup"><span data-stu-id="08cdd-121">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="08cdd-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="08cdd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="08cdd-123"><dt>PWM. h (include PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08cdd-123"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08cdd-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08cdd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08cdd-125">**\_pourcentage du \_ cycle \_ de \_ \_ \_ vie \_ du pin PWM d’IOCTL activé**</span><span class="sxs-lookup"><span data-stu-id="08cdd-125">**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




