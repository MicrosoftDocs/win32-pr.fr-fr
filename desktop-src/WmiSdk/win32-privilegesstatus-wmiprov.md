---
description: Le \_ PrivilegesStatus Win32 &\# 8194 ; La classe WMI fournit des informations sur les privilèges requis pour effectuer une opération. Elle peut être retournée en cas d’échec d’une opération ou lorsqu’une instance partiellement remplie a été retournée.
ms.assetid: 85bda855-1488-4d7a-99ed-798e9859fef7
ms.tgt_platform: multiple
title: Classe Win32_PrivilegesStatus (WMI)
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
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 658803be4e70849531bf52e7368e4e9cbcc2f0a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210721"
---
# <a name="win32_privilegesstatus-class-wmi"></a><span data-ttu-id="cafca-104">Classe Win32_PrivilegesStatus (WMI)</span><span class="sxs-lookup"><span data-stu-id="cafca-104">Win32_PrivilegesStatus class (WMI)</span></span>

<span data-ttu-id="cafca-105">La [classe WMI](retrieving-a-class.md) **Win32 \_ PrivilegesStatus** fournit des informations sur les privilèges requis pour effectuer une opération.   </span><span class="sxs-lookup"><span data-stu-id="cafca-105">The **Win32\_PrivilegesStatus**   [WMI class](retrieving-a-class.md) reports information about privileges required to complete an operation.</span></span> <span data-ttu-id="cafca-106">Elle peut être retournée en cas d’échec d’une opération ou lorsqu’une instance partiellement remplie a été retournée.</span><span class="sxs-lookup"><span data-stu-id="cafca-106">It may be returned when an operation failed or when a partially populated instance has been returned.</span></span>

<span data-ttu-id="cafca-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="cafca-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="cafca-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="cafca-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cafca-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cafca-109">Syntax</span></span>

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}")]
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

## <a name="members"></a><span data-ttu-id="cafca-110">Membres</span><span class="sxs-lookup"><span data-stu-id="cafca-110">Members</span></span>

<span data-ttu-id="cafca-111">La classe **Win32 \_ PrivilegesStatus** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cafca-111">The **Win32\_PrivilegesStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="cafca-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cafca-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cafca-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cafca-113">Properties</span></span>

<span data-ttu-id="cafca-114">La classe **Win32 \_ PrivilegesStatus** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="cafca-114">The **Win32\_PrivilegesStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cafca-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="cafca-115">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafca-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cafca-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafca-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cafca-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cafca-118">Toute chaîne définie par l’utilisateur qui décrit une erreur ou un état opérationnel.</span><span class="sxs-lookup"><span data-stu-id="cafca-118">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="cafca-119">Cette propriété est héritée de [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="cafca-119">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafca-120">**Opération**</span><span class="sxs-lookup"><span data-stu-id="cafca-120">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafca-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cafca-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafca-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cafca-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cafca-123">Opération qui se produit au moment d’une défaillance ou d’une anomalie.</span><span class="sxs-lookup"><span data-stu-id="cafca-123">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="cafca-124">En règle générale, Windows Management Instrumentation (WMI) définit cette propriété sur le nom d’une API COM pour la méthode WMI, telle que la suivante : [**IWbemServices :: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="cafca-124">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="cafca-125">Cette propriété est héritée de [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="cafca-125">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafca-126">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="cafca-126">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafca-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cafca-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafca-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cafca-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cafca-129">Paramètres impliqués dans une modification d’erreur ou d’État.</span><span class="sxs-lookup"><span data-stu-id="cafca-129">Parameters involved in an error or status change.</span></span> <span data-ttu-id="cafca-130">Par exemple, si une application tente de récupérer une classe qui n’existe pas, cette propriété est définie sur le nom de la classe incriminée.</span><span class="sxs-lookup"><span data-stu-id="cafca-130">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="cafca-131">Cette propriété est héritée de [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="cafca-131">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafca-132">**PrivilegesNotHeld**</span><span class="sxs-lookup"><span data-stu-id="cafca-132">**PrivilegesNotHeld**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafca-133">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="cafca-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cafca-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cafca-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cafca-135">Liste des privilèges d’accès requis manquants pour terminer une opération.</span><span class="sxs-lookup"><span data-stu-id="cafca-135">Listing required access privileges missing to complete an operation.</span></span> <span data-ttu-id="cafca-136">Les types de privilèges d’accès se trouvent sous les privilèges Windows.</span><span class="sxs-lookup"><span data-stu-id="cafca-136">The types of access privileges can be found under the Windows Privileges.</span></span>

