---
description: Contient des méthodes qui gèrent la luminosité de l’analyse.
ms.assetid: e7e4139e-b985-4163-9c95-03008a2cc8cb
title: WmiMonitorBrightnessMethods, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods
- WmiMonitorBrightnessMethods.Active
- WmiMonitorBrightnessMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 36fe823703d5d5e4f1f6008d02c600828fe2b53f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521050"
---
# <a name="wmimonitorbrightnessmethods-class"></a><span data-ttu-id="58b02-103">WmiMonitorBrightnessMethods, classe</span><span class="sxs-lookup"><span data-stu-id="58b02-103">WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="58b02-104">La classe WMI **WmiMonitorBrightnessMethods** contient des méthodes qui gèrent la luminosité de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="58b02-104">The **WmiMonitorBrightnessMethods** WMI class contains methods that manage monitor brightness.</span></span>

## <a name="syntax"></a><span data-ttu-id="58b02-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58b02-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightnessMethods
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="58b02-106">Membres</span><span class="sxs-lookup"><span data-stu-id="58b02-106">Members</span></span>

<span data-ttu-id="58b02-107">La classe **WmiMonitorBrightnessMethods** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="58b02-107">The **WmiMonitorBrightnessMethods** class has these types of members:</span></span>

-   [<span data-ttu-id="58b02-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="58b02-108">Methods</span></span>](#wmimonitorbrightnessmethods-class)
-   [<span data-ttu-id="58b02-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="58b02-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="58b02-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="58b02-110">Methods</span></span>

<span data-ttu-id="58b02-111">La classe **WmiMonitorBrightnessMethods** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="58b02-111">The **WmiMonitorBrightnessMethods** class has these methods.</span></span>



| <span data-ttu-id="58b02-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="58b02-112">Method</span></span>                                                                                                         | <span data-ttu-id="58b02-113">Description</span><span class="sxs-lookup"><span data-stu-id="58b02-113">Description</span></span>                                                    |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="58b02-114">**WmiRevertToPolicyBrightness**</span><span class="sxs-lookup"><span data-stu-id="58b02-114">**WmiRevertToPolicyBrightness**</span></span>](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) | <span data-ttu-id="58b02-115">Rétablit la luminosité sur le paramètre de stratégie.</span><span class="sxs-lookup"><span data-stu-id="58b02-115">Sets the brightness back to the policy setting.</span></span><br/>     |
| [<span data-ttu-id="58b02-116">**WmiSetALSBrightness**</span><span class="sxs-lookup"><span data-stu-id="58b02-116">**WmiSetALSBrightness**</span></span>](wmisetalsbrightness-method-in-class-wmimonitorbrightnessmethods.md)                 | <span data-ttu-id="58b02-117">Définit la valeur de luminosité du capteur de lumière ambiante.</span><span class="sxs-lookup"><span data-stu-id="58b02-117">Sets the ambient light sensor brightness value.</span></span><br/>     |
| [<span data-ttu-id="58b02-118">**WmiSetALSBrightnessState**</span><span class="sxs-lookup"><span data-stu-id="58b02-118">**WmiSetALSBrightnessState**</span></span>](wmisetalsbrightnessstate-method-in-class-wmimonitorbrightnessmethods.md)       | <span data-ttu-id="58b02-119">Contrôle l’état de luminosité du capteur de lumière ambiante.</span><span class="sxs-lookup"><span data-stu-id="58b02-119">Controls the ambient light sensor brightness state.</span></span><br/> |
| [<span data-ttu-id="58b02-120">**WmiSetBrightness**</span><span class="sxs-lookup"><span data-stu-id="58b02-120">**WmiSetBrightness**</span></span>](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md)                       | <span data-ttu-id="58b02-121">Définit la luminosité de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="58b02-121">Sets the monitor brightness.</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="58b02-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="58b02-122">Properties</span></span>

<span data-ttu-id="58b02-123">La classe **WmiMonitorBrightnessMethods** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="58b02-123">The **WmiMonitorBrightnessMethods** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58b02-124">**Actif**</span><span class="sxs-lookup"><span data-stu-id="58b02-124">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58b02-125">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="58b02-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="58b02-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58b02-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58b02-127">Indique le moniteur actif.</span><span class="sxs-lookup"><span data-stu-id="58b02-127">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="58b02-128">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="58b02-128">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58b02-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="58b02-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58b02-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58b02-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58b02-131">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="58b02-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="58b02-132">Nom de l’instance d’analyse spécifique.</span><span class="sxs-lookup"><span data-stu-id="58b02-132">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="58b02-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58b02-133">Requirements</span></span>



| <span data-ttu-id="58b02-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58b02-134">Requirement</span></span> | <span data-ttu-id="58b02-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="58b02-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58b02-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58b02-136">Minimum supported client</span></span><br/> | <span data-ttu-id="58b02-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58b02-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="58b02-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58b02-138">Minimum supported server</span></span><br/> | <span data-ttu-id="58b02-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58b02-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="58b02-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="58b02-140">Namespace</span></span><br/>                | <span data-ttu-id="58b02-141">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="58b02-141">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="58b02-142">MOF</span><span class="sxs-lookup"><span data-stu-id="58b02-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58b02-143"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58b02-143"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="58b02-144">DLL</span><span class="sxs-lookup"><span data-stu-id="58b02-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58b02-145"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58b02-145"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58b02-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58b02-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58b02-147">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="58b02-147">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




