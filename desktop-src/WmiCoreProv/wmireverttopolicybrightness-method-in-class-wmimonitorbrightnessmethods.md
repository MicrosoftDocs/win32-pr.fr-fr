---
description: La méthode WmiRevertToPolicyBrightness est utilisée pour rétablir la luminosité du paramètre de stratégie. Cette méthode n’a aucun effet sur les paramètres de luminosité du ALS.
ms.assetid: 9a520c3f-3563-4ef4-b397-14e487c8e8bb
title: Méthode WmiRevertToPolicyBrightness de la classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiRevertToPolicyBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 03e1ed74486c7a5a2f2c61dc858e715850ec516e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203358"
---
# <a name="wmireverttopolicybrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="1c642-104">Méthode WmiRevertToPolicyBrightness de la classe WmiMonitorBrightnessMethods</span><span class="sxs-lookup"><span data-stu-id="1c642-104">WmiRevertToPolicyBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="1c642-105">La méthode **WmiRevertToPolicyBrightness** est utilisée pour rétablir la luminosité du paramètre de stratégie.</span><span class="sxs-lookup"><span data-stu-id="1c642-105">The **WmiRevertToPolicyBrightness** method is used to revert the brightness to the policy setting.</span></span> <span data-ttu-id="1c642-106">Cette méthode n’a aucun effet sur les paramètres de luminosité du ALS.</span><span class="sxs-lookup"><span data-stu-id="1c642-106">This method has no effect on the ALS brightness settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c642-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c642-107">Syntax</span></span>


```mof
uint32 WmiRevertToPolicyBrightness();
```



## <a name="parameters"></a><span data-ttu-id="1c642-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c642-108">Parameters</span></span>

<span data-ttu-id="1c642-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1c642-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1c642-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1c642-110">Return value</span></span>

<span data-ttu-id="1c642-111">Retourne zéro (0) pour indiquer la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="1c642-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="1c642-112">Tout autre nombre indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="1c642-112">Any other number indicates an error.</span></span> <span data-ttu-id="1c642-113">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1c642-113">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c642-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c642-114">Requirements</span></span>



| <span data-ttu-id="1c642-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c642-115">Requirement</span></span> | <span data-ttu-id="1c642-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c642-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c642-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c642-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1c642-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c642-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1c642-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c642-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1c642-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c642-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1c642-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1c642-121">Namespace</span></span><br/>                | <span data-ttu-id="1c642-122">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="1c642-122">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="1c642-123">MOF</span><span class="sxs-lookup"><span data-stu-id="1c642-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c642-124"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c642-124"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c642-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1c642-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c642-126"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c642-126"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c642-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c642-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c642-128">**WmiMonitorBrightnessMethods**</span><span class="sxs-lookup"><span data-stu-id="1c642-128">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="1c642-129">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="1c642-129">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

