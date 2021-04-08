---
description: Définit la luminosité de l’affichage d’un moniteur d’ordinateur.
ms.assetid: 900cf5fd-6888-4f0b-8e0b-01eeaaeeeb8f
title: Méthode WmiSetBrightness de la classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods.WmiSetBrightness
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 599610b0d81de283d97ca347486c4adcbe0103dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034729"
---
# <a name="wmisetbrightness-method-of-the-wmimonitorbrightnessmethods-class"></a><span data-ttu-id="7769d-103">Méthode WmiSetBrightness de la classe WmiMonitorBrightnessMethods</span><span class="sxs-lookup"><span data-stu-id="7769d-103">WmiSetBrightness method of the WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="7769d-104">La méthode **WmiSetBrightness** définit la luminosité d’affichage d’un moniteur d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7769d-104">The **WmiSetBrightness** method sets the display brightness of a computer monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="7769d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7769d-105">Syntax</span></span>


```mof
uint32 WmiSetBrightness(
   uint32 Timeout,
   uint8  Brightness
);
```



## <a name="parameters"></a><span data-ttu-id="7769d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7769d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7769d-107">*Délai d'expiration*</span><span class="sxs-lookup"><span data-stu-id="7769d-107">*Timeout*</span></span> 
</dt> <dd>

<span data-ttu-id="7769d-108">Délai d’attente, en secondes.</span><span class="sxs-lookup"><span data-stu-id="7769d-108">Timeout, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="7769d-109">*Luminosité*</span><span class="sxs-lookup"><span data-stu-id="7769d-109">*Brightness*</span></span> 
</dt> <dd>

<span data-ttu-id="7769d-110">Luminosité, en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="7769d-110">Brightness, in percent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7769d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7769d-111">Return value</span></span>

<span data-ttu-id="7769d-112">Retourne zéro (0) pour indiquer la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="7769d-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="7769d-113">Tout autre nombre indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="7769d-113">Any other number indicates an error.</span></span> <span data-ttu-id="7769d-114">Pour plus d’informations sur les codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="7769d-114">For more information about error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

## <a name="examples"></a><span data-ttu-id="7769d-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="7769d-115">Examples</span></span>

<span data-ttu-id="7769d-116">Pour une description détaillée de la récupération et de la définition de la luminosité du moniteur, consultez la rubrique de blog [Utiliser PowerShell pour signaler et définir la luminosité](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="7769d-116">For an extended discussion of retrieving and setting monitor brightness, see the Scripting Guy's [Use PowerShell to Report and Set Monitor Brightness](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx) blog topic.</span></span>

<span data-ttu-id="7769d-117">L’exemple PowerShell suivant définit la luminosité de l’analyse sur 50%.</span><span class="sxs-lookup"><span data-stu-id="7769d-117">The following PowerShell sample sets the brightness of the monitor to 50%.</span></span>


```PowerShell
$brightness = 50
$delay = 5
$myMonitor = Get-WmiObject -Namespace root\wmi -Class WmiMonitorBrightnessMethods
$myMonitor.wmisetbrightness($delay, $brightness)
```



## <a name="requirements"></a><span data-ttu-id="7769d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7769d-118">Requirements</span></span>



| <span data-ttu-id="7769d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7769d-119">Requirement</span></span> | <span data-ttu-id="7769d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7769d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7769d-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7769d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7769d-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7769d-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7769d-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7769d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7769d-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7769d-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7769d-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7769d-125">Namespace</span></span><br/>                | <span data-ttu-id="7769d-126">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="7769d-126">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="7769d-127">MOF</span><span class="sxs-lookup"><span data-stu-id="7769d-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7769d-128"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7769d-128"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="7769d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7769d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7769d-130"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7769d-130"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7769d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7769d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7769d-132">**WmiMonitorBrightnessMethods**</span><span class="sxs-lookup"><span data-stu-id="7769d-132">**WmiMonitorBrightnessMethods**</span></span>](wmimonitorbrightnessmethods.md)
</dt> <dt>

[<span data-ttu-id="7769d-133">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="7769d-133">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

