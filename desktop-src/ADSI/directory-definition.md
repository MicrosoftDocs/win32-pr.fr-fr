---
title: Définition de répertoire
description: L’exemple de composant de fournisseur utilise une conception d’annuaire relativement simple pour clarifier la relation entre les composants et pour indiquer les conditions minimales requises pour être un fournisseur ADSI.
ms.assetid: d8dcd255-4a17-4c80-a749-61c1af605dba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8a46ee47bfa280fb9cffce32480fdad3164a648eee59a0c0b2740834b1f21cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691946"
---
# <a name="directory-definition"></a>Définition de répertoire

L’exemple de composant de fournisseur utilise une conception d’annuaire relativement simple pour clarifier la relation entre les composants et pour indiquer les conditions minimales requises pour être un fournisseur ADSI.

Le « répertoire » du composant de fournisseur d’exemple se compose de deux nœuds racine : « Seattle » et « Toronto ». Seattle contient deux autres sous-niveaux, « Bellevue » et « Redmond ». Chacune de ces entrées contient plusieurs comptes d’utilisateur. L’entrée « Toronto » n’a pas de sous-niveaux supplémentaires, mais elle contient directement plusieurs comptes d’utilisateur. L’illustration suivante montre ces deux nœuds racines connectés à un réseau.

![définition de répertoire](images/dssmdo.png)

En termes hiérarchiques, le nœud d’espace de noms contient « Seattle » et « Toronto ». « Seattle » contient « Bellevue » et « Redmond ». « Bellevue » et « Redmond » contiennent chacun un ensemble de comptes d’utilisateur. « Toronto » contient directement les comptes d’utilisateur sans nœuds organisationnels intermédiaires.

Le composant de fournisseur d’exemple représente cette structure avec uniquement deux types d’objets Active Directory : un objet conteneur et un objet feuille. « Seattle », « Toronto », « Bellevue » et « Redmond » sont des objets conteneurs et chaque compte d’utilisateur est un objet feuille.

L’exemple de composant fournisseur crée une classe de schéma appelée « unité d’organisation » pour un type d’objet conteneur et une classe de schéma appelée « utilisateur » pour un compte d’utilisateur.

Les propriétés de chaque classe de schéma, leurs méthodes et les règles qui régissent les relations d’imbrication pour ces objets sont toutes définies dans la [gestion des schémas](schema-management.md).

 

 




