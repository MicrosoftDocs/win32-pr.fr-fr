---
description: Les compteurs de performances spécifiques à votre application peuvent vous aider à optimiser les performances lors du développement et du débogage de l’application.
ms.assetid: 016386f6-4675-409e-8446-599e4ff96109
title: Ajout de compteurs de performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8660af9406de4dedec3ecbd76169a23b342aa7d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013907"
---
# <a name="adding-performance-counters"></a>Ajout de compteurs de performances

> [!IMPORTANT]
> En raison des limitations de performances et de fiabilité significatives, la méthode permettant de fournir des données de compteurs de performances que cette rubrique décrit peut être modifiée ou non disponible à l’avenir. Au lieu de cela, Microsoft vous recommande d’utiliser la méthode décrite dans la rubrique [fourniture de données de compteur à l’aide de la Version 2,0](providing-counter-data-using-version-2-0.md) pour la création de nouveaux compteurs de performances et la migration des compteurs de performances existants pour utiliser également cette méthode.

Les compteurs de performances spécifiques à votre application peuvent vous aider à optimiser les performances lors du développement et du débogage de l’application. Une fois votre application terminée et installée sur les systèmes cibles, les compteurs peuvent aider les administrateurs système à ajuster les paramètres configurables pour votre application.

## <a name="adding-a-performance-object-and-its-counters"></a>Ajout d’un objet de performance et de ses compteurs

1. Concevez les types d’objets et les compteurs pour l’application. Pour plus d’informations, consultez [conception d’objets et de compteurs](object-and-counter-design.md).
2. Créez un fichier d’initialisation (.ini) contenant les noms et les descriptions des objets et des compteurs de performance que vous fournissez. Pour plus d’informations, consultez [Ajout de noms de compteur et de descriptions au registre](adding-counter-names-and-descriptions-to-the-registry.md).
3. Créez un fichier d’en-tête (. h) contenant les décalages relatifs auxquels les objets de compteur et les compteurs seront installés dans le registre. Pour plus d’informations, consultez [Ajout de noms de compteur et de descriptions au registre](adding-counter-names-and-descriptions-to-the-registry.md).
4. Configurez les entrées d’analyse des performances nécessaires dans le registre. Cela comprend les étapes suivantes.
    1. Créez une clé de Registre dans la clé **services** de l’application. Si vous n’avez pas ce type de nœud, créez-le sous la clé de Registre suivante : `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` . Pour plus d’informations, consultez [création de la clé de performance de l’application](creating-the-applications-performance-key.md).
    2. Utilisez l’utilitaire **lodctr** avec les fichiers .ini et. h pour installer les informations dans le registre. Cet utilitaire ne fonctionne que si une clé de performance existe dans la clé des **services** de l’application. Pour plus d’informations, consultez [Ajout de noms de compteur et de descriptions au registre](adding-counter-names-and-descriptions-to-the-registry.md).
5. Créez une DLL de performance contenant un ensemble de fonctions exportées qui fournissent les données de compteur interrogées au consommateur. Pour plus d’informations, consultez [création d’une DLL d’extension de performance](creating-a-performance-extension-dll.md).
6. Modifiez le fichier d’installation de l’application pour automatiser l’ajout d’informations au registre (comme décrit à l’étape 4), puis copiez votre DLL de performance dans le répertoire de votre application lors de l’installation.

Pour plus d’informations sur les entrées de Registre supplémentaires, consultez [création d’autres entrées de Registre](creating-other-registry-entries.md).
