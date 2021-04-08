---
description: Vous utilisez les fonctions PDH pour collecter les données de performances.
ms.assetid: 2510480e-cfea-4f7c-af0b-6d229c150c91
title: Utilisation des fonctions PDH pour consommer des données de compteur
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 431bf160ef6ca54b4a37363d7fe6ed48bb25d953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865089"
---
# <a name="using-the-pdh-functions-to-consume-counter-data"></a>Utilisation des fonctions PDH pour consommer des données de compteur

Utilisez les fonctions PDH pour collecter les données de performances. Les fonctions PDH sont plus faciles à utiliser que les [fonctions de Registre](using-the-registry-functions-to-consume-counter-data.md) et peuvent être utilisées pour accéder aux données de compteur à la fois dans les fournisseurs v1 et v2. PDH possède des API pour la collecte des données de performances actuelles, l’enregistrement des données de performances dans des fichiers journaux et la lecture de données à partir de fichiers journaux.

> [!Note]
> Vous ne pouvez pas utiliser les fonctions de couche d’abstraction d’assistance des données de performances si vous écrivez des applications Windows OneCore. Utilisez plutôt des [fonctions de consommateur de Perflib v2](using-the-perflib-functions-to-consume-counter-data.md).

PDH est une API de haut niveau qui simplifie la collecte des données des compteurs de performances. Elle facilite l’analyse des requêtes, la mise en cache des métadonnées, la correspondance des instances entre les exemples, le calcul des valeurs mises en forme à partir des valeurs brutes, la lecture des données des fichiers journaux et l’enregistrement des données dans les fichiers journaux. PDH utilise automatiquement les [fonctions de Registre](using-the-registry-functions-to-consume-counter-data.md) lors de la collecte de données à partir de **fournisseurs v1** et il utilise les [fonctions de consommateur v2](using-the-perflib-functions-to-consume-counter-data.md) lors de la collecte de données à partir de **fournisseurs v2**.

Pour collecter des données de performances à l’aide des fonctions PDH, procédez comme suit.

1. [Créer une requête](creating-a-query.md)
2. [Ajouter des compteurs à la requête](creating-a-query.md)
3. [Collecter les données de performances](collecting-performance-data.md)
4. [Afficher les données de performances](displaying-performance-data.md)
5. [Fermer la requête](creating-a-query.md)

Vous pouvez collecter des données de performances à partir de sources ou de fichiers journaux en temps réel. Pour plus d’informations sur la façon d’écrire des données de performances dans des fichiers journaux, consultez [utilisation des fichiers journaux](working-with-log-files.md).

## <a name="see-also"></a>Voir aussi

- [Collecte des données de performances](collecting-performance-data.md)
- [Exploration des compteurs](browsing-counters.md)
- [Vérification des valeurs de retour de l’interface PDH](checking-pdh-interface-return-values.md)
- [Exemples](examples.md)
