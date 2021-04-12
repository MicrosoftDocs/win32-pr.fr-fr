---
description: SetShareInfo&\# 8194 ; La méthode de classe WMI définit les paramètres d’une ressource partagée.
ms.assetid: f6379261-9325-4b7f-92df-438c5029569f
ms.tgt_platform: multiple
title: Méthode SetShareInfo de la classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 54b599ed3124c0d06468bd15589d6aa8a93fb7c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201133"
---
# <a name="setshareinfo-method-of-the-win32_share-class"></a><span data-ttu-id="d3fa6-103">Méthode SetShareInfo de la \_ classe de partage Win32</span><span class="sxs-lookup"><span data-stu-id="d3fa6-103">SetShareInfo method of the Win32\_Share class</span></span>

<span data-ttu-id="d3fa6-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetShareInfo** définit les paramètres d’une ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="d3fa6-104">The **SetShareInfo** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the parameters of a shared resource.</span></span>

<span data-ttu-id="d3fa6-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="d3fa6-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d3fa6-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d3fa6-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d3fa6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3fa6-107">Syntax</span></span>


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="d3fa6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3fa6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3fa6-109">*MaximumAllowed* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d3fa6-109">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d3fa6-110">Limite du nombre maximal d’utilisateurs autorisés à utiliser cette ressource simultanément.</span><span class="sxs-lookup"><span data-stu-id="d3fa6-110">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

<span data-ttu-id="d3fa6-111">Exemple : 10.</span><span class="sxs-lookup"><span data-stu-id="d3fa6-111">Example: 10.</span></span> <span data-ttu-id="d3fa6-112">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="d3fa6-112">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="d3fa6-113">*Description* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d3fa6-113">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d3fa6-114">Commentaire facultatif pour décrire la ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="d3fa6-114">Optional comment to describe the resource being shared.</span></span>

</dd> <dt>

<span data-ttu-id="d3fa6-115">*Accès* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d3fa6-115">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d3fa6-116">Descripteur de sécurité pour les autorisations au niveau de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d3fa6-116">Security descriptor for user-level permissions.</span></span> <span data-ttu-id="d3fa6-117">Un descripteur de sécurité contient des informations sur l’autorisation, le propriétaire et les capacités d’accès de la ressource.</span><span class="sxs-lookup"><span data-stu-id="d3fa6-117">A security descriptor contains information about the permission, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="d3fa6-118">Pour plus d’informations, [**consultez \_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="d3fa6-118">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3fa6-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d3fa6-119">Return value</span></span>

<span data-ttu-id="d3fa6-120">Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="d3fa6-120">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d3fa6-121">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="d3fa6-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d3fa6-122">**Accès refusé** (2)</span><span class="sxs-lookup"><span data-stu-id="d3fa6-122">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d3fa6-123">**Échec inconnu** (8)</span><span class="sxs-lookup"><span data-stu-id="d3fa6-123">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d3fa6-124">**Nom non valide** (9)</span><span class="sxs-lookup"><span data-stu-id="d3fa6-124">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d3fa6-125">**Niveau non valide** (10)</span><span class="sxs-lookup"><span data-stu-id="d3fa6-125">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d3fa6-126">**Paramètre non valide** (21)</span><span class="sxs-lookup"><span data-stu-id="d3fa6-126">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="d3fa6-127">**Partage en double** (22)</span><span class="sxs-lookup"><span data-stu-id="d3fa6-127">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="d3fa6-128">**Chemin d’accès Redirigé** (23)</span><span class="sxs-lookup"><span data-stu-id="d3fa6-128">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="d3fa6-129">**Périphérique ou répertoire inconnu** (24)</span><span class="sxs-lookup"><span data-stu-id="d3fa6-129">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="d3fa6-130">**Nom de réseau introuvable** (25)</span><span class="sxs-lookup"><span data-stu-id="d3fa6-130">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="d3fa6-131">**Autre** (26 4294967295)</span><span class="sxs-lookup"><span data-stu-id="d3fa6-131">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="d3fa6-132">Notes</span><span class="sxs-lookup"><span data-stu-id="d3fa6-132">Remarks</span></span>

<span data-ttu-id="d3fa6-133">La méthode **SetShareInfo** est une méthode d’objet dynamique qui est utilisée sur une occurrence de cette classe.</span><span class="sxs-lookup"><span data-stu-id="d3fa6-133">**SetShareInfo** method is a dynamic object method and is used on an occurrence of this class.</span></span>

<span data-ttu-id="d3fa6-134">Seuls les membres du groupe local Administrateurs ou opérateurs de compte ou ceux ayant une appartenance de groupe communication, impression ou opérateur de serveur peuvent exécuter **SetShareInfo**.</span><span class="sxs-lookup"><span data-stu-id="d3fa6-134">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute **SetShareInfo**.</span></span> <span data-ttu-id="d3fa6-135">L’opérateur Print peut uniquement définir des files d’attente d’impression.</span><span class="sxs-lookup"><span data-stu-id="d3fa6-135">The print operator can only set printer queues.</span></span> <span data-ttu-id="d3fa6-136">L’opérateur de communication ne peut définir que des files d’attente d’appareils de communication.</span><span class="sxs-lookup"><span data-stu-id="d3fa6-136">The Communication operator can only set communication device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="d3fa6-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="d3fa6-137">Examples</span></span>

<span data-ttu-id="d3fa6-138">L’exemple PowerShell suivant met à jour le nom du partage **newShare** .</span><span class="sxs-lookup"><span data-stu-id="d3fa6-138">The following PowerShell sample updates the name of the **newShare** share.</span></span>


```PowerShell
$newShare = Get-WmiObject win32_share | Where-Object {$_.name -eq "newShare"}
[void]$newShare.SetShareInfo($null,"This is my new description",$null)
```



## <a name="requirements"></a><span data-ttu-id="d3fa6-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3fa6-139">Requirements</span></span>



| <span data-ttu-id="d3fa6-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3fa6-140">Requirement</span></span> | <span data-ttu-id="d3fa6-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3fa6-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3fa6-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3fa6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d3fa6-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3fa6-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d3fa6-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3fa6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d3fa6-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3fa6-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d3fa6-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d3fa6-146">Namespace</span></span><br/>                | <span data-ttu-id="d3fa6-147">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d3fa6-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d3fa6-148">MOF</span><span class="sxs-lookup"><span data-stu-id="d3fa6-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3fa6-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3fa6-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3fa6-150">DLL</span><span class="sxs-lookup"><span data-stu-id="d3fa6-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3fa6-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3fa6-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3fa6-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3fa6-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="d3fa6-153">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3fa6-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d3fa6-154">**\_Partage Win32**</span><span class="sxs-lookup"><span data-stu-id="d3fa6-154">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

