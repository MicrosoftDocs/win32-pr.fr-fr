---
title: Objets dynamiques
description: dans Windows Server 2003 et versions ultérieures de Windows, Active Directory Domain Services assurer la prise en charge du stockage des entrées dynamiques dans l’annuaire.
ms.assetid: ac5779b6-f226-414c-92a9-091719b1515b
ms.tgt_platform: multiple
keywords:
- objets dynamiques AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e74660728179365f6585bce2462cd22f2508e68318eb84312d039a431330329b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191717"
---
# <a name="dynamic-objects"></a>Objets dynamiques

dans Windows Server 2003 et versions ultérieures de Windows, Active Directory Domain Services assurer la prise en charge du stockage des entrées dynamiques dans l’annuaire. Une entrée dynamique est un objet du répertoire qui a une valeur de durée de vie (TTL, Time-to-Live) associée. La durée de vie d’une entrée est définie lors de la création de l’entrée. La durée de vie est décrémentée automatiquement, et lorsqu’elle expire, l’entrée dynamique disparaît. Le client peut faire en sorte qu’une entrée dynamique reste plus longue que sa durée de vie restante en actualisant (en modifiant) sa valeur TTL. Les clients qui stockent des données dynamiques dans l’annuaire doivent actualiser régulièrement ces données pour empêcher leur disparition.

De nombreux services et applications qui utilisent le protocole LDAP pour stocker et accéder à des données relativement statiques et globalement intéressantes à partir d’un serveur de Active Directory préfèrent également continuer à utiliser l’accès LDAP pour leurs besoins en données dynamiques. En outre, pour certaines applications, il peut être souhaitable de décharger la tâche des objets de garbage collection dans le DS qui ont une durée de vie limitée au service d’annuaire. Les partitions de l’annuaire d’applications (avec la possibilité d’un positionnement contrôlé des réplicas) et l’authentification TTLs par objet permettent d’héberger des données dynamiques dans Active Directory Domain Services, ce qui permet d’y accéder via LDAP.

Une nouvelle classe d’objet auxiliaire appelée **DynamicObject** avec OID = 1.3.6.1.4.1.1466.101.119.2 sera définie dans le schéma AD de base à utiliser par les entrées dynamiques. Cette classe auxiliaire contient l’attribut appelé **entryTTL** avec OID = 1.3.6.1.4.1.1466.101.119.3 en tant qu’attribut système-peut contenir. La valeur de cet attribut est la « durée en secondes » pendant laquelle l’entrée de répertoire correspondante continuera d’exister avant d’apparaître dans le répertoire. Si le client ne fournit pas de valeur pour cet attribut explicitement lors de la création de l’objet, le DS fournit une valeur par défaut spécifiée ultérieurement.

Une nouvelle opération LDAP étendue avec OID = 1.3.6.1.4.1.1466.101.119.1 pour l’actualisation du client d’une entrée dynamique dans l’annuaire sera définie et publiée dans l’attribut **supportedExtension** de l’objet DSE racine.

Dans l’implémentation réelle, **entryTTL** est un attribut construit. L’heure d’expiration réelle de l’objet est stockée sous la forme d’une heure absolue lorsque l’objet peut être détruit dans un attribut système uniquement appelé **ms-DS-Entry-Time-to-Live**.

Tous les objets dynamiques présentent les limitations suivantes :

-   Un objet dynamique supprimé en raison de sa durée de vie expirée ne laisse pas de désactivation tombstone.
-   tous les contrôleurs de contrôleur contenant des réplicas d’objets dynamiques doivent s’exécuter sur Windows Server 2003.
-   Les entrées dynamiques avec des valeurs TTL sont prises en charge dans toutes les partitions, à l’exception de la partition de configuration et de schéma.
-   Active Directory Domain Services ne publiez pas l’attribut facultatif **dynamicSubtrees** , comme décrit dans la RFC 2589, dans l’objet DSE racine.
-   Les entrées dynamiques sont gérées de la même façon que les entrées non dynamiques lors du traitement des opérations de recherche, de comparaison, d’ajout, de suppression, de modification et de modifyDN.
-   Il n’existe aucun moyen de modifier une entrée statique en entrée dynamique, et vice-versa.
-   Une entrée non dynamique ne peut pas être ajoutée subordonnée à une entrée dynamique.

 

 




