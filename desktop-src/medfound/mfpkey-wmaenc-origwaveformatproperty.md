---
description: Spécifie la structure WAVEFORMATEX décrivant le contenu audio d’entrée.
ms.assetid: d424f243-5ad6-46f2-b99b-9bb780715e8a
title: MFPKEY_WMAENC_ORIGWAVEFORMAT, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df477daa61e39eb6b2a86aa26c27de4088e943d41f40ac9b708a0201698088c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113139"
---
# <a name="mfpkey_wmaenc_origwaveformat-property"></a>MFPKEY \_ WMAENC \_ ORIGWAVEFORMAT, propriété

Spécifie la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) décrivant le contenu audio d’entrée.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMACOriginalWaveFormat g

## <a name="data-type"></a>Type de données

\_Tableau VT \| \_ UI1 ([**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) en tant que tableau d’octets)

## <a name="remarks"></a>Remarques

lors du transcodage de contenu Windows Media Audio à une vitesse de transmission inférieure, vous pouvez transmettre la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) du contenu au codec pour permettre au codec d’optimiser ses algorithmes. Cette fonctionnalité, appelée « recompression intelligente », fournit de meilleurs résultats que la décompression du contenu, puis l’alimentation des exemples PCM reconstruits par le biais du codec.

Lors du passage de la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) , incluez les octets supplémentaires à la fin de la structure spécifiée par **WAVEFORMATEX. cbSize**.

L’encodeur audio accepte uniquement les entrées et sorties pour lesquelles le nombre de canaux, le nombre de bits par échantillon et le taux d’échantillonnage sont identiques. Vous pouvez transcoder du contenu uniquement à une vitesse de transmission inférieure dans ces paramètres. Dans tous les cas, vous devez décoder le contenu et transmettre les exemples non compressés comme entrée à l’encodeur. La définition de cette propriété donne à l’encodeur des informations sur le traitement qui a déjà été effectué sur le contenu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
