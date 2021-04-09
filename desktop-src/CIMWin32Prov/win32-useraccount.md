---
description: Le \_ UserAccount Win32&\# 32 ; La classe WMI contient des informations sur un compte d’utilisateur sur un système informatique exécutant Windows.
ms.assetid: 747b2ce2-ae38-47de-bf3a-97058df56a7a
ms.tgt_platform: multiple
title: Classe Win32_UserAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount
- Win32_UserAccount.AccountType
- Win32_UserAccount.Caption
- Win32_UserAccount.Description
- Win32_UserAccount.Disabled
- Win32_UserAccount.Domain
- Win32_UserAccount.FullName
- Win32_UserAccount.InstallDate
- Win32_UserAccount.LocalAccount
- Win32_UserAccount.Lockout
- Win32_UserAccount.Name
- Win32_UserAccount.PasswordChangeable
- Win32_UserAccount.PasswordExpires
- Win32_UserAccount.PasswordRequired
- Win32_UserAccount.SID
- Win32_UserAccount.SIDType
- Win32_UserAccount.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5af83f7a52e9f3db9dbaa4a959bfe01ae740746
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033625"
---
# <a name="win32_useraccount-class"></a><span data-ttu-id="eaafd-103">\_Classe UserAccount Win32</span><span class="sxs-lookup"><span data-stu-id="eaafd-103">Win32\_UserAccount class</span></span>

<span data-ttu-id="eaafd-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ UserAccount** WMI contient des informations sur un compte d’utilisateur sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="eaafd-104">The **Win32\_UserAccount** [WMI class](../wmisdk/retrieving-a-class.md) contains information about a user account on a computer system running Windows.</span></span>

> [!Note]  
> <span data-ttu-id="eaafd-105">Étant donné que le **nom** et le **domaine** sont tous les deux des propriétés de clé, l’énumération de **\_ UserAccount Win32** sur un réseau de grande taille peut avoir un impact négatif sur les performances.</span><span class="sxs-lookup"><span data-stu-id="eaafd-105">Because both the **Name** and **Domain** are key properties, enumerating **Win32\_UserAccount** on a large network can negatively affect performance.</span></span> <span data-ttu-id="eaafd-106">L’appel de **GetObject** ou l’interrogation d’une instance spécifique a moins d’impact.</span><span class="sxs-lookup"><span data-stu-id="eaafd-106">Calling **GetObject** or querying for a specific instance has less impact.</span></span>

 

<span data-ttu-id="eaafd-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="eaafd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="eaafd-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="eaafd-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaafd-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eaafd-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserAccount : Win32_Account
{
  uint32   AccountType;
  string   Caption;
  string   Description;
  boolean  Disabled;
  string   Domain;
  string   FullName;
  datetime InstallDate;
  boolean  LocalAccount;
  boolean  Lockout;
  string   Name;
  boolean  PasswordChangeable;
  boolean  PasswordExpires;
  boolean  PasswordRequired;
  string   SID;
  uint8    SIDType;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="eaafd-110">Membres</span><span class="sxs-lookup"><span data-stu-id="eaafd-110">Members</span></span>

<span data-ttu-id="eaafd-111">La classe **Win32 \_ UserAccount** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="eaafd-111">The **Win32\_UserAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="eaafd-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="eaafd-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="eaafd-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eaafd-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="eaafd-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="eaafd-114">Methods</span></span>

<span data-ttu-id="eaafd-115">La classe **Win32 \_ UserAccount** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="eaafd-115">The **Win32\_UserAccount** class has these methods.</span></span>



| <span data-ttu-id="eaafd-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="eaafd-116">Method</span></span>                                                     | <span data-ttu-id="eaafd-117">Description</span><span class="sxs-lookup"><span data-stu-id="eaafd-117">Description</span></span>                                             |
|:-----------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="eaafd-118">**Renommer**</span><span class="sxs-lookup"><span data-stu-id="eaafd-118">**Rename**</span></span>](rename-method-in-class-win32-useraccount.md) | <span data-ttu-id="eaafd-119">Autorise l’attribution d’un nouveau nom au compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eaafd-119">Allows for the renaming of the user account.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="eaafd-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="eaafd-120">Properties</span></span>

