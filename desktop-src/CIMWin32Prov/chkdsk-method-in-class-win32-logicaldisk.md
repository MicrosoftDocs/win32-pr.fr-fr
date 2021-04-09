---
description: Appelle l’opération chkdsk sur le disque.
ms.assetid: 65942702-b660-46cd-b614-e3e1ec3df7b9
ms.tgt_platform: multiple
title: Méthode CHKDSK de la classe Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.Chkdsk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 662fc8739f90eea15295b762edc446ac16677aef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111107"
---
# <a name="chkdsk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="a530d-103">Méthode CHKDSK de la \_ classe disque logique Win32</span><span class="sxs-lookup"><span data-stu-id="a530d-103">Chkdsk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="a530d-104">La méthode d’instance **chkdsk** appelle l’opération **chkdsk** sur le disque.</span><span class="sxs-lookup"><span data-stu-id="a530d-104">The **Chkdsk** instance method invokes the **chkdsk** operation on the disk.</span></span>

<span data-ttu-id="a530d-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="a530d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a530d-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a530d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a530d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a530d-107">Syntax</span></span>


```mof
uint32 Chkdsk(
  [in] boolean FixErrors = ,
  [in] boolean VigorousIndexCheck = ,
  [in] boolean SkipFolderCycle = ,
  [in] boolean ForceDismount = ,
  [in] boolean RecoverBadSectors = ,
  [in] boolean OKToRunAtBootUp = 
);
```



## <a name="parameters"></a><span data-ttu-id="a530d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a530d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a530d-109">*FixErrors* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a530d-109">*FixErrors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a530d-110">Indique ce qui doit être fait pour les erreurs détectées sur le disque.</span><span class="sxs-lookup"><span data-stu-id="a530d-110">Indicates what should be done to errors found on the disk.</span></span> <span data-ttu-id="a530d-111">Si la **valeur est true**, les erreurs sont résolues.</span><span class="sxs-lookup"><span data-stu-id="a530d-111">If **true**, then errors are fixed.</span></span> <span data-ttu-id="a530d-112">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="a530d-112">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="a530d-113">*VigorousIndexCheck* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a530d-113">*VigorousIndexCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a530d-114">Si la **valeur est true**, une vérification moins énergique des entrées d’index doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="a530d-114">If **true**, a less vigorous check of index entries should be performed.</span></span> <span data-ttu-id="a530d-115">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="a530d-115">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="a530d-116">*SkipFolderCycle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a530d-116">*SkipFolderCycle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a530d-117">Si la **valeur est true**, la vérification du cycle de dossier doit être ignorée.</span><span class="sxs-lookup"><span data-stu-id="a530d-117">If **true**, the folder cycle checking should be skipped.</span></span> <span data-ttu-id="a530d-118">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="a530d-118">The default is **true**.</span></span>

</dd> <dt>

<span data-ttu-id="a530d-119">*ForceDismount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a530d-119">*ForceDismount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a530d-120">Si la **valeur est true**, le disque doit être forcé à démonter avant la vérification.</span><span class="sxs-lookup"><span data-stu-id="a530d-120">If **true**, the drive should be forced to dismount before checking.</span></span> <span data-ttu-id="a530d-121">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="a530d-121">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="a530d-122">*RecoverBadSectors* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a530d-122">*RecoverBadSectors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a530d-123">Si la **valeur est true**, les secteurs incorrects doivent être localisés et les informations lisibles doivent être récupérées à partir de ces secteurs.</span><span class="sxs-lookup"><span data-stu-id="a530d-123">If **true**, the bad sectors should be located and the readable information should be recovered from these sectors.</span></span> <span data-ttu-id="a530d-124">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="a530d-124">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="a530d-125">*OKToRunAtBootUp* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a530d-125">*OKToRunAtBootUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a530d-126">Si la **valeur est true**, l’opération **chkdsk** doit être effectuée au prochain démarrage, au cas où l’opération n’aurait pas pu être effectuée parce que le disque est verrouillé au moment où cette méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="a530d-126">If **true**, the **chkdsk** operation should be performed at next boot up time, in case the operation could not be performed because the disk is locked at time this method is called.</span></span> <span data-ttu-id="a530d-127">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="a530d-127">The default is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a530d-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a530d-128">Return value</span></span>

<span data-ttu-id="a530d-129">Retourne la valeur 0 (zéro) en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="a530d-129">Returns a value of 0 (zero) if successful.</span></span> <span data-ttu-id="a530d-130">D’autres valeurs sont répertoriées dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="a530d-130">Other values are listed in the following list.</span></span> <span data-ttu-id="a530d-131">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a530d-131">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a530d-132">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a530d-132">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a530d-133">**Opération réussie-CHKDSK terminée**</span><span class="sxs-lookup"><span data-stu-id="a530d-133">**Success - Chkdsk completed**</span></span>
</dt> <dd>

