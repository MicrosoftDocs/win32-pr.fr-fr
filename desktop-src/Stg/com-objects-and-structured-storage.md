---
title: objets COM et Stockage structurés
description: L’une des utilisations actuelles les plus courantes des propriétés persistantes consiste à les utiliser pour stocker des données sur un objet système, tel qu’un document, avec cet objet.
ms.assetid: 95136e9a-4c80-4704-ae65-9759487cf8f8
keywords:
- objets COM et Stockage structurés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4c1405ddfaa060aa249090fc58b25b294a8c9aecc5f7b885d21b55bc162198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663589"
---
# <a name="com-objects-and-structured-storage"></a>objets COM et Stockage structurés

L’une des utilisations actuelles les plus courantes des propriétés persistantes consiste à les utiliser pour stocker des données sur un objet système, tel qu’un document, avec cet objet. Bien entendu, le potentiel de stockage des propriétés avec n’importe quel objet, tel qu’une imprimante, n’est nécessaire qu’à la consultation de ses propriétés pour déterminer son emplacement, son type, etc. un objet utilisateur peut avoir un jeu de propriétés qui comprend des données telles que le prénom, le nom, le Office et le Téléphone. Les applications peuvent être écrites pour interroger un ensemble d’objets à l’ensemble du système en fonction de leurs propriétés, par exemple, pour afficher toutes les imprimantes situées dans une certaine génération. Toutefois, les systèmes actuels utilisent le plus souvent des propriétés sur les documents.

La norme de jeu de propriétés primaire définie par COM est [le jeu de propriétés d’informations de résumé](the-summary-information-property-set.md). Ce jeu de propriétés est à la fois simple et couramment utilisé. La plupart des documents créés par des applications ont un ensemble commun d’attributs utiles pour les utilisateurs de ces documents. Ces attributs incluent le nom de l’auteur du document, l’objet du document, le moment où il a été créé, etc. deux autres jeux de propriétés sont définis pour Microsoft Office 95, Office 97 et versions ultérieures. Il s’agit du jeu de propriétés Résumé du document COM et du jeu de propriétés User-Defined propriétés. pour plus d’informations, consultez [structured Stockage serialized Property Set Format](structured-storage-serialized-property-set-format.md).

dans Windows 3,1, chaque application avait une façon différente de stocker ces données dans ses documents. Pour examiner les informations de synthèse d’un document donné, l’utilisateur devait exécuter l’application qui a créé le document, l’ouvrir et appeler la boîte de dialogue informations récapitulatives de l’application, de sorte que seule l’application puisse afficher ses informations de synthèse.

Les jeux de propriétés COM et les interfaces de jeu de propriétés permettent de voir les propriétés du document sans exécuter l’application de création. par exemple, toutes les versions de Microsoft Word 6,0 ou version ultérieure, ainsi que de nombreuses autres applications prenant en charge les com, enregistrent désormais leurs documents à l’aide du stockage structuré com et du jeu de propriétés standard décrit ici. ainsi, d’autres applications Office Suite peuvent afficher [la propriété informations de synthèse définie](the-summary-information-property-set.md) pour ce type de fichier, tant que ce fichier est un fichier de stockage structuré com, et que l’application de création a enregistré les informations dans le format du jeu de propriétés com. l’interpréteur de commandes Windows 95 ou Windows 98, par exemple, l’utilise et permet à l’utilisateur final d’afficher les propriétés d’un document Word 6,0 ou version ultérieure directement à partir de l’interpréteur de commandes.

Pour utiliser des jeux de propriétés à partir d’autres applications, les autres applications doivent reconnaître comment interpréter les propriétés dans un jeu de propriétés, ce qui implique une norme. COM a novateur cette approche en définissant un jeu de propriétés standard, le jeu de propriétés informations résumées COM. Toute application qui a la définition de cet ensemble de propriétés peut accéder facilement aux informations de résumé contenues dans tout document créé par une application COM qui utilise cette spécification de jeu de propriétés.

 

 




