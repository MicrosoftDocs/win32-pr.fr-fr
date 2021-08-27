---
description: Un objet se compose d’un en-tête standard et d’attributs spécifiques à l’objet. étant donné que tous les objets ont la même structure, il existe un seul gestionnaire d’objets dans Windows qui gère tous les objets.
ms.assetid: 104113f3-bfd1-4ff7-b92f-2f753c0f5185
title: Gestionnaire d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b87b239d685d53b29243212e06ba2fd5af20e1249794355ed2169278c7f46c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885347"
---
# <a name="object-manager"></a>Gestionnaire d’objets

Un objet se compose d’un en-tête standard et d’attributs spécifiques à l’objet. étant donné que tous les objets ont la même structure, il existe un seul gestionnaire d’objets dans Windows qui gère tous les objets.

L’en-tête d’objet comprend des éléments tels que le nom de l’objet, afin que d’autres processus puissent faire référence à l’objet par son nom et un descripteur de sécurité, afin que le gestionnaire d’objets puisse contrôler les processus qui accèdent à la ressource système.

Les tâches exécutées par le gestionnaire d’objets sont les suivantes :

-   Création d'objets
-   Vérification qu’un processus a le droit d’utiliser l’objet
-   Création de handles d’objet et retour à l’appelant
-   Gestion des quotas de ressources
-   Création de descripteurs dupliqués
-   Fermeture des handles aux objets

 

 



