---
description: Le fournisseur de classes WDM définit la classe WMIBinaryMofResource dans \\ l' \\ espace de noms WMI racine pour prendre en charge la tâche de suivi de l’état des données dans l’espace de stockage WMI.
ms.assetid: 57416a36-5b3a-4d04-808c-09adc597c47a
title: WMIBinaryMofResource, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIBinaryMofResource
- WMIBinaryMofResource.HighDateTime
- WMIBinaryMofResource.LowDateTime
- WMIBinaryMofResource.MofProcessed
- WMIBinaryMofResource.Name
api_type:
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 715436ef19308c811e5486926b3cd7e59ee9de0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863330"
---
# <a name="wmibinarymofresource-class"></a><span data-ttu-id="00724-103">WMIBinaryMofResource, classe</span><span class="sxs-lookup"><span data-stu-id="00724-103">WMIBinaryMofResource class</span></span>

<span data-ttu-id="00724-104">Le fournisseur de classes WDM définit la classe **WMIBinaryMofResource** dans \\ l' \\ espace de noms WMI racine pour prendre en charge la tâche de suivi de l’état des données dans l’espace de stockage WMI.</span><span class="sxs-lookup"><span data-stu-id="00724-104">The WDM class provider defines the **WMIBinaryMofResource** class in the \\root\\wmi namespace to support the task of keeping track of the status of data in the WMI repository.</span></span>

## <a name="syntax"></a><span data-ttu-id="00724-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00724-105">Syntax</span></span>

``` syntax
class WMIBinaryMofResource
{
  uint32  HighDateTime;
  uint32  LowDateTime;
  boolean MofProcessed;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="00724-106">Membres</span><span class="sxs-lookup"><span data-stu-id="00724-106">Members</span></span>

<span data-ttu-id="00724-107">La classe **WMIBinaryMofResource** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="00724-107">The **WMIBinaryMofResource** class has these types of members:</span></span>

-   [<span data-ttu-id="00724-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="00724-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="00724-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="00724-109">Properties</span></span>

<span data-ttu-id="00724-110">La classe **WMIBinaryMofResource** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="00724-110">The **WMIBinaryMofResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00724-111">**HighDateTime**</span><span class="sxs-lookup"><span data-stu-id="00724-111">**HighDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00724-112">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00724-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00724-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00724-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00724-114">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="00724-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="00724-115">Moitié supérieure de l’horodatage.</span><span class="sxs-lookup"><span data-stu-id="00724-115">High half of the date-time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="00724-116">**LowDateTime**</span><span class="sxs-lookup"><span data-stu-id="00724-116">**LowDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00724-117">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="00724-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="00724-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00724-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00724-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="00724-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="00724-120">Moitié inférieure de l’horodatage.</span><span class="sxs-lookup"><span data-stu-id="00724-120">Low half of the date-time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="00724-121">**MofProcessed**</span><span class="sxs-lookup"><span data-stu-id="00724-121">**MofProcessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00724-122">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="00724-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="00724-123">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="00724-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="00724-124">Indicateur précisant si le fichier. mof a été entièrement traité.</span><span class="sxs-lookup"><span data-stu-id="00724-124">Flag indicating whether the .mof file was fully processed.</span></span>

</dd> <dt>

<span data-ttu-id="00724-125">**Nom**</span><span class="sxs-lookup"><span data-stu-id="00724-125">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00724-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00724-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00724-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00724-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00724-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="00724-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="00724-129">Nom du pilote compatible WDM pour lequel un fichier MOF binaire a été compilé avec succès dans l’espace de stockage WMI.</span><span class="sxs-lookup"><span data-stu-id="00724-129">Name of the WDM enabled driver that has a binary MOF file successfully compiled in the WMI repository.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00724-130">Notes</span><span class="sxs-lookup"><span data-stu-id="00724-130">Remarks</span></span>

<span data-ttu-id="00724-131">Le fournisseur de classes WDM crée une instance de **WMIBinaryMofResource** pour chaque pilote WDM qui fournit un fichier MOF binaire.</span><span class="sxs-lookup"><span data-stu-id="00724-131">The WDM class provider creates an instance of **WMIBinaryMofResource** for each WDM driver that supplies a binary MOF file.</span></span>

<span data-ttu-id="00724-132">Chaque fois que WMI Initialise le fournisseur, le fournisseur compare l’horodatage avec l’horodateur du fichier image du pilote.</span><span class="sxs-lookup"><span data-stu-id="00724-132">Whenever WMI initializes the provider, the provider compares the timestamp with the timestamp of the driver image file.</span></span> <span data-ttu-id="00724-133">Si les horodateurs diffèrent, WMI RECOMPILE le fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="00724-133">If the timestamps differ, WMI re-compiles the MOF file.</span></span>

## <a name="requirements"></a><span data-ttu-id="00724-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00724-134">Requirements</span></span>



| <span data-ttu-id="00724-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00724-135">Requirement</span></span> | <span data-ttu-id="00724-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="00724-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="00724-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00724-137">Minimum supported client</span></span><br/> | <span data-ttu-id="00724-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="00724-138">Windows XP</span></span><br/>                                                              |
| <span data-ttu-id="00724-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00724-139">Minimum supported server</span></span><br/> | <span data-ttu-id="00724-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="00724-140">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="00724-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="00724-141">Namespace</span></span><br/>                | <span data-ttu-id="00724-142">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="00724-142">Root\\WMI</span></span><br/>                                                               |
| <span data-ttu-id="00724-143">MOF</span><span class="sxs-lookup"><span data-stu-id="00724-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00724-144"><dt>WMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00724-144"><dt>Wmi.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00724-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00724-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00724-146">Fournisseur WDM</span><span class="sxs-lookup"><span data-stu-id="00724-146">WDM Provider</span></span>](wdm-provider.md)
</dt> </dl>

 

