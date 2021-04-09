---
description: Contient le pourcentage de cycle de responsabilité actuel d’un pin ou d’un canal dans un contrôleur de modulation d’impulsions (PWM).
ms.assetid: 09C0232A-DF5C-4A1C-8138-D3D65E45731B
title: Structure de PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 607fcb1ab429e7cbe9aee593f75d48f0f9d308bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110682"
---
# <a name="pwm_pin_get_active_duty_cycle_percentage_output-structure"></a><span data-ttu-id="27e81-103">\_Structure de \_ sortie de \_ pourcentage du \_ \_ cycle de vie \_ \_ d’un code confidentiel</span><span class="sxs-lookup"><span data-stu-id="27e81-103">PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_OUTPUT structure</span></span>

<span data-ttu-id="27e81-104">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="27e81-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="27e81-105">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="27e81-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="27e81-106">Contient le pourcentage de cycle de responsabilité actuel d’un pin ou d’un canal dans un contrôleur de modulation d’impulsions (PWM).</span><span class="sxs-lookup"><span data-stu-id="27e81-106">Contains the current duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="27e81-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27e81-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="27e81-108">Membres</span><span class="sxs-lookup"><span data-stu-id="27e81-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="27e81-109">**Percentage**</span><span class="sxs-lookup"><span data-stu-id="27e81-109">**Percentage**</span></span>
</dt> <dd>

<span data-ttu-id="27e81-110">Cycle de vie du signal PWM actuel, en tant que \_ pourcentage PWM, qui est une valeur ULONGLONG.</span><span class="sxs-lookup"><span data-stu-id="27e81-110">The current PWM signal duty cycle, as a PWM\_PERCENTAGE, which is a ULONGLONG value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27e81-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27e81-111">Requirements</span></span>



| <span data-ttu-id="27e81-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27e81-112">Requirement</span></span> | <span data-ttu-id="27e81-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="27e81-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27e81-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27e81-114">Minimum supported client</span></span><br/> | <span data-ttu-id="27e81-115">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27e81-115">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="27e81-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27e81-116">Minimum supported server</span></span><br/> | <span data-ttu-id="27e81-117">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27e81-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="27e81-118">Version KMDF minimale</span><span class="sxs-lookup"><span data-stu-id="27e81-118">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="27e81-119">1,19</span><span class="sxs-lookup"><span data-stu-id="27e81-119">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="27e81-120">Version UMDF minimale</span><span class="sxs-lookup"><span data-stu-id="27e81-120">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="27e81-121">2.19</span><span class="sxs-lookup"><span data-stu-id="27e81-121">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="27e81-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="27e81-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="27e81-123"><dt>PWM. h (include PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="27e81-123"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27e81-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27e81-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27e81-125">**\_pourcentage du \_ \_ cycle d' \_ \_ utilisation \_ \_ du code confidentiel PWM d’IOCTL**</span><span class="sxs-lookup"><span data-stu-id="27e81-125">**IOCTL\_PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




