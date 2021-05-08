---
description: Contient le type de connexion du moniteur.
ms.assetid: f5658246-fbb8-4530-8dfb-f1ca792fe9d5
title: WmiMonitorConnectionParams, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorConnectionParams
- WmiMonitorConnectionParams.Active
- WmiMonitorConnectionParams.InstanceName
- WmiMonitorConnectionParams.VideoOutputTechnology
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: a88b80773ec60b161df51fc759cc932d5c53c931
ms.sourcegitcommit: cfcac5a083b72fd7f2a5188166d470cc0e95d02d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/08/2021
ms.locfileid: "109626691"
---
# <a name="wmimonitorconnectionparams-class"></a><span data-ttu-id="ed912-103">WmiMonitorConnectionParams, classe</span><span class="sxs-lookup"><span data-stu-id="ed912-103">WmiMonitorConnectionParams class</span></span>

<span data-ttu-id="ed912-104">La classe WMI WmiMonitorConnectionParams contient le type de connexion du moniteur.</span><span class="sxs-lookup"><span data-stu-id="ed912-104">The WmiMonitorConnectionParams WMI class contains the connection type of the monitor.</span></span>

<span data-ttu-id="ed912-105">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ed912-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed912-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed912-106">Syntax</span></span>

``` syntax
class WmiMonitorConnectionParams
{
  boolean Active;
  string  InstanceName;
  uint32  VideoOutputTechnology;
};
```

## <a name="members"></a><span data-ttu-id="ed912-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ed912-107">Members</span></span>

<span data-ttu-id="ed912-108">La classe **WmiMonitorConnectionParams** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ed912-108">The **WmiMonitorConnectionParams** class has these types of members:</span></span>

-   [<span data-ttu-id="ed912-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ed912-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ed912-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ed912-110">Properties</span></span>

<span data-ttu-id="ed912-111">La classe **WmiMonitorConnectionParams** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ed912-111">The **WmiMonitorConnectionParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ed912-112">**Actif**</span><span class="sxs-lookup"><span data-stu-id="ed912-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed912-113">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ed912-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ed912-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed912-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed912-115">Indique le moniteur actif.</span><span class="sxs-lookup"><span data-stu-id="ed912-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="ed912-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="ed912-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed912-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ed912-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed912-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed912-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed912-119">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="ed912-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ed912-120">Nom de l’instance d’analyse spécifique.</span><span class="sxs-lookup"><span data-stu-id="ed912-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="ed912-121">**VideoOutputTechnology**</span><span class="sxs-lookup"><span data-stu-id="ed912-121">**VideoOutputTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed912-122">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed912-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed912-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed912-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed912-124">Type de connexion de la technologie de sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="ed912-124">Video output technology connection type.</span></span> <span data-ttu-id="ed912-125">Les valeurs valides sont documentées dans l’énumération de la [ \_ \_ \_ technologie de sortie vidéo D3DKMDT](/windows-hardware/drivers/ddi/d3dkmdt/ne-d3dkmdt-_d3dkmdt_video_output_technology) .</span><span class="sxs-lookup"><span data-stu-id="ed912-125">Valid values are documented in the [D3DKMDT\_VIDEO\_OUTPUT\_TECHNOLOGY](/windows-hardware/drivers/ddi/d3dkmdt/ne-d3dkmdt-_d3dkmdt_video_output_technology) enumeration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed912-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed912-126">Requirements</span></span>



| <span data-ttu-id="ed912-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed912-127">Requirement</span></span> | <span data-ttu-id="ed912-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed912-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed912-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed912-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ed912-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed912-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ed912-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed912-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ed912-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed912-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ed912-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ed912-133">Namespace</span></span><br/>                | <span data-ttu-id="ed912-134">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="ed912-134">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="ed912-135">MOF</span><span class="sxs-lookup"><span data-stu-id="ed912-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed912-136"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed912-136"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed912-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ed912-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed912-138"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed912-138"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed912-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed912-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed912-140">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="ed912-140">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




