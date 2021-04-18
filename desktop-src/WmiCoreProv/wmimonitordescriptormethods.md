---
description: Contient des méthodes qui obtiennent le contenu brut de la définition d’entrée vidéo de la norme VESA (Video Electronics standard Association) (E-EDID) améliorée des données d’identification d’affichage étendu (E-EDID) v. 1. x blocs de données 128 octets standard.
ms.assetid: c13d4ddd-d171-44d5-9e70-3a6f89ad55da
title: WmiMonitorDescriptorMethods, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods
- WmiMonitorDescriptorMethods.Active
- WmiMonitorDescriptorMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 578c08c48ada4859b69e00655c5eea8c075515fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526184"
---
# <a name="wmimonitordescriptormethods-class"></a><span data-ttu-id="49dbe-103">WmiMonitorDescriptorMethods, classe</span><span class="sxs-lookup"><span data-stu-id="49dbe-103">WmiMonitorDescriptorMethods class</span></span>

<span data-ttu-id="49dbe-104">La classe WMI **WmiMonitorDescriptorMethods** contient des méthodes qui obtiennent le contenu brut de la définition d’entrée vidéo de la norme VESA (Video Electronics standard Association) améliorée Extended Display Identification Data (E-EDID) v. 1. x blocs de données 128 octets standard.</span><span class="sxs-lookup"><span data-stu-id="49dbe-104">The **WmiMonitorDescriptorMethods** WMI class contains methods that obtain the raw content of Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) v.1.x standard 128-byte data blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="49dbe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49dbe-105">Syntax</span></span>

``` syntax
class WmiMonitorDescriptorMethods : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="49dbe-106">Membres</span><span class="sxs-lookup"><span data-stu-id="49dbe-106">Members</span></span>

<span data-ttu-id="49dbe-107">La classe **WmiMonitorDescriptorMethods** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="49dbe-107">The **WmiMonitorDescriptorMethods** class has these types of members:</span></span>

-   [<span data-ttu-id="49dbe-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="49dbe-108">Methods</span></span>](#wmimonitordescriptormethods-class)
-   [<span data-ttu-id="49dbe-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="49dbe-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="49dbe-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="49dbe-110">Methods</span></span>

<span data-ttu-id="49dbe-111">La classe **WmiMonitorDescriptorMethods** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="49dbe-111">The **WmiMonitorDescriptorMethods** class has these methods.</span></span>



| <span data-ttu-id="49dbe-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="49dbe-112">Method</span></span>                                                                                           | <span data-ttu-id="49dbe-113">Description</span><span class="sxs-lookup"><span data-stu-id="49dbe-113">Description</span></span>                                                                   |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="49dbe-114">**WmiGetMonitorRawEEdidV1Block**</span><span class="sxs-lookup"><span data-stu-id="49dbe-114">**WmiGetMonitorRawEEdidV1Block**</span></span>](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md) | <span data-ttu-id="49dbe-115">Accède aux données brutes d’un bloc de descripteur EDID v. 1. x spécifié.</span><span class="sxs-lookup"><span data-stu-id="49dbe-115">Accesses the raw data for a specified EDID v.1.x descriptor block.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="49dbe-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="49dbe-116">Properties</span></span>

<span data-ttu-id="49dbe-117">La classe **WmiMonitorDescriptorMethods** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="49dbe-117">The **WmiMonitorDescriptorMethods** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="49dbe-118">**Actif**</span><span class="sxs-lookup"><span data-stu-id="49dbe-118">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49dbe-119">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="49dbe-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="49dbe-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49dbe-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49dbe-121">Indique le moniteur actif.</span><span class="sxs-lookup"><span data-stu-id="49dbe-121">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="49dbe-122">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="49dbe-122">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49dbe-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="49dbe-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49dbe-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="49dbe-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49dbe-125">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="49dbe-125">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="49dbe-126">Nom de l’instance d’analyse spécifique.</span><span class="sxs-lookup"><span data-stu-id="49dbe-126">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="49dbe-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49dbe-127">Requirements</span></span>



| <span data-ttu-id="49dbe-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49dbe-128">Requirement</span></span> | <span data-ttu-id="49dbe-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="49dbe-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49dbe-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49dbe-130">Minimum supported client</span></span><br/> | <span data-ttu-id="49dbe-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49dbe-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="49dbe-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49dbe-132">Minimum supported server</span></span><br/> | <span data-ttu-id="49dbe-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49dbe-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="49dbe-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="49dbe-134">Namespace</span></span><br/>                | <span data-ttu-id="49dbe-135">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="49dbe-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="49dbe-136">MOF</span><span class="sxs-lookup"><span data-stu-id="49dbe-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49dbe-137"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49dbe-137"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="49dbe-138">DLL</span><span class="sxs-lookup"><span data-stu-id="49dbe-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49dbe-139"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49dbe-139"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49dbe-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49dbe-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49dbe-141">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="49dbe-141">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




