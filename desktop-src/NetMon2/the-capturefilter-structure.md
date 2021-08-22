---
description: Dans Moniteur réseau, le filtre de capture est défini par la structure CAPTUREFILTER.
ms.assetid: 03cd35f2-4da5-4ef6-b73f-0bf6e0e33135
title: Structure CAPTUREFILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5c6d8d8f8baa3710b7dff4e33c98eb8791a65dc76931caa9068bbc1280f33e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339362"
---
# <a name="the-capturefilter-structure"></a>Structure CAPTUREFILTER

Dans Moniteur réseau, le [filtre de capture](capture-filters.md) est défini par la structure [**capturefilter**](capturefilter.md) . L’absence ou la combinaison d’indicateurs, de valeurs et d’expressions détermine les frames qui seront transmis ou supprimés par le pilote Moniteur réseau. L’illustration suivante montre les trois zones de l’analyse de filtre de capture : ETYPE/SAP, adresse et correspondance de modèle.

![trois zones de l’analyse de filtre de capture](images/capfilter.png)

Le tableau suivant répertorie la fonction de chaque élément de filtre de capture.



| Filter, élément                                       | Action                                                                                                                                                                                                       |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ETYPE/SAP](writing-etypesap-filter-portion.md)     | Évalue les paramètres ETYPE/SAP. La combinaison d’indicateurs détermine les types de paramètres ou les valeurs qui sont inclus ou exclus.                                                                                    |
| [Adresse](writing-addresstable-filter-portion.md)   | Évalue les adresses source et de destination et les paires d’adresses. Différentes combinaisons d’indicateurs déterminent les valeurs individuelles ou les combinaisons de paires d’adresses qui sont incluses ou exclues.                   |
| [Correspondance de modèle](writing-the-patternmatch-filter.md) | Définit des correspondances de modèle complexes dans un frame. Les indicateurs sont fournis pour différents types et décalages. Vous pouvez combiner des correspondances de modèle avec des instructions AND logiques AND ou Operator.                              |
| [Découpage](clipping-a-frame.md)                     | Découpe les trames d’une manière spécifiée par différentes valeurs d’octets. Vous pouvez utiliser uniquement cet élément pour découper tous les frames ou les utiliser avec d’autres éléments de filtre de capture. par exemple, pour rechercher, puis détourer une image unique. |
| [**Déclencheur**](trigger.md)                           | Cet élément de filtre de capture est obsolète. Les déclencheurs ne font plus partie d’un filtre de capture ; elles sont maintenant contenues dans leurs propres balises d’objet BLOB, qui sont spécifiées séparément.                                     |



 

Un frame est évalué par rapport aux trois parties du filtre de capture. Par conséquent, une trame transmise avec succès doit passer chaque élément. N’oubliez pas que le pilote Moniteur réseau évalue l’absence de l’un des trois éléments comme **vrai**. Par exemple, le pilote évalue l’absence d’une section ETYPE/SAP en tant que « toutes les trames avec la valeur ETYPE/SAP sont valides ».

 

 



