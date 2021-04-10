---
description: Le \_ PrivilegesStatus Win32&\# 8194 ; La classe WMI fournit des informations sur les privilèges requis pour effectuer une opération. Elle peut être retournée en cas d’échec d’une opération ou lorsqu’une instance partiellement remplie a été retournée.
ms.assetid: 295ec2bd-7996-4031-8503-d4e869d8368d
ms.tgt_platform: multiple
title: Win32_PrivilegesStatus, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrivilegesStatus
- Win32_PrivilegesStatus.Description
- Win32_PrivilegesStatus.Operation
- Win32_PrivilegesStatus.ParameterInfo
- Win32_PrivilegesStatus.ProviderName
- Win32_PrivilegesStatus.StatusCode
- Win32_PrivilegesStatus.PrivilegesNotHeld
- Win32_PrivilegesStatus.PrivilegesRequired
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ab399ce08374a954b3bbc015cfee7b4d20167b70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861169"
---
# <a name="win32_privilegesstatus-class-cimwin32-wmi-providers"></a><span data-ttu-id="0cf96-104">Win32_PrivilegesStatus, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="0cf96-104">Win32_PrivilegesStatus class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="0cf96-105">La  [classe WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ PrivilegesStatus** fournit des informations sur les privilèges requis pour effectuer une opération.</span><span class="sxs-lookup"><span data-stu-id="0cf96-105">The **Win32\_PrivilegesStatus** [WMI class](../wmisdk/retrieving-a-class.md) reports information about privileges required to complete an operation.</span></span> <span data-ttu-id="0cf96-106">Elle peut être retournée en cas d’échec d’une opération ou lorsqu’une instance partiellement remplie a été retournée.</span><span class="sxs-lookup"><span data-stu-id="0cf96-106">It may be returned when an operation failed or when a partially populated instance has been returned.</span></span>

