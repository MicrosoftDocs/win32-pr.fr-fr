---
description: Supprime un nom de partage de la liste des ressources partagées d’un serveur, en déconnectant les connexions à la ressource partagée.
ms.assetid: 175f9c0e-0017-4a86-8e05-ad78e2c93c11
ms.tgt_platform: multiple
title: Méthode Delete de la classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2048ba9dac91b139888f27c037d64849de8a4ee8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110806"
---
# <a name="delete-method-of-the-win32_share-class"></a><span data-ttu-id="0c09f-103">Méthode Delete de la \_ classe de partage Win32</span><span class="sxs-lookup"><span data-stu-id="0c09f-103">Delete method of the Win32\_Share class</span></span>

<span data-ttu-id="0c09f-104">La méthode **Delete** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) supprime un nom de partage de la liste des ressources partagées d’un serveur, en déconnectant les connexions à la ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="0c09f-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes a share name from a server's list of shared resources, disconnecting connections to the shared resource.</span></span>

<span data-ttu-id="0c09f-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="0c09f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0c09f-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0c09f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0c09f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c09f-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="0c09f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c09f-108">Parameters</span></span>

<span data-ttu-id="0c09f-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0c09f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0c09f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0c09f-110">Return value</span></span>

<span data-ttu-id="0c09f-111">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="0c09f-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="0c09f-112">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="0c09f-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="0c09f-113">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="0c09f-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="0c09f-114">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="0c09f-114">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0c09f-115">**Accès refusé** (2)</span><span class="sxs-lookup"><span data-stu-id="0c09f-115">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0c09f-116">**Échec inconnu** (8)</span><span class="sxs-lookup"><span data-stu-id="0c09f-116">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0c09f-117">**Nom non valide** (9)</span><span class="sxs-lookup"><span data-stu-id="0c09f-117">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0c09f-118">**Niveau non valide** (10)</span><span class="sxs-lookup"><span data-stu-id="0c09f-118">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0c09f-119">**Paramètre non valide** (21)</span><span class="sxs-lookup"><span data-stu-id="0c09f-119">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="0c09f-120">**Partage en double** (22)</span><span class="sxs-lookup"><span data-stu-id="0c09f-120">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="0c09f-121">**Chemin d’accès Redirigé** (23)</span><span class="sxs-lookup"><span data-stu-id="0c09f-121">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="0c09f-122">**Périphérique ou répertoire inconnu** (24)</span><span class="sxs-lookup"><span data-stu-id="0c09f-122">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="0c09f-123">**Nom de réseau introuvable** (25)</span><span class="sxs-lookup"><span data-stu-id="0c09f-123">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="0c09f-124">**Autre** (26 4294967295)</span><span class="sxs-lookup"><span data-stu-id="0c09f-124">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="0c09f-125">Notes</span><span class="sxs-lookup"><span data-stu-id="0c09f-125">Remarks</span></span>

<span data-ttu-id="0c09f-126">La méthode **Delete** est une méthode d’objet qui est utilisée sur une instance d’une classe.</span><span class="sxs-lookup"><span data-stu-id="0c09f-126">The **Delete** method is an object method and is used on an instance of a class.</span></span>

<span data-ttu-id="0c09f-127">Seuls les membres du groupe local Administrateurs ou opérateurs de compte ou ceux ayant une appartenance de groupe communication, impression ou opérateur de serveur peuvent exécuter la méthode avec succès.</span><span class="sxs-lookup"><span data-stu-id="0c09f-127">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute the method.</span></span> <span data-ttu-id="0c09f-128">L’opérateur Print peut uniquement supprimer des files d’attente d’impression.</span><span class="sxs-lookup"><span data-stu-id="0c09f-128">The Print operator can delete only printer queues.</span></span> <span data-ttu-id="0c09f-129">L’opérateur de communication peut supprimer uniquement les files d’attente de communication des appareils.</span><span class="sxs-lookup"><span data-stu-id="0c09f-129">The Communication operator can delete only communication-device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="0c09f-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="0c09f-130">Examples</span></span>

<span data-ttu-id="0c09f-131">L’exemple de code VBScript suivant supprime le partage spécifié.</span><span class="sxs-lookup"><span data-stu-id="0c09f-131">The following VBScript code sample deletes the specified share.</span></span>


```VB
On Error Resume Next

ComputerName = InputBox("Enter the computer name:", "Delete Share", "localhost")

SName = InputBox("Enter the name of the share:", "Delete Share")



Set Shares = GetObject("winmgmts:\\" & ComputerName & _
 "\root\cimv2").ExecQuery("SELECT * FROM Win32_Share WHERE name = '" & SName & "'")



For Each Share in Shares
 Share.Delete()
Next
```



<span data-ttu-id="0c09f-132">L’exemple de code PowerShell suivant supprime les partages vides.</span><span class="sxs-lookup"><span data-stu-id="0c09f-132">The following PowerShell code sample deletes blank shares.</span></span>


```PowerShell
$Shares = Get-WMIObject Win32_Share | Where {$_.Name -eq ""}

Foreach ($Share in $Shares) {
   $Share.Delete()
}
"{0} blank shares found and removed" -f $shares.count
```



## <a name="requirements"></a><span data-ttu-id="0c09f-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c09f-133">Requirements</span></span>



| <span data-ttu-id="0c09f-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c09f-134">Requirement</span></span> | <span data-ttu-id="0c09f-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c09f-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c09f-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c09f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0c09f-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c09f-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0c09f-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c09f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0c09f-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c09f-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0c09f-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0c09f-140">Namespace</span></span><br/>                | <span data-ttu-id="0c09f-141">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0c09f-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0c09f-142">MOF</span><span class="sxs-lookup"><span data-stu-id="0c09f-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c09f-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c09f-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c09f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0c09f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c09f-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c09f-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c09f-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c09f-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="0c09f-147">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0c09f-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0c09f-148">**\_Partage Win32**</span><span class="sxs-lookup"><span data-stu-id="0c09f-148">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

