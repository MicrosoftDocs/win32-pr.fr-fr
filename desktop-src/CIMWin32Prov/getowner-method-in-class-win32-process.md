---
description: GetOwner&\# 8194 ; La méthode de classe WMI récupère le nom d’utilisateur et le nom de domaine sous lesquels le processus est en cours d’exécution.
ms.assetid: bbd6d22b-ca54-42f3-8098-d3034048ec4d
ms.tgt_platform: multiple
title: Méthode GetOwner de la classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwner
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 007acbe997f555e9a439ed27740a447d3bf7fe4d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110490"
---
# <a name="getowner-method-of-the-win32_process-class"></a><span data-ttu-id="4589a-103">Méthode GetOwner de la \_ classe de processus Win32</span><span class="sxs-lookup"><span data-stu-id="4589a-103">GetOwner method of the Win32\_Process class</span></span>

<span data-ttu-id="4589a-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **GetOwner** récupère le nom d’utilisateur et le nom de domaine sous lesquels le processus s’exécute.</span><span class="sxs-lookup"><span data-stu-id="4589a-104">The **GetOwner** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method retrieves the user name and domain name under which the process is running.</span></span>

<span data-ttu-id="4589a-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="4589a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4589a-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4589a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4589a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4589a-107">Syntax</span></span>


```mof
uint32 GetOwner(
  [out] string User,
  [out] string Domain
);
```



## <a name="parameters"></a><span data-ttu-id="4589a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4589a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4589a-109">*Utilisateur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4589a-109">*User* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4589a-110">Retourne le nom d’utilisateur du propriétaire de ce processus.</span><span class="sxs-lookup"><span data-stu-id="4589a-110">Returns the user name of the owner of this process.</span></span>

</dd> <dt>

<span data-ttu-id="4589a-111">*Domaine* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4589a-111">*Domain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4589a-112">Retourne le nom de domaine sous lequel ce processus s’exécute.</span><span class="sxs-lookup"><span data-stu-id="4589a-112">Returns the domain name under which this process is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4589a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4589a-113">Return value</span></span>

<span data-ttu-id="4589a-114">Retourne zéro (0) pour indiquer la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="4589a-114">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="4589a-115">Tout autre nombre indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="4589a-115">Any other number indicates an error.</span></span> <span data-ttu-id="4589a-116">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="4589a-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="4589a-117">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="4589a-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="4589a-118">**Achèvement réussi** (0)</span><span class="sxs-lookup"><span data-stu-id="4589a-118">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4589a-119">**Accès refusé** (2)</span><span class="sxs-lookup"><span data-stu-id="4589a-119">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4589a-120">**Privilèges insuffisants** (3)</span><span class="sxs-lookup"><span data-stu-id="4589a-120">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4589a-121">**Échec inconnu** (8)</span><span class="sxs-lookup"><span data-stu-id="4589a-121">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="4589a-122">**Chemin introuvable** (9)</span><span class="sxs-lookup"><span data-stu-id="4589a-122">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="4589a-123">**Paramètre non valide** (21)</span><span class="sxs-lookup"><span data-stu-id="4589a-123">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="4589a-124">**Autre** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="4589a-124">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="4589a-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="4589a-125">Examples</span></span>

<span data-ttu-id="4589a-126">[Le pourcentage d’UC du processus d’analyse par nom avec propriétaire](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) L’exemple VBScript collecte le pourcentage d’utilisation du processeur ou du processeur et recherche le propriétaire du processus.</span><span class="sxs-lookup"><span data-stu-id="4589a-126">[The Monitor Process CPU Pct by Name with Owner](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) VBScript sample collects the CPU or Processor utilization percent and looks up the process owner.</span></span>

<span data-ttu-id="4589a-127">Les [serveurs obtenir tous les serveurs qu’une liste d’utilisateurs est connectée](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) à PowerShell sont des exemples de requêtes WMI pour le propriétaire de tous les processus de explorer.exe.</span><span class="sxs-lookup"><span data-stu-id="4589a-127">The [Get all servers that a list of users is logged onto](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) PowerShell sample querys WMI for the owner of all explorer.exe processes.</span></span>

<span data-ttu-id="4589a-128">L’exemple de code VBScript suivant obtient le propriétaire de chaque processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4589a-128">The following VBScript code example obtains the owner for each running process.</span></span>


```VB
strComputer = "."
Set colProcesses = GetObject("winmgmts:" & _
   "{impersonationLevel=impersonate}!\\" & strComputer & _
   "\root\cimv2").ExecQuery("Select * from Win32_Process")

For Each objProcess in colProcesses

    Return = objProcess.GetOwner(strNameOfUser)
    If Return <> 0 Then
        Wscript.Echo "Could not get owner info for process " & _  
            objProcess.Name & VBNewLine _
            & "Error = " & Return
    Else 
        Wscript.Echo "Process " _
            & objProcess.Name & " is owned by " _ 
            & "\" & strNameOfUser & "."
    End If
Next
```



## <a name="requirements"></a><span data-ttu-id="4589a-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4589a-129">Requirements</span></span>



| <span data-ttu-id="4589a-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4589a-130">Requirement</span></span> | <span data-ttu-id="4589a-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="4589a-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4589a-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4589a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4589a-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4589a-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4589a-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4589a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4589a-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4589a-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4589a-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4589a-136">Namespace</span></span><br/>                | <span data-ttu-id="4589a-137">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4589a-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4589a-138">MOF</span><span class="sxs-lookup"><span data-stu-id="4589a-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4589a-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4589a-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4589a-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4589a-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4589a-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4589a-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4589a-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4589a-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="4589a-143">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4589a-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4589a-144">**\_Processus Win32**</span><span class="sxs-lookup"><span data-stu-id="4589a-144">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

