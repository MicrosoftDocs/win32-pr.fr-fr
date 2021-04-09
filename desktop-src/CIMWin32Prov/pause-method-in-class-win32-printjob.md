---
description: La méthode de mise en pause de la classe WMI interrompt un travail d’impression.
ms.assetid: f1e3906f-1ca2-45c0-9863-5762e4e2119a
ms.tgt_platform: multiple
title: Méthode pause de la classe Win32_PrintJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob.Pause
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 785ba54b56c65fd298b6ef763ec2d7eca0d8f61a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861749"
---
# <a name="pause-method-of-the-win32_printjob-class"></a><span data-ttu-id="a3935-103">Méthode pause de la \_ classe PrintJob Win32</span><span class="sxs-lookup"><span data-stu-id="a3935-103">Pause method of the Win32\_PrintJob class</span></span>

<span data-ttu-id="a3935-104">La méthode de mise en **Pause** de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) interrompt un travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="a3935-104">The **Pause** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method suspends a print job.</span></span>

<span data-ttu-id="a3935-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="a3935-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a3935-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a3935-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a3935-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3935-107">Syntax</span></span>


```mof
uint32 Pause();
```



## <a name="parameters"></a><span data-ttu-id="a3935-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3935-108">Parameters</span></span>

<span data-ttu-id="a3935-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a3935-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3935-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a3935-110">Return value</span></span>

<span data-ttu-id="a3935-111">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="a3935-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="a3935-112">**0**</span><span class="sxs-lookup"><span data-stu-id="a3935-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a3935-113">Succès</span><span class="sxs-lookup"><span data-stu-id="a3935-113">Success</span></span>

</dd> <dt>

<span data-ttu-id="a3935-114">**5**</span><span class="sxs-lookup"><span data-stu-id="a3935-114">**5**</span></span>
</dt> <dd>

<span data-ttu-id="a3935-115">accès refusé</span><span class="sxs-lookup"><span data-stu-id="a3935-115">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="a3935-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="a3935-116">Examples</span></span>

<span data-ttu-id="a3935-117">L’exemple de code VBScript [suspendre toutes les imprimantes avec des files d’attente à l’impression vides](https://Gallery.TechNet.Microsoft.Com/cf2b6b61-8ffe-444b-857b-e3a205bc693c) met en pause toutes les imprimantes qui n’ont aucun travail d’impression en attente.</span><span class="sxs-lookup"><span data-stu-id="a3935-117">The [Pause All Printers with Empty Print Queues](https://Gallery.TechNet.Microsoft.Com/cf2b6b61-8ffe-444b-857b-e3a205bc693c) VBScript code sample pauses any printers that have no pending print jobs.</span></span>

<span data-ttu-id="a3935-118">L’exemple de code VBScript suivant met en pause tous les travaux d’impression sur un serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="a3935-118">The following VBScript code sample pauses all the print jobs on a print server.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrintJobs =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrintJob") 
 
For Each objPrintJob in colPrintJobs  
    objPrintJob.Pause 
Next 
```



## <a name="requirements"></a><span data-ttu-id="a3935-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3935-119">Requirements</span></span>



| <span data-ttu-id="a3935-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3935-120">Requirement</span></span> | <span data-ttu-id="a3935-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3935-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3935-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3935-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a3935-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3935-123">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="a3935-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3935-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a3935-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3935-125">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="a3935-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a3935-126">Namespace</span></span><br/>                | <span data-ttu-id="a3935-127">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="a3935-127">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="a3935-128">MOF</span><span class="sxs-lookup"><span data-stu-id="a3935-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3935-129"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3935-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3935-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a3935-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3935-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3935-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="a3935-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3935-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3935-133">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="a3935-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="a3935-134">**\_PrintJob Win32**</span><span class="sxs-lookup"><span data-stu-id="a3935-134">**Win32\_PrintJob**</span></span>](win32-printjob.md)
</dt> </dl>

 

