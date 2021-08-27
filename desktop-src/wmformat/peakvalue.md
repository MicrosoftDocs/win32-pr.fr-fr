---
title: PeakValue
description: L’attribut PeakValue contient une valeur d’amplitude de 16 bits désignant le niveau de volume maximal de contenu audio.
ms.assetid: 885f6d4c-661a-4681-96b6-c1a282c8bf18
keywords:
- Format Windows Media PeakValue
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e3089ac6d4b789d740f256a5c44c1911eb3501bc654c3b94d0006d405616572
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110259"
---
# <a name="peakvalue"></a>PeakValue

L’attribut **PeakValue** contient une valeur d’amplitude de 16 bits désignant le niveau de volume maximal de contenu audio. Avec [**AverageLevel**](averagelevel.md), cet attribut est utilisé pour la normalisation. La normalisation est le processus qui consiste à ajuster le niveau de volume de lecture des fichiers audio afin que les parties les plus intenses de lecture des fichiers au même niveau et le volume moyen pour chacun d’eux soient identiques.

## <a name="global-constant"></a>Constante globale

\_wszPeakValue g

## <a name="data-type"></a>Type de données

**\_valeur DWORD de type WMT \_**

## <a name="remarks"></a>Remarques

Cet attribut est défini par l’objet writer en fonction des informations du codec. seuls les flux compressés avec l’un des codecs Windows Media Audio ont une valeur définie automatiquement.

**PeakValue** n’est pas en lecture seule. toutefois, si le fichier est lu par le Lecteur Windows Media, vous ne devez pas modifier cette valeur. le Lecteur Windows Media l’utilise pour normaliser les niveaux de fichiers dans une sélection.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




