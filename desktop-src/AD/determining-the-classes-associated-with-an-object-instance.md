---
title: Détermination des classes associées à une instance d’objet
description: Chaque objet de Active Directory Domain Services a deux attributs dont les valeurs identifient la hiérarchie des classes d’objets dont l’objet est une instance.
ms.assetid: bb46f165-8c6e-4af1-b387-e0e30a4c6226
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67bc3fe900170e4a856d996f7e373918f242df2e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462051"
---
# <a name="determining-the-classes-associated-with-an-object-instance"></a><span data-ttu-id="018f1-103">Détermination des classes associées à une instance d’objet</span><span class="sxs-lookup"><span data-stu-id="018f1-103">Determining the Classes Associated With an Object Instance</span></span>

<span data-ttu-id="018f1-104">Chaque objet de Active Directory Domain Services a deux attributs dont les valeurs identifient la hiérarchie des classes d’objets dont l’objet est une instance.</span><span class="sxs-lookup"><span data-stu-id="018f1-104">Every object in Active Directory Domain Services has two attributes whose values identify the hierarchy of object classes of which the object is an instance.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="018f1-105">Attribut</span><span class="sxs-lookup"><span data-stu-id="018f1-105">Attribute</span></span></th>
<th><span data-ttu-id="018f1-106">Description</span><span class="sxs-lookup"><span data-stu-id="018f1-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="018f1-107"><strong>structuralObjectClass</strong></span><span class="sxs-lookup"><span data-stu-id="018f1-107"><strong>structuralObjectClass</strong></span></span></td>
<td><span data-ttu-id="018f1-108">Identifie les classes structurelles et abstraites dont l’objet est une instance.</span><span class="sxs-lookup"><span data-stu-id="018f1-108">Identifies the structural and abstract classes of which the object is an instance.</span></span> <span data-ttu-id="018f1-109">Par exemple, les valeurs d’un objet utilisateur peuvent être :</span><span class="sxs-lookup"><span data-stu-id="018f1-109">For example, the values for a user object can be:</span></span>
<ul>
<li><span data-ttu-id="018f1-110"><strong>top</strong></span><span class="sxs-lookup"><span data-stu-id="018f1-110"><strong>top</strong></span></span></li>
<li><span data-ttu-id="018f1-111"><strong>person</strong></span><span class="sxs-lookup"><span data-stu-id="018f1-111"><strong>person</strong></span></span></li>
<li><span data-ttu-id="018f1-112"><strong>organizationalPerson</strong></span><span class="sxs-lookup"><span data-stu-id="018f1-112"><strong>organizationalPerson</strong></span></span></li>
<li><span data-ttu-id="018f1-113"><strong>user</strong></span><span class="sxs-lookup"><span data-stu-id="018f1-113"><strong>user</strong></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="018f1-114"><strong>objectClass</strong></span><span class="sxs-lookup"><span data-stu-id="018f1-114"><strong>objectClass</strong></span></span></td>
<td><span data-ttu-id="018f1-115">Identifie les classes incluses dans <strong>structuralObjectClass</strong>, ainsi que toutes les classes auxiliaires qui sont attachées dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="018f1-115">Identifies the classes included in <strong>structuralObjectClass</strong>, plus any auxiliary classes that are dynamically attached.</span></span> <span data-ttu-id="018f1-116">Par exemple, si une &quot; &quot; classe auxiliaire de véhicule est attachée à un objet utilisateur, les valeurs peuvent être :</span><span class="sxs-lookup"><span data-stu-id="018f1-116">For example, if a &quot;vehicle&quot; auxiliary class is attached to a user object, the values can be:</span></span>
<ul>
<li><span data-ttu-id="018f1-117"><strong>top</strong></span><span class="sxs-lookup"><span data-stu-id="018f1-117"><strong>top</strong></span></span></li>
<li><span data-ttu-id="018f1-118"><strong>véhicule</strong></span><span class="sxs-lookup"><span data-stu-id="018f1-118"><strong>vehicle</strong></span></span></li>
<li><span data-ttu-id="018f1-119"><strong>person</strong></span><span class="sxs-lookup"><span data-stu-id="018f1-119"><strong>person</strong></span></span></li>
<li><span data-ttu-id="018f1-120"><strong>organizationalPerson</strong></span><span class="sxs-lookup"><span data-stu-id="018f1-120"><strong>organizationalPerson</strong></span></span></li>
<li><span data-ttu-id="018f1-121"><strong>user</strong></span><span class="sxs-lookup"><span data-stu-id="018f1-121"><strong>user</strong></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="018f1-122">N’oubliez pas qu’aucun de ces attributs n’inclut des classes auxiliaires liées statiquement avec les classes d’objets dont l’objet est une instance.</span><span class="sxs-lookup"><span data-stu-id="018f1-122">Be aware that neither of these attributes include auxiliary classes that are statically linked with the object classes of which the object is an instance.</span></span> <span data-ttu-id="018f1-123">Par exemple, la classe auxiliaire **securityPrincipal** est liée de manière statique à la classe **User** , car elle est incluse dans les valeurs **systemAuxiliaryClass** de l’objet **classSchema** de l’utilisateur. elle n’est pas incluse dans les attributs **objectClass** ou **structuralObjectClass** des instances de la classe User.</span><span class="sxs-lookup"><span data-stu-id="018f1-123">For example, the **securityPrincipal** auxiliary class is statically linked with the **user** class because it is included in the **systemAuxiliaryClass** values of the user **classSchema** object; it is not included in either the **objectClass** or **structuralObjectClass** attributes of instances of the user class.</span></span>

 

 