<span data-ttu-id="eaafd-121">La classe **Win32 \_ UserAccount** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="eaafd-121">The **Win32\_UserAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eaafd-122">**AccountType**</span><span class="sxs-lookup"><span data-stu-id="eaafd-122">**AccountType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaafd-123">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eaafd-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaafd-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-125">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ info User info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| usri2 \_ Flags »)</span><span class="sxs-lookup"><span data-stu-id="eaafd-125">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|usri2\_flags")</span></span>
</dt> </dl>

<span data-ttu-id="eaafd-126">Indicateurs qui décrivent les caractéristiques d’un compte d’utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="eaafd-126">Flags that describe the characteristics of a Windows user account.</span></span>

<dt>

<span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>

<span data-ttu-id="eaafd-127"><span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>**Compte dupliqué temporaire** (256)</span><span class="sxs-lookup"><span data-stu-id="eaafd-127"><span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>**Temporary duplicate account** (256)</span></span>


</dt> <dd>

<span data-ttu-id="eaafd-128">**\_ \_ compte DUPLIQUÉ temporaire \_ uf**</span><span class="sxs-lookup"><span data-stu-id="eaafd-128">**UF\_TEMP\_DUPLICATE\_ACCOUNT**</span></span>

<span data-ttu-id="eaafd-129">Compte d’utilisateur local pour les utilisateurs qui ont un compte principal dans un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="eaafd-129">Local user account for users who have a primary account in another domain.</span></span> <span data-ttu-id="eaafd-130">Ce compte fournit un accès utilisateur à ce domaine uniquement, et non à un domaine qui approuve ce domaine.</span><span class="sxs-lookup"><span data-stu-id="eaafd-130">This account provides user access to this domain only—not to any domain that trusts this domain.</span></span>

</dd> <dt>

<span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

<span data-ttu-id="eaafd-131"><span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>**Compte normal** (512)</span><span class="sxs-lookup"><span data-stu-id="eaafd-131"><span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>**Normal account** (512)</span></span>


</dt> <dd>

<span data-ttu-id="eaafd-132">**\_compte standard \_ uf**</span><span class="sxs-lookup"><span data-stu-id="eaafd-132">**UF\_NORMAL\_ACCOUNT**</span></span>

<span data-ttu-id="eaafd-133">Type de compte par défaut qui représente un utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="eaafd-133">Default account type that represents a typical user.</span></span>

</dd> <dt>

<span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

<span data-ttu-id="eaafd-134"><span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>**Compte de confiance interdomaine** (2048)</span><span class="sxs-lookup"><span data-stu-id="eaafd-134"><span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>**Interdomain trust account** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="eaafd-135">**\_compte de confiance interdomaine UF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eaafd-135">**UF\_INTERDOMAIN\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="eaafd-136">Compte d’un domaine système qui approuve d’autres domaines.</span><span class="sxs-lookup"><span data-stu-id="eaafd-136">Account for a system domain that trusts other domains.</span></span>

</dd> <dt>

<span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

<span data-ttu-id="eaafd-137"><span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>**Compte de confiance de station de travail** (4096)</span><span class="sxs-lookup"><span data-stu-id="eaafd-137"><span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>**Workstation trust account** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="eaafd-138">**compte d’approbation de station de \_ travail UF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eaafd-138">**UF\_WORKSTATION\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="eaafd-139">Compte d’ordinateur pour un système d’ordinateur exécutant Windows qui est membre de ce domaine.</span><span class="sxs-lookup"><span data-stu-id="eaafd-139">Computer account for a computer system running Windows that is a member of this domain.</span></span>

</dd> <dt>

<span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

