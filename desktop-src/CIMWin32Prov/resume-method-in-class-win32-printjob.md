---
description: La méthode de reprise de la classe WMI continue un travail d’impression suspendu.
ms.assetid: acfbca2b-19af-4339-bbca-834db50c3d8d
ms.tgt_platform: multiple
title: Méthode Resume de la classe Win32_PrintJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob.Resume
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f8ca1602eb29e1e18d83d2e8b79760d13f63e101
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513305"
---
# <a name="resume-method-of-the-win32_printjob-class"></a><span data-ttu-id="4b491-103">Méthode Resume de la \_ classe PrintJob Win32</span><span class="sxs-lookup"><span data-stu-id="4b491-103">Resume method of the Win32\_PrintJob class</span></span>

<span data-ttu-id="4b491-104">La méthode de **reprise** de la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) continue un travail d’impression suspendu.</span><span class="sxs-lookup"><span data-stu-id="4b491-104">The **Resume** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method continues a paused print job.</span></span>

<span data-ttu-id="4b491-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="4b491-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4b491-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4b491-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4b491-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b491-107">Syntax</span></span>


```mof
uint32 Resume();
```



## <a name="parameters"></a><span data-ttu-id="4b491-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b491-108">Parameters</span></span>

<span data-ttu-id="4b491-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4b491-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b491-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4b491-110">Return value</span></span>

<span data-ttu-id="4b491-111">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="4b491-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="4b491-112">**0**</span><span class="sxs-lookup"><span data-stu-id="4b491-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="4b491-113">Succès</span><span class="sxs-lookup"><span data-stu-id="4b491-113">Success</span></span>

</dd> <dt>

<span data-ttu-id="4b491-114">**5**</span><span class="sxs-lookup"><span data-stu-id="4b491-114">**5**</span></span>
</dt> <dd>

<span data-ttu-id="4b491-115">accès refusé</span><span class="sxs-lookup"><span data-stu-id="4b491-115">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="4b491-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="4b491-116">Examples</span></span>

<span data-ttu-id="4b491-117">L’exemple de code VBScript suivant reprend tous les travaux d’impression sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4b491-117">The following VBScript code sample resumes all the print jobs on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrintJobs =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrintJob") 
 
For Each objPrintJob in colPrintJobs  
    objPrintJob.Resume 
Next 
```



## <a name="requirements"></a><span data-ttu-id="4b491-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b491-118">Requirements</span></span>



| <span data-ttu-id="4b491-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b491-119">Requirement</span></span> | <span data-ttu-id="4b491-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b491-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b491-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b491-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4b491-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b491-122">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="4b491-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b491-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4b491-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b491-124">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="4b491-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4b491-125">Namespace</span></span><br/>                | <span data-ttu-id="4b491-126">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4b491-126">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="4b491-127">MOF</span><span class="sxs-lookup"><span data-stu-id="4b491-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b491-128"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b491-128"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b491-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4b491-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b491-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b491-130"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="4b491-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b491-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b491-132">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="4b491-132">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="4b491-133">**\_PrintJob Win32**</span><span class="sxs-lookup"><span data-stu-id="4b491-133">**Win32\_PrintJob**</span></span>](win32-printjob.md)
</dt> </dl>

 

