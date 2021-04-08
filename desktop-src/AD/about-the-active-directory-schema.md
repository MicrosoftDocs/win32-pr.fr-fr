---
title: À propos du schéma Active Directory
description: Chaque objet de Active Directory Domain Services est une instance d’une classe d’objet définie dans le schéma de Active Directory.
ms.assetid: 8fc9cd2d-8fed-4fda-918c-79b01f9a19bb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f55513b359a7ef293b005d93a20ac43f470d515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839090"
---
# <a name="about-the-active-directory-schema"></a><span data-ttu-id="64a50-103">À propos du schéma Active Directory</span><span class="sxs-lookup"><span data-stu-id="64a50-103">About the Active Directory Schema</span></span>

<span data-ttu-id="64a50-104">Chaque objet de Active Directory Domain Services est une instance d’une classe d’objet définie dans le schéma de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="64a50-104">Every object in Active Directory Domain Services is an instance of an object class defined in the Active Directory schema.</span></span> <span data-ttu-id="64a50-105">Une classe d’objet représente une catégorie d’objets, tels qu’utilisateurs, imprimantes ou programmes d’application, qui partagent un ensemble de caractéristiques communes.</span><span class="sxs-lookup"><span data-stu-id="64a50-105">An object class represents a category of objects, such as users, printers, or application programs, that share a set of common characteristics.</span></span> <span data-ttu-id="64a50-106">La définition de chaque classe d’objet contient une liste des attributs qui peuvent être utilisés pour décrire les instances de la classe.</span><span class="sxs-lookup"><span data-stu-id="64a50-106">The definition for each object class contains a list of the attributes that can be used to describe instances of the class.</span></span> <span data-ttu-id="64a50-107">Par exemple, la classe Utilisateur a des attributs tels que **givenName**, **surname** et **streetAddress**.</span><span class="sxs-lookup"><span data-stu-id="64a50-107">For example, the User class has attributes such as **givenName**, **surname**, and **streetAddress**.</span></span> <span data-ttu-id="64a50-108">La liste d’attributs pour une classe est divisée en celles qu’un objet de cette classe doit contenir, ainsi que les attributs supplémentaires qu’un objet peut contenir.</span><span class="sxs-lookup"><span data-stu-id="64a50-108">The list of attributes for a class is divided into those that an object of that class must contain, and additional attributes that an object may contain.</span></span> <span data-ttu-id="64a50-109">Le répertoire est organisé dans une hiérarchie ; la définition de chaque classe répertorie également les classes dont les objets peuvent être des parents d’objets d’une classe donnée, ce qui contrôle la forme de la hiérarchie de répertoires.</span><span class="sxs-lookup"><span data-stu-id="64a50-109">The directory is arranged in a hierarchy; the definition of each class also lists the classes whose objects can be parents of objects of a given class—this controls the shape of the directory hierarchy.</span></span>

<span data-ttu-id="64a50-110">Le schéma définit également de manière formelle chaque attribut.</span><span class="sxs-lookup"><span data-stu-id="64a50-110">The schema also formally defines each attribute.</span></span> <span data-ttu-id="64a50-111">La définition de chaque attribut comprend des identificateurs uniques pour l’attribut, la syntaxe de l’attribut (autrement dit, le type de données pour les valeurs de l’attribut), des limites de plage facultatives pour les valeurs d’attribut, si l’attribut peut avoir une seule valeur ou plusieurs valeurs, et si l’attribut est indexé.</span><span class="sxs-lookup"><span data-stu-id="64a50-111">The definition for each attribute includes unique identifiers for the attribute, the syntax for the attribute (that is, the data type for the attribute's values), optional range limits for the attribute values, whether the attribute can have only one value or multiple values, and whether the attribute is indexed.</span></span> <span data-ttu-id="64a50-112">Le schéma d’annuaire définit chaque attribut exactement une fois : les définitions de classe d’objet contiennent des références aux attributs définis dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="64a50-112">The directory schema defines each attribute exactly once—object class definitions contain references to the attributes defined in the schema.</span></span> <span data-ttu-id="64a50-113">Par exemple, l’attribut « Description » n’est défini qu’une seule fois et est référencé par de nombreuses classes d’objets.</span><span class="sxs-lookup"><span data-stu-id="64a50-113">For example, the "description" attribute is defined only once and is referenced by many object classes.</span></span> <span data-ttu-id="64a50-114">Cela diffère d’un schéma de base de données relationnelle, où les « attributs » (colonnes) sont définis séparément pour chaque table.</span><span class="sxs-lookup"><span data-stu-id="64a50-114">This is different than a relational database schema, where the "attributes" (columns) are separately defined for each table.</span></span>

 

 




