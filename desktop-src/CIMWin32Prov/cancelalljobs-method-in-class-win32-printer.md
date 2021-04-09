---
description: Supprime tous les travaux, y compris celui qui est actuellement en cours d’impression dans la file d’attente.
ms.assetid: d7466513-b123-43af-ab17-b3213ba80284
ms.tgt_platform: multiple
title: Méthode CancelAllJobs de la classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.CancelAllJobs
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d2d816dab837aafd7b6e9c6beff75c4e62b19b2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860766"
---
# <a name="cancelalljobs-method-of-the-win32_printer-class"></a><span data-ttu-id="eb8e9-103">Méthode CancelAllJobs de la \_ classe Printer Win32</span><span class="sxs-lookup"><span data-stu-id="eb8e9-103">CancelAllJobs method of the Win32\_Printer class</span></span>

<span data-ttu-id="eb8e9-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CancelAllJobs** supprime tous les travaux, y compris celui qui est actuellement en cours d’impression à partir de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="eb8e9-104">The **CancelAllJobs** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method removes all jobs, including the one currently printing from the queue.</span></span>

<span data-ttu-id="eb8e9-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="eb8e9-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="eb8e9-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="eb8e9-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb8e9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb8e9-107">Syntax</span></span>


```mof
uint32 CancelAllJobs();
```



## <a name="parameters"></a><span data-ttu-id="eb8e9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb8e9-108">Parameters</span></span>

<span data-ttu-id="eb8e9-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="eb8e9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb8e9-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb8e9-110">Return value</span></span>

<span data-ttu-id="eb8e9-111">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="eb8e9-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="eb8e9-112">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="eb8e9-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="eb8e9-113">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="eb8e9-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="eb8e9-114">**0**</span><span class="sxs-lookup"><span data-stu-id="eb8e9-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="eb8e9-115">Succès</span><span class="sxs-lookup"><span data-stu-id="eb8e9-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="eb8e9-116">**5**</span><span class="sxs-lookup"><span data-stu-id="eb8e9-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="eb8e9-117">accès refusé</span><span class="sxs-lookup"><span data-stu-id="eb8e9-117">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="eb8e9-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="eb8e9-118">Examples</span></span>

<span data-ttu-id="eb8e9-119">La fonction [notifier les utilisateurs lorsqu’une file d’attente à l’impression est purgée](https://Gallery.TechNet.Microsoft.Com/9f8ad84e-239d-45bf-a14f-ad8f3fc4988a) utilise Msg.exe pour envoyer une alerte réseau à tous les utilisateurs qui avaient des documents dans une file d’attente à l’impression sur le lieu d’être purgés.</span><span class="sxs-lookup"><span data-stu-id="eb8e9-119">The [Notify Users When a Print Queue is Purged](https://Gallery.TechNet.Microsoft.Com/9f8ad84e-239d-45bf-a14f-ad8f3fc4988a) uses Msg.exe to send a network alert to any users who had documents in a print queue about to be purged.</span></span> <span data-ttu-id="eb8e9-120">Après l’envoi des alertes, le script vide la file d’attente à l’impression.</span><span class="sxs-lookup"><span data-stu-id="eb8e9-120">After sending the alerts, the script purges the print queue.</span></span>

<span data-ttu-id="eb8e9-121">L’exemple de code VBScript [Supprimer tous les travaux d’impression](https://Gallery.TechNet.Microsoft.Com/0e89fa7c-a837-4607-b421-c870142e7323) supprime tous les travaux d’impression sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="eb8e9-121">The [Delete all print jobs](https://Gallery.TechNet.Microsoft.Com/0e89fa7c-a837-4607-b421-c870142e7323) VBScript code sample deletes all print jobs on the local computer.</span></span>

<span data-ttu-id="eb8e9-122">L’exemple VBScript suivant supprime tous les travaux d’impression pour une imprimante nommée HP QuietJet.</span><span class="sxs-lookup"><span data-stu-id="eb8e9-122">The following VBScript sample deletes all the print jobs for a printer named HP QuietJet.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'HP QuietJet'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.CancelAllJobs() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="eb8e9-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb8e9-123">Requirements</span></span>



| <span data-ttu-id="eb8e9-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb8e9-124">Requirement</span></span> | <span data-ttu-id="eb8e9-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb8e9-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb8e9-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb8e9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="eb8e9-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb8e9-127">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="eb8e9-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb8e9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="eb8e9-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb8e9-129">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="eb8e9-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="eb8e9-130">Namespace</span></span><br/>                | <span data-ttu-id="eb8e9-131">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="eb8e9-131">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="eb8e9-132">MOF</span><span class="sxs-lookup"><span data-stu-id="eb8e9-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb8e9-133"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb8e9-133"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb8e9-134">DLL</span><span class="sxs-lookup"><span data-stu-id="eb8e9-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb8e9-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb8e9-135"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="eb8e9-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb8e9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb8e9-137">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="eb8e9-137">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="eb8e9-138">**\_Imprimante Win32**</span><span class="sxs-lookup"><span data-stu-id="eb8e9-138">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

