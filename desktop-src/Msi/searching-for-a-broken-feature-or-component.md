---
description: Le programme d’installation peut augmenter la résilience des applications en réinstallant automatiquement les composants endommagés.
ms.assetid: aa565e34-f89d-4d26-945d-67b439586523
title: Recherche d’une fonctionnalité ou d’un composant endommagé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8398d084a543ee4c9491242faa287c60d83a5f7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203399"
---
# <a name="searching-for-a-broken-feature-or-component"></a>Recherche d’une fonctionnalité ou d’un composant endommagé

Le programme d’installation peut augmenter la [résilience](resiliency.md) des applications en réinstallant automatiquement les composants endommagés. Plus précisément, le programme d’installation réinstalle un composant ou une fonctionnalité s’il détecte que le fichier ou la clé de Registre spécifiée dans la colonne keyPath de la [table Component](component-table.md) est manquant.

Si le chemin d’accès du keyPath du composant d’une fonctionnalité est endommagé dans la source ou si une erreur se produit dans la manière dont le chemin d’accès de la base de données est créé dans la base de données, le programme d’installation peut tenter d’ouvrir un package d’installation et réinstaller la fonctionnalité chaque fois que le raccourci de la fonctionnalité est activé.

Pour déterminer la cause des tentatives répétées de réinstallation d’une fonctionnalité ou d’une application, consultez le journal des événements pour connaître les deux entrées suivantes.

``` syntax
Detection of product 'MyProduct', feature 'MyFeature' failed during
 request for component 'MyComponent'
Detection of product 'MyProduct', feature 'MyFeature', component
 'MyComponent' failed
```

Le premier message indique quel composant dans le package du produit était en cours d’installation. Il s’agit du composant référencé dans la \_ colonne composant du [tableau de raccourcis](shortcut-table.md).

Le deuxième message indique quel composant est en échec de détection. Il s’agit du composant avec le chemin d’accès de la keyPath manquant ou endommagé qui déclenche la réinstallation.

 

 



