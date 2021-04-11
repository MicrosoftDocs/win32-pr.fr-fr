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
# <a name="searching-for-a-broken-feature-or-component"></a><span data-ttu-id="c2632-103">Recherche d’une fonctionnalité ou d’un composant endommagé</span><span class="sxs-lookup"><span data-stu-id="c2632-103">Searching for a Broken Feature or Component</span></span>

<span data-ttu-id="c2632-104">Le programme d’installation peut augmenter la [résilience](resiliency.md) des applications en réinstallant automatiquement les composants endommagés.</span><span class="sxs-lookup"><span data-stu-id="c2632-104">The installer can increase application [resiliency](resiliency.md) by automatically reinstalling damaged components.</span></span> <span data-ttu-id="c2632-105">Plus précisément, le programme d’installation réinstalle un composant ou une fonctionnalité s’il détecte que le fichier ou la clé de Registre spécifiée dans la colonne keyPath de la [table Component](component-table.md) est manquant.</span><span class="sxs-lookup"><span data-stu-id="c2632-105">Specifically, the installer reinstalls a component or feature if it finds that the file or registry key specified in the KeyPath column of the [Component table](component-table.md) is missing.</span></span>

<span data-ttu-id="c2632-106">Si le chemin d’accès du keyPath du composant d’une fonctionnalité est endommagé dans la source ou si une erreur se produit dans la manière dont le chemin d’accès de la base de données est créé dans la base de données, le programme d’installation peut tenter d’ouvrir un package d’installation et réinstaller la fonctionnalité chaque fois que le raccourci de la fonctionnalité est activé.</span><span class="sxs-lookup"><span data-stu-id="c2632-106">If the KeyPath of a feature's component is damaged in the source, or if there is an error in how the KeyPath is authored in the database, the installer may attempt to open an installation package and reinstall the feature each time the feature's shortcut is activated.</span></span>

<span data-ttu-id="c2632-107">Pour déterminer la cause des tentatives répétées de réinstallation d’une fonctionnalité ou d’une application, consultez le journal des événements pour connaître les deux entrées suivantes.</span><span class="sxs-lookup"><span data-stu-id="c2632-107">To determine the cause of repeated attempts to reinstall a feature or application, check the Event Log for two entries such as the following.</span></span>

``` syntax
Detection of product 'MyProduct', feature 'MyFeature' failed during
 request for component 'MyComponent'
Detection of product 'MyProduct', feature 'MyFeature', component
 'MyComponent' failed
```

<span data-ttu-id="c2632-108">Le premier message indique quel composant dans le package du produit était en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="c2632-108">The first message states which component in the product's package was being installed.</span></span> <span data-ttu-id="c2632-109">Il s’agit du composant référencé dans la \_ colonne composant du [tableau de raccourcis](shortcut-table.md).</span><span class="sxs-lookup"><span data-stu-id="c2632-109">This is the component referenced in the Component\_ column of the [Shortcut table](shortcut-table.md).</span></span>

<span data-ttu-id="c2632-110">Le deuxième message indique quel composant est en échec de détection.</span><span class="sxs-lookup"><span data-stu-id="c2632-110">The second message states which component is failing detection.</span></span> <span data-ttu-id="c2632-111">Il s’agit du composant avec le chemin d’accès de la keyPath manquant ou endommagé qui déclenche la réinstallation.</span><span class="sxs-lookup"><span data-stu-id="c2632-111">This is the component with the missing or damaged KeyPath that's triggering the reinstall.</span></span>

 

 



