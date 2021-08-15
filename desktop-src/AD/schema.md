---
title: Schéma (AD DS)
description: Active Directory schéma est implémenté comme un ensemble d’instances de classes d’objets stockées dans le répertoire.
ms.assetid: 77c297ca-0dfc-4545-9832-4202e066822b
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a12d18012abf3e2cf9fc9fdd6831be34d62c88279ad78a0e351534d1899e062
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183968"
---
# <a name="schema-ad-ds"></a>Schéma (AD DS)

Active Directory schéma est implémenté comme un ensemble d’instances de classes d’objets stockées dans le répertoire. Cela est très différent de nombreux répertoires qui ont un schéma, mais le stocke sous la forme d’un fichier texte lu au démarrage. Le stockage du schéma dans l’annuaire présente de nombreux avantages. Par exemple, les applications utilisateur peuvent la lire pour découvrir les objets et les propriétés disponibles.

Active Directory schéma peut être mis à jour de manière dynamique. Autrement dit, une application peut étendre le schéma avec de nouveaux attributs et classes et utiliser les extensions immédiatement. Les mises à jour de schéma sont effectuées en créant ou en modifiant les objets de schéma stockés dans l’annuaire. Comme chaque objet dans Active Directory, les listes de contrôle d’accès (ACL) protègent les objets de schéma, de sorte que les utilisateurs autorisés peuvent modifier le schéma.

Pour plus d’informations, consultez [Active Directory le schéma](active-directory-schema.md).

 

 