<span data-ttu-id="eaafd-140"><span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>**Compte de confiance du serveur** (8192)</span><span class="sxs-lookup"><span data-stu-id="eaafd-140"><span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>**Server trust account** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="eaafd-141">**\_compte de \_ confiance du serveur uf \_**</span><span class="sxs-lookup"><span data-stu-id="eaafd-141">**UF\_SERVER\_TRUST\_ACCOUNT**</span></span>

<span data-ttu-id="eaafd-142">Compte d’un contrôleur de domaine de sauvegarde du système qui est membre de ce domaine.</span><span class="sxs-lookup"><span data-stu-id="eaafd-142">Account for a system backup domain controller that is a member of this domain.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eaafd-143">**Caption**</span><span class="sxs-lookup"><span data-stu-id="eaafd-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaafd-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaafd-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaafd-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-146">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="eaafd-146">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="eaafd-147">Domaine et nom d’utilisateur du compte.</span><span class="sxs-lookup"><span data-stu-id="eaafd-147">Domain and username of the account.</span></span>

<span data-ttu-id="eaafd-148">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="eaafd-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eaafd-149">**Description**</span><span class="sxs-lookup"><span data-stu-id="eaafd-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaafd-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaafd-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaafd-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-152">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="eaafd-152">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="eaafd-153">Description du compte.</span><span class="sxs-lookup"><span data-stu-id="eaafd-153">Description of the account.</span></span>

<span data-ttu-id="eaafd-154">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="eaafd-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eaafd-155">**Désactivé**</span><span class="sxs-lookup"><span data-stu-id="eaafd-155">**Disabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaafd-156">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="eaafd-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="eaafd-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-158">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| \_ info utilisateur \| UF \_ ACCOUNTDISABLE »)</span><span class="sxs-lookup"><span data-stu-id="eaafd-158">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|USER\_INFO\|UF\_ACCOUNTDISABLE")</span></span>
</dt> </dl>

<span data-ttu-id="eaafd-159">Le compte d’utilisateur Windows est désactivé.</span><span class="sxs-lookup"><span data-stu-id="eaafd-159">Windows user account is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="eaafd-160">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="eaafd-160">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaafd-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaafd-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaafd-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-163">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APId \| Network Management Functions \| nom_domaine")</span><span class="sxs-lookup"><span data-stu-id="eaafd-163">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="eaafd-164">Nom du domaine Windows auquel appartient un compte d’utilisateur, par exemple : « NA-SALES ».</span><span class="sxs-lookup"><span data-stu-id="eaafd-164">Name of the Windows domain to which a user account belongs, for example: "NA-SALES".</span></span>

</dd> <dt>

<span data-ttu-id="eaafd-165">**FullName**</span><span class="sxs-lookup"><span data-stu-id="eaafd-165">**FullName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaafd-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaafd-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-167">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="eaafd-167">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-168">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **usri2 \_ Full \_ Name**»)</span><span class="sxs-lookup"><span data-stu-id="eaafd-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**usri2\_full\_name**")</span></span>
</dt> </dl>

<span data-ttu-id="eaafd-169">Nom complet d’un utilisateur local, par exemple : « Dan Wilson ».</span><span class="sxs-lookup"><span data-stu-id="eaafd-169">Full name of a local user, for example: "Dan Wilson".</span></span>

</dd> <dt>

<span data-ttu-id="eaafd-170">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="eaafd-170">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaafd-171">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="eaafd-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaafd-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-173">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="eaafd-173">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="eaafd-174">Date d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="eaafd-174">Date the object is installed.</span></span> <span data-ttu-id="eaafd-175">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="eaafd-175">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="eaafd-176">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="eaafd-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eaafd-177">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="eaafd-177">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaafd-178">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="eaafd-178">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaafd-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-180">Qualificateurs : [ **fixe**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="eaafd-180">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="eaafd-181">Si la **valeur est true**, le compte est défini sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="eaafd-181">If **true**, the account is defined on the local computer.</span></span>