<span data-ttu-id="cafca-137">Exemple : « SE \_ arrêter le \_ nom »</span><span class="sxs-lookup"><span data-stu-id="cafca-137">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="cafca-138">**PrivilegesRequired**</span><span class="sxs-lookup"><span data-stu-id="cafca-138">**PrivilegesRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafca-139">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="cafca-139">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cafca-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cafca-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cafca-141">Liste de tous les privilèges requis pour effectuer une opération.</span><span class="sxs-lookup"><span data-stu-id="cafca-141">Listing of all of the privileges required to perform an operation.</span></span> <span data-ttu-id="cafca-142">Cela comprend les valeurs de la propriété **PrivilegesNotHeld** .</span><span class="sxs-lookup"><span data-stu-id="cafca-142">This includes values from the **PrivilegesNotHeld** property.</span></span>

<span data-ttu-id="cafca-143">Exemple : « SE \_ arrêter le \_ nom »</span><span class="sxs-lookup"><span data-stu-id="cafca-143">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="cafca-144">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="cafca-144">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafca-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cafca-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafca-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cafca-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cafca-147">Identifie le fournisseur qui provoque ou signale une modification d’erreur ou d’État.</span><span class="sxs-lookup"><span data-stu-id="cafca-147">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="cafca-148">Si aucun fournisseur n’est impliqué, cette chaîne est définie sur « Windows Management ».</span><span class="sxs-lookup"><span data-stu-id="cafca-148">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="cafca-149">Cette propriété est héritée de [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="cafca-149">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafca-150">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="cafca-150">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafca-151">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cafca-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cafca-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cafca-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cafca-153">Contient une erreur ou un code d’information pour une opération.</span><span class="sxs-lookup"><span data-stu-id="cafca-153">Contains an error or information code for an operation.</span></span> <span data-ttu-id="cafca-154">Il peut s’agir de n’importe quelle valeur définie par le fournisseur, mais la valeur 0 (zéro) est généralement réservée pour indiquer la réussite.</span><span class="sxs-lookup"><span data-stu-id="cafca-154">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="cafca-155">Cette propriété est héritée de [**\_ \_ NotifyStatus**](--notifystatus.md).</span><span class="sxs-lookup"><span data-stu-id="cafca-155">This property is inherited from [**\_\_NotifyStatus**](--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cafca-156">Notes</span><span class="sxs-lookup"><span data-stu-id="cafca-156">Remarks</span></span>

<span data-ttu-id="cafca-157">La classe **Win32 \_ PrivilegesStatus** est dérivée de [**\_ \_ ExtendedStatus**](--extendedstatus.md).</span><span class="sxs-lookup"><span data-stu-id="cafca-157">The **Win32\_PrivilegesStatus** class is derived from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cafca-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cafca-158">Requirements</span></span>



| <span data-ttu-id="cafca-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cafca-159">Requirement</span></span> | <span data-ttu-id="cafca-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="cafca-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cafca-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cafca-161">Minimum supported client</span></span><br/> | <span data-ttu-id="cafca-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cafca-162">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="cafca-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cafca-163">Minimum supported server</span></span><br/> | <span data-ttu-id="cafca-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cafca-164">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="cafca-165">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cafca-165">Namespace</span></span><br/>                | <span data-ttu-id="cafca-166">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="cafca-166">Root\\WMI</span></span><br/>                                                               |
| <span data-ttu-id="cafca-167">MOF</span><span class="sxs-lookup"><span data-stu-id="cafca-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cafca-168"><dt>WMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cafca-168"><dt>Wmi.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cafca-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cafca-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cafca-170">**\_\_ExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="cafca-170">**\_\_ExtendedStatus**</span></span>](--extendedstatus.md)
</dt> </dl>

 

 




