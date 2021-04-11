---
title: objectCategory et objectClass
description: Les attributs objectCategory et objectClass peuvent faire référence à une classe de schéma donnée d’un objet d’annuaire.
ms.assetid: 66dadedb-61e4-4184-9b87-0fff036a94d9
ms.tgt_platform: multiple
keywords:
- interface ADSI de objectCategory et objectClass
- attributs ASI, recherche sur les attributs objectCategory et objectClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbbb8c5fe737b7c81193a75cdae6b772db64e69c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028557"
---
# <a name="objectcategory-vs-objectclass"></a><span data-ttu-id="6363a-105">objectCategory et objectClass</span><span class="sxs-lookup"><span data-stu-id="6363a-105">objectCategory vs. objectClass</span></span>

<span data-ttu-id="6363a-106">Les attributs **objectCategory** et **objectClass** peuvent faire référence à une classe de schéma donnée d’un objet d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="6363a-106">Both the **objectCategory** and **objectClass** attributes can refer to a given schema class of a directory object.</span></span> <span data-ttu-id="6363a-107">Toutefois, il existe une distinction importante dans la sémantique entre les deux.</span><span class="sxs-lookup"><span data-stu-id="6363a-107">However, there is an important distinction in semantics between the two.</span></span> <span data-ttu-id="6363a-108">« objectClass = Joy » fait référence à des objets de répertoire dans lesquels « Joy » représente toute classe dans la hiérarchie de classes d’objets.</span><span class="sxs-lookup"><span data-stu-id="6363a-108">"objectClass=joy" refers to such directory objects in which "joy" represents any class in the object class hierarchy.</span></span> <span data-ttu-id="6363a-109">« objectCategory = Joy », en revanche, fait référence aux objets d’annuaire dans lesquels « Joy » identifie une classe spécifique dans la hiérarchie de classes d’objets.</span><span class="sxs-lookup"><span data-stu-id="6363a-109">"objectCategory=joy", on the other hand, refers to those directory objects in which "joy" identifies a specific class in the object class hierarchy.</span></span>

<span data-ttu-id="6363a-110">**objectClass** peut prendre plusieurs valeurs, alors que **objectCategory** accepte une seule valeur.</span><span class="sxs-lookup"><span data-stu-id="6363a-110">**objectClass** can take multiple values whereas **objectCategory** takes a single value.</span></span> <span data-ttu-id="6363a-111">Pour cette raison, **objectCategory** est mieux adapté à la correspondance de type d’objets dans une recherche de répertoire.</span><span class="sxs-lookup"><span data-stu-id="6363a-111">Because of this, **objectCategory** is better suited for type matching of objects in a directory search.</span></span> <span data-ttu-id="6363a-112">ADSI utilise ce critère comme critère de correspondance par défaut.</span><span class="sxs-lookup"><span data-stu-id="6363a-112">ADSI uses this as the default matching criterion.</span></span> <span data-ttu-id="6363a-113">Les recherches utilisant un **objectClass** ne sont pas évolutives pour les bases de données volumineuses.</span><span class="sxs-lookup"><span data-stu-id="6363a-113">Searches using one **objectClass** are not scalable to large databases.</span></span> <span data-ttu-id="6363a-114">ADSI prend en charge les syntaxes « (objectCategory = SomeDN) » et « (objectCategory = LDAP \_ Display \_ name \_ of \_ Class) ».</span><span class="sxs-lookup"><span data-stu-id="6363a-114">ADSI supports "(objectCategory=SomeDN)" and "(objectCategory=Ldap\_Display\_Name\_of\_Class)" syntaxes.</span></span>

<span data-ttu-id="6363a-115">La seule exception à cela est que le filtre de recherche LDAP « (objectClass = \* ) » ne spécifie pas de recherche sur la classe d’objet, mais teste simplement la présence des objets.</span><span class="sxs-lookup"><span data-stu-id="6363a-115">The exception to all of this is that the LDAP search filter "(objectClass=\*)" does not specify a search on object class, but merely tests for the presence of the objects.</span></span>

 

 




