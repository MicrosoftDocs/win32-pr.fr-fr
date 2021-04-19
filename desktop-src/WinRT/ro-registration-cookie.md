---
description: Représente les fabriques d’activation inscrites en appelant la fonction RoRegisterActivationFactories.
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: RO_REGISTRATION_COOKIE (Roapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe9b5242901c1beff4152bc16108976d6f7de275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514613"
---
# <a name="ro_registration_cookie"></a><span data-ttu-id="946ae-103">déborder le \_ cookie d’inscription \_</span><span class="sxs-lookup"><span data-stu-id="946ae-103">RO\_REGISTRATION\_COOKIE</span></span>

<span data-ttu-id="946ae-104">Représente les fabriques d’activation inscrites en appelant la fonction [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) .</span><span class="sxs-lookup"><span data-stu-id="946ae-104">Represents activation factories that are registered by calling the [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) function.</span></span>


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a><span data-ttu-id="946ae-105">Notes</span><span class="sxs-lookup"><span data-stu-id="946ae-105">Remarks</span></span>

<span data-ttu-id="946ae-106">La fonction [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) retourne un **\_ \_ cookie d’inscription Roll** quand les fabriques de classes activables sont inscrites auprès du Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="946ae-106">The [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) function returns a **RO\_REGISTRATION\_COOKIE** when a activatable class factories are registered with the Windows Runtime.</span></span> <span data-ttu-id="946ae-107">La fonction [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) utilise le cookie pour supprimer les fabriques de classes.</span><span class="sxs-lookup"><span data-stu-id="946ae-107">The [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) function uses the cookie to remove the class factories.</span></span>

## <a name="requirements"></a><span data-ttu-id="946ae-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="946ae-108">Requirements</span></span>



| <span data-ttu-id="946ae-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="946ae-109">Requirement</span></span> | <span data-ttu-id="946ae-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="946ae-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="946ae-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="946ae-111">Minimum supported client</span></span><br/> | <span data-ttu-id="946ae-112">Windows 8</span><span class="sxs-lookup"><span data-stu-id="946ae-112">Windows 8</span></span><br/>                                                               |
| <span data-ttu-id="946ae-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="946ae-113">Minimum supported server</span></span><br/> | <span data-ttu-id="946ae-114">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="946ae-114">Windows Server 2012</span></span><br/>                                                     |
| <span data-ttu-id="946ae-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="946ae-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="946ae-116"><dt>Roapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="946ae-116"><dt>Roapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="946ae-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="946ae-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="946ae-118">**RoRegisterActivationFactories**</span><span class="sxs-lookup"><span data-stu-id="946ae-118">**RoRegisterActivationFactories**</span></span>](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)
</dt> <dt>

[<span data-ttu-id="946ae-119">**RoRevokeActivationFactories**</span><span class="sxs-lookup"><span data-stu-id="946ae-119">**RoRevokeActivationFactories**</span></span>](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)
</dt> </dl>

 

 
