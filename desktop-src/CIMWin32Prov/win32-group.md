---
description: Représente des données relatives à un compte de groupe.
ms.assetid: a53d1276-3dc9-419a-bbb8-5dd07794a971
ms.tgt_platform: multiple
title: Classe Win32_Group
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group
- Win32_Group.Caption
- Win32_Group.Description
- Win32_Group.InstallDate
- Win32_Group.Status
- Win32_Group.LocalAccount
- Win32_Group.SID
- Win32_Group.SIDType
- Win32_Group.Domain
- Win32_Group.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a8849ba149e0de570150682d3afbad3a4ee33f36
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111214"
---
# <a name="win32_group-class"></a><span data-ttu-id="3f988-103">\_Classe de groupe Win32</span><span class="sxs-lookup"><span data-stu-id="3f988-103">Win32\_Group class</span></span>

<span data-ttu-id="3f988-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ groupe Win32** représente des données relatives à un compte de groupe.</span><span class="sxs-lookup"><span data-stu-id="3f988-104">The **Win32\_Group** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents data about a group account.</span></span> <span data-ttu-id="3f988-105">Un compte de groupe autorise la modification des privilèges d’accès pour une liste d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="3f988-105">A group account allows access privileges to be changed for a list of users.</span></span> <span data-ttu-id="3f988-106">Exemple : Marketing2.</span><span class="sxs-lookup"><span data-stu-id="3f988-106">Example: Marketing2.</span></span>

<span data-ttu-id="3f988-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3f988-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3f988-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="3f988-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f988-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f988-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Group : Win32_Account
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

## <a name="members"></a><span data-ttu-id="3f988-110">Membres</span><span class="sxs-lookup"><span data-stu-id="3f988-110">Members</span></span>

<span data-ttu-id="3f988-111">La classe de **\_ groupe Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3f988-111">The **Win32\_Group** class has these types of members:</span></span>

-   [<span data-ttu-id="3f988-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3f988-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="3f988-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3f988-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3f988-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3f988-114">Methods</span></span>

<span data-ttu-id="3f988-115">La classe de **\_ groupe Win32** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="3f988-115">The **Win32\_Group** class has these methods.</span></span>



| <span data-ttu-id="3f988-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="3f988-116">Method</span></span>                                               | <span data-ttu-id="3f988-117">Description</span><span class="sxs-lookup"><span data-stu-id="3f988-117">Description</span></span>                        |
|:-----------------------------------------------------|:-----------------------------------|
| [<span data-ttu-id="3f988-118">**Renommer**</span><span class="sxs-lookup"><span data-stu-id="3f988-118">**Rename**</span></span>](rename-method-in-class-win32-group.md) | <span data-ttu-id="3f988-119">Modifie le nom du groupe.</span><span class="sxs-lookup"><span data-stu-id="3f988-119">Changes the group name.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3f988-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3f988-120">Properties</span></span>

<span data-ttu-id="3f988-121">La classe de **\_ groupe Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3f988-121">The **Win32\_Group** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3f988-122">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3f988-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f988-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3f988-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f988-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f988-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f988-125">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="3f988-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3f988-126">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3f988-126">A short textual description of the object.</span></span>

<span data-ttu-id="3f988-127">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3f988-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3f988-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="3f988-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f988-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3f988-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f988-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f988-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f988-131">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="3f988-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3f988-132">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3f988-132">A textual description of the object.</span></span>

<span data-ttu-id="3f988-133">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3f988-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3f988-134">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="3f988-134">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f988-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3f988-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f988-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f988-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f988-137">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Domain"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APId \| Network Management Functions \| nom_domaine")</span><span class="sxs-lookup"><span data-stu-id="3f988-137">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Domain"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Functions\|domainname")</span></span>
</dt> </dl>

<span data-ttu-id="3f988-138">Nom du domaine Windows auquel appartient le compte de groupe.</span><span class="sxs-lookup"><span data-stu-id="3f988-138">Name of the Windows domain to which the group account belongs.</span></span>

