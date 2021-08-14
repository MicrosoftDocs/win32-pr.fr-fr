---
description: Le gestionnaire de distribution fournit la mise en pool des ressources pour les distributeurs de ressources et garantit qu’une ressource fournie par un distributeur de ressources est correctement inscrite dans la transaction des objets d’application.
ms.assetid: c8986943-56a1-4668-9e80-7ab2a42333a8
title: Gestionnaire de distributeur COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec090ba8c6324363c80a00685e4bc9cfa11185fa1b95ad5db3575608c9fe60ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991689"
---
# <a name="com-dispenser-manager"></a>Gestionnaire de distributeur COM+

Le gestionnaire de distribution fournit la mise en pool des ressources pour les distributeurs de ressources et garantit qu’une ressource fournie par un distributeur de ressources est correctement inscrite dans la transaction de l’objet d’application. Le gestionnaire de distribution récupère automatiquement les ressources qui sont toujours réservées à la fin de la durée de vie d’un objet, ce qui élimine le risque de fuites de ressources. Le gestionnaire de distribution peut demander à un distributeur de ressources de créer une ressource ou de détruire des ressources inactives si nécessaire pour ajuster les niveaux d’inventaire, plutôt que d’utiliser des paramètres statiques.

> [!Note]  
> Étant donné que les interfaces de distributeur de ressources exposées à l’application ne doivent pas nécessairement être des interfaces COM, le gestionnaire de distribution peut être utilisé dans un processus sans initialiser COM, par exemple pour prendre en charge le distributeur de ressources ODBC.

 

Lors de la création d’une ressource, le distributeur de ressources peut spécifier la durée pendant laquelle une ressource inactive est autorisée à rester dans le pool avant sa destruction. Un thread qui s’exécute dans le gestionnaire de distribution recherche toujours ces ressources inactives.

## <a name="the-inventory-statistics-manager"></a>Gestionnaire des statistiques d’inventaire

Le gestionnaire de distribution utilise le *Gestionnaire de statistiques d’inventaire* pour gérer les niveaux d’inventaire des ressources de pool. Le gestionnaire des statistiques d’inventaire conserve un enregistrement de lorsque chaque ressource a été utilisée et supprime les ressources de l’inventaire lorsqu’elles n’ont pas été utilisées pendant *x* secondes, où la valeur de *x* est définie par ressource lors de la création de la ressource.

## <a name="the-holder-component"></a>Composant du détenteur

Le gestionnaire du distributeur interroge chaque *détenteur*, un composant créé par le gestionnaire du distributeur, qui répertorie l’inventaire des ressources pour chaque distributeur de ressources, toutes les 10 secondes pour lui permettre de réajuster son inventaire des ressources. Chaque détenteur appelle le gestionnaire de statistiques d’inventaire pour suggérer des niveaux de stock pour chaque type de ressource. Par conséquent, le détenteur peut demander au distributeur de ressources de créer ou de détruire un inventaire.

Le détenteur et le distributeur de ressources communiquent pour demander des ressources d’un type particulier. Les relations suivantes existent entre le conteneur et le distributeur de ressources :

-   Le détenteur peut demander une ressource à partir du distributeur de ressources. Le distributeur de ressources retourne une ressource disponible ou en crée une nouvelle.
-   Le détenteur peut notifier au distributeur de ressources qu’une application n’a plus besoin d’une ressource, puis la renvoyer au pool de ressources.
-   Le détenteur et le distributeur de ressources fonctionnent ensemble pour conserver la taille du pool de ressources.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts du distributeur de ressources COM+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