<span data-ttu-id="eaafd-182">Cette propriété est héritée [**du \_ compte Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="eaafd-182">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="eaafd-183">**Verrouillage.**</span><span class="sxs-lookup"><span data-stu-id="eaafd-183">**Lockout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaafd-184">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="eaafd-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-185">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="eaafd-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-186">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ lockout**»)</span><span class="sxs-lookup"><span data-stu-id="eaafd-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_LOCKOUT**")</span></span>
</dt> </dl>

<span data-ttu-id="eaafd-187">Si la **valeur est true**, le compte d’utilisateur est verrouillé sur le système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="eaafd-187">If **true**, the user account is locked out of the Windows operating system.</span></span>

</dd> <dt>

<span data-ttu-id="eaafd-188">**Nom**</span><span class="sxs-lookup"><span data-stu-id="eaafd-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaafd-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaafd-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaafd-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-191">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management structures \| Name")</span><span class="sxs-lookup"><span data-stu-id="eaafd-191">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="eaafd-192">Nom du compte d’utilisateur Windows sur le domaine que la propriété de **domaine** de cette classe spécifie.</span><span class="sxs-lookup"><span data-stu-id="eaafd-192">Name of the Windows user account on the domain that the **Domain** property of this class specifies.</span></span>

<span data-ttu-id="eaafd-193">Exemple : « danwilson ».</span><span class="sxs-lookup"><span data-stu-id="eaafd-193">Example: "danwilson".</span></span>

<span data-ttu-id="eaafd-194">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="eaafd-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eaafd-195">**PasswordChangeable**</span><span class="sxs-lookup"><span data-stu-id="eaafd-195">**PasswordChangeable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaafd-196">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="eaafd-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-197">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="eaafd-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-198">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF passwd impossibilité \_ \_ \_ change**»)</span><span class="sxs-lookup"><span data-stu-id="eaafd-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_PASSWD\_CANT\_CHANGE**")</span></span>
</dt> </dl>

<span data-ttu-id="eaafd-199">Si la **valeur est true**, le mot de passe de ce compte d’utilisateur peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="eaafd-199">If **true**, the password on this user account can be changed.</span></span>

</dd> <dt>

<span data-ttu-id="eaafd-200">**PasswordExpires**</span><span class="sxs-lookup"><span data-stu-id="eaafd-200">**PasswordExpires**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaafd-201">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="eaafd-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-202">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="eaafd-202">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-203">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ info utilisateur \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)uf ne pas faire \| **\_ \_ expirer \_ passwd**»)</span><span class="sxs-lookup"><span data-stu-id="eaafd-203">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_DONT\_EXPIRE\_PASSWD**")</span></span>
</dt> </dl>

<span data-ttu-id="eaafd-204">Si la **valeur est true**, le mot de passe de ce compte d’utilisateur expire.</span><span class="sxs-lookup"><span data-stu-id="eaafd-204">If **true**, the password on this user account expires.</span></span>

</dd> <dt>

<span data-ttu-id="eaafd-205">**PasswordRequired**</span><span class="sxs-lookup"><span data-stu-id="eaafd-205">**PasswordRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaafd-206">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="eaafd-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-207">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="eaafd-207">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-208">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Network Management structures \| [**\_ Information User info \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **UF \_ passwd passwd \_ NOTREQD**»)</span><span class="sxs-lookup"><span data-stu-id="eaafd-208">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USER\_INFO\_2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)\|**UF\_PASSWD\_NOTREQD**")</span></span>
</dt> </dl>

<span data-ttu-id="eaafd-209">Si la **valeur est true**, un mot de passe est requis sur un compte d’utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="eaafd-209">If **true**, a password is required on a Windows user account.</span></span> <span data-ttu-id="eaafd-210">Si la **valeur est false**, ce compte ne requiert pas de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="eaafd-210">If **false**, this account does not require a password.</span></span>

</dd> <dt>

