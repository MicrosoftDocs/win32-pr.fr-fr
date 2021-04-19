---
description: WMI définit un ensemble de propriétés système associées à toutes les classes et instances de classes en plus des propriétés spécifiques à la classe.
ms.assetid: ea8ca4e4-9969-48fc-9b9f-5a5c8442006d
ms.tgt_platform: multiple
title: Propriétés système CIM pour les objets MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0425afecc399c3cd1399e8bf565908b1c7c5d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531710"
---
# <a name="cim-system-properties-for-mib-objects"></a><span data-ttu-id="8edd7-103">Propriétés système CIM pour les objets MIB</span><span class="sxs-lookup"><span data-stu-id="8edd7-103">CIM System Properties for MIB Objects</span></span>

<span data-ttu-id="8edd7-104">WMI définit un ensemble de propriétés système associées à toutes les classes et instances de classes en plus des propriétés spécifiques à la classe.</span><span class="sxs-lookup"><span data-stu-id="8edd7-104">WMI defines a set of system properties that are associated with all classes and instances of classes in addition to class-specific properties.</span></span>

> [!Note]  
> <span data-ttu-id="8edd7-105">Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="8edd7-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="8edd7-106">Le fournisseur SNMP utilise les propriétés système CIM suivantes lors du mappage des définitions d’objets MIB aux définitions de classe CIM.</span><span class="sxs-lookup"><span data-stu-id="8edd7-106">The SNMP Provider uses the following CIM system properties when mapping MIB object definitions to CIM class definitions.</span></span> <span data-ttu-id="8edd7-107">Les propriétés obligatoires doivent être présentes pour que le fournisseur SNMP résolve entièrement un objet de groupe.</span><span class="sxs-lookup"><span data-stu-id="8edd7-107">Mandatory properties must be present for the SNMP Provider to fully resolve a group object.</span></span> <span data-ttu-id="8edd7-108">L’impossibilité de définir une propriété obligatoire renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="8edd7-108">Failure to define a mandatory property returns an error.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8edd7-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="8edd7-109">Property</span></span></th>
<th><span data-ttu-id="8edd7-110">Description</span><span class="sxs-lookup"><span data-stu-id="8edd7-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8edd7-111"><strong>__CLASS</strong></span><span class="sxs-lookup"><span data-stu-id="8edd7-111"><strong>__CLASS</strong></span></span></td>
<td><span data-ttu-id="8edd7-112"><strong>chaîne</strong> Requise</span><span class="sxs-lookup"><span data-stu-id="8edd7-112"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="8edd7-113">Pour les instances, la classe à laquelle appartient l’objet.</span><span class="sxs-lookup"><span data-stu-id="8edd7-113">For instances, the class to which the object belongs.</span></span> <span data-ttu-id="8edd7-114">Pour les classes, il s’agit du nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="8edd7-114">For classes, this is the class name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8edd7-115"><strong>__DYNASTY</strong></span><span class="sxs-lookup"><span data-stu-id="8edd7-115"><strong>__DYNASTY</strong></span></span></td>
<td><span data-ttu-id="8edd7-116"><strong>chaîne</strong> Facultatif</span><span class="sxs-lookup"><span data-stu-id="8edd7-116"><strong>string</strong>Optional</span></span><br/> <span data-ttu-id="8edd7-117">Nom de la classe qui est la classe de base la plus fine pour l’objet actuel (pas sa classe parent immédiate).</span><span class="sxs-lookup"><span data-stu-id="8edd7-117">Name of the class that is the ultimate base class for the current object (not its immediate parent class).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8edd7-118"><strong>__GENUS</strong></span><span class="sxs-lookup"><span data-stu-id="8edd7-118"><strong>__GENUS</strong></span></span></td>
<td><span data-ttu-id="8edd7-119"><strong>UInt32</strong> Requise</span><span class="sxs-lookup"><span data-stu-id="8edd7-119"><strong>uint32</strong>Mandatory</span></span><br/> <span data-ttu-id="8edd7-120">Type d'objet.</span><span class="sxs-lookup"><span data-stu-id="8edd7-120">Type of object.</span></span> <span data-ttu-id="8edd7-121">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8edd7-121">Values are:</span></span><br/> <dl> <span data-ttu-id="8edd7-122">1 = classe</span><span class="sxs-lookup"><span data-stu-id="8edd7-122">1 = class</span></span><br />
<span data-ttu-id="8edd7-123">2 = instance</span><span class="sxs-lookup"><span data-stu-id="8edd7-123">2 = instance</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8edd7-124"><strong>__NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="8edd7-124"><strong>__NAMESPACE</strong></span></span></td>
<td><span data-ttu-id="8edd7-125"><strong>chaîne</strong> Requise</span><span class="sxs-lookup"><span data-stu-id="8edd7-125"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="8edd7-126">Espace de noms où se trouve l’objet.</span><span class="sxs-lookup"><span data-stu-id="8edd7-126">Namespace where the object is located.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8edd7-127"><strong>__PATH</strong></span><span class="sxs-lookup"><span data-stu-id="8edd7-127"><strong>__PATH</strong></span></span></td>
<td><span data-ttu-id="8edd7-128"><strong>chaîne</strong> Requise</span><span class="sxs-lookup"><span data-stu-id="8edd7-128"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="8edd7-129">Chemin d’accès absolu à l’objet.</span><span class="sxs-lookup"><span data-stu-id="8edd7-129">Absolute path to the object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8edd7-130"><strong>__PROPERTYCOUNT</strong></span><span class="sxs-lookup"><span data-stu-id="8edd7-130"><strong>__PROPERTYCOUNT</strong></span></span></td>
<td><span data-ttu-id="8edd7-131"><strong>UInt32</strong> Requise</span><span class="sxs-lookup"><span data-stu-id="8edd7-131"><strong>uint32</strong>Mandatory</span></span><br/> <span data-ttu-id="8edd7-132">Nombre de propriétés non-système définies pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="8edd7-132">Number of non-system properties defined for the object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8edd7-133"><strong>__RELPATH</strong></span><span class="sxs-lookup"><span data-stu-id="8edd7-133"><strong>__RELPATH</strong></span></span></td>
<td><span data-ttu-id="8edd7-134"><strong>chaîne</strong> Requise</span><span class="sxs-lookup"><span data-stu-id="8edd7-134"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="8edd7-135">Chemin d’accès relatif à l’objet.</span><span class="sxs-lookup"><span data-stu-id="8edd7-135">Relative path to the object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8edd7-136"><strong>__SERVER</strong></span><span class="sxs-lookup"><span data-stu-id="8edd7-136"><strong>__SERVER</strong></span></span></td>
<td><span data-ttu-id="8edd7-137"><strong>chaîne</strong> Requise</span><span class="sxs-lookup"><span data-stu-id="8edd7-137"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="8edd7-138">Serveur qui fournit l’objet.</span><span class="sxs-lookup"><span data-stu-id="8edd7-138">Server supplying the object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8edd7-139"><strong>__SUPERCLASS</strong></span><span class="sxs-lookup"><span data-stu-id="8edd7-139"><strong>__SUPERCLASS</strong></span></span></td>
<td><span data-ttu-id="8edd7-140"><strong>chaîne</strong> Facultatif</span><span class="sxs-lookup"><span data-stu-id="8edd7-140"><strong>string</strong>Optional</span></span><br/> <span data-ttu-id="8edd7-141">Classe parente immédiate de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8edd7-141">Immediate parent class of the object.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




