---
description: Utilisé pour contrôler l’état de luminosité du capteur de lumière ambiante.
ms.assetid: ff400d4e-be8c-450b-ad53-d43b0ab84ab3
title: Méthode WmiSetALSBrightnessState de la classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetALSBrightnessState
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 593b007f75c7eb134de4bb4c9f83c7246e9a51b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538203"
---
# <a name="wmisetalsbrightnessstate-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="83833-103">Méthode WmiSetALSBrightnessState de la classe WmiMonitorBrightnessMethods</span><span class="sxs-lookup"><span data-stu-id="83833-103">WmiSetALSBrightnessState method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="83833-104">La méthode **WmiSetALSBrightnessState** est utilisée pour contrôler l’état de luminosité du capteur de lumière ambiante.</span><span class="sxs-lookup"><span data-stu-id="83833-104">The **WmiSetALSBrightnessState** method is used to control the ambient light sensor brightness state.</span></span> <span data-ttu-id="83833-105">Si un remplacement de luminosité actif a été établi à l’aide de la méthode [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) , ce remplacement est prioritaire par rapport à la luminosité de la als définie à l’aide de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="83833-105">If an active brightness override was established by using the [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md) method, that override will take precedence over the ALS brightness set by using this method.</span></span> <span data-ttu-id="83833-106">Pour que le remplacement de la luminosité d’un ALS activé prenne effet, la stratégie de luminosité doit être restaurée à l’aide de la méthode [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) .</span><span class="sxs-lookup"><span data-stu-id="83833-106">For an enabled ALS brightness override to take effect, the brightness policy has to be reverted by using the [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="83833-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83833-107">Syntax</span></span>


```mof
uint32 WmiSetALSBrightnessState(
   boolean State
);
```



## <a name="parameters"></a><span data-ttu-id="83833-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83833-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83833-109">*State*</span><span class="sxs-lookup"><span data-stu-id="83833-109">*State*</span></span> 
</dt> <dd>

<span data-ttu-id="83833-110">État de luminosité du ALS.</span><span class="sxs-lookup"><span data-stu-id="83833-110">ALS brightness state.</span></span> <span data-ttu-id="83833-111">La valeur False désactive le remplacement de luminosité ALS et la valeur true l’active.</span><span class="sxs-lookup"><span data-stu-id="83833-111">False disables the ALS brightness override and true enables it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83833-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83833-112">Return value</span></span>

<span data-ttu-id="83833-113">Retourne zéro (0) pour indiquer la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="83833-113">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="83833-114">Tout autre nombre indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="83833-114">Any other number indicates an error.</span></span> <span data-ttu-id="83833-115">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="83833-115">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="requirements"></a><span data-ttu-id="83833-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83833-116">Requirements</span></span>



| <span data-ttu-id="83833-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83833-117">Requirement</span></span> | <span data-ttu-id="83833-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="83833-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83833-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83833-119">Minimum supported client</span></span><br/> | <span data-ttu-id="83833-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83833-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="83833-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83833-121">Minimum supported server</span></span><br/> | <span data-ttu-id="83833-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83833-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="83833-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="83833-123">Namespace</span></span><br/>                | <span data-ttu-id="83833-124">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="83833-124">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="83833-125">MOF</span><span class="sxs-lookup"><span data-stu-id="83833-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83833-126"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83833-126"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="83833-127">DLL</span><span class="sxs-lookup"><span data-stu-id="83833-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83833-128"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83833-128"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83833-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83833-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83833-130">**WmiMonitorBrightnessMethods**</span><span class="sxs-lookup"><span data-stu-id="83833-130">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="83833-131">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="83833-131">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

