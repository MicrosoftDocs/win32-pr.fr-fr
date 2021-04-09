---
description: Renomme un nom de compte d’utilisateur.
ms.assetid: 90258256-7470-4ec8-afce-bea0f64b90fb
ms.tgt_platform: multiple
title: Renommer la méthode de la classe Win32_UserAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 27d495804fb68bc74eda269c2dd7921540f05f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111247"
---
# <a name="rename-method-of-the-win32_useraccount-class"></a><span data-ttu-id="84d47-103">Renommer la méthode de la \_ classe UserAccount Win32</span><span class="sxs-lookup"><span data-stu-id="84d47-103">Rename method of the Win32\_UserAccount class</span></span>

<span data-ttu-id="84d47-104">La méthode de la classe **Renommer** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) renomme le nom d’un compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="84d47-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames a user account name.</span></span>

<span data-ttu-id="84d47-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="84d47-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="84d47-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="84d47-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="84d47-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84d47-107">Syntax</span></span>


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="84d47-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84d47-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84d47-109">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84d47-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84d47-110">Nouveau nom du compte.</span><span class="sxs-lookup"><span data-stu-id="84d47-110">New account name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84d47-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="84d47-111">Return value</span></span>

<span data-ttu-id="84d47-112">Retourne l’une des valeurs répertoriées dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="84d47-112">Returns one of the values listed in the following list.</span></span> <span data-ttu-id="84d47-113">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="84d47-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="84d47-114">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="84d47-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="84d47-115">**Success**</span><span class="sxs-lookup"><span data-stu-id="84d47-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="84d47-116">0</span><span class="sxs-lookup"><span data-stu-id="84d47-116">0</span></span>

<span data-ttu-id="84d47-117">Réussite.</span><span class="sxs-lookup"><span data-stu-id="84d47-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="84d47-118">**Instance introuvable**</span><span class="sxs-lookup"><span data-stu-id="84d47-118">**Instance not found**</span></span>
</dt> <dd>

<span data-ttu-id="84d47-119">1</span><span class="sxs-lookup"><span data-stu-id="84d47-119">1</span></span>

<span data-ttu-id="84d47-120">Instance introuvable.</span><span class="sxs-lookup"><span data-stu-id="84d47-120">Instance not found.</span></span>

</dd> <dt>

<span data-ttu-id="84d47-121">**Instance obligatoire**</span><span class="sxs-lookup"><span data-stu-id="84d47-121">**Instance required**</span></span>
</dt> <dd>

<span data-ttu-id="84d47-122">2</span><span class="sxs-lookup"><span data-stu-id="84d47-122">2</span></span>

<span data-ttu-id="84d47-123">Instance obligatoire.</span><span class="sxs-lookup"><span data-stu-id="84d47-123">Instance required.</span></span>

</dd> <dt>

<span data-ttu-id="84d47-124">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="84d47-124">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="84d47-125">3</span><span class="sxs-lookup"><span data-stu-id="84d47-125">3</span></span>

<span data-ttu-id="84d47-126">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="84d47-126">Invalid parameter.</span></span>

</dd> <dt>

<span data-ttu-id="84d47-127">**Utilisateur non trouvé.**</span><span class="sxs-lookup"><span data-stu-id="84d47-127">**User not found**</span></span>
</dt> <dd>

<span data-ttu-id="84d47-128">4</span><span class="sxs-lookup"><span data-stu-id="84d47-128">4</span></span>

<span data-ttu-id="84d47-129">Utilisateur introuvable.</span><span class="sxs-lookup"><span data-stu-id="84d47-129">User not found.</span></span>

</dd> <dt>

<span data-ttu-id="84d47-130">**Domaine introuvable**</span><span class="sxs-lookup"><span data-stu-id="84d47-130">**Domain not found**</span></span>
</dt> <dd>

<span data-ttu-id="84d47-131">5</span><span class="sxs-lookup"><span data-stu-id="84d47-131">5</span></span>

<span data-ttu-id="84d47-132">Domaine introuvable.</span><span class="sxs-lookup"><span data-stu-id="84d47-132">Domain not found.</span></span>

</dd> <dt>

<span data-ttu-id="84d47-133">**L’opération est autorisée uniquement sur le contrôleur de domaine principal du domaine**</span><span class="sxs-lookup"><span data-stu-id="84d47-133">**Operation is allowed only on the primary domain controller of the domain**</span></span>
</dt> <dd>

