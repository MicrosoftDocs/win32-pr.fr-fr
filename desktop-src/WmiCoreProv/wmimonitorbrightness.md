---
description: Représente les paramètres de luminosité d’un moniteur d’ordinateur.
ms.assetid: 01fa3efc-2a1d-4405-989f-2c180842c6b9
title: WmiMonitorBrightness, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightness
- WmiMonitorBrightness.Active
- WmiMonitorBrightness.CurrentBrightness
- WmiMonitorBrightness.InstanceName
- WmiMonitorBrightness.Level
- WmiMonitorBrightness.Levels
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: b8d16c8dc20291a03fb205441c8826c85125970c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521944"
---
# <a name="wmimonitorbrightness-class"></a><span data-ttu-id="04177-103">WmiMonitorBrightness, classe</span><span class="sxs-lookup"><span data-stu-id="04177-103">WmiMonitorBrightness class</span></span>

<span data-ttu-id="04177-104">La classe WMI **WmiMonitorBrightness** représente les paramètres de luminosité d’un moniteur d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="04177-104">The **WmiMonitorBrightness** WMI class represents the brightness parameters of a computer monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="04177-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04177-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightness : MSMonitorClass
{
  boolean Active;
  uint8   CurrentBrightness;
          InstanceName;
  uint8   Level[];
  uint32  Levels;
};
```

## <a name="members"></a><span data-ttu-id="04177-106">Membres</span><span class="sxs-lookup"><span data-stu-id="04177-106">Members</span></span>

<span data-ttu-id="04177-107">La classe **WmiMonitorBrightness** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="04177-107">The **WmiMonitorBrightness** class has these types of members:</span></span>

-   [<span data-ttu-id="04177-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="04177-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="04177-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="04177-109">Properties</span></span>

<span data-ttu-id="04177-110">La classe **WmiMonitorBrightness** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="04177-110">The **WmiMonitorBrightness** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="04177-111">**Actif**</span><span class="sxs-lookup"><span data-stu-id="04177-111">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04177-112">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="04177-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="04177-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="04177-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04177-114">Indique si le moniteur cible est actif.</span><span class="sxs-lookup"><span data-stu-id="04177-114">Indicates if the target monitor is active.</span></span>

</dd> <dt>

<span data-ttu-id="04177-115">**CurrentBrightness**</span><span class="sxs-lookup"><span data-stu-id="04177-115">**CurrentBrightness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04177-116">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="04177-116">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="04177-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="04177-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04177-118">Luminosité actuelle.</span><span class="sxs-lookup"><span data-stu-id="04177-118">Current brightness.</span></span> <span data-ttu-id="04177-119">Cette valeur doit être comprise entre les *niveaux*.</span><span class="sxs-lookup"><span data-stu-id="04177-119">This value must be a value taken from *Levels*.</span></span>

<span data-ttu-id="04177-120">Exemple : 100</span><span class="sxs-lookup"><span data-stu-id="04177-120">Example: 100</span></span>

</dd> <dt>

<span data-ttu-id="04177-121">InstanceName</span><span class="sxs-lookup"><span data-stu-id="04177-121">InstanceName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04177-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="04177-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04177-123">Qualificateurs : Clé</span><span class="sxs-lookup"><span data-stu-id="04177-123">Qualifiers: Key</span></span>
</dt> </dl>

<span data-ttu-id="04177-124">Nom de l’instance d’analyse spécifique.</span><span class="sxs-lookup"><span data-stu-id="04177-124">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="04177-125">**Niveau**</span><span class="sxs-lookup"><span data-stu-id="04177-125">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04177-126">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="04177-126">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="04177-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="04177-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04177-128">Tableau contenant les niveaux de luminosité possibles.</span><span class="sxs-lookup"><span data-stu-id="04177-128">Array containing the possible brightness levels.</span></span>

<span data-ttu-id="04177-129">Exemple : \[ 0, 1, 2,..., 100 \] .</span><span class="sxs-lookup"><span data-stu-id="04177-129">Example: \[0, 1, 2, ..., 100\].</span></span>

</dd> <dt>

<span data-ttu-id="04177-130">**Niveaux**</span><span class="sxs-lookup"><span data-stu-id="04177-130">**Levels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04177-131">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="04177-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="04177-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="04177-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04177-133">Nombre total de niveaux de luminosité pris en charge par le moniteur, comme décrit dans *niveau*.</span><span class="sxs-lookup"><span data-stu-id="04177-133">The total number of brightness levels the monitor supports, as described in *Level*.</span></span>

<span data-ttu-id="04177-134">Exemple : 101</span><span class="sxs-lookup"><span data-stu-id="04177-134">Example: 101</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="04177-135">Exemples</span><span class="sxs-lookup"><span data-stu-id="04177-135">Examples</span></span>

<span data-ttu-id="04177-136">Pour plus d’informations et pour obtenir des exemples de code sur l’utilisation de cette classe dans PowerShell, consultez [Utiliser PowerShell pour créer des rapports et définir la luminosité](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx)de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="04177-136">For more information and code samples on using this class in PowerShell, see [Use PowerShell to Report and Set Monitor Brightness](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx).</span></span>

## <a name="requirements"></a><span data-ttu-id="04177-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04177-137">Requirements</span></span>



| <span data-ttu-id="04177-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04177-138">Requirement</span></span> | <span data-ttu-id="04177-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="04177-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04177-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04177-140">Minimum supported client</span></span><br/> | <span data-ttu-id="04177-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04177-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="04177-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04177-142">Minimum supported server</span></span><br/> | <span data-ttu-id="04177-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04177-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="04177-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="04177-144">Namespace</span></span><br/>                | <span data-ttu-id="04177-145">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="04177-145">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="04177-146">MOF</span><span class="sxs-lookup"><span data-stu-id="04177-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04177-147"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04177-147"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="04177-148">DLL</span><span class="sxs-lookup"><span data-stu-id="04177-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04177-149"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04177-149"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04177-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04177-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04177-151">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="04177-151">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




