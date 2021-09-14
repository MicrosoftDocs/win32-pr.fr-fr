---
title: Stockage structuré
description: la Stockage structurée fournit la persistance des fichiers et des données dans COM en gérant un seul fichier comme une collection structurée d’objets appelés stockages et flux.
ms.assetid: 57a5f34d-c3db-47c5-9836-6e2163732d30
keywords:
- structured Stockage Strctd Stg
- Stockage structuré Strctd Stg, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606fef01d67cd78997f21dcd9008785d30985315
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237269"
---
# <a name="structured-storage"></a>Stockage structuré

## <a name="purpose"></a>Objectif

la Stockage structurée fournit la persistance des fichiers et des données dans COM en gérant un seul fichier comme une collection structurée d’objets appelés stockages et flux.

l’objectif de la Stockage structurée est de réduire les pénalités de performances et la surcharge associées au stockage d’objets distincts dans un seul fichier. la Stockage structurée fournit une solution en définissant la façon de gérer une entité de fichier unique comme une collection structurée de deux types de stockages d’objets et de flux via une implémentation standard appelée fichiers composés. Cela permet à l’utilisateur d’interagir avec un fichier composé, et de le gérer, comme s’il s’agissait d’un fichier unique plutôt que d’une hiérarchie imbriquée d’objets distincts.

## <a name="where-applicable"></a>Le cas échéant

les Stockage structurées peuvent être utilisées sur les systèmes d’exploitation Microsoft COM.

## <a name="developer-audience"></a>Développeurs concernés

la documentation structurée Stockage est destinée aux programmeurs C et C++ expérimentés et aux développeurs de systèmes basés sur COM.

le Stockage structuré prend principalement en charge les langages de programmation C et C++, mais toute technologie COM prendra également en charge tout langage de programmation qui utilise des pointeurs d’interface.

une bonne compréhension des technologies COM est prérequise pour l’utilisation du développement des Stockage structurées.

## <a name="run-time-requirements"></a>Conditions d’exécution

Pour plus d’informations sur les systèmes d’exploitation requis pour utiliser un élément d’API particulier, consultez la section Configuration requise de la documentation relative à l’élément.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                               | Description                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Vue d'ensemble](about-structured-storage.md)<br/>                 | informations générales sur les Stockage structurées.<br/>                                                                                                                                                                                                                                                 |
| [utilisation de Stockage structurées](using-structured-storage.md)<br/> | utilisation d’informations pour les Stockage structurées.<br/>                                                                                                                                                                                                                                                     |
| [Référence](structured-storage-reference.md)<br/>            | Documentation des interfaces, des fonctions, des structures et des énumérations spécifiques Stockage.<br/>                                                                                                                                                                                             |
| [Exemples](samples.md)<br/>                                   | Exemples de code écrits en C++. pour plus d’informations, consultez [noms dans IStorage](names-in-istorage.md), [en-tête de jeu de propriétés](property-set-header.md), [Section](section.md), stockage des [jeux de propriétés](storing-property-sets.md)et [utilisation de Stockage structurés](using-structured-storage.md).<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[COM (Component Object Model)](../com/the-component-object-model.md)
</dt> </dl>

 

