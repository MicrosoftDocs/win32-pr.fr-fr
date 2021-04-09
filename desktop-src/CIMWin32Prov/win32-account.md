---
description: Contient des informations sur les comptes d’utilisateur et les comptes de groupe connus du système informatique exécutant Windows.
ms.assetid: c0916f20-05be-4282-9642-28cec606bfd7
ms.tgt_platform: multiple
title: Classe Win32_Account
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Account
- Win32_Account.Caption
- Win32_Account.Description
- Win32_Account.Domain
- Win32_Account.InstallDate
- Win32_Account.LocalAccount
- Win32_Account.Name
- Win32_Account.SID
- Win32_Account.SIDType
- Win32_Account.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2af601799095192d7af4ffedce0c8e0cd28bff21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111378"
---
# <a name="win32_account-class"></a><span data-ttu-id="259cc-103">\_Classe de compte Win32</span><span class="sxs-lookup"><span data-stu-id="259cc-103">Win32\_Account class</span></span>

<span data-ttu-id="259cc-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) du **\_ compte Win32** contient des informations sur les comptes d’utilisateurs et les comptes de groupe connus du système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="259cc-104">The **Win32\_Account** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) contains information about user accounts and group accounts known to the computer system running Windows.</span></span> <span data-ttu-id="259cc-105">Les noms d’utilisateurs ou de groupes reconnus par un domaine Windows sont des descendants (ou membres) de cette classe.</span><span class="sxs-lookup"><span data-stu-id="259cc-105">User or group names recognized by a Windows domain are descendants (or members) of this class.</span></span>

<span data-ttu-id="259cc-106">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="259cc-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="259cc-107">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="259cc-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="259cc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="259cc-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4C9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Account : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  string   Domain;
  datetime InstallDate;
  boolean  LocalAccount;
  string   Name;
  string   SID;
  uint8    SIDType;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="259cc-109">Membres</span><span class="sxs-lookup"><span data-stu-id="259cc-109">Members</span></span>

<span data-ttu-id="259cc-110">La classe de **\_ compte Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="259cc-110">The **Win32\_Account** class has these types of members:</span></span>

-   [<span data-ttu-id="259cc-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="259cc-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="259cc-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="259cc-112">Properties</span></span>

<span data-ttu-id="259cc-113">La classe de **\_ compte Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="259cc-113">The **Win32\_Account** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="259cc-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="259cc-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="259cc-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="259cc-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="259cc-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="259cc-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="259cc-117">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="259cc-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="259cc-118">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="259cc-118">Short description of the object.</span></span>

<span data-ttu-id="259cc-119">Cette propriété est héritée de la classe [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="259cc-119">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="259cc-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="259cc-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="259cc-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="259cc-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="259cc-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="259cc-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="259cc-123">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="259cc-123">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="259cc-124">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="259cc-124">Description of the object.</span></span>

<span data-ttu-id="259cc-125">Cette propriété est héritée de la classe [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="259cc-125">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="259cc-126">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="259cc-126">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="259cc-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="259cc-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="259cc-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="259cc-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="259cc-129">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| Network Management Functions \| Domain »)</span><span class="sxs-lookup"><span data-stu-id="259cc-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Functions\|Domain")</span></span>
</dt> </dl>

<span data-ttu-id="259cc-130">Nom du domaine Windows auquel appartient un groupe ou un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="259cc-130">Name of the Windows domain to which a group or user belongs.</span></span>

<span data-ttu-id="259cc-131">Exemple : « NA-SALES »</span><span class="sxs-lookup"><span data-stu-id="259cc-131">Example: "NA-SALES"</span></span>

</dd> <dt>

<span data-ttu-id="259cc-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="259cc-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="259cc-133">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="259cc-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="259cc-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="259cc-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="259cc-135">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="259cc-135">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="259cc-136">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="259cc-136">Date and time that the object was installed.</span></span> <span data-ttu-id="259cc-137">Cette propriété ne requiert pas de valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="259cc-137">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="259cc-138">Cette propriété est héritée de la classe [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="259cc-138">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="259cc-139">**LocalAccount**</span><span class="sxs-lookup"><span data-stu-id="259cc-139">**LocalAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="259cc-140">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="259cc-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="259cc-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="259cc-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="259cc-142">Qualificateurs : [ **fixe**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="259cc-142">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="259cc-143">Si la **valeur est true**, le compte est défini sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="259cc-143">If **TRUE**, the account is defined on the local machine.</span></span> <span data-ttu-id="259cc-144">Pour récupérer uniquement les comptes définis sur l’ordinateur local, créez une requête qui comprend la condition « LocalAccount =**true**».</span><span class="sxs-lookup"><span data-stu-id="259cc-144">To retrieve only accounts defined on the local machine, design a query that includes the condition "LocalAccount=**TRUE**".</span></span>

</dd> <dt>

<span data-ttu-id="259cc-145">**Nom**</span><span class="sxs-lookup"><span data-stu-id="259cc-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="259cc-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="259cc-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="259cc-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="259cc-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="259cc-148">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Network Management structures \| Name")</span><span class="sxs-lookup"><span data-stu-id="259cc-148">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|name")</span></span>
</dt> </dl>

<span data-ttu-id="259cc-149">Nom du compte système Windows sur le domaine spécifié par la propriété de **domaine** de cette classe.</span><span class="sxs-lookup"><span data-stu-id="259cc-149">Name of the Windows system account on the domain specified by the **Domain** property of this class.</span></span> <span data-ttu-id="259cc-150">Cette propriété remplace la propriété **Name** héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="259cc-150">This property overrides the **Name** property inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="259cc-151">**SID**</span><span class="sxs-lookup"><span data-stu-id="259cc-151">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="259cc-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="259cc-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="259cc-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="259cc-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="259cc-154">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api, \| identificateurs de sécurité (SID)")</span><span class="sxs-lookup"><span data-stu-id="259cc-154">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Security Identifiers (SIDs)")</span></span>
</dt> </dl>