<span data-ttu-id="eaafd-211">**SID**</span><span class="sxs-lookup"><span data-stu-id="eaafd-211">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaafd-212">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaafd-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaafd-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-214">Qualificateurs : [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| identificateurs de sécurité (SID)")</span><span class="sxs-lookup"><span data-stu-id="eaafd-214">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="eaafd-215">Identificateur de sécurité (SID) pour ce compte.</span><span class="sxs-lookup"><span data-stu-id="eaafd-215">Security identifier (SID) for this account.</span></span> <span data-ttu-id="eaafd-216">Un SID est une valeur de chaîne de longueur variable qui est utilisée pour identifier un tiers de confiance.</span><span class="sxs-lookup"><span data-stu-id="eaafd-216">A SID is a string value of variable length that is used to identify a trustee.</span></span> <span data-ttu-id="eaafd-217">Chaque compte possède un SID unique qu’une autorité, comme un domaine Windows, émet.</span><span class="sxs-lookup"><span data-stu-id="eaafd-217">Each account has a unique SID that an authority, such as a Windows domain, issues.</span></span> <span data-ttu-id="eaafd-218">Le SID est stocké dans la base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="eaafd-218">The SID is stored in the security database.</span></span> <span data-ttu-id="eaafd-219">Lorsqu’un utilisateur ouvre une session, le système récupère le SID de l’utilisateur à partir de la base de données, place le SID dans le jeton d’accès utilisateur, puis utilise le SID dans le jeton d’accès utilisateur pour identifier l’utilisateur dans toutes les interactions suivantes avec la sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="eaafd-219">When a user logs on, the system retrieves the user SID from the database, places the SID in the user access token, and then uses the SID in the user access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="eaafd-220">Chaque SID est un identificateur unique pour un utilisateur ou un groupe, et un autre utilisateur ou groupe ne peut pas avoir le même SID.</span><span class="sxs-lookup"><span data-stu-id="eaafd-220">Each SID is a unique identifier for a user or group, and a different user or group cannot have the same SID.</span></span>

<span data-ttu-id="eaafd-221">Cette propriété est héritée [**du \_ compte Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="eaafd-221">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="eaafd-222">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="eaafd-222">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaafd-223">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="eaafd-223">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaafd-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-225">Qualificateurs : [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Access Control types énumération types \| [**sid \_ \_ use**](/windows/win32/api/winnt/ne-winnt-sid_name_use)")</span><span class="sxs-lookup"><span data-stu-id="eaafd-225">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Access Control Enumeration Types\|[**SID\_NAME\_USE**](/windows/win32/api/winnt/ne-winnt-sid_name_use)")</span></span>
</dt> </dl>

<span data-ttu-id="eaafd-226">Valeur énumérée qui spécifie le type de SID.</span><span class="sxs-lookup"><span data-stu-id="eaafd-226">Enumerated value that specifies the type of SID.</span></span>

<span data-ttu-id="eaafd-227">Cette propriété est héritée [**du \_ compte Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="eaafd-227">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="eaafd-228">**SidTypeUser** (1)</span><span class="sxs-lookup"><span data-stu-id="eaafd-228">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="eaafd-229">**SidTypeGroup** (2)</span><span class="sxs-lookup"><span data-stu-id="eaafd-229">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="eaafd-230">**SidTypeDomain** (3)</span><span class="sxs-lookup"><span data-stu-id="eaafd-230">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="eaafd-231">**SidTypeAlias** (4)</span><span class="sxs-lookup"><span data-stu-id="eaafd-231">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="eaafd-232">**SidTypeWellKnownGroup** (5)</span><span class="sxs-lookup"><span data-stu-id="eaafd-232">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="eaafd-233">**SidTypeDeletedAccount** (6)</span><span class="sxs-lookup"><span data-stu-id="eaafd-233">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="eaafd-234">**SidTypeInvalid** (7)</span><span class="sxs-lookup"><span data-stu-id="eaafd-234">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="eaafd-235">**SidTypeUnknown** (8)</span><span class="sxs-lookup"><span data-stu-id="eaafd-235">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="eaafd-236">**SidTypeComputer** (9)</span><span class="sxs-lookup"><span data-stu-id="eaafd-236">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eaafd-237">**État**</span><span class="sxs-lookup"><span data-stu-id="eaafd-237">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eaafd-238">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eaafd-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-239">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="eaafd-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eaafd-240">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="eaafd-240">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="eaafd-241">État actuel d’un objet.</span><span class="sxs-lookup"><span data-stu-id="eaafd-241">Current status of an object.</span></span> <span data-ttu-id="eaafd-242">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="eaafd-242">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="eaafd-243">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prédit », qui est un élément tel qu’un lecteur de disque dur intelligent qui peut fonctionner correctement, mais prédit une défaillance dans un avenir proche.</span><span class="sxs-lookup"><span data-stu-id="eaafd-243">Operational statuses include: "OK", "Degraded", and "Pred Fail", which is an element such as a SMART-enabled hard disk drive that may be functioning properly, but predicts a failure in the near future.</span></span> <span data-ttu-id="eaafd-244">Les États non opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service », qui peuvent s’appliquer pendant la réargentation miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="eaafd-244">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service", which can apply during mirror resilvering of a disk, reloading a user permissions list, or other administrative work.</span></span>

<span data-ttu-id="eaafd-245">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="eaafd-245">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="eaafd-246">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="eaafd-246">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="eaafd-247">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="eaafd-247">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="eaafd-248">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="eaafd-248">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="eaafd-249">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="eaafd-249">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eaafd-250">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="eaafd-250">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="eaafd-251">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="eaafd-251">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="eaafd-252">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="eaafd-252">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="eaafd-253">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="eaafd-253">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="eaafd-254">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="eaafd-254">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="eaafd-255">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="eaafd-255">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="eaafd-256">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="eaafd-256">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="eaafd-257">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="eaafd-257">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="eaafd-258">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="eaafd-258">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="eaafd-259"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="eaafd-259"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="eaafd-260">Notes</span><span class="sxs-lookup"><span data-stu-id="eaafd-260">Remarks</span></span>

<span data-ttu-id="eaafd-261">La classe **Win32 \_ UserAccount** est dérivée [**du \_ compte Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="eaafd-261">The **Win32\_UserAccount** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

> [!Note]  
> <span data-ttu-id="eaafd-262">Une erreur n’est pas retournée pour une tentative d’écriture dans une propriété en lecture seule, et la valeur de la propriété reste inchangée.</span><span class="sxs-lookup"><span data-stu-id="eaafd-262">An error is not returned for an attempt to write to a read-only property, and the value of the property remains unchanged.</span></span>

 

## <a name="examples"></a><span data-ttu-id="eaafd-263">Exemples</span><span class="sxs-lookup"><span data-stu-id="eaafd-263">Examples</span></span>

<span data-ttu-id="eaafd-264">L’exemple de code [répertorier les comptes d’utilisateurs locaux à l’aide](https://Gallery.TechNet.Microsoft.Com/827623f5-eb55-4035-8f57-25c4afb444cd) de code WMI VBScript sur la Galerie TechNet utilise **Win32 \_ UserAccount** pour renvoyer des informations sur les comptes d’utilisateurs locaux détectés sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="eaafd-264">The [List Local User Accounts Using WMI](https://Gallery.TechNet.Microsoft.Com/827623f5-eb55-4035-8f57-25c4afb444cd) VBScript code sample on TechNet Gallery uses **Win32\_UserAccount** to Returns information about the local user accounts found on a computer.</span></span>

<span data-ttu-id="eaafd-265">[Traduire le SID en compte d’utilisateur et le compte d’utilisateur en sid](https://Gallery.TechNet.Microsoft.Com/f1c83aed-fe60-48d5-90ab-22388fcbd54f) L’exemple de code PowerShell sur la Galerie TechNet utilise **Win32 \_ UserAccount** pour convertir un SID en compte d’utilisateur et/ou un compte d’utilisateur en sid.</span><span class="sxs-lookup"><span data-stu-id="eaafd-265">[The Translate SID to User Account and User Account to SID](https://Gallery.TechNet.Microsoft.Com/f1c83aed-fe60-48d5-90ab-22388fcbd54f) PowerShell code sample on TechNet Gallery uses **Win32\_UserAccount** to translate a SID to User Account and/or a User Account to SID.</span></span>

<span data-ttu-id="eaafd-266">L’exemple de code VBScript suivant vous montre comment obtenir le nom complet d’un utilisateur sur un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="eaafd-266">The following VBScript code example shows you how to get the full name of a user on a local computer.</span></span> <span data-ttu-id="eaafd-267">Le nom complet est le nom de la langue humaine. par exemple, une personne peut avoir le nom d’utilisateur « kensanchez » et le nom complet peut être « Ken Sanchez ». vous devez donc remplacer le nom de domaine réel et le nom d’utilisateur par « MyDomainName » et « MyUserName ».</span><span class="sxs-lookup"><span data-stu-id="eaafd-267">The full name is the human language name, for example, a person may have the user name of "kensanchez" and the full name may be "Ken Sanchez", so you substitute the real domain name and user name for "MyDomainName" and "MyUserName".</span></span> <span data-ttu-id="eaafd-268">Pour une requête efficace, vous devez spécifier les propriétés Domain et User Name.</span><span class="sxs-lookup"><span data-stu-id="eaafd-268">For an efficient query, you must specify both the domain and user name properties.</span></span>

<span data-ttu-id="eaafd-269">Si vous êtes un administrateur sur un ordinateur distant, vous pouvez attribuer le nom de l’ordinateur distant pour strComputer (au lieu de « . »), puis utiliser le type de script suivant pour obtenir le nom complet d’un compte d’utilisateur sur un ordinateur local, à partir d’un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="eaafd-269">If you are an administrator on a remote computer, you can assign the name of the remote computer for strComputer (instead of "."), and then use the following type of script to get the full name of a user account on a local computer—from a remote computer.</span></span>


```VB
On Error Resume Next
strComputer = "."

Set objUserAccount = GetObject("winmgmts{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2:Win32_UserAccount.Domain='MyDomainName',Name='MyUserName' ")

If Err = 0 Then
    WScript.Echo objUserAccount.FullName
Else
    WScript.Echo "No object found" & Err.Number
End If
```




```CSharp
using System.Management;

{
     ManagementScope mgmtScope = new ManagementScope("\\\\.\\Root\\CIMv2");
     ObjectQuery oQuery = new ObjectQuery("SELECT * FROM Win32_UserAccount Where Name=\"myUserName\"");
     ManagementObjectSearcher mgmtSearch = new ManagementObjectSearcher(mgmtScope, oQuery);
     ManagementObjectCollection objCollection = mgmtSearch.Get();
     foreach (ManagementObject mgmtObject in objCollection)
     {
          Console.WriteLine("Full Name : {0}", mgmtObject["FullName"]);
     }
}
```



## <a name="requirements"></a><span data-ttu-id="eaafd-270">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eaafd-270">Requirements</span></span>



| <span data-ttu-id="eaafd-271">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eaafd-271">Requirement</span></span> | <span data-ttu-id="eaafd-272">Valeur</span><span class="sxs-lookup"><span data-stu-id="eaafd-272">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eaafd-273">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eaafd-273">Minimum supported client</span></span><br/> | <span data-ttu-id="eaafd-274">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eaafd-274">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eaafd-275">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eaafd-275">Minimum supported server</span></span><br/> | <span data-ttu-id="eaafd-276">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eaafd-276">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eaafd-277">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="eaafd-277">Namespace</span></span><br/>                | <span data-ttu-id="eaafd-278">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="eaafd-278">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eaafd-279">MOF</span><span class="sxs-lookup"><span data-stu-id="eaafd-279">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eaafd-280"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eaafd-280"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eaafd-281">DLL</span><span class="sxs-lookup"><span data-stu-id="eaafd-281">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaafd-282"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eaafd-282"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaafd-283">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eaafd-283">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaafd-284">**\_Compte Win32**</span><span class="sxs-lookup"><span data-stu-id="eaafd-284">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

[<span data-ttu-id="eaafd-285">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="eaafd-285">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
