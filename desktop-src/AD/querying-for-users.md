---
title: Interrogation des utilisateurs
description: Pour rechercher un utilisateur, la requête doit contenir l’expression de recherche \ 0034 ;( (utilisateur objectClass) (objectCategory person)) \ 0034 ;.
ms.assetid: a9f12de4-e1e2-41bb-b2cc-ff9c9fa1c39a
ms.tgt_platform: multiple
keywords:
- utilisateurs Active Directory, interrogation pour les utilisateurs
- Active Directory, utiliser, utilisateurs, interroger des utilisateurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ae6939cef858c3dfc108611a1b0e7ab0367c302a091ca436c9c69b2fb5277b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025317"
---
# <a name="querying-for-users"></a>Interrogation des utilisateurs

Pour rechercher un utilisateur, la requête doit contenir l’expression de recherche « (& (objectClass = user) (objectCategory = person)) ».

Étant donné que la classe Computer est une sous-classe de l’utilisateur, une requête contenant uniquement (objectClass = user) retourne des objets User et Computer. En outre, la catégorie d’objet de l’objet utilisateur est personne (pas utilisateur); par conséquent, l’expression (objectCategory = user) ne retourne aucun utilisateur. Si vous utilisez l’expression (objectCategory = person), la requête retourne les objets User et contact.

Les utilisateurs peuvent être placés dans n’importe quel conteneur ou unité d’organisation d’un domaine, ainsi que la racine du domaine. Cela signifie que les utilisateurs peuvent se trouver à de nombreux emplacements dans la hiérarchie de répertoires. Vous pouvez effectuer une recherche détaillée « (objectCategory = user) » pour rechercher tous les utilisateurs dans un conteneur, une unité d’organisation, un domaine, une arborescence de domaine ou une forêt, en fonction de l’objet auquel le pointeur [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) que vous utilisez est lié.

 

 