<span data-ttu-id="3f988-139">Exemple : « NA-SALES »</span><span class="sxs-lookup"><span data-stu-id="3f988-139">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="3f988-140">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3f988-140">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f988-141">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3f988-141">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3f988-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f988-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f988-143">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="3f988-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3f988-144">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="3f988-144">Indicates when the object was installed.</span></span> <span data-ttu-id="3f988-145">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="3f988-145">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="3f988-146">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3f988-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3f988-147">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="3f988-147">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f988-148">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="3f988-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3f988-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f988-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f988-150">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3f988-150">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3f988-151">Si la **valeur est true**, le compte est défini sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="3f988-151">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="3f988-152">Pour récupérer uniquement les comptes définis sur l’ordinateur local, créez une requête qui comprend la condition « LocalAccount =**true**».</span><span class="sxs-lookup"><span data-stu-id="3f988-152">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

<span data-ttu-id="3f988-153">Cette propriété est héritée [**du \_ compte Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="3f988-153">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="3f988-154">**Nom**</span><span class="sxs-lookup"><span data-stu-id="3f988-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f988-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3f988-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f988-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f988-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f988-157">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Network Management structures \| Name")</span><span class="sxs-lookup"><span data-stu-id="3f988-157">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="3f988-158">Nom du compte de groupe Windows sur le domaine spécifié par la propriété de **domaine** de cette classe.</span><span class="sxs-lookup"><span data-stu-id="3f988-158">Name of the Windows group account on the domain specified by the **Domain** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="3f988-159">**SID**</span><span class="sxs-lookup"><span data-stu-id="3f988-159">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f988-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3f988-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f988-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f988-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f988-162">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api, \| identificateurs de sécurité (SID)")</span><span class="sxs-lookup"><span data-stu-id="3f988-162">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="3f988-163">Identificateur de sécurité (SID) pour ce compte.</span><span class="sxs-lookup"><span data-stu-id="3f988-163">Security identifier (SID) for this account.</span></span> <span data-ttu-id="3f988-164">Un SID est une valeur de chaîne de longueur variable utilisée pour identifier un tiers de confiance.</span><span class="sxs-lookup"><span data-stu-id="3f988-164">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="3f988-165">Chaque compte possède un SID unique émis par une autorité (par exemple, un domaine Windows), stocké dans une base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3f988-165">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="3f988-166">Lorsqu’un utilisateur ouvre une session, le système récupère le SID de l’utilisateur à partir de la base de données et le place dans le jeton d’accès de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3f988-166">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="3f988-167">Le système utilise le SID dans le jeton d’accès de l’utilisateur pour identifier l’utilisateur dans toutes les interactions suivantes avec la sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="3f988-167">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="3f988-168">Lorsqu’un SID a été utilisé en tant qu’identificateur unique pour un utilisateur ou un groupe, il ne peut pas être réutilisé pour identifier un autre utilisateur ou groupe.</span><span class="sxs-lookup"><span data-stu-id="3f988-168">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

<span data-ttu-id="3f988-169">Cette propriété est héritée [**du \_ compte Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="3f988-169">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

</dd> <dt>

<span data-ttu-id="3f988-170">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="3f988-170">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f988-171">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="3f988-171">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="3f988-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f988-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f988-173">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Access Control types énumération types \| sid \_ \_ use")</span><span class="sxs-lookup"><span data-stu-id="3f988-173">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="3f988-174">Valeurs énumérées qui spécifient le type d’identificateur de sécurité (SID).</span><span class="sxs-lookup"><span data-stu-id="3f988-174">Enumerated values that specify the type of security identifier (SID).</span></span>

<span data-ttu-id="3f988-175">Cette propriété est héritée [**du \_ compte Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="3f988-175">This property is inherited from [**Win32\_Account**](win32-account.md).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="3f988-176">**SidTypeUser** (1)</span><span class="sxs-lookup"><span data-stu-id="3f988-176">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="3f988-177">**SidTypeGroup** (2)</span><span class="sxs-lookup"><span data-stu-id="3f988-177">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="3f988-178">**SidTypeDomain** (3)</span><span class="sxs-lookup"><span data-stu-id="3f988-178">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="3f988-179">**SidTypeAlias** (4)</span><span class="sxs-lookup"><span data-stu-id="3f988-179">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="3f988-180">**SidTypeWellKnownGroup** (5)</span><span class="sxs-lookup"><span data-stu-id="3f988-180">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="3f988-181">**SidTypeDeletedAccount** (6)</span><span class="sxs-lookup"><span data-stu-id="3f988-181">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="3f988-182">**SidTypeInvalid** (7)</span><span class="sxs-lookup"><span data-stu-id="3f988-182">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="3f988-183">**SidTypeUnknown** (8)</span><span class="sxs-lookup"><span data-stu-id="3f988-183">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="3f988-184">**SidTypeComputer** (9)</span><span class="sxs-lookup"><span data-stu-id="3f988-184">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3f988-185">**État**</span><span class="sxs-lookup"><span data-stu-id="3f988-185">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f988-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3f988-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f988-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3f988-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f988-188">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="3f988-188">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3f988-189">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3f988-189">String that indicates the current status of the object.</span></span> <span data-ttu-id="3f988-190">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="3f988-190">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="3f988-191">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="3f988-191">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="3f988-192">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="3f988-192">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="3f988-193">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="3f988-193">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3f988-194">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="3f988-194">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3f988-195">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="3f988-195">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3f988-196">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3f988-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3f988-197">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3f988-197">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3f988-198">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="3f988-198">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3f988-199">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="3f988-199">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3f988-200">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="3f988-200">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3f988-201">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="3f988-201">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3f988-202">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="3f988-202">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3f988-203">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="3f988-203">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3f988-204">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="3f988-204">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3f988-205">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="3f988-205">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3f988-206">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="3f988-206">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3f988-207">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="3f988-207">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3f988-208">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="3f988-208">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3f988-209">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="3f988-209">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="3f988-210"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3f988-210"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="3f988-211">Notes</span><span class="sxs-lookup"><span data-stu-id="3f988-211">Remarks</span></span>

<span data-ttu-id="3f988-212">La classe de **\_ groupe Win32** est dérivée du [**\_ compte Win32**](win32-account.md).</span><span class="sxs-lookup"><span data-stu-id="3f988-212">The **Win32\_Group** class is derived from [**Win32\_Account**](win32-account.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3f988-213">Exemples</span><span class="sxs-lookup"><span data-stu-id="3f988-213">Examples</span></span>

<span data-ttu-id="3f988-214">Le code suivant, extrait de la [liste des groupes locaux à l’aide](https://Gallery.TechNet.Microsoft.Com/4474e390-776d-428e-906d-20668ce5933f) de l’exemple de code WMI VBScript sur la Galerie TechNet, utilise le **\_ groupe Win32** pour renvoyer des informations sur les groupes locaux détectés sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3f988-214">The following code, taken from the [List Local Groups Using WMI](https://Gallery.TechNet.Microsoft.Com/4474e390-776d-428e-906d-20668ce5933f) VBScript code example on TechNet Gallery, uses **Win32\_Group** to return information about the local groups found on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_Group  Where LocalAccount = True") 
 
For Each objItem in colItems 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Domain: " & objItem.Domain 
    Wscript.Echo "Local Account: " & objItem.LocalAccount 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "SID: " & objItem.SID 
    Wscript.Echo "SID Type: " & objItem.SIDType 
    Wscript.Echo "Status: " & objItem.Status 
    Wscript.Echo 
Next 
```



## <a name="requirements"></a><span data-ttu-id="3f988-215">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f988-215">Requirements</span></span>



| <span data-ttu-id="3f988-216">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f988-216">Requirement</span></span> | <span data-ttu-id="3f988-217">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f988-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f988-218">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f988-218">Minimum supported client</span></span><br/> | <span data-ttu-id="3f988-219">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3f988-219">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3f988-220">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f988-220">Minimum supported server</span></span><br/> | <span data-ttu-id="3f988-221">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f988-221">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3f988-222">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3f988-222">Namespace</span></span><br/>                | <span data-ttu-id="3f988-223">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3f988-223">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3f988-224">MOF</span><span class="sxs-lookup"><span data-stu-id="3f988-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f988-225"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f988-225"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f988-226">DLL</span><span class="sxs-lookup"><span data-stu-id="3f988-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f988-227"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f988-227"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f988-228">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f988-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f988-229">**\_Compte Win32**</span><span class="sxs-lookup"><span data-stu-id="3f988-229">**Win32\_Account**</span></span>](win32-account.md)
</dt> <dt>

<span data-ttu-id="3f988-230">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3f988-230">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