<span data-ttu-id="259cc-155">Identificateur de sécurité (SID) pour ce compte.</span><span class="sxs-lookup"><span data-stu-id="259cc-155">Security identifier (SID) for this account.</span></span> <span data-ttu-id="259cc-156">Un SID est une valeur de chaîne de longueur variable utilisée pour identifier un tiers de confiance.</span><span class="sxs-lookup"><span data-stu-id="259cc-156">A SID is a string value of variable length used to identify a trustee.</span></span> <span data-ttu-id="259cc-157">Chaque compte possède un SID unique émis par une autorité (par exemple, un domaine Windows), stocké dans une base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="259cc-157">Each account has a unique SID issued by an authority (such as a Windows domain), stored in a security database.</span></span> <span data-ttu-id="259cc-158">Lorsqu’un utilisateur ouvre une session, le système récupère le SID de l’utilisateur à partir de la base de données et le place dans le jeton d’accès de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="259cc-158">When a user logs on, the system retrieves the user's SID from the database and places it in the user's access token.</span></span> <span data-ttu-id="259cc-159">Le système utilise le SID dans le jeton d’accès de l’utilisateur pour identifier l’utilisateur dans toutes les interactions suivantes avec la sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="259cc-159">The system uses the SID in the user's access token to identify the user in all subsequent interactions with Windows security.</span></span> <span data-ttu-id="259cc-160">Lorsqu’un SID a été utilisé en tant qu’identificateur unique pour un utilisateur ou un groupe, il ne peut pas être réutilisé pour identifier un autre utilisateur ou groupe.</span><span class="sxs-lookup"><span data-stu-id="259cc-160">When a SID has been used as the unique identifier for a user or group, it cannot be used again to identify another user or group.</span></span>

</dd> <dt>

<span data-ttu-id="259cc-161">**SIDType**</span><span class="sxs-lookup"><span data-stu-id="259cc-161">**SIDType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="259cc-162">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="259cc-162">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="259cc-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="259cc-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="259cc-164">Qualificateurs : [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Access Control types énumération types \| sid \_ \_ use")</span><span class="sxs-lookup"><span data-stu-id="259cc-164">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Access Control Enumeration Types\|SID\_NAME\_USE")</span></span>
</dt> </dl>

<span data-ttu-id="259cc-165">Valeurs énumérées qui spécifient le type d’identificateur de sécurité (SID).</span><span class="sxs-lookup"><span data-stu-id="259cc-165">Enumerated values that specify the type of security identifier (SID).</span></span>

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

<span data-ttu-id="259cc-166">**SidTypeUser** (1)</span><span class="sxs-lookup"><span data-stu-id="259cc-166">**SidTypeUser** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

<span data-ttu-id="259cc-167">**SidTypeGroup** (2)</span><span class="sxs-lookup"><span data-stu-id="259cc-167">**SidTypeGroup** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

<span data-ttu-id="259cc-168">**SidTypeDomain** (3)</span><span class="sxs-lookup"><span data-stu-id="259cc-168">**SidTypeDomain** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

