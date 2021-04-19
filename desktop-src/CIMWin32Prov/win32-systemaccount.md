---
description: Le \_ SystemAccount Win32&\# 8194 ; La classe WMI représente un compte système.
ms.assetid: 0f745d93-cbac-428e-bf27-56f6e97d529f
ms.tgt_platform: multiple
title: Classe Win32_SystemAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemAccount
- Win32_SystemAccount.Caption
- Win32_SystemAccount.Description
- Win32_SystemAccount.InstallDate
- Win32_SystemAccount.Status
- Win32_SystemAccount.LocalAccount
- Win32_SystemAccount.SID
- Win32_SystemAccount.SIDType
- Win32_SystemAccount.Domain
- Win32_SystemAccount.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ef246a0ee372c5755aeb30980095e7f2f6ca1dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513948"
---
# <a name="win32_systemaccount-class"></a><span data-ttu-id="d0e5a-103">\_Classe SystemAccount Win32</span><span class="sxs-lookup"><span data-stu-id="d0e5a-103">Win32\_SystemAccount class</span></span>

<span data-ttu-id="d0e5a-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ SystemAccount** représente un compte système.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-104">The **Win32\_SystemAccount** [WMI class](../wmisdk/retrieving-a-class.md) represents a system account.</span></span> <span data-ttu-id="d0e5a-105">Le compte système est utilisé par le système d’exploitation et les services.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-105">The system account is used by the operating system and services.</span></span> <span data-ttu-id="d0e5a-106">Il existe de nombreux services et processus dans Windows qui ont besoin de la possibilité d’ouvrir une session en interne, par exemple, lors d’une installation de Windows.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-106">There are many services and processes within Windows that need the capability to logon internally, for example, during a Windows installation.</span></span> <span data-ttu-id="d0e5a-107">Le compte système a été conçu à cet effet.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-107">The system account was designed for that purpose.</span></span>

<span data-ttu-id="d0e5a-108">Le compte système est un compte interne qui n’apparaît pas dans le gestionnaire des utilisateurs, ne peut pas être ajouté à des groupes et ne peut pas avoir de droits d’utilisateur attribués.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-108">The system account is an internal account that does not show up in User Manager, cannot be added to any groups, and cannot have user rights assigned to it.</span></span> <span data-ttu-id="d0e5a-109">Toutefois, le compte système n’apparaît pas sur un volume de système de fichiers NTFS dans le gestionnaire de fichiers, qui se trouve dans la section autorisations du menu sécurité.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-109">However, the system account does show up on an NTFS file system volume in file manager, which is located in the Permissions section of the Security menu.</span></span> <span data-ttu-id="d0e5a-110">Par défaut, le compte système dispose du contrôle total sur tous les fichiers sur un volume de système de fichiers NTFS, ce qui signifie que le compte système dispose des mêmes privilèges fonctionnels que le compte administrateur.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-110">By default, the system account is granted full control to all files on an NTFS file system volume, which means that the system account has the same functional privileges as the administrator account.</span></span>

<span data-ttu-id="d0e5a-111">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d0e5a-112">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-112">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0e5a-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0e5a-113">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemAccount : Win32_Account
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  LocalAccount;
  string   SID;
  uint8    SIDType;
  string   Domain;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="d0e5a-114">Membres</span><span class="sxs-lookup"><span data-stu-id="d0e5a-114">Members</span></span>

<span data-ttu-id="d0e5a-115">La classe **Win32 \_ SystemAccount** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d0e5a-115">The **Win32\_SystemAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="d0e5a-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d0e5a-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d0e5a-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d0e5a-117">Properties</span></span>

<span data-ttu-id="d0e5a-118">La classe **Win32 \_ SystemAccount** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-118">The **Win32\_SystemAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d0e5a-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d0e5a-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0e5a-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d0e5a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0e5a-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0e5a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0e5a-122">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-122">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d0e5a-123">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-123">A short textual description of the object.</span></span>