<span data-ttu-id="a530d-134">0</span><span class="sxs-lookup"><span data-stu-id="a530d-134">0</span></span>

<span data-ttu-id="a530d-135">Opération réussie- [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) terminée</span><span class="sxs-lookup"><span data-stu-id="a530d-135">Success - [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) Completed</span></span>

</dd> <dt>

<span data-ttu-id="a530d-136">**Réussite-verrouillé et CHKDSK planifié au redémarrage**</span><span class="sxs-lookup"><span data-stu-id="a530d-136">**Success - Locked and chkdsk scheduled on reboot**</span></span>
</dt> <dd>

<span data-ttu-id="a530d-137">1</span><span class="sxs-lookup"><span data-stu-id="a530d-137">1</span></span>

</dd> <dt>

<span data-ttu-id="a530d-138">**Échec : système de fichiers inconnu**</span><span class="sxs-lookup"><span data-stu-id="a530d-138">**Failure - Unknown file system**</span></span>
</dt> <dd>

<span data-ttu-id="a530d-139">2</span><span class="sxs-lookup"><span data-stu-id="a530d-139">2</span></span>

</dd> <dt>

<span data-ttu-id="a530d-140">**Échec-erreur inconnue**</span><span class="sxs-lookup"><span data-stu-id="a530d-140">**Failure - Unknown error**</span></span>
</dt> <dd>

<span data-ttu-id="a530d-141">3</span><span class="sxs-lookup"><span data-stu-id="a530d-141">3</span></span>

</dd> <dt>

<span data-ttu-id="a530d-142">**Échec : système de fichiers non pris en charge**</span><span class="sxs-lookup"><span data-stu-id="a530d-142">**Failure - Unsupported File System**</span></span>
</dt> <dd>

<span data-ttu-id="a530d-143">4</span><span class="sxs-lookup"><span data-stu-id="a530d-143">4</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a530d-144">Notes</span><span class="sxs-lookup"><span data-stu-id="a530d-144">Remarks</span></span>

<span data-ttu-id="a530d-145">Cette méthode s’applique uniquement aux instances de disque logique qui représentent un disque physique de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a530d-145">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="a530d-146">Elle ne s’applique pas aux lecteurs logiques mappés.</span><span class="sxs-lookup"><span data-stu-id="a530d-146">It is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="a530d-147">Exemples</span><span class="sxs-lookup"><span data-stu-id="a530d-147">Examples</span></span>

<span data-ttu-id="a530d-148">L’exemple de code[is CHKDSK Dirty défini sur un serveur](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) de code PowerShell examine le système distant et retourne la valeur true ou false si l’indicateur chkdsk/f a été défini.</span><span class="sxs-lookup"><span data-stu-id="a530d-148">The[Is CHKDSK Dirty Bit Set on a server](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) PowerShell code sample examines the remote system and returns a true or false if the chkdsk /f flag was set.</span></span>

<span data-ttu-id="a530d-149">L’exemple de code PowerShell [Disk Scan à](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) distance démarre ou planifie l’analyse du disque.</span><span class="sxs-lookup"><span data-stu-id="a530d-149">The [Remotely scan disk](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) PowerShell code sample remotely starts or schedules Scan Disk.</span></span>

<span data-ttu-id="a530d-150">L’exemple de code VBScript suivant exécute ChkDsk.exe sur le lecteur D sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a530d-150">The following VBScript code sample Runs ChkDsk.exe against drive D on a computer.</span></span>


```VB
Const FIX_ERRORS = True 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk.DeviceID='D:'") 
 
errReturn = objDisk.ChkDsk(FIX_ERRORS) 
```



## <a name="requirements"></a><span data-ttu-id="a530d-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a530d-151">Requirements</span></span>



| <span data-ttu-id="a530d-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a530d-152">Requirement</span></span> | <span data-ttu-id="a530d-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="a530d-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a530d-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a530d-154">Minimum supported client</span></span><br/> | <span data-ttu-id="a530d-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a530d-155">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a530d-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a530d-156">Minimum supported server</span></span><br/> | <span data-ttu-id="a530d-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a530d-157">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a530d-158">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a530d-158">Namespace</span></span><br/>                | <span data-ttu-id="a530d-159">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="a530d-159">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a530d-160">MOF</span><span class="sxs-lookup"><span data-stu-id="a530d-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a530d-161"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a530d-161"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a530d-162">DLL</span><span class="sxs-lookup"><span data-stu-id="a530d-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a530d-163"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a530d-163"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a530d-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a530d-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a530d-165">**\_Disque logique Win32**</span><span class="sxs-lookup"><span data-stu-id="a530d-165">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="a530d-166">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="a530d-166">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

