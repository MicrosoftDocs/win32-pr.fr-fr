---
title: Stockage structuré
description: Le stockage structuré fournit la persistance des fichiers et des données dans COM en gérant un seul fichier comme une collection structurée d’objets appelés stockages et flux.
ms.assetid: 57a5f34d-c3db-47c5-9836-6e2163732d30
keywords:
- Stockage structuré Strctd STG
- Stockage structuré Strctd STG, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606fef01d67cd78997f21dcd9008785d30985315
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315707"
---
# <a name="structured-storage"></a>Stockage structuré

## <a name="purpose"></a>Objectif

Le stockage structuré fournit la persistance des fichiers et des données dans COM en gérant un seul fichier comme une collection structurée d’objets appelés stockages et flux.

L’objectif du stockage structuré est de réduire les pénalités de performances et la surcharge associées au stockage d’objets distincts dans un seul fichier. Le stockage structuré fournit une solution en définissant comment gérer une entité de fichier unique comme une collection structurée de deux types de stockages d’objets et de flux via une implémentation standard appelée fichiers composés. Cela permet à l’utilisateur d’interagir avec un fichier composé, et de le gérer, comme s’il s’agissait d’un fichier unique plutôt que d’une hiérarchie imbriquée d’objets distincts.

## <a name="where-applicable"></a>Le cas échéant

Le stockage structuré peut être utilisé sur les systèmes d’exploitation basés sur Microsoft COM.

## <a name="developer-audience"></a>Développeurs concernés

La documentation sur le stockage structuré est destinée aux programmeurs C et C++ expérimentés et aux développeurs de systèmes COM.

Le stockage structuré prend principalement en charge les langages de programmation C et C++. Toutefois, toute technologie COM prendra également en charge tout langage de programmation qui utilise des pointeurs d’interface.

Une bonne compréhension des technologies COM est prérequise pour l’utilisation du stockage structuré.

## <a name="run-time-requirements"></a>Conditions d’exécution

Pour plus d’informations sur les systèmes d’exploitation requis pour utiliser un élément d’API particulier, consultez la section Configuration requise de la documentation relative à l’élément.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                               | Description                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Vue d'ensemble](about-structured-storage.md)<br/>                 | Informations générales sur le stockage structuré.<br/>                                                                                                                                                                                                                                                 |
| [Utilisation du stockage structuré](using-structured-storage.md)<br/> | Utilisation d’informations pour le stockage structuré.<br/>                                                                                                                                                                                                                                                     |
| [Référence](structured-storage-reference.md)<br/>            | Documentation des interfaces, des fonctions, des structures et des énumérations spécifiques au stockage structuré.<br/>                                                                                                                                                                                             |
| [Exemples](samples.md)<br/>                                   | Exemples de code écrits en C++. Pour plus d’informations, consultez [noms dans IStorage](names-in-istorage.md), [en-tête de jeu de propriétés](property-set-header.md), [section](section.md), stockage des [jeux de propriétés](storing-property-sets.md)et [utilisation du stockage structuré](using-structured-storage.md).<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[COM (Component Object Model)](../com/the-component-object-model.md)
</dt> </dl>

 