<span data-ttu-id="d0e5a-124">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0e5a-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0e5a-125">**Description**</span><span class="sxs-lookup"><span data-stu-id="d0e5a-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0e5a-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d0e5a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0e5a-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0e5a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0e5a-128">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d0e5a-128">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d0e5a-129">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-129">A textual description of the object.</span></span>

<span data-ttu-id="d0e5a-130">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0e5a-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0e5a-131">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="d0e5a-131">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0e5a-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d0e5a-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0e5a-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0e5a-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0e5a-134">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APId \| Network Management Functions \| nom_domaine")</span><span class="sxs-lookup"><span data-stu-id="d0e5a-134">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="d0e5a-135">Nom du domaine Windows auquel appartient le compte système.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-135">Name of the Windows domain to which the system account belongs.</span></span>

<span data-ttu-id="d0e5a-136">Exemple : « NA-SALES »</span><span class="sxs-lookup"><span data-stu-id="d0e5a-136">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="d0e5a-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d0e5a-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0e5a-138">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d0e5a-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d0e5a-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0e5a-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0e5a-140">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="d0e5a-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d0e5a-141">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-141">Indicates when the object was installed.</span></span> <span data-ttu-id="d0e5a-142">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d0e5a-143">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0e5a-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0e5a-144">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="d0e5a-144">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0e5a-145">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d0e5a-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0e5a-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0e5a-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0e5a-147">Qualificateurs : [ **fixe**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-147">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="d0e5a-148">Si la **valeur est true**, le compte est défini sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-148">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="d0e5a-149">Pour récupérer uniquement les comptes définis sur l’ordinateur local, créez une requête qui comprend la condition « LocalAccount =**true**».</span><span class="sxs-lookup"><span data-stu-id="d0e5a-149">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

<span data-ttu-id="d0e5a-150">Cette propriété est héritée [**du \_ compte Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="d0e5a-150">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0e5a-151">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d0e5a-151">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0e5a-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d0e5a-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0e5a-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0e5a-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0e5a-154">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management structures \| Name")</span><span class="sxs-lookup"><span data-stu-id="d0e5a-154">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="d0e5a-155">Nom du compte système Windows sur le domaine spécifié par la propriété de **domaine** de cette classe.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-155">Name of the Windows system account on the domain specified by the **Domain** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="d0e5a-156">**SID**</span><span class="sxs-lookup"><span data-stu-id="d0e5a-156">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0e5a-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d0e5a-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0e5a-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0e5a-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0e5a-159">Qualificateurs : [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api, \| identificateurs de sécurité (SID)")</span><span class="sxs-lookup"><span data-stu-id="d0e5a-159">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="d0e5a-160">Identificateur de sécurité (SID) pour ce compte.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-160">Security identifier (SID) for this account.</span></span> <span data-ttu-id="d0e5a-161">Un SID est une valeur de chaîne de longueur variable utilisée pour identifier un tiers de confiance.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-161">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="d0e5a-162">Chaque compte possède un SID unique émis par une autorité (par exemple, un domaine Windows), stocké dans une base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-162">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="d0e5a-163">Lorsqu’un utilisateur ouvre une session, le système récupère le SID de l’utilisateur à partir de la base de données et le place dans le jeton d’accès de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-163">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="d0e5a-164">Le système utilise le SID dans le jeton d’accès de l’utilisateur pour identifier l’utilisateur dans toutes les interactions suivantes avec la sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-164">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="d0e5a-165">Lorsqu’un SID a été utilisé en tant qu’identificateur unique pour un utilisateur ou un groupe, il ne peut pas être réutilisé pour identifier un autre utilisateur ou groupe.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-165">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

<span data-ttu-id="d0e5a-166">Cette propriété est héritée [**du \_ compte Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="d0e5a-166">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0e5a-167">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="d0e5a-167">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0e5a-168">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="d0e5a-168">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d0e5a-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0e5a-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0e5a-170">Qualificateurs : [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Access Control types énumération types \| sid \_ \_ use")</span><span class="sxs-lookup"><span data-stu-id="d0e5a-170">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="d0e5a-171">Valeurs énumérées qui spécifient le type d’identificateur de sécurité (SID).</span><span class="sxs-lookup"><span data-stu-id="d0e5a-171">Enumerated values that specify the type of security identifier (SID).</span></span>

<span data-ttu-id="d0e5a-172">Cette propriété est héritée [**du \_ compte Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="d0e5a-172">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="d0e5a-173">**SidTypeUser** (1)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-173">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="d0e5a-174">**SidTypeGroup** (2)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-174">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="d0e5a-175">**SidTypeDomain** (3)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-175">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="d0e5a-176">**SidTypeAlias** (4)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-176">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="d0e5a-177">**SidTypeWellKnownGroup** (5)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-177">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="d0e5a-178">**SidTypeDeletedAccount** (6)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-178">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="d0e5a-179">**SidTypeInvalid** (7)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-179">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="d0e5a-180">**SidTypeUnknown** (8)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-180">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="d0e5a-181">**SidTypeComputer** (9)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-181">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d0e5a-182">**État**</span><span class="sxs-lookup"><span data-stu-id="d0e5a-182">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0e5a-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d0e5a-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0e5a-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d0e5a-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0e5a-185">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="d0e5a-185">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d0e5a-186">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-186">String that indicates the current status of the object.</span></span> <span data-ttu-id="d0e5a-187">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-187">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d0e5a-188">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="d0e5a-188">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d0e5a-189">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="d0e5a-189">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d0e5a-190">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="d0e5a-190">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d0e5a-191">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-191">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d0e5a-192">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="d0e5a-192">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d0e5a-193">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0e5a-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d0e5a-194">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d0e5a-194">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d0e5a-195">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-195">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d0e5a-196">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-196">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d0e5a-197">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-197">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d0e5a-198">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="d0e5a-198">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d0e5a-199">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-199">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d0e5a-200">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-200">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d0e5a-201">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-201">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d0e5a-202">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-202">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d0e5a-203">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-203">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d0e5a-204">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-204">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d0e5a-205">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-205">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d0e5a-206">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="d0e5a-206">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="d0e5a-207"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d0e5a-207"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="d0e5a-208">Notes</span><span class="sxs-lookup"><span data-stu-id="d0e5a-208">Remarks</span></span>

<span data-ttu-id="d0e5a-209">La classe **Win32 \_ SystemAccount** est dérivée [**du \_ compte Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="d0e5a-209">The **Win32\_SystemAccount** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0e5a-210">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0e5a-210">Requirements</span></span>



| <span data-ttu-id="d0e5a-211">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0e5a-211">Requirement</span></span> | <span data-ttu-id="d0e5a-212">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0e5a-212">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0e5a-213">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0e5a-213">Minimum supported client</span></span><br/> | <span data-ttu-id="d0e5a-214">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0e5a-214">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d0e5a-215">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0e5a-215">Minimum supported server</span></span><br/> | <span data-ttu-id="d0e5a-216">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0e5a-216">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d0e5a-217">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d0e5a-217">Namespace</span></span><br/>                | <span data-ttu-id="d0e5a-218">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d0e5a-218">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d0e5a-219">MOF</span><span class="sxs-lookup"><span data-stu-id="d0e5a-219">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0e5a-220"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0e5a-220"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0e5a-221">DLL</span><span class="sxs-lookup"><span data-stu-id="d0e5a-221">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0e5a-222"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0e5a-222"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0e5a-223">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0e5a-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0e5a-224">**\_Compte Win32**</span><span class="sxs-lookup"><span data-stu-id="d0e5a-224">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

[<span data-ttu-id="d0e5a-225">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="d0e5a-225">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
