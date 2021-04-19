---
title: Propriété Name
description: La propriété Name est une chaîne utilisée par les clients pour identifier, Rechercher ou annoncer un objet pour l’utilisateur. Tous les objets prennent en charge la propriété Name.
ms.assetid: 7533955a-9538-4ead-a6ca-f61dd1b4d5c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e93d8b90190f81179d681600f4b1bfacf4665e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512669"
---
# <a name="name-property"></a>Propriété Name

La propriété **Name** est une chaîne utilisée par les clients pour identifier, Rechercher ou annoncer un objet pour l’utilisateur. Tous les objets prennent en charge la propriété **Name** .

Par exemple, le texte d’un contrôle bouton est son nom, tandis que le nom d’une zone de liste ou d’un contrôle d’édition est le texte statique qui précède immédiatement le contrôle dans l’ordre de tabulation. Même les objets graphiques qui n’affichent pas de nom fournissent du texte lorsqu’ils sont interrogés pour la propriété **Name** .

La propriété **Name** est récupérée en appelant [**IAccessible :: \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname).

## <a name="selecting-names"></a>Sélection de noms

Le nom d’un objet doit être intuitif afin que les utilisateurs comprennent la signification ou l’objectif de l’objet. En outre, la propriété **Name** doit être unique par rapport à tous les objets frères dans le parent.

La navigation dans les tables présente des problèmes particulièrement difficiles pour certains utilisateurs. Par conséquent, les développeurs de serveurs doivent faire en sorte que les noms des cellules de tableau soient aussi descriptifs que possible. Par exemple, vous pouvez créer un nom de cellule en combinant les noms de la ligne et de la colonne qu’il occupe, par exemple « a1 ». Toutefois, il est généralement préférable d’utiliser des noms plus descriptifs, tels que « Nancy, février » où « Nancy » est la ligne actuelle et « février » est la colonne actuelle.

## <a name="delegating-requests"></a>Délégation de requêtes

Si un objet n’a pas accès à sa propriété **Name** , il délègue les demandes à son parent, s’identifiant lui-même par son ID enfant. Par exemple, si un client appelle la propriété **Name** d’un contrôle d’édition, le contrôle d’édition délègue la requête à son parent, qui retourne la valeur du contrôle de texte statique qui étiquette le contrôle d’édition.

 

 




