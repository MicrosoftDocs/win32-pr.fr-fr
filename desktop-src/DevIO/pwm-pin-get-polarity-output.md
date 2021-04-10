---
description: Contient une valeur de polarité à retourner.
ms.assetid: 432C10EF-AC08-4781-9BCA-A31E0DF12704
title: Structure de PWM_PIN_GET_POLARITY_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_POLARITY_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 81cf7b658a0024c3280db1523af34aaf2ef17262
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950581"
---
# <a name="pwm_pin_get_polarity_output-structure"></a><span data-ttu-id="01dec-103">Structure de sortie de la polarité du \_ code confidentiel PWM \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="01dec-103">PWM\_PIN\_GET\_POLARITY\_OUTPUT structure</span></span>

<span data-ttu-id="01dec-104">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="01dec-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="01dec-105">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="01dec-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="01dec-106">Contient une valeur de polarité à retourner.</span><span class="sxs-lookup"><span data-stu-id="01dec-106">Contains a polarity value to return.</span></span>

## <a name="syntax"></a><span data-ttu-id="01dec-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01dec-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_GET_POLARITY_OUTPUT {
  PWM_POLARITY Polarity;
} PWM_PIN_GET_POLARITY_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="01dec-108">Membres</span><span class="sxs-lookup"><span data-stu-id="01dec-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="01dec-109">**Polarité**</span><span class="sxs-lookup"><span data-stu-id="01dec-109">**Polarity**</span></span>
</dt> <dd>

<span data-ttu-id="01dec-110">Polarité de la broche ou du canal en tant que valeur de [**\_ polarité PWM**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) .</span><span class="sxs-lookup"><span data-stu-id="01dec-110">The polarity of the pin or channel as a [**PWM\_POLARITY**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) value.</span></span> <span data-ttu-id="01dec-111">La polarité est soit active élevée, soit faible.</span><span class="sxs-lookup"><span data-stu-id="01dec-111">The polarity is either Active High or Active Low.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01dec-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01dec-112">Requirements</span></span>



| <span data-ttu-id="01dec-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01dec-113">Requirement</span></span> | <span data-ttu-id="01dec-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="01dec-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01dec-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01dec-115">Minimum supported client</span></span><br/> | <span data-ttu-id="01dec-116">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01dec-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="01dec-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01dec-117">Minimum supported server</span></span><br/> | <span data-ttu-id="01dec-118">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01dec-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="01dec-119">Version KMDF minimale</span><span class="sxs-lookup"><span data-stu-id="01dec-119">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="01dec-120">1,19</span><span class="sxs-lookup"><span data-stu-id="01dec-120">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="01dec-121">Version UMDF minimale</span><span class="sxs-lookup"><span data-stu-id="01dec-121">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="01dec-122">2.19</span><span class="sxs-lookup"><span data-stu-id="01dec-122">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="01dec-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="01dec-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="01dec-124"><dt>PWM. h (include PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01dec-124"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01dec-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01dec-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01dec-126">**\_polarité du \_ code confidentiel PWM \_ d’IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="01dec-126">**IOCTL\_PWM\_PIN\_GET\_POLARITY**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_POLARITY**)
</dt> <dt>

[<span data-ttu-id="01dec-127">**\_polarité PWM**</span><span class="sxs-lookup"><span data-stu-id="01dec-127">**PWM\_POLARITY**</span></span>](/windows/win32/api/pwm/ne-pwm-pwm_polarity)
</dt> </dl>

 