<span data-ttu-id="0cf96-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0cf96-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0cf96-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="0cf96-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cf96-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0cf96-109">Syntax</span></span>

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}"), AMENDMENT]
class Win32_PrivilegesStatus : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string PrivilegesNotHeld[];
  string PrivilegesRequired[];
};
```

## <a name="members"></a><span data-ttu-id="0cf96-110">Membres</span><span class="sxs-lookup"><span data-stu-id="0cf96-110">Members</span></span>

<span data-ttu-id="0cf96-111">La classe **Win32 \_ PrivilegesStatus** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0cf96-111">The **Win32\_PrivilegesStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="0cf96-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0cf96-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0cf96-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0cf96-113">Properties</span></span>

<span data-ttu-id="0cf96-114">La classe **Win32 \_ PrivilegesStatus** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0cf96-114">The **Win32\_PrivilegesStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0cf96-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="0cf96-115">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cf96-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0cf96-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cf96-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0cf96-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cf96-118">Toute chaîne définie par l’utilisateur qui décrit une erreur ou un état opérationnel.</span><span class="sxs-lookup"><span data-stu-id="0cf96-118">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="0cf96-119">Cette propriété est héritée de [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="0cf96-119">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cf96-120">**Opération**</span><span class="sxs-lookup"><span data-stu-id="0cf96-120">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cf96-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0cf96-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cf96-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0cf96-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cf96-123">Opération qui se produit au moment d’une défaillance ou d’une anomalie.</span><span class="sxs-lookup"><span data-stu-id="0cf96-123">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="0cf96-124">En règle générale, Windows Management Instrumentation (WMI) définit cette propriété sur le nom d’une API COM pour la méthode WMI, telle que la suivante : [**IWbemServices :: CreateInstanceEnum**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="0cf96-124">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="0cf96-125">Cette propriété est héritée de [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="0cf96-125">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cf96-126">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="0cf96-126">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cf96-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0cf96-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cf96-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0cf96-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cf96-129">Paramètres impliqués dans une modification d’erreur ou d’État.</span><span class="sxs-lookup"><span data-stu-id="0cf96-129">Parameters involved in an error or status change.</span></span> <span data-ttu-id="0cf96-130">Par exemple, si une application tente de récupérer une classe qui n’existe pas, cette propriété est définie sur le nom de la classe incriminée.</span><span class="sxs-lookup"><span data-stu-id="0cf96-130">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="0cf96-131">Cette propriété est héritée de [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="0cf96-131">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cf96-132">**PrivilegesNotHeld**</span><span class="sxs-lookup"><span data-stu-id="0cf96-132">**PrivilegesNotHeld**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cf96-133">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="0cf96-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0cf96-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0cf96-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cf96-135">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| AccessControl \| Windows NT PRIVILEGES")</span><span class="sxs-lookup"><span data-stu-id="0cf96-135">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|AccessControl\|Windows NT Privileges")</span></span>
</dt> </dl>

<span data-ttu-id="0cf96-136">Liste des privilèges d’accès requis manquants pour terminer une opération.</span><span class="sxs-lookup"><span data-stu-id="0cf96-136">Listing required access privileges missing to complete an operation.</span></span> <span data-ttu-id="0cf96-137">Les types de privilèges d’accès se trouvent sous les privilèges Windows.</span><span class="sxs-lookup"><span data-stu-id="0cf96-137">The types of access privileges can be found under the Windows Privileges.</span></span>

<span data-ttu-id="0cf96-138">Exemple : « SE \_ arrêter le \_ nom »</span><span class="sxs-lookup"><span data-stu-id="0cf96-138">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="0cf96-139">**PrivilegesRequired**</span><span class="sxs-lookup"><span data-stu-id="0cf96-139">**PrivilegesRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cf96-140">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="0cf96-140">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0cf96-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0cf96-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cf96-142">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| AccessControl \| Windows NT PRIVILEGES")</span><span class="sxs-lookup"><span data-stu-id="0cf96-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|AccessControl\|Windows NT Privileges")</span></span>
</dt> </dl>

<span data-ttu-id="0cf96-143">Liste de tous les privilèges requis pour effectuer une opération.</span><span class="sxs-lookup"><span data-stu-id="0cf96-143">Listing of all of the privileges required to perform an operation.</span></span> <span data-ttu-id="0cf96-144">Cela comprend les valeurs de la propriété **PrivilegesNotHeld** .</span><span class="sxs-lookup"><span data-stu-id="0cf96-144">This includes values from the **PrivilegesNotHeld** property.</span></span>

<span data-ttu-id="0cf96-145">Exemple : « SE \_ arrêter le \_ nom »</span><span class="sxs-lookup"><span data-stu-id="0cf96-145">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="0cf96-146">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="0cf96-146">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cf96-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0cf96-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cf96-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0cf96-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cf96-149">Identifie le fournisseur qui provoque ou signale une modification d’erreur ou d’État.</span><span class="sxs-lookup"><span data-stu-id="0cf96-149">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="0cf96-150">Si aucun fournisseur n’est impliqué, cette chaîne est définie sur « Windows Management ».</span><span class="sxs-lookup"><span data-stu-id="0cf96-150">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="0cf96-151">Cette propriété est héritée de [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="0cf96-151">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cf96-152">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="0cf96-152">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cf96-153">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0cf96-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0cf96-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0cf96-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cf96-155">Contient une erreur ou un code d’information pour une opération.</span><span class="sxs-lookup"><span data-stu-id="0cf96-155">Contains an error or information code for an operation.</span></span> <span data-ttu-id="0cf96-156">Il peut s’agir de n’importe quelle valeur définie par le fournisseur, mais la valeur 0 (zéro) est généralement réservée pour indiquer la réussite.</span><span class="sxs-lookup"><span data-stu-id="0cf96-156">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span>

<span data-ttu-id="0cf96-157">Cette propriété est héritée de [**\_ \_ NotifyStatus**](../wmisdk/--notifystatus.md).</span><span class="sxs-lookup"><span data-stu-id="0cf96-157">This property is inherited from [**\_\_NotifyStatus**](../wmisdk/--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0cf96-158">Notes</span><span class="sxs-lookup"><span data-stu-id="0cf96-158">Remarks</span></span>

<span data-ttu-id="0cf96-159">La classe **Win32 \_ PrivilegesStatus** est dérivée de [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="0cf96-159">The **Win32\_PrivilegesStatus** class is derived from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0cf96-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0cf96-160">Requirements</span></span>



| <span data-ttu-id="0cf96-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0cf96-161">Requirement</span></span> | <span data-ttu-id="0cf96-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cf96-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cf96-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cf96-163">Minimum supported client</span></span><br/> | <span data-ttu-id="0cf96-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0cf96-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0cf96-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cf96-165">Minimum supported server</span></span><br/> | <span data-ttu-id="0cf96-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0cf96-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0cf96-167">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0cf96-167">Namespace</span></span><br/>                | <span data-ttu-id="0cf96-168">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0cf96-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0cf96-169">MOF</span><span class="sxs-lookup"><span data-stu-id="0cf96-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0cf96-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0cf96-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0cf96-171">DLL</span><span class="sxs-lookup"><span data-stu-id="0cf96-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cf96-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cf96-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cf96-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cf96-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cf96-174">**\_\_ExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="0cf96-174">**\_\_ExtendedStatus**</span></span>](../wmisdk/--extendedstatus.md)
</dt> </dl>

 

 
