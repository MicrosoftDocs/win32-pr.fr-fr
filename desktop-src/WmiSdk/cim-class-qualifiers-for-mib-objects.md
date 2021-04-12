---
description: Le fournisseur SNMP utilise les qualificateurs de classe CIM suivants lors du mappage des définitions d’objets MIB aux définitions de classe CIM.
ms.assetid: 458167dc-562e-47b8-8760-797ae13f9459
ms.tgt_platform: multiple
title: Qualificateurs de classe CIM pour les objets MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60fe97debc7fd81b48a6daf0f5a955374546458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209995"
---
# <a name="cim-class-qualifiers-for-mib-objects"></a><span data-ttu-id="fe607-103">Qualificateurs de classe CIM pour les objets MIB</span><span class="sxs-lookup"><span data-stu-id="fe607-103">CIM Class Qualifiers for MIB Objects</span></span>

<span data-ttu-id="fe607-104">Le fournisseur SNMP utilise les qualificateurs de classe CIM suivants lors du mappage des définitions d’objets MIB aux définitions de classe CIM.</span><span class="sxs-lookup"><span data-stu-id="fe607-104">The SNMP Provider uses the following CIM class qualifiers when mapping MIB object definitions to CIM class definitions.</span></span> <span data-ttu-id="fe607-105">Un qualificateur obligatoire doit être présent pour permettre au fournisseur SNMP de résoudre entièrement un objet de groupe.</span><span class="sxs-lookup"><span data-stu-id="fe607-105">A mandatory qualifier must be present for the SNMP Provider to fully resolve a group object.</span></span> <span data-ttu-id="fe607-106">L’impossibilité de définir un qualificateur obligatoire renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="fe607-106">Failure to define a mandatory qualifier returns an error.</span></span> <span data-ttu-id="fe607-107">La spécification d’une valeur de qualificateur non conforme retourne également une erreur.</span><span class="sxs-lookup"><span data-stu-id="fe607-107">Specifying an illegal qualifier value also returns an error.</span></span>

> [!Note]  
> <span data-ttu-id="fe607-108">Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="fe607-108">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 



| <span data-ttu-id="fe607-109">Qualificateur</span><span class="sxs-lookup"><span data-stu-id="fe607-109">Qualifier</span></span>           | <span data-ttu-id="fe607-110">Description</span><span class="sxs-lookup"><span data-stu-id="fe607-110">Description</span></span>                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe607-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="fe607-111">**Description**</span></span>     | <span data-ttu-id="fe607-112">**chaîne** Facultatif</span><span class="sxs-lookup"><span data-stu-id="fe607-112">**string** Optional</span></span><br/> <span data-ttu-id="fe607-113">Description de la classe.</span><span class="sxs-lookup"><span data-stu-id="fe607-113">Description of the class.</span></span><br/>                                                                      |
| <span data-ttu-id="fe607-114">**ObjectID de groupe \_**</span><span class="sxs-lookup"><span data-stu-id="fe607-114">**Group\_Objectid**</span></span> | <span data-ttu-id="fe607-115">**chaîne** Obligatoire, si la classe est pour le fournisseur de classes SNMP.</span><span class="sxs-lookup"><span data-stu-id="fe607-115">**string** Mandatory, if the class is for the SNMP class provider.</span></span><br/> <span data-ttu-id="fe607-116">Identificateur d’objet de la collection fabriquée.</span><span class="sxs-lookup"><span data-stu-id="fe607-116">Object identifier of the fabricated collection.</span></span><br/> |
| <span data-ttu-id="fe607-117">**Importations de modules \_**</span><span class="sxs-lookup"><span data-stu-id="fe607-117">**Module\_Imports**</span></span> | <span data-ttu-id="fe607-118">**chaîne** Facultatif</span><span class="sxs-lookup"><span data-stu-id="fe607-118">**string** Optional</span></span><br/> <span data-ttu-id="fe607-119">Liste séparée par des virgules des noms de module MIB utilisés pour résoudre les importations.</span><span class="sxs-lookup"><span data-stu-id="fe607-119">Comma-separated list of MIB module names used to resolve imports.</span></span><br/>                              |
| <span data-ttu-id="fe607-120">**Nom du module \_**</span><span class="sxs-lookup"><span data-stu-id="fe607-120">**Module\_Name**</span></span>    | <span data-ttu-id="fe607-121">**chaîne** Facultatif</span><span class="sxs-lookup"><span data-stu-id="fe607-121">**string** Optional</span></span><br/> <span data-ttu-id="fe607-122">Nom d’identité d’un module MIB.</span><span class="sxs-lookup"><span data-stu-id="fe607-122">Identity name of a MIB module.</span></span><br/>                                                                 |
| <span data-ttu-id="fe607-123">**Référence**</span><span class="sxs-lookup"><span data-stu-id="fe607-123">**Reference**</span></span>       | <span data-ttu-id="fe607-124">**chaîne** Facultatif</span><span class="sxs-lookup"><span data-stu-id="fe607-124">**string** Optional</span></span><br/> <span data-ttu-id="fe607-125">Fait référence à un autre document qui contient plus d’informations sur la classe.</span><span class="sxs-lookup"><span data-stu-id="fe607-125">Refers to another document that contains more information about the class.</span></span><br/>                     |
| <span data-ttu-id="fe607-126">**Singleton**</span><span class="sxs-lookup"><span data-stu-id="fe607-126">**Singleton**</span></span>       | <span data-ttu-id="fe607-127">Valeur **booléenne** Obligatoire pour les classes mappées à partir de collections scalaires.</span><span class="sxs-lookup"><span data-stu-id="fe607-127">**Bool** Mandatory for classes mapped from scalar collections.</span></span><br/> <span data-ttu-id="fe607-128">Indique une classe qui ne peut avoir qu’une seule instance.</span><span class="sxs-lookup"><span data-stu-id="fe607-128">Indicates a class that can only have one instance.</span></span><br/>  |



 

 

 




