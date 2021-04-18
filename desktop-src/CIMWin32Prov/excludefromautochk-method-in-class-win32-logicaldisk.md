---
description: Exclut les disques de l’opération Autochk à exécuter au redémarrage suivant.
ms.assetid: 5df2bc3b-e149-4853-aa02-af4cb8af6da0
ms.tgt_platform: multiple
title: Méthode ExcludeFromAutochk de la classe Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ExcludeFromAutochk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c41d93111742e975490d97169c7e9147ba5fb1ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512887"
---
# <a name="excludefromautochk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="57fe3-103">Méthode ExcludeFromAutochk de la \_ classe disque logique Win32</span><span class="sxs-lookup"><span data-stu-id="57fe3-103">ExcludeFromAutochk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="57fe3-104">La méthode **ExcludeFromAutochk** exclut les disques de l’opération **Autochk** à exécuter au redémarrage suivant.</span><span class="sxs-lookup"><span data-stu-id="57fe3-104">The **ExcludeFromAutochk** method excludes disks from the **autochk** operation to be run at the next reboot.</span></span>

<span data-ttu-id="57fe3-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="57fe3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="57fe3-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="57fe3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="57fe3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57fe3-107">Syntax</span></span>


```mof
uint32 ExcludeFromAutochk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a><span data-ttu-id="57fe3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57fe3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57fe3-109">*Disque logique* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="57fe3-109">*LogicalDisk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57fe3-110">Liste des lecteurs qui doivent être exclus de **Autochk** au prochain redémarrage.</span><span class="sxs-lookup"><span data-stu-id="57fe3-110">List of drives that should be excluded from **autochk** at the next reboot.</span></span> <span data-ttu-id="57fe3-111">La syntaxe de chaîne se compose de la lettre de lecteur suivie d’un signe deux-points pour le disque logique.</span><span class="sxs-lookup"><span data-stu-id="57fe3-111">The string syntax consists of the drive letter followed by a colon for the logical disk.</span></span>

<span data-ttu-id="57fe3-112">Exemple : "C :"</span><span class="sxs-lookup"><span data-stu-id="57fe3-112">Example: "C:"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57fe3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="57fe3-113">Return value</span></span>

<span data-ttu-id="57fe3-114">Retourne la valeur 0 (zéro) quand aucune erreur ne se produit.</span><span class="sxs-lookup"><span data-stu-id="57fe3-114">Returns a value of 0 (zero) when no error occurs.</span></span> <span data-ttu-id="57fe3-115">Les valeurs sont répertoriées dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="57fe3-115">Values are listed in the following list.</span></span> <span data-ttu-id="57fe3-116">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="57fe3-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="57fe3-117">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="57fe3-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="57fe3-118">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="57fe3-118">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="57fe3-119">**Erreur : lecteur distant** (1)</span><span class="sxs-lookup"><span data-stu-id="57fe3-119">**Error - Remote Drive** (1)</span></span>
</dt> <dt>

<span data-ttu-id="57fe3-120">**Erreur : lecteur amovible** (2)</span><span class="sxs-lookup"><span data-stu-id="57fe3-120">**Error - Removable Drive** (2)</span></span>
</dt> <dt>

<span data-ttu-id="57fe3-121">**Erreur : le lecteur n’est pas un répertoire racine** (3)</span><span class="sxs-lookup"><span data-stu-id="57fe3-121">**Error - Drive Not Root Directory** (3)</span></span>
</dt> <dt>

<span data-ttu-id="57fe3-122">**Erreur : lecteur inconnu** (4)</span><span class="sxs-lookup"><span data-stu-id="57fe3-122">**Error - Unknown Drive** (4)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="57fe3-123">Notes</span><span class="sxs-lookup"><span data-stu-id="57fe3-123">Remarks</span></span>

<span data-ttu-id="57fe3-124">S’il n’est pas exclu, **Autochk** est exécuté sur le disque lorsque le bit d’intégrité est défini pour le disque.</span><span class="sxs-lookup"><span data-stu-id="57fe3-124">If not excluded, **autochk** is performed on the disk when the dirty bit is set for the disk.</span></span> <span data-ttu-id="57fe3-125">Notez que les appels pour exclure des disques ne sont pas cumulatifs.</span><span class="sxs-lookup"><span data-stu-id="57fe3-125">Note that the calls to exclude disks are not cumulative.</span></span> <span data-ttu-id="57fe3-126">Si un appel est effectué pour exclure certains disques, la nouvelle liste n’est pas ajoutée à la liste des disques déjà marqués pour l’exclusion.</span><span class="sxs-lookup"><span data-stu-id="57fe3-126">If a call is made to exclude some disks, then the new list is not added to the list of disks that are already marked for exclusion.</span></span> <span data-ttu-id="57fe3-127">La nouvelle liste de disques remplace la liste précédente.</span><span class="sxs-lookup"><span data-stu-id="57fe3-127">The new list of disks overwrites the previous list.</span></span> <span data-ttu-id="57fe3-128">Cette méthode s’applique uniquement aux instances de disque logique qui représentent un disque physique de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="57fe3-128">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="57fe3-129">Elle ne s’applique pas aux lecteurs logiques mappés.</span><span class="sxs-lookup"><span data-stu-id="57fe3-129">It is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="57fe3-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="57fe3-130">Examples</span></span>

<span data-ttu-id="57fe3-131">L’exemple de code VBScript suivant garantit que Autochk.exe ne s’exécutera pas sur le lecteur C lors du prochain redémarrage de l’ordinateur, même si le « bit d’intégrité » a été défini sur le lecteur C.</span><span class="sxs-lookup"><span data-stu-id="57fe3-131">The following VBScript code sample ensures that Autochk.exe will not run against drive C the next time the computer reboots, even if the "dirty bit" has been set on drive C.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ExcludeFromAutoChk(Array("C:")) 
```



## <a name="requirements"></a><span data-ttu-id="57fe3-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57fe3-132">Requirements</span></span>



| <span data-ttu-id="57fe3-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57fe3-133">Requirement</span></span> | <span data-ttu-id="57fe3-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="57fe3-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57fe3-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57fe3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="57fe3-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57fe3-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="57fe3-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57fe3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="57fe3-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57fe3-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="57fe3-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="57fe3-139">Namespace</span></span><br/>                | <span data-ttu-id="57fe3-140">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="57fe3-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="57fe3-141">MOF</span><span class="sxs-lookup"><span data-stu-id="57fe3-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57fe3-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57fe3-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="57fe3-143">DLL</span><span class="sxs-lookup"><span data-stu-id="57fe3-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57fe3-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57fe3-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57fe3-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57fe3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57fe3-146">**\_Disque logique Win32**</span><span class="sxs-lookup"><span data-stu-id="57fe3-146">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="57fe3-147">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="57fe3-147">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

