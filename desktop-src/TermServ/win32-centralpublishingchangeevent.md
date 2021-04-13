---
title: Classe Win32_CentralPublishingChangeEvent
description: Événement qui représente une modification des paramètres RDV centraux.
ms.assetid: 95be015e-a185-4548-a7f7-a22b351a34c8
ms.tgt_platform: multiple
keywords:
- Win32_CentralPublishingChangeEvent de la classe Services Bureau à distance
- Win32_CentralPublishingChangeEvent de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_CentralPublishingChangeEvent
- Win32_CentralPublishingChangeEvent.SECURITY_DESCRIPTOR
- Win32_CentralPublishingChangeEvent.TIME_CREATED
- Win32_CentralPublishingChangeEvent.TargetInstance
- Win32_CentralPublishingChangeEvent.OperationType
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4695479eb33301bda51b558375a18186fa08161e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465778"
---
# <a name="win32_centralpublishingchangeevent-class"></a><span data-ttu-id="5a57f-105">\_Classe CentralPublishingChangeEvent Win32</span><span class="sxs-lookup"><span data-stu-id="5a57f-105">Win32\_CentralPublishingChangeEvent class</span></span>

<span data-ttu-id="5a57f-106">Événement qui représente une modification des paramètres RDV centraux.</span><span class="sxs-lookup"><span data-stu-id="5a57f-106">An event that represents a change to the central RDV settings.</span></span>

<span data-ttu-id="5a57f-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5a57f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a57f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a57f-108">Syntax</span></span>

``` syntax
class Win32_CentralPublishingChangeEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  object TargetInstance;
  uint32 OperationType;
};
```

## <a name="members"></a><span data-ttu-id="5a57f-109">Membres</span><span class="sxs-lookup"><span data-stu-id="5a57f-109">Members</span></span>

<span data-ttu-id="5a57f-110">La classe **Win32 \_ CentralPublishingChangeEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5a57f-110">The **Win32\_CentralPublishingChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="5a57f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5a57f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5a57f-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5a57f-112">Properties</span></span>

<span data-ttu-id="5a57f-113">La classe **Win32 \_ CentralPublishingChangeEvent** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5a57f-113">The **Win32\_CentralPublishingChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5a57f-114">**OperationType**</span><span class="sxs-lookup"><span data-stu-id="5a57f-114">**OperationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a57f-115">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5a57f-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a57f-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a57f-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a57f-117">Type d’opération correspondant à l’événement.</span><span class="sxs-lookup"><span data-stu-id="5a57f-117">The type of operation corresponding to the event.</span></span>

<dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="5a57f-118">**Créer** (0)</span><span class="sxs-lookup"><span data-stu-id="5a57f-118">**Create** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify"></span><span id="modify"></span><span id="MODIFY"></span>

<span data-ttu-id="5a57f-119">**Modifier** (1)</span><span class="sxs-lookup"><span data-stu-id="5a57f-119">**Modify** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>

<span data-ttu-id="5a57f-120">**Supprimer** (2)</span><span class="sxs-lookup"><span data-stu-id="5a57f-120">**Delete** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a57f-121">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="5a57f-121">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a57f-122">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="5a57f-122">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="5a57f-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a57f-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a57f-124">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="5a57f-124">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="5a57f-125">Cette propriété est héritée de l' [**\_ \_ événement**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="5a57f-125">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="5a57f-126">Pour plus d’informations sur les constantes utilisées pour définir ce descripteur de sécurité, voir la rubrique sur les [constantes de sécurité WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="5a57f-126">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="5a57f-127">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="5a57f-127">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a57f-128">Type de données : **objet**</span><span class="sxs-lookup"><span data-stu-id="5a57f-128">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="5a57f-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a57f-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a57f-130">Objet modifié par l’opération correspondant à l’événement.</span><span class="sxs-lookup"><span data-stu-id="5a57f-130">Object changed by the operation corresponding to the event.</span></span>

</dd> <dt>

<span data-ttu-id="5a57f-131">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="5a57f-131">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a57f-132">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5a57f-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5a57f-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a57f-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a57f-134">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="5a57f-134">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="5a57f-135">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="5a57f-135">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="5a57f-136">Les informations sont au format de temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="5a57f-136">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="5a57f-137">Cette propriété est héritée de l' [**\_ \_ événement**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="5a57f-137">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="5a57f-138">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5a57f-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a57f-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a57f-139">Requirements</span></span>



| <span data-ttu-id="5a57f-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a57f-140">Requirement</span></span> | <span data-ttu-id="5a57f-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a57f-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a57f-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a57f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="5a57f-143">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a57f-143">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5a57f-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a57f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="5a57f-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5a57f-145">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="5a57f-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5a57f-146">Namespace</span></span><br/>                | <span data-ttu-id="5a57f-147">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="5a57f-147">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5a57f-148">MOF</span><span class="sxs-lookup"><span data-stu-id="5a57f-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a57f-149"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a57f-149"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="5a57f-150">DLL</span><span class="sxs-lookup"><span data-stu-id="5a57f-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a57f-151"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a57f-151"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

