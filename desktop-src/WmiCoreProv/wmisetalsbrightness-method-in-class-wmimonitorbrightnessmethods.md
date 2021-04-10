---
description: Utilisé pour définir la valeur de luminosité du capteur de lumière ambiante.
ms.assetid: 8b3ec692-4043-42b3-8dd6-7a147620e382
title: Méthode WmiSetALSBrightness de la classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 0768917f9197b6ee3de52877e031acbbdc8f9aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210907"
---
# <a name="wmisetalsbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="9747d-103">Méthode WmiSetALSBrightness de la classe WmiMonitorBrightnessMethods</span><span class="sxs-lookup"><span data-stu-id="9747d-103">WmiSetALSBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="9747d-104">La méthode **WmiSetALSBrightness** est utilisée pour définir la valeur de luminosité du capteur de lumière ambiante.</span><span class="sxs-lookup"><span data-stu-id="9747d-104">The **WmiSetALSBrightness** method is used to set the ambient light sensor brightness value.</span></span> <span data-ttu-id="9747d-105">Si un remplacement de luminosité actif a été établi à l’aide de la méthode [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) , ce remplacement est prioritaire par rapport à la luminosité de la als définie à l’aide de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="9747d-105">If an active brightness override was established by using the [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) method, that override will take precedence over the ALS brightness set by using this method.</span></span> <span data-ttu-id="9747d-106">Pour que le remplacement de la luminosité d’un ALS activé prenne effet, la stratégie de luminosité doit être restaurée à l’aide de la méthode [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) .</span><span class="sxs-lookup"><span data-stu-id="9747d-106">For an enabled ALS brightness override to take effect, the brightness policy has to be reverted by using the [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9747d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9747d-107">Syntax</span></span>


```mof
uint32 WmiSetALSBrightness(
   uint8 Brightness
);
```



## <a name="parameters"></a><span data-ttu-id="9747d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9747d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9747d-109">*Luminosité*</span><span class="sxs-lookup"><span data-stu-id="9747d-109">*Brightness*</span></span> 
</dt> <dd>

<span data-ttu-id="9747d-110">Luminosité du ALS en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="9747d-110">The ALS brightness as a percentage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9747d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9747d-111">Return value</span></span>

<span data-ttu-id="9747d-112">Retourne zéro (0) pour indiquer la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9747d-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="9747d-113">Tout autre nombre indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="9747d-113">Any other number indicates an error.</span></span> <span data-ttu-id="9747d-114">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9747d-114">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="9747d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9747d-115">Requirements</span></span>



| <span data-ttu-id="9747d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9747d-116">Requirement</span></span> | <span data-ttu-id="9747d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9747d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9747d-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9747d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9747d-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9747d-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9747d-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9747d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9747d-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9747d-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9747d-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9747d-122">Namespace</span></span><br/>                | <span data-ttu-id="9747d-123">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="9747d-123">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="9747d-124">MOF</span><span class="sxs-lookup"><span data-stu-id="9747d-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9747d-125"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9747d-125"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="9747d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9747d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9747d-127"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9747d-127"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9747d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9747d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9747d-129">**WmiMonitorBrightnessMethods**</span><span class="sxs-lookup"><span data-stu-id="9747d-129">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="9747d-130">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="9747d-130">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