<span data-ttu-id="84d47-134">6</span><span class="sxs-lookup"><span data-stu-id="84d47-134">6</span></span>

<span data-ttu-id="84d47-135">L’opération est autorisée uniquement sur le contrôleur de domaine principal du domaine.</span><span class="sxs-lookup"><span data-stu-id="84d47-135">Operation is allowed only on the primary domain controller of the domain.</span></span>

</dd> <dt>

<span data-ttu-id="84d47-136">**L’opération n’est pas autorisée sur le dernier compte d’administration.**</span><span class="sxs-lookup"><span data-stu-id="84d47-136">**Operation is not allowed on the last administrative account.**</span></span>
</dt> <dd>

<span data-ttu-id="84d47-137">7</span><span class="sxs-lookup"><span data-stu-id="84d47-137">7</span></span>

</dd> <dt>

<span data-ttu-id="84d47-138">**L’opération n’est pas autorisée sur les groupes spéciaux spécifiés ; utilisateur, administrateur, local ou invité.**</span><span class="sxs-lookup"><span data-stu-id="84d47-138">**Operation is not allowed on specified special groups; user, admin, local or guest.**</span></span>
</dt> <dd>

<span data-ttu-id="84d47-139">8</span><span class="sxs-lookup"><span data-stu-id="84d47-139">8</span></span>

<span data-ttu-id="84d47-140">L’opération n’est pas autorisée sur les groupes spéciaux spécifiés : utilisateur, administrateur, local ou invité.</span><span class="sxs-lookup"><span data-stu-id="84d47-140">Operation is not allowed on specified special groups: user, admin, local, or guest.</span></span>

</dd> <dt>

<span data-ttu-id="84d47-141">**Autre erreur d’API**</span><span class="sxs-lookup"><span data-stu-id="84d47-141">**Other API error**</span></span>
</dt> <dd>

<span data-ttu-id="84d47-142">9</span><span class="sxs-lookup"><span data-stu-id="84d47-142">9</span></span>

<span data-ttu-id="84d47-143">Autre erreur d’API.</span><span class="sxs-lookup"><span data-stu-id="84d47-143">Other API error.</span></span>

</dd> <dt>

<span data-ttu-id="84d47-144">**Erreur interne**</span><span class="sxs-lookup"><span data-stu-id="84d47-144">**Internal error**</span></span>
</dt> <dd>

<span data-ttu-id="84d47-145">10</span><span class="sxs-lookup"><span data-stu-id="84d47-145">10</span></span>

<span data-ttu-id="84d47-146">Erreur interne.</span><span class="sxs-lookup"><span data-stu-id="84d47-146">Internal error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84d47-147">Notes</span><span class="sxs-lookup"><span data-stu-id="84d47-147">Remarks</span></span>

<span data-ttu-id="84d47-148">Cette fonctionnalité est implémentée en tant que méthode pour fournir un contexte distinct pour le nouveau nom qui peut être distingué de la valeur de propriété de clé pour le nom associé à l’instance à modifier.</span><span class="sxs-lookup"><span data-stu-id="84d47-148">This functionality is implemented as a method to provide a separate context for the new name that is distinguishable from the key property value for Name that is associated with the instance to be modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="84d47-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84d47-149">Requirements</span></span>



| <span data-ttu-id="84d47-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84d47-150">Requirement</span></span> | <span data-ttu-id="84d47-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="84d47-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84d47-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84d47-152">Minimum supported client</span></span><br/> | <span data-ttu-id="84d47-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84d47-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="84d47-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84d47-154">Minimum supported server</span></span><br/> | <span data-ttu-id="84d47-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84d47-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="84d47-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="84d47-156">Namespace</span></span><br/>                | <span data-ttu-id="84d47-157">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="84d47-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="84d47-158">MOF</span><span class="sxs-lookup"><span data-stu-id="84d47-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84d47-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84d47-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="84d47-160">DLL</span><span class="sxs-lookup"><span data-stu-id="84d47-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84d47-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84d47-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84d47-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84d47-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84d47-163">**\_UserAccount Win32**</span><span class="sxs-lookup"><span data-stu-id="84d47-163">**Win32\_UserAccount**</span></span>](win32-useraccount.md)
</dt> <dt>

<span data-ttu-id="84d47-164">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="84d47-164">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

