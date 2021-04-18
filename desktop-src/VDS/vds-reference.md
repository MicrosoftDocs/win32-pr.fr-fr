---
description: Cette section décrit l’interface de programmation d’applications du service de disque virtuel (VDS).
ms.assetid: d00fc772-331f-4d71-a418-e34acdfb6652
title: Référence VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369111add0b3f4b7e2742c764a6cbf8b1d8bfdd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519750"
---
# <a name="vds-reference"></a><span data-ttu-id="5a30a-103">Référence VDS</span><span class="sxs-lookup"><span data-stu-id="5a30a-103">VDS Reference</span></span>

<span data-ttu-id="5a30a-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5a30a-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="5a30a-105">Cette section décrit l’interface de programmation d’applications du service de disque virtuel (VDS).</span><span class="sxs-lookup"><span data-stu-id="5a30a-105">This section describes the application programming interface to the Virtual Disk Service (VDS).</span></span>

<span data-ttu-id="5a30a-106">Les développeurs d’applications utilisent les interfaces, structures, énumérations et constantes symboliques dans cette API pour interroger et configurer le stockage, des disques aux groupes de stockage.</span><span class="sxs-lookup"><span data-stu-id="5a30a-106">Application developers use the interfaces, structures, enumerations, and symbolic constants in this API to query and configure storage—from disks to storage arrays.</span></span> <span data-ttu-id="5a30a-107">Pour obtenir une vue détaillée de la relation entre les types VDS, consultez le [modèle d’objet VDS](vds-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="5a30a-107">For a detailed look at the relationship among VDS types, see the [VDS Object Model](vds-object-model.md).</span></span>

<span data-ttu-id="5a30a-108">Les fabricants de stockage implémentent un grand nombre des interfaces définies dans cette section.</span><span class="sxs-lookup"><span data-stu-id="5a30a-108">Storage manufacturers implement many of the interfaces defined in this section.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5a30a-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="5a30a-109">In this Section</span></span>

<dl> <dt>

[<span data-ttu-id="5a30a-110">Constantes VDS</span><span class="sxs-lookup"><span data-stu-id="5a30a-110">VDS Constants</span></span>](vds-constants.md)
</dt> <dd>

<span data-ttu-id="5a30a-111">Répertorie les constantes symboliques dans l’API VDS.</span><span class="sxs-lookup"><span data-stu-id="5a30a-111">Lists the symbolic constants in the VDS API.</span></span>

</dd> <dt>

[<span data-ttu-id="5a30a-112">Types de données VDS</span><span class="sxs-lookup"><span data-stu-id="5a30a-112">VDS Data Types</span></span>](vds-data-types.md)
</dt> <dd>

<span data-ttu-id="5a30a-113">Répertorie les types de données utilisés avec VDS.</span><span class="sxs-lookup"><span data-stu-id="5a30a-113">Lists the data types used with VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="5a30a-114">Énumérations VDS</span><span class="sxs-lookup"><span data-stu-id="5a30a-114">VDS Enumerations</span></span>](vds-enumerations.md)
</dt> <dd>

<span data-ttu-id="5a30a-115">Décrit les énumérations utilisées avec VDS.</span><span class="sxs-lookup"><span data-stu-id="5a30a-115">Describes the enumerations used with VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="5a30a-116">Interfaces VDS</span><span class="sxs-lookup"><span data-stu-id="5a30a-116">VDS Interfaces</span></span>](vds-interfaces.md)
</dt> <dd>

<span data-ttu-id="5a30a-117">Décrit les interfaces VDS et les méthodes qu’elles exposent.</span><span class="sxs-lookup"><span data-stu-id="5a30a-117">Describes VDS interfaces and the methods they expose.</span></span>

</dd> <dt>

[<span data-ttu-id="5a30a-118">Structures VDS</span><span class="sxs-lookup"><span data-stu-id="5a30a-118">VDS Structures</span></span>](vds-structures.md)
</dt> <dd>

<span data-ttu-id="5a30a-119">Décrit les structures passées comme paramètres aux méthodes VDS.</span><span class="sxs-lookup"><span data-stu-id="5a30a-119">Describes the structures passed as parameters to VDS methods.</span></span>

</dd> <dt>

[<span data-ttu-id="5a30a-120">Codes de retour courants du service de disque virtuel</span><span class="sxs-lookup"><span data-stu-id="5a30a-120">Virtual Disk Service Common Return Codes</span></span>](virtual-disk-service-common-return-codes.md)
</dt> <dd>

<span data-ttu-id="5a30a-121">Décrit les codes d’erreur les plus courants spécifiques à VDS.</span><span class="sxs-lookup"><span data-stu-id="5a30a-121">Describes the most common error codes that are specific to VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="5a30a-122">Glossaire du service de disque virtuel</span><span class="sxs-lookup"><span data-stu-id="5a30a-122">Virtual Disk Service Glossary</span></span>](virtual-disk-service-glossary-all.md)
</dt> <dd>

<span data-ttu-id="5a30a-123">Glossaire des termes techniques utilisés dans la documentation VDS.</span><span class="sxs-lookup"><span data-stu-id="5a30a-123">Glossary of technical terms used in VDS documentation.</span></span>

</dd> </dl>

 

 
