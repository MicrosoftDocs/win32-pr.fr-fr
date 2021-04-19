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
ms.openlocfilehash: ff71c6b64cbc4bf4ccc4f346e62a5eae066e78ce
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106510242"
---
# <a name="optimalbitrate"></a>OptimalBitrate

L’attribut **OptimalBitrate** contient la vitesse de transmission de la meilleure lecture du fichier.

## <a name="global-constant"></a>Constante globale

\_wszWMOptimalBitrate g

## <a name="data-type"></a>Type de données

**\_valeur DWORD de type WMT \_**

## <a name="remarks"></a>Notes

Il s’agit d’un attribut codé.

Pour les fichiers qui contiennent des flux à débit binaire variable (VBR), cette valeur est le taux binaire de pointe pour les flux dans le fichier. Pour les fichiers sans VBR, cette valeur est identique à la [**vitesse de transmission**](bit-rate.md).

Cet attribut ne peut pas être dupliqué au niveau du fichier. Si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) du format Windows Media.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




