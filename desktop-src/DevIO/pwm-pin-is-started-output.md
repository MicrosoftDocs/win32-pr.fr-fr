---
description: Contient l’état actuel de génération de signal d’un code confidentiel.
ms.assetid: 07D76F8D-C5B5-4500-BFA2-452989868027
title: Structure de PWM_PIN_IS_STARTED_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_IS_STARTED_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 11350c3bb0fbec0f05ab3153c339f8fa30baeed5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517173"
---
# <a name="pwm_pin_is_started_output-structure"></a><span data-ttu-id="89701-103">La \_ structure de sortie du code confidentiel PWM \_ est \_ démarrée \_</span><span class="sxs-lookup"><span data-stu-id="89701-103">PWM\_PIN\_IS\_STARTED\_OUTPUT structure</span></span>

<span data-ttu-id="89701-104">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="89701-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="89701-105">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="89701-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="89701-106">Contient l’état actuel de génération de signal d’un code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="89701-106">Contains the current signal generation state of a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="89701-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89701-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_IS_STARTED_OUTPUT {
  BOOLEAN IsStarted;
} PWM_PIN_IS_STARTED_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="89701-108">Membres</span><span class="sxs-lookup"><span data-stu-id="89701-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="89701-109">**IsStarted (**</span><span class="sxs-lookup"><span data-stu-id="89701-109">**IsStarted**</span></span>
</dt> <dd>

<span data-ttu-id="89701-110">État de génération de signal actuel du code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="89701-110">The pin current signal generation state.</span></span> <span data-ttu-id="89701-111">La valeur true indique que le code PIN est démarré.</span><span class="sxs-lookup"><span data-stu-id="89701-111">A value of true means that the pin is started.</span></span> <span data-ttu-id="89701-112">La valeur false indique que le code PIN est arrêté.</span><span class="sxs-lookup"><span data-stu-id="89701-112">A value of false means that the pin is stopped.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89701-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89701-113">Requirements</span></span>



| <span data-ttu-id="89701-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89701-114">Requirement</span></span> | <span data-ttu-id="89701-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="89701-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89701-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89701-116">Minimum supported client</span></span><br/> | <span data-ttu-id="89701-117">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89701-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="89701-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89701-118">Minimum supported server</span></span><br/> | <span data-ttu-id="89701-119">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89701-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="89701-120">Version KMDF minimale</span><span class="sxs-lookup"><span data-stu-id="89701-120">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="89701-121">1,19</span><span class="sxs-lookup"><span data-stu-id="89701-121">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="89701-122">Version UMDF minimale</span><span class="sxs-lookup"><span data-stu-id="89701-122">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="89701-123">2.19</span><span class="sxs-lookup"><span data-stu-id="89701-123">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="89701-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="89701-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="89701-125"><dt>PWM. h (include PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89701-125"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89701-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89701-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89701-127">**le \_ pin PWM IOCTL \_ \_ est \_ démarré**</span><span class="sxs-lookup"><span data-stu-id="89701-127">**IOCTL\_PWM\_PIN\_IS\_STARTED**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**)
</dt> </dl>

 

 




