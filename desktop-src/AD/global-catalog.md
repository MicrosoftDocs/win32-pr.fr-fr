---
title: Catalogue global
description: Un domaine exécuté par Active Directory Domain Services peut être constitué de plusieurs partitions ou contextes d’attribution de noms.
ms.assetid: eac02c1f-0c37-4eee-822d-07913ea8775a
ms.tgt_platform: multiple
keywords:
- Active Directory de catalogue global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81abf04ab3e4d95819f91b5db8753a265e49ca79b2f405a32665dc46a8f2db5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189113"
---
# <a name="global-catalog"></a>Catalogue global

Un domaine exécuté par Active Directory Domain Services peut être constitué de plusieurs partitions ou contextes d’attribution de noms. Le nom unique (DN) d’un objet contient suffisamment d’informations pour localiser un réplica de la partition qui contient l’objet. Cependant, de nombreuses fois, l’utilisateur ou l’application ne connaît pas le DN de l’objet cible ou la partition qui peut contenir l’objet. Le [*catalogue global (GC)*](/previous-versions/windows/desktop/legacy/ms681905(v=vs.85)) permet aux utilisateurs et aux applications de rechercher des objets dans une arborescence de domaine Active Directory, en fonction d’un ou plusieurs attributs de l’objet cible.

Le catalogue global contient un réplica partiel de chaque contexte de nommage dans le répertoire. Il contient également les contextes de nommage de schéma et de configuration. Cela signifie que le catalogue global contient un réplica de chaque objet dans l’annuaire, mais avec seulement un petit nombre de leurs attributs. Les attributs du GC sont ceux qui sont utilisés le plus fréquemment dans les opérations de recherche (comme le prénom et le nom d’un utilisateur, ainsi que les noms de connexion) et ceux qui sont requis pour localiser un réplica complet de l’objet. Le catalogue global permet aux utilisateurs de trouver rapidement des objets intéressants sans savoir quel domaine les détient et sans avoir besoin d’un espace de noms étendu contigu dans l’entreprise.

Le catalogue global est généré automatiquement par le système de réplication Active Directory Domain Services. La topologie de réplication pour le catalogue global est générée automatiquement. Les propriétés répliquées dans le catalogue global incluent un ensemble de base défini par Microsoft. Les administrateurs peuvent spécifier des propriétés supplémentaires pour répondre aux besoins de leur installation.

 

 