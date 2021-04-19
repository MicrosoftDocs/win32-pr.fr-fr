---
description: Les types de données pris en charge par VDS définissent les valeurs de retour de fonction, les paramètres de fonction et les membres de structure. Les types de données définissent la taille et la signification de ces éléments.
ms.assetid: f17e8c7e-e3cb-49ca-9060-2299dda55770
title: Types de données VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a868606110d9cf1c3cad5c3036789d041a5d86c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541995"
---
# <a name="vds-data-types"></a><span data-ttu-id="67b09-104">Types de données VDS</span><span class="sxs-lookup"><span data-stu-id="67b09-104">VDS Data Types</span></span>

<span data-ttu-id="67b09-105">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="67b09-105">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="67b09-106">Les types de données pris en charge par VDS définissent les valeurs de retour de fonction, les paramètres de fonction et les membres de structure.</span><span class="sxs-lookup"><span data-stu-id="67b09-106">The data types supported by VDS define function return values, function parameters, and structure members.</span></span> <span data-ttu-id="67b09-107">Les types de données définissent la taille et la signification de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="67b09-107">Data types define the size and meaning of these elements.</span></span>



| <span data-ttu-id="67b09-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="67b09-108">Data type</span></span>                                                                                      | <span data-ttu-id="67b09-109">Description</span><span class="sxs-lookup"><span data-stu-id="67b09-109">Description</span></span>                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67b09-110"><span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**\_ID d’objet VDS \_**</span><span class="sxs-lookup"><span data-stu-id="67b09-110"><span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**VDS\_OBJECT\_ID**</span></span><br/> | <span data-ttu-id="67b09-111">ID de l’objet VDS.</span><span class="sxs-lookup"><span data-stu-id="67b09-111">VDS object ID.</span></span> <span data-ttu-id="67b09-112">Il n’est pas garanti que ces valeurs soient uniques entre les redémarrages.</span><span class="sxs-lookup"><span data-stu-id="67b09-112">These values are not guaranteed to be unique across reboots.</span></span> <br/> <span data-ttu-id="67b09-113">Ce type est déclaré dans VDS. h (VdsHwPrv. h pour les fournisseurs de matériel) en tant que GUID.</span><span class="sxs-lookup"><span data-stu-id="67b09-113">This type is declared in Vds.h (VdsHwPrv.h for hardware providers) as a GUID.</span></span> <br/> |
| <span data-ttu-id="67b09-114"><span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**\_ID de chemin VDS \_**</span><span class="sxs-lookup"><span data-stu-id="67b09-114"><span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**VDS\_PATH\_ID**</span></span><br/>       | <span data-ttu-id="67b09-115">ID de chemin d’accès VDS pour MPIO (Multipath I/O).</span><span class="sxs-lookup"><span data-stu-id="67b09-115">VDS path ID for multipath I/O (MPIO).</span></span> <br/> <span data-ttu-id="67b09-116">Ce type est déclaré dans VDS. h (VdsHwPrv. h pour les fournisseurs de matériel) en tant que UINT64.</span><span class="sxs-lookup"><span data-stu-id="67b09-116">This type is declared in Vds.h (VdsHwPrv.h for hardware providers) as a UINT64.</span></span><br/>                                      |



 

 

