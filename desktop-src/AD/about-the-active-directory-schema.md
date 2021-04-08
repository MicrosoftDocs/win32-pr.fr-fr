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
# <a name="about-the-active-directory-schema"></a>À propos du schéma Active Directory

Chaque objet de Active Directory Domain Services est une instance d’une classe d’objet définie dans le schéma de Active Directory. Une classe d’objet représente une catégorie d’objets, tels qu’utilisateurs, imprimantes ou programmes d’application, qui partagent un ensemble de caractéristiques communes. La définition de chaque classe d’objet contient une liste des attributs qui peuvent être utilisés pour décrire les instances de la classe. Par exemple, la classe Utilisateur a des attributs tels que **givenName**, **surname** et **streetAddress**. La liste d’attributs pour une classe est divisée en celles qu’un objet de cette classe doit contenir, ainsi que les attributs supplémentaires qu’un objet peut contenir. Le répertoire est organisé dans une hiérarchie ; la définition de chaque classe répertorie également les classes dont les objets peuvent être des parents d’objets d’une classe donnée, ce qui contrôle la forme de la hiérarchie de répertoires.

Le schéma définit également de manière formelle chaque attribut. La définition de chaque attribut comprend des identificateurs uniques pour l’attribut, la syntaxe de l’attribut (autrement dit, le type de données pour les valeurs de l’attribut), des limites de plage facultatives pour les valeurs d’attribut, si l’attribut peut avoir une seule valeur ou plusieurs valeurs, et si l’attribut est indexé. Le schéma d’annuaire définit chaque attribut exactement une fois : les définitions de classe d’objet contiennent des références aux attributs définis dans le schéma. Par exemple, l’attribut « Description » n’est défini qu’une seule fois et est référencé par de nombreuses classes d’objets. Cela diffère d’un schéma de base de données relationnelle, où les « attributs » (colonnes) sont définis séparément pour chaque table.

 

 




