---
description: Répertorie les modes source pris en charge pour un moniteur vidéo dans son descripteur de moniteur, le cas échéant.
ms.assetid: cca59d28-bd93-4df2-989e-0516dd8eae83
title: WmiMonitorListedSupportedSourceModes, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedSupportedSourceModes
- WmiMonitorListedSupportedSourceModes.Active
- WmiMonitorListedSupportedSourceModes.InstanceName
- WmiMonitorListedSupportedSourceModes.NumOfMonitorSourceModes
- WmiMonitorListedSupportedSourceModes.PreferredMonitorSourceModeIndex
- WmiMonitorListedSupportedSourceModes.MonitorSourceModes
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 35cb4b3548654c72686a8843cc697f109f661d87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534337"
---
# <a name="wmimonitorlistedsupportedsourcemodes-class"></a><span data-ttu-id="29a4b-103">WmiMonitorListedSupportedSourceModes, classe</span><span class="sxs-lookup"><span data-stu-id="29a4b-103">WmiMonitorListedSupportedSourceModes class</span></span>

<span data-ttu-id="29a4b-104">Le **WmiMonitorListedSupportedSourceModes** répertorie les modes source pris en charge pour un moniteur vidéo dans son descripteur de moniteur, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="29a4b-104">The **WmiMonitorListedSupportedSourceModes** lists the supported source modes for a video monitor in its monitor descriptor, if any exist.</span></span> <span data-ttu-id="29a4b-105">Pour les analyses qui n’ont pas de description, cette liste de modes est générée en fonction du type d’analyse, tel que spécifié par le pilote de bus d’analyse.</span><span class="sxs-lookup"><span data-stu-id="29a4b-105">For monitors that have no description, this list of modes is generated based on the type of monitor, as specified by the monitor bus driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="29a4b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29a4b-106">Syntax</span></span>

``` syntax
class WmiMonitorListedSupportedSourceModes : MSMonitorClass
{
  boolean             Active;
  string              InstanceName;
  uint16              NumOfMonitorSourceModes;
  uint16              PreferredMonitorSourceModeIndex;
  VideoModeDescriptor MonitorSourceModes[];
};
```

## <a name="members"></a><span data-ttu-id="29a4b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="29a4b-107">Members</span></span>

<span data-ttu-id="29a4b-108">La classe **WmiMonitorListedSupportedSourceModes** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="29a4b-108">The **WmiMonitorListedSupportedSourceModes** class has these types of members:</span></span>

-   [<span data-ttu-id="29a4b-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="29a4b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="29a4b-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="29a4b-110">Properties</span></span>

<span data-ttu-id="29a4b-111">La classe **WmiMonitorListedSupportedSourceModes** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="29a4b-111">The **WmiMonitorListedSupportedSourceModes** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="29a4b-112">**Actif**</span><span class="sxs-lookup"><span data-stu-id="29a4b-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29a4b-113">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="29a4b-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="29a4b-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="29a4b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29a4b-115">Indique le moniteur actif.</span><span class="sxs-lookup"><span data-stu-id="29a4b-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="29a4b-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="29a4b-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29a4b-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="29a4b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29a4b-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="29a4b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29a4b-119">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="29a4b-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="29a4b-120">Nom de l’instance d’analyse spécifique.</span><span class="sxs-lookup"><span data-stu-id="29a4b-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="29a4b-121">**MonitorSourceModes**</span><span class="sxs-lookup"><span data-stu-id="29a4b-121">**MonitorSourceModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29a4b-122">Type de données : tableau **VideoModeDescriptor**</span><span class="sxs-lookup"><span data-stu-id="29a4b-122">Data type: **VideoModeDescriptor** array</span></span>
</dt> <dt>

<span data-ttu-id="29a4b-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="29a4b-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29a4b-124">Les listes analysent les modes source représentés par les instances de la classe [**VideoModeDescriptor**](videomodedescriptor.md) .</span><span class="sxs-lookup"><span data-stu-id="29a4b-124">Lists monitor source modes represented by instances of the [**VideoModeDescriptor**](videomodedescriptor.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="29a4b-125">**NumOfMonitorSourceModes**</span><span class="sxs-lookup"><span data-stu-id="29a4b-125">**NumOfMonitorSourceModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29a4b-126">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="29a4b-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="29a4b-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="29a4b-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29a4b-128">Nombre de modes source pris en charge du moniteur pris en charge.</span><span class="sxs-lookup"><span data-stu-id="29a4b-128">Number of listed supported monitor source mode.</span></span>

</dd> <dt>

<span data-ttu-id="29a4b-129">**PreferredMonitorSourceModeIndex**</span><span class="sxs-lookup"><span data-stu-id="29a4b-129">**PreferredMonitorSourceModeIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29a4b-130">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="29a4b-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="29a4b-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="29a4b-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="29a4b-132">Index du mode source de l’analyse par défaut.</span><span class="sxs-lookup"><span data-stu-id="29a4b-132">Preferred monitor source mode index.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29a4b-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29a4b-133">Requirements</span></span>



| <span data-ttu-id="29a4b-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29a4b-134">Requirement</span></span> | <span data-ttu-id="29a4b-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="29a4b-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29a4b-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29a4b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="29a4b-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29a4b-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="29a4b-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29a4b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="29a4b-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29a4b-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="29a4b-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="29a4b-140">Namespace</span></span><br/>                | <span data-ttu-id="29a4b-141">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="29a4b-141">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="29a4b-142">MOF</span><span class="sxs-lookup"><span data-stu-id="29a4b-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29a4b-143"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29a4b-143"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="29a4b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="29a4b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29a4b-145"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29a4b-145"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29a4b-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29a4b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29a4b-147">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="29a4b-147">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




