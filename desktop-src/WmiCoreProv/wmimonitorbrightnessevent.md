---
description: Représente une modification de la luminosité d’une analyse.
ms.assetid: c2eb5630-a52f-4ad4-aaee-1cc8afef8c9e
title: WmiMonitorBrightnessEvent, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessEvent
- WmiMonitorBrightnessEvent.Active
- WmiMonitorBrightnessEvent.Brightness
- WmiMonitorBrightnessEvent.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 7e53f90627c959db0140b01cf3b3d385afcc6e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526185"
---
# <a name="wmimonitorbrightnessevent-class"></a><span data-ttu-id="3aa1d-103">WmiMonitorBrightnessEvent, classe</span><span class="sxs-lookup"><span data-stu-id="3aa1d-103">WmiMonitorBrightnessEvent class</span></span>

<span data-ttu-id="3aa1d-104">La classe d’événements **WmiMonitorBrightnessEvent** WMI représente une modification de la luminosité d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="3aa1d-104">The **WmiMonitorBrightnessEvent** WMI event class represents a change in the brightness of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aa1d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3aa1d-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightnessEvent : WMIEvent
{
  boolean Active;
  uint8   Brightness;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="3aa1d-106">Membres</span><span class="sxs-lookup"><span data-stu-id="3aa1d-106">Members</span></span>

<span data-ttu-id="3aa1d-107">La classe **WmiMonitorBrightnessEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3aa1d-107">The **WmiMonitorBrightnessEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="3aa1d-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3aa1d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3aa1d-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3aa1d-109">Properties</span></span>

<span data-ttu-id="3aa1d-110">La classe **WmiMonitorBrightnessEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3aa1d-110">The **WmiMonitorBrightnessEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3aa1d-111">**Actif**</span><span class="sxs-lookup"><span data-stu-id="3aa1d-111">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3aa1d-112">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="3aa1d-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3aa1d-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3aa1d-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3aa1d-114">Indique le moniteur actif.</span><span class="sxs-lookup"><span data-stu-id="3aa1d-114">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="3aa1d-115">**Luminosité**</span><span class="sxs-lookup"><span data-stu-id="3aa1d-115">**Brightness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3aa1d-116">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="3aa1d-116">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="3aa1d-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3aa1d-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3aa1d-118">Luminosité actuelle de l’analyse en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="3aa1d-118">Current monitor brightness as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="3aa1d-119">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="3aa1d-119">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3aa1d-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3aa1d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3aa1d-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3aa1d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3aa1d-122">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="3aa1d-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3aa1d-123">Nom de l’instance d’analyse spécifique.</span><span class="sxs-lookup"><span data-stu-id="3aa1d-123">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3aa1d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3aa1d-124">Requirements</span></span>



| <span data-ttu-id="3aa1d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3aa1d-125">Requirement</span></span> | <span data-ttu-id="3aa1d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3aa1d-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa1d-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3aa1d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3aa1d-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3aa1d-128">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3aa1d-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3aa1d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3aa1d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3aa1d-130">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3aa1d-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3aa1d-131">Namespace</span></span><br/>                | <span data-ttu-id="3aa1d-132">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="3aa1d-132">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="3aa1d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="3aa1d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3aa1d-134"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3aa1d-134"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="3aa1d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3aa1d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3aa1d-136"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3aa1d-136"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aa1d-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3aa1d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aa1d-138">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="3aa1d-138">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> <dt>

[<span data-ttu-id="3aa1d-139">**WmiMonitorBrightness**</span><span class="sxs-lookup"><span data-stu-id="3aa1d-139">**WmiMonitorBrightness**</span></span>](wmimonitorbrightness.md)
</dt> <dt>

[<span data-ttu-id="3aa1d-140">Réception d’un événement WMI</span><span class="sxs-lookup"><span data-stu-id="3aa1d-140">Receiving a WMI Event</span></span>](/windows/desktop/WmiSdk/receiving-a-wmi-event)
</dt> </dl>

 