<span data-ttu-id="259cc-169">**SidTypeAlias** (4)</span><span class="sxs-lookup"><span data-stu-id="259cc-169">**SidTypeAlias** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

<span data-ttu-id="259cc-170">**SidTypeWellKnownGroup** (5)</span><span class="sxs-lookup"><span data-stu-id="259cc-170">**SidTypeWellKnownGroup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

<span data-ttu-id="259cc-171">**SidTypeDeletedAccount** (6)</span><span class="sxs-lookup"><span data-stu-id="259cc-171">**SidTypeDeletedAccount** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

<span data-ttu-id="259cc-172">**SidTypeInvalid** (7)</span><span class="sxs-lookup"><span data-stu-id="259cc-172">**SidTypeInvalid** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

<span data-ttu-id="259cc-173">**SidTypeUnknown** (8)</span><span class="sxs-lookup"><span data-stu-id="259cc-173">**SidTypeUnknown** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

<span data-ttu-id="259cc-174">**SidTypeComputer** (9)</span><span class="sxs-lookup"><span data-stu-id="259cc-174">**SidTypeComputer** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="259cc-175">**État**</span><span class="sxs-lookup"><span data-stu-id="259cc-175">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="259cc-176">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="259cc-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="259cc-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="259cc-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="259cc-178">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="259cc-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="259cc-179">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="259cc-179">Current status of the object.</span></span> <span data-ttu-id="259cc-180">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="259cc-180">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="259cc-181">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédit une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="259cc-181">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicts a failure in the near future).</span></span> <span data-ttu-id="259cc-182">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="259cc-182">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="259cc-183">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="259cc-183">The latter, "Service", can apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="259cc-184">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="259cc-184">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="259cc-185">Cette propriété est héritée de la classe [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="259cc-185">This property is inherited from the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class.</span></span>

<span data-ttu-id="259cc-186">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="259cc-186">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="259cc-187">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="259cc-187">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="259cc-188">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="259cc-188">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="259cc-189">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="259cc-189">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="259cc-190">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="259cc-190">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="259cc-191">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="259cc-191">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="259cc-192">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="259cc-192">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="259cc-193">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="259cc-193">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="259cc-194">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="259cc-194">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="259cc-195">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="259cc-195">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="259cc-196">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="259cc-196">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="259cc-197">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="259cc-197">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="259cc-198">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="259cc-198">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="259cc-199"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="259cc-199"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="259cc-200">Notes</span><span class="sxs-lookup"><span data-stu-id="259cc-200">Remarks</span></span>

<span data-ttu-id="259cc-201">La classe de **\_ compte Win32** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="259cc-201">The **Win32\_Account** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="259cc-202">Exemples</span><span class="sxs-lookup"><span data-stu-id="259cc-202">Examples</span></span>

<span data-ttu-id="259cc-203">Le code PowerShell suivant récupère les comptes locaux.</span><span class="sxs-lookup"><span data-stu-id="259cc-203">The following PowerShell code retrieves the local accounts.</span></span>


```PowerShell
Get-WmiObject Win32_Account -Filter "Domain='$Env:ComputerName'"
```



<span data-ttu-id="259cc-204">Le code PowerShell suivant récupère les comptes de domaine.</span><span class="sxs-lookup"><span data-stu-id="259cc-204">The following PowerShell code retrieves the domain accounts.</span></span>


```PowerShell
 Get-WmiObject Win32_Account -Filter "Domain='$Env:UserDomain'" 
```



## <a name="requirements"></a><span data-ttu-id="259cc-205">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="259cc-205">Requirements</span></span>



| <span data-ttu-id="259cc-206">Condition requise</span><span class="sxs-lookup"><span data-stu-id="259cc-206">Requirement</span></span> | <span data-ttu-id="259cc-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="259cc-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="259cc-208">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="259cc-208">Minimum supported client</span></span><br/> | <span data-ttu-id="259cc-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="259cc-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="259cc-210">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="259cc-210">Minimum supported server</span></span><br/> | <span data-ttu-id="259cc-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="259cc-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="259cc-212">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="259cc-212">Namespace</span></span><br/>                | <span data-ttu-id="259cc-213">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="259cc-213">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="259cc-214">MOF</span><span class="sxs-lookup"><span data-stu-id="259cc-214">MOF</span></span><br/>                      | <dl> <span data-ttu-id="259cc-215"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="259cc-215"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="259cc-216">DLL</span><span class="sxs-lookup"><span data-stu-id="259cc-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="259cc-217"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="259cc-217"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="259cc-218">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="259cc-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="259cc-219">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="259cc-219">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="259cc-220">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="259cc-220">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

