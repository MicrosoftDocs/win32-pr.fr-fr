---
description: Moniteur réseau ou votre DLL d’analyseur peut mettre en forme les données affichées dans le volet d’informations de l’interface utilisateur Moniteur réseau.
ms.assetid: 60ab9253-ec0f-4c97-a475-ce2a74d469c4
title: Mise en forme des données affichées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017946dab9db443cf7083109dd75ccee1f6d278a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525144"
---
# <a name="formatting-displayed-data"></a>Mise en forme des données affichées

Moniteur réseau ou votre DLL d’analyseur peut mettre en forme les données affichées dans le volet d’informations de l’interface utilisateur Moniteur réseau.

Moniteur réseau fournit un formateur générique qui fournit les services de base nécessaires pour afficher la plupart des types de données qui existent dans un protocole. Toutefois, le formateur générique ne prend pas en charge tous les types de données. Par exemple, le formateur générique ne prend pas en charge les éléments suivants :

-   Plusieurs types d’adresses.
-   Noms conviviaux pour la source et la destination.
-   Identificateurs d’objets.
-   Types de données entiers volumineux.
-   Types de données entiers de longueur variable.

L’exemple suivant identifie deux chaînes mises en forme pour la propriété ID de privilège.

-   La première ligne de code illustre la sortie du formateur générique. La sortie est basée sur le type de données.
-   La deuxième ligne de code illustre la sortie d’un formateur personnalisé avec une chaîne de données de propriété.

``` syntax
Privilege ID (PID) = 0x0029
Privilege ID   (PID) = 0x0029   The Process has privileges
```

> [!Note]  
> Dans la mesure du possible, utilisez le formateur générique pour afficher vos données, car il vous permet de contrôler la taille de votre DLL d’analyseur et fournit de meilleures fonctionnalités multiplateforme pour votre DLL d’analyseur.

 

 

 



