---
title: AverageLevel
description: L’attribut AverageLevel contient une valeur d’amplitude de 16 bits désignant le niveau de volume moyen de contenu audio.
ms.assetid: e6270ac8-5de3-4dee-824c-ba25fdd272c8
keywords:
- Format Windows Media AverageLevel
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd8745c5983eca67a02506b6cdeeabaca0a61a4c3f8b2a6993a73359d87adba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028157"
---
# <a name="averagelevel"></a>AverageLevel

L’attribut **AverageLevel** contient une valeur d’amplitude de 16 bits désignant le niveau de volume moyen de contenu audio. Avec [**PeakValue**](peakvalue.md), cet attribut est utilisé pour la normalisation. La normalisation est le processus qui consiste à ajuster le niveau de volume de lecture des fichiers audio afin que les parties les plus intenses de lecture des fichiers au même niveau et le volume moyen pour chaque volume soient identiques.

## <a name="global-constant"></a>Constante globale

\_wszAverageLevel g

## <a name="data-type"></a>Type de données

**\_valeur DWORD de type WMT \_**

## <a name="remarks"></a>Remarques

Cet attribut est défini par l’objet writer en fonction des informations du codec. seuls les flux compressés avec l’un des codecs Windows Media Audio ont une valeur définie automatiquement.

**AverageLevel** n’est pas en lecture seule. toutefois, si le fichier est lu par le Lecteur Windows Media, vous ne devez pas modifier cette valeur. le Lecteur Windows Media l’utilise pour normaliser les niveaux de fichiers dans une sélection.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




