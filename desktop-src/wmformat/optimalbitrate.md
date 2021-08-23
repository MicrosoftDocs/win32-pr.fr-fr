---
title: OptimalBitrate
description: L’attribut OptimalBitrate contient la vitesse de transmission de la meilleure lecture du fichier.
ms.assetid: cd13b9b5-34d2-4ebb-9f10-3bf42dd9de81
keywords:
- Format Windows Media OptimalBitrate
topic_type:
- apiref
api_name:
- OptimalBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f670c2acd2f2190a5ee2bfd76994c219c6f967dbbd933520a8d4627236a0d36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930629"
---
# <a name="optimalbitrate"></a>OptimalBitrate

L’attribut **OptimalBitrate** contient la vitesse de transmission de la meilleure lecture du fichier.

## <a name="global-constant"></a>Constante globale

\_wszWMOptimalBitrate g

## <a name="data-type"></a>Type de données

**\_valeur DWORD de type WMT \_**

## <a name="remarks"></a>Remarques

Il s’agit d’un attribut codé.

Pour les fichiers qui contiennent des flux à débit binaire variable (VBR), cette valeur est le taux binaire de pointe pour les flux dans le fichier. Pour les fichiers sans VBR, cette valeur est identique à la [**vitesse de transmission**](bit-rate.md).

Cet attribut ne peut pas être dupliqué au niveau du fichier. si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) de Format multimédia Windows.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




