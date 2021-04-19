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
ms.openlocfilehash: 37ef933ec1b10555aa4c88a24261313abb261163
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106510235"
---
# <a name="peakvalue"></a>PeakValue

L’attribut **PeakValue** contient une valeur d’amplitude de 16 bits désignant le niveau de volume maximal de contenu audio. Avec [**AverageLevel**](averagelevel.md), cet attribut est utilisé pour la normalisation. La normalisation est le processus qui consiste à ajuster le niveau de volume de lecture des fichiers audio afin que les parties les plus intenses de lecture des fichiers au même niveau et le volume moyen pour chacun d’eux soient identiques.

## <a name="global-constant"></a>Constante globale

\_wszPeakValue g

## <a name="data-type"></a>Type de données

**\_valeur DWORD de type WMT \_**

## <a name="remarks"></a>Notes

Cet attribut est défini par l’objet writer en fonction des informations du codec. Seuls les flux compressés avec l’un des codecs Windows Media Audio ont une valeur définie automatiquement.

**PeakValue** n’est pas en lecture seule. Toutefois, si le fichier est lu par le lecteur Windows Media, vous ne devez pas modifier cette valeur. Le lecteur Windows Media l’utilise pour normaliser les niveaux de fichiers dans une sélection.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




