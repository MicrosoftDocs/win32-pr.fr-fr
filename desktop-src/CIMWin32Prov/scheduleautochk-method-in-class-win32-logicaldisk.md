---
description: Planifie l’exécution de Autochk sur le lecteur de disque représenté par le disque \_ logique Win32 au prochain redémarrage si le bit modifié est défini.
ms.assetid: 34f4c26b-6bfb-45d9-9d6c-0a9b735355f3
ms.tgt_platform: multiple
title: Méthode ScheduleAutoChk de la classe Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ScheduleAutoChk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2707810d919c119aff35f2313e9aa5218f7948f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950515"
---
# <a name="scheduleautochk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="1e65a-103">Méthode ScheduleAutoChk de la \_ classe disque logique Win32</span><span class="sxs-lookup"><span data-stu-id="1e65a-103">ScheduleAutoChk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="1e65a-104">La méthode de la classe **ScheduleAutoChk** planifie l’exécution de Autochk sur le lecteur de disque représenté par le disque [**\_ logique Win32**](win32-logicaldisk.md) au redémarrage suivant si le bit modifié est défini.</span><span class="sxs-lookup"><span data-stu-id="1e65a-104">The **ScheduleAutoChk** class method schedules Autochk to be run on the disk drive represented by the [**Win32\_LogicalDisk**](win32-logicaldisk.md) at the next reboot if the dirty bit is set.</span></span>

<span data-ttu-id="1e65a-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1e65a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1e65a-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1e65a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1e65a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e65a-107">Syntax</span></span>


```mof
uint32 ScheduleAutoChk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a><span data-ttu-id="1e65a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e65a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e65a-109">*Disque logique* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e65a-109">*LogicalDisk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e65a-110">Spécifie la liste des lecteurs à planifier pour Autochk au prochain redémarrage.</span><span class="sxs-lookup"><span data-stu-id="1e65a-110">Specifies the list of drives to schedule for Autochk at the next reboot.</span></span> <span data-ttu-id="1e65a-111">La syntaxe de chaîne se compose de la lettre de lecteur suivie d’un signe deux-points pour le disque logique, par exemple : « C : »</span><span class="sxs-lookup"><span data-stu-id="1e65a-111">The string syntax consists of the drive letter followed by a colon for the logical disk, for example: "C:"</span></span>

> [!Note]  
> <span data-ttu-id="1e65a-112">Vérifiez toujours la validité des lettres de lecteur dans le tableau de disques *logiques* lorsque les données proviennent d’une source inconnue ou d’une source qui n’est pas digne de confiance.</span><span class="sxs-lookup"><span data-stu-id="1e65a-112">Always check the validity of the drive letters in the *LogicalDisk* array when the data comes from an unknown source, or a source that you do not trust.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e65a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e65a-113">Return value</span></span>

<span data-ttu-id="1e65a-114">Retourne la valeur 0 (zéro) en cas de réussite, et une autre valeur si une autre erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="1e65a-114">Returns a value of 0 (zero) if successful, and some other value if any other error occurs.</span></span> <span data-ttu-id="1e65a-115">Les valeurs sont répertoriées dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="1e65a-115">Values are listed in the following list.</span></span> <span data-ttu-id="1e65a-116">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1e65a-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1e65a-117">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1e65a-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1e65a-118">**Aucune erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="1e65a-118">**No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1e65a-119">**Erreur : lecteur distant** (1)</span><span class="sxs-lookup"><span data-stu-id="1e65a-119">**Error - Remote Drive** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1e65a-120">**Erreur : lecteur amovible** (2)</span><span class="sxs-lookup"><span data-stu-id="1e65a-120">**Error - Removable Drive** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1e65a-121">**Erreur : le lecteur n’est pas un répertoire racine** (3)</span><span class="sxs-lookup"><span data-stu-id="1e65a-121">**Error - Drive Not Root Directory** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1e65a-122">**Erreur : lecteur inconnu** (4)</span><span class="sxs-lookup"><span data-stu-id="1e65a-122">**Error - Unknown Drive** (4)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="1e65a-123">Notes</span><span class="sxs-lookup"><span data-stu-id="1e65a-123">Remarks</span></span>

<span data-ttu-id="1e65a-124">Cette méthode s’applique uniquement aux instances de disque logique qui représentent un disque physique de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1e65a-124">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="1e65a-125">Cette méthode n’est pas applicable aux lecteurs logiques mappés.</span><span class="sxs-lookup"><span data-stu-id="1e65a-125">This method is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="1e65a-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="1e65a-126">Examples</span></span>

<span data-ttu-id="1e65a-127">Les exemples VBScript et PowerShell suivants planifient Autochk.exe pour s’exécuter sur le lecteur C lors du prochain redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1e65a-127">The following VBScript and PowerShell samples schedule Autochk.exe to run against drive C the next time the computer reboots.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ScheduleAutoChk(Array("C:")) 
```


```PowerShell

Invoke-WmiMethod -path win32_logicaldisk -Name ScheduleAutoChk -ArgumentList @(&quot;C:&quot;)
```





## <a name="requirements"></a><span data-ttu-id="1e65a-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e65a-128">Requirements</span></span>



| <span data-ttu-id="1e65a-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e65a-129">Requirement</span></span> | <span data-ttu-id="1e65a-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e65a-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e65a-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e65a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1e65a-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e65a-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1e65a-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e65a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1e65a-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e65a-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1e65a-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1e65a-135">Namespace</span></span><br/>                | <span data-ttu-id="1e65a-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1e65a-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1e65a-137">MOF</span><span class="sxs-lookup"><span data-stu-id="1e65a-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e65a-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e65a-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e65a-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1e65a-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e65a-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e65a-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e65a-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e65a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e65a-142">**\_Disque logique Win32**</span><span class="sxs-lookup"><span data-stu-id="1e65a-142">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> </dl>

 

