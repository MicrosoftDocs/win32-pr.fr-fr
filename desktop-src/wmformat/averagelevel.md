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
ms.openlocfilehash: 632379e42fa6c64e44018173b9d40340add4ee61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030211"
---
# <a name="averagelevel"></a>AverageLevel

L’attribut **AverageLevel** contient une valeur d’amplitude de 16 bits désignant le niveau de volume moyen de contenu audio. Avec [**PeakValue**](peakvalue.md), cet attribut est utilisé pour la normalisation. La normalisation est le processus qui consiste à ajuster le niveau de volume de lecture des fichiers audio afin que les parties les plus intenses de lecture des fichiers au même niveau et le volume moyen pour chaque volume soient identiques.

## <a name="global-constant"></a>Constante globale

\_wszAverageLevel g

## <a name="data-type"></a>Type de données

**\_valeur DWORD de type WMT \_**

## <a name="remarks"></a>Notes

Cet attribut est défini par l’objet writer en fonction des informations du codec. Seuls les flux compressés avec l’un des codecs Windows Media Audio ont une valeur définie automatiquement.

**AverageLevel** n’est pas en lecture seule. Toutefois, si le fichier est lu par le lecteur Windows Media, vous ne devez pas modifier cette valeur. Le lecteur Windows Media l’utilise pour normaliser les niveaux de fichiers dans une sélection.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




