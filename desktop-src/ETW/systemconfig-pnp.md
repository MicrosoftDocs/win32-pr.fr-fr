---
description: Cette classe est la classe de type d’événement pour les événements PnP. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 01e9a8bb-3f54-4e20-b4db-1b4bba745d4f
title: Classe SystemConfig_PnP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_PnP
- SystemConfig_PnP.IDLength
- SystemConfig_PnP.DescriptionLength
- SystemConfig_PnP.FriendlyNameLength
- SystemConfig_PnP.DeviceID
- SystemConfig_PnP.DeviceDescription
- SystemConfig_PnP.FriendlyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2bd4cdbbec5c61f453a0ef6fae3fef0bd494edac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484665"
---
# <a name="systemconfig_pnp-class"></a><span data-ttu-id="c697d-104">\_Classe PNP SystemConfig</span><span class="sxs-lookup"><span data-stu-id="c697d-104">SystemConfig\_PnP class</span></span>

<span data-ttu-id="c697d-105">Cette classe est la classe de type d’événement pour les événements PnP.</span><span class="sxs-lookup"><span data-stu-id="c697d-105">This class is the event type class for PnP events.</span></span>

<span data-ttu-id="c697d-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="c697d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c697d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c697d-107">Syntax</span></span>

``` syntax
[EventType(22), EventTypeName("PnP")]
class SystemConfig_PnP : SystemConfig
{
  uint32 IDLength;
  uint32 DescriptionLength;
  uint32 FriendlyNameLength;
  string DeviceID;
  string DeviceDescription;
  string FriendlyName;
};
```

## <a name="members"></a><span data-ttu-id="c697d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c697d-108">Members</span></span>

<span data-ttu-id="c697d-109">La **classe \_ PNP SystemConfig** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c697d-109">The **SystemConfig\_PnP** class has these types of members:</span></span>

-   [<span data-ttu-id="c697d-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c697d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c697d-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c697d-111">Properties</span></span>

<span data-ttu-id="c697d-112">La **classe \_ PNP SystemConfig** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c697d-112">The **SystemConfig\_PnP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c697d-113">**DescriptionLength**</span><span class="sxs-lookup"><span data-stu-id="c697d-113">**DescriptionLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c697d-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c697d-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c697d-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c697d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c697d-116">Qualificateurs : WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="c697d-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="c697d-117">Longueur, en caractères, de la chaîne DeviceDescription.</span><span class="sxs-lookup"><span data-stu-id="c697d-117">Length, in characters, of the DeviceDescription string.</span></span>

</dd> <dt>

<span data-ttu-id="c697d-118">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="c697d-118">**DeviceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c697d-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c697d-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c697d-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c697d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c697d-121">Qualificateurs : WmiDataId (5), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="c697d-121">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="c697d-122">Description de l’appareil PnP.</span><span class="sxs-lookup"><span data-stu-id="c697d-122">Description of the PnP device.</span></span>

</dd> <dt>

<span data-ttu-id="c697d-123">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c697d-123">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c697d-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c697d-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c697d-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c697d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c697d-126">Qualificateurs : WmiDataId (4), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="c697d-126">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="c697d-127">Identifie l’appareil PnP.</span><span class="sxs-lookup"><span data-stu-id="c697d-127">Identifies the PnP device.</span></span>

</dd> <dt>

<span data-ttu-id="c697d-128">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="c697d-128">**FriendlyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c697d-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c697d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c697d-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c697d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c697d-131">Qualificateurs : WmiDataId (6), StringTermination ("NullTerminated"), format ("w")</span><span class="sxs-lookup"><span data-stu-id="c697d-131">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="c697d-132">Nom de l’appareil PnP à utiliser dans une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c697d-132">Name of the PnP device to use in a user interface.</span></span>

</dd> <dt>

<span data-ttu-id="c697d-133">**FriendlyNameLength**</span><span class="sxs-lookup"><span data-stu-id="c697d-133">**FriendlyNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c697d-134">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c697d-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c697d-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c697d-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c697d-136">Qualificateurs : WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="c697d-136">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="c697d-137">Longueur, en caractères, de la chaîne FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="c697d-137">Length, in characters, of the FriendlyName string.</span></span>

</dd> <dt>

<span data-ttu-id="c697d-138">**IDLength**</span><span class="sxs-lookup"><span data-stu-id="c697d-138">**IDLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c697d-139">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c697d-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c697d-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c697d-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c697d-141">Qualificateurs : WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="c697d-141">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="c697d-142">Longueur, en caractères, de la chaîne DeviceID.</span><span class="sxs-lookup"><span data-stu-id="c697d-142">Length, in characters, of the DeviceID string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c697d-143">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c697d-143">Requirements</span></span>



| <span data-ttu-id="c697d-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c697d-144">Requirement</span></span> | <span data-ttu-id="c697d-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="c697d-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c697d-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c697d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c697d-147">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c697d-147">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c697d-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c697d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c697d-149">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c697d-149">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c697d-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c697d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c697d-151">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="c697d-151">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




