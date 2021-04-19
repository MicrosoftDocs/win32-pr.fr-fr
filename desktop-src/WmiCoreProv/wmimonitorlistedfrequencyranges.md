---
description: Répertorie les plages de fréquences prises en charge par l’analyse.
ms.assetid: e4713650-5f8c-4808-8b4f-1d29c54ab4e3
title: WmiMonitorListedFrequencyRanges, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedFrequencyRanges
- WmiMonitorListedFrequencyRanges.Active
- WmiMonitorListedFrequencyRanges.InstanceName
- WmiMonitorListedFrequencyRanges.NumOfMonitorFreqRanges
- WmiMonitorListedFrequencyRanges.MonitorFreqRanges
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e13828f6d5e844147fc0b041617c8452c503ceef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529277"
---
# <a name="wmimonitorlistedfrequencyranges-class"></a><span data-ttu-id="4afe3-103">WmiMonitorListedFrequencyRanges, classe</span><span class="sxs-lookup"><span data-stu-id="4afe3-103">WmiMonitorListedFrequencyRanges class</span></span>

<span data-ttu-id="4afe3-104">La classe WMI **WmiMonitorListedFrequencyRanges** répertorie les plages de fréquences prises en charge par l’analyse.</span><span class="sxs-lookup"><span data-stu-id="4afe3-104">The **WmiMonitorListedFrequencyRanges** WMI class lists the frequency ranges supported by the monitor.</span></span> <span data-ttu-id="4afe3-105">Ces plages se trouvent dans la définition d’entrée vidéo du bloc de données d’identification étendues (E-EDID) Enhanced Display standard Association (VESA) ou dans le fichier INF de Windows qui contient les données des pilotes de périphérique.</span><span class="sxs-lookup"><span data-stu-id="4afe3-105">These ranges are found in Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) block or in the Windows INF file that contains device driver data.</span></span>

## <a name="syntax"></a><span data-ttu-id="4afe3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4afe3-106">Syntax</span></span>

``` syntax
class WmiMonitorListedFrequencyRanges : MSMonitorClass
{
  boolean                  Active;
  string                   InstanceName;
  uint16                   NumOfMonitorFreqRanges;
  FrequencyRangeDescriptor MonitorFreqRanges[];
};
```

## <a name="members"></a><span data-ttu-id="4afe3-107">Membres</span><span class="sxs-lookup"><span data-stu-id="4afe3-107">Members</span></span>

<span data-ttu-id="4afe3-108">La classe **WmiMonitorListedFrequencyRanges** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4afe3-108">The **WmiMonitorListedFrequencyRanges** class has these types of members:</span></span>

-   [<span data-ttu-id="4afe3-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4afe3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4afe3-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4afe3-110">Properties</span></span>

<span data-ttu-id="4afe3-111">La classe **WmiMonitorListedFrequencyRanges** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4afe3-111">The **WmiMonitorListedFrequencyRanges** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4afe3-112">**Actif**</span><span class="sxs-lookup"><span data-stu-id="4afe3-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afe3-113">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4afe3-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4afe3-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4afe3-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4afe3-115">Indique le moniteur actif.</span><span class="sxs-lookup"><span data-stu-id="4afe3-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="4afe3-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="4afe3-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afe3-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4afe3-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4afe3-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4afe3-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4afe3-119">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="4afe3-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4afe3-120">Nom de l’instance d’analyse spécifique.</span><span class="sxs-lookup"><span data-stu-id="4afe3-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="4afe3-121">**MonitorFreqRanges**</span><span class="sxs-lookup"><span data-stu-id="4afe3-121">**MonitorFreqRanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afe3-122">Type de données : tableau **FrequencyRangeDescriptor**</span><span class="sxs-lookup"><span data-stu-id="4afe3-122">Data type: **FrequencyRangeDescriptor** array</span></span>
</dt> <dt>

<span data-ttu-id="4afe3-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4afe3-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4afe3-124">Liste des plages de fréquence d’analyse représentées par des instances de la classe [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md) .</span><span class="sxs-lookup"><span data-stu-id="4afe3-124">List of monitor frequency ranges represented by instances of the [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="4afe3-125">**NumOfMonitorFreqRanges**</span><span class="sxs-lookup"><span data-stu-id="4afe3-125">**NumOfMonitorFreqRanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4afe3-126">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4afe3-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4afe3-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4afe3-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4afe3-128">Nombre de plages de fréquence d’analyse prises en charge.</span><span class="sxs-lookup"><span data-stu-id="4afe3-128">Number of listed supported monitor frequency ranges.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4afe3-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4afe3-129">Requirements</span></span>



| <span data-ttu-id="4afe3-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4afe3-130">Requirement</span></span> | <span data-ttu-id="4afe3-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="4afe3-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4afe3-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4afe3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4afe3-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4afe3-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4afe3-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4afe3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4afe3-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4afe3-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4afe3-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4afe3-136">Namespace</span></span><br/>                | <span data-ttu-id="4afe3-137">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="4afe3-137">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="4afe3-138">MOF</span><span class="sxs-lookup"><span data-stu-id="4afe3-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4afe3-139"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4afe3-139"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="4afe3-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4afe3-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4afe3-141"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4afe3-141"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4afe3-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4afe3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4afe3-143">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="4afe3-143">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




