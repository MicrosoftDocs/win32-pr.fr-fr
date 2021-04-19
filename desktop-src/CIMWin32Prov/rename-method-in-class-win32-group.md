---
description: Autorise la modification du nom du groupe.
ms.assetid: 7eb1360e-7416-4a90-abc6-c9a85a114316
ms.tgt_platform: multiple
title: Renommer la méthode de la classe Win32_Group
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c111a0c12d0fdc1ce3f6d6bcaa0e7b0f57831054
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513912"
---
# <a name="rename-method-of-the-win32_group-class"></a><span data-ttu-id="da48a-103">Renommer la méthode de la \_ classe de groupe Win32</span><span class="sxs-lookup"><span data-stu-id="da48a-103">Rename method of the Win32\_Group class</span></span>

<span data-ttu-id="da48a-104">La méthode de la classe **Renommer** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) permet de modifier le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="da48a-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method allows the group name to be changed.</span></span>

<span data-ttu-id="da48a-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="da48a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="da48a-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="da48a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="da48a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da48a-107">Syntax</span></span>


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="da48a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da48a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da48a-109">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da48a-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da48a-110">Nom du compte d’utilisateur Windows sur le domaine spécifié par la propriété de **domaine** de cette classe.</span><span class="sxs-lookup"><span data-stu-id="da48a-110">Name of the Windows user account on the domain specified by the **Domain** property of this class.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da48a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da48a-111">Return value</span></span>

<span data-ttu-id="da48a-112">La méthode **Rename** peut retourner les codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="da48a-112">The **Rename** method can return the error codes listed in the following list.</span></span> <span data-ttu-id="da48a-113">Pour les valeurs entières autres que celles listées, reportez-vous à [ \_ codes de retour WMI](/windows/desktop/WmiSdk/wmi-return-codes).</span><span class="sxs-lookup"><span data-stu-id="da48a-113">For integer values other than those listed, refer to [WMI\_Return Codes](/windows/desktop/WmiSdk/wmi-return-codes).</span></span>

<dl> <dt>

<span data-ttu-id="da48a-114">**Success**</span><span class="sxs-lookup"><span data-stu-id="da48a-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="da48a-115">0</span><span class="sxs-lookup"><span data-stu-id="da48a-115">0</span></span>

<span data-ttu-id="da48a-116">Réussite.</span><span class="sxs-lookup"><span data-stu-id="da48a-116">Success.</span></span>

</dd> <dt>

<span data-ttu-id="da48a-117">**Instance introuvable**</span><span class="sxs-lookup"><span data-stu-id="da48a-117">**Instance not found**</span></span>
</dt> <dd>

<span data-ttu-id="da48a-118">1</span><span class="sxs-lookup"><span data-stu-id="da48a-118">1</span></span>

</dd> <dt>

<span data-ttu-id="da48a-119">**Instance obligatoire**</span><span class="sxs-lookup"><span data-stu-id="da48a-119">**Instance required**</span></span>
</dt> <dd>

<span data-ttu-id="da48a-120">2</span><span class="sxs-lookup"><span data-stu-id="da48a-120">2</span></span>

</dd> <dt>

<span data-ttu-id="da48a-121">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="da48a-121">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="da48a-122">3</span><span class="sxs-lookup"><span data-stu-id="da48a-122">3</span></span>

</dd> <dt>

<span data-ttu-id="da48a-123">**Groupe introuvable**</span><span class="sxs-lookup"><span data-stu-id="da48a-123">**Group not found**</span></span>
</dt> <dd>

<span data-ttu-id="da48a-124">4</span><span class="sxs-lookup"><span data-stu-id="da48a-124">4</span></span>

</dd> <dt>

<span data-ttu-id="da48a-125">**Domaine introuvable**</span><span class="sxs-lookup"><span data-stu-id="da48a-125">**Domain not found**</span></span>
</dt> <dd>

<span data-ttu-id="da48a-126">5</span><span class="sxs-lookup"><span data-stu-id="da48a-126">5</span></span>

</dd> <dt>

<span data-ttu-id="da48a-127">**L’opération est autorisée uniquement sur le contrôleur de domaine principal du domaine**</span><span class="sxs-lookup"><span data-stu-id="da48a-127">**Operation is allowed only on the primary domain controller of the domain**</span></span>
</dt> <dd>

<span data-ttu-id="da48a-128">6</span><span class="sxs-lookup"><span data-stu-id="da48a-128">6</span></span>

</dd> <dt>

<span data-ttu-id="da48a-129">**L’opération n’est pas autorisée sur les groupes spéciaux spécifiés ; utilisateur, administrateur, local ou invité.**</span><span class="sxs-lookup"><span data-stu-id="da48a-129">**Operation is not allowed on specified special groups; user, admin, local or guest.**</span></span>
</dt> <dd>

<span data-ttu-id="da48a-130">7</span><span class="sxs-lookup"><span data-stu-id="da48a-130">7</span></span>

</dd> <dt>

<span data-ttu-id="da48a-131">**Autre erreur d’API**</span><span class="sxs-lookup"><span data-stu-id="da48a-131">**Other API error**</span></span>
</dt> <dd>

<span data-ttu-id="da48a-132">8</span><span class="sxs-lookup"><span data-stu-id="da48a-132">8</span></span>

</dd> <dt>

<span data-ttu-id="da48a-133">**Erreur interne**</span><span class="sxs-lookup"><span data-stu-id="da48a-133">**Internal error**</span></span>
</dt> <dd>

<span data-ttu-id="da48a-134">9</span><span class="sxs-lookup"><span data-stu-id="da48a-134">9</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da48a-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da48a-135">Requirements</span></span>



| <span data-ttu-id="da48a-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da48a-136">Requirement</span></span> | <span data-ttu-id="da48a-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="da48a-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da48a-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da48a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="da48a-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da48a-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da48a-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da48a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="da48a-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da48a-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da48a-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="da48a-142">Namespace</span></span><br/>                | <span data-ttu-id="da48a-143">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="da48a-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="da48a-144">MOF</span><span class="sxs-lookup"><span data-stu-id="da48a-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da48a-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da48a-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="da48a-146">DLL</span><span class="sxs-lookup"><span data-stu-id="da48a-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da48a-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da48a-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da48a-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da48a-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="da48a-149">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="da48a-149">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="da48a-150">**\_Groupe Win32**</span><span class="sxs-lookup"><span data-stu-id="da48a-150">**Win32\_Group**</span></span>](win32-group.md)
</dt> <dt>

[<span data-ttu-id="da48a-151">**\_LogicalFileSecuritySetting Win32**</span><span class="sxs-lookup"><span data-stu-id="da48a-151">**Win32\_LogicalFileSecuritySetting**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)
</dt> </dl>

 

