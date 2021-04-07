---
title: Recherche d’objets par nom
description: La plupart des objets dans Active Directory Domain Services utilisent la propriété CN comme attribut de nom.
ms.assetid: c5df7403-23bc-440e-8cd6-215ab8037aed
ms.tgt_platform: multiple
keywords:
- Active Directory, utilisation, recherche, par nom
- objet AD, recherche par nom
- Recherche d’objets par nom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914faa443402a1d20698aabaf0bf4a112279a322
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671278"
---
# <a name="finding-objects-by-name"></a><span data-ttu-id="f177e-106">Recherche d’objets par nom</span><span class="sxs-lookup"><span data-stu-id="f177e-106">Finding Objects by Name</span></span>

<span data-ttu-id="f177e-107">La plupart des objets dans Active Directory Domain Services utilisent la propriété **CN** comme attribut de nom.</span><span class="sxs-lookup"><span data-stu-id="f177e-107">Most objects in Active Directory Domain Services use the **cn** property as their naming attribute.</span></span> <span data-ttu-id="f177e-108">Toutefois, certains objets utilisent un attribut de nom autre que **CN**.</span><span class="sxs-lookup"><span data-stu-id="f177e-108">Some objects, however, use a naming attribute other than **cn**.</span></span> <span data-ttu-id="f177e-109">Par exemple, un contrôleur de domaine utilise la propriété **domainDNS** pour l’attribut Naming et une unité d’organisation utilise la propriété **OrganizationalUnit** pour l’attribut Naming.</span><span class="sxs-lookup"><span data-stu-id="f177e-109">For example, a domain controller uses the **domainDNS** property for the naming attribute and an organizational unit uses the **organizationalUnit** property for the naming attribute.</span></span> <span data-ttu-id="f177e-110">Pour éviter d’avoir à utiliser un attribut de nom différent pour les différents types d’objets, la propriété **Name** , qui contient le nom unique relatif de l’objet, doit être utilisée pour rechercher des objets par nom.</span><span class="sxs-lookup"><span data-stu-id="f177e-110">To avoid having to use a different naming attribute for different object types, the **name** property, which contains the relative distinguished name of the object, should be used to search for objects by name.</span></span>

## <a name="examples"></a><span data-ttu-id="f177e-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="f177e-111">Examples</span></span>

<span data-ttu-id="f177e-112">Les exemples de code suivants illustrent des chaînes de requête différentes qui peuvent être utilisées pour rechercher des objets par nom.</span><span class="sxs-lookup"><span data-stu-id="f177e-112">The following code examples show different query strings that can be used to find objects by name.</span></span>

<span data-ttu-id="f177e-113">La chaîne de requête suivante recherche tous les objets dont le nom commence par « Jeff ».</span><span class="sxs-lookup"><span data-stu-id="f177e-113">The following query string finds all objects with a name that begins with "Jeff".</span></span>


```C++
(name=Jeff*)
```



<span data-ttu-id="f177e-114">La chaîne de requête suivante recherche tous les objets ordinateurs dont le nom commence par « leaseed » ou « Corp ».</span><span class="sxs-lookup"><span data-stu-id="f177e-114">The following query string finds all computer objects with a name that begins with "leased" or "corp".</span></span>


```C++
(&(objectCategory=computer)(|(name=leased*)(name=corp*)))
```



<span data-ttu-id="f177e-115">La chaîne de requête suivante recherche tous les utilisateurs et dont le nom commence par « Karen » ou « Jeff ».</span><span class="sxs-lookup"><span data-stu-id="f177e-115">The following query string finds all users and with a name that begins with "Karen" or "Jeff".</span></span>


```C++
(&(&(objectClass=user)(objectCategory=person))(|(name=Karen*)(name=Jeff*)))
```



 

 




