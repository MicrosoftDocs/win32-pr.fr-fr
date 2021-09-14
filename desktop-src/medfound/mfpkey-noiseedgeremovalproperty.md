---
description: Spécifie si le codec doit tenter de détecter les bords bruyants du cadre et les supprimer.
ms.assetid: fdb4f3a8-1447-4e1e-a208-0f9b717f7626
title: MFPKEY_NOISEEDGEREMOVAL, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30acd92bae7693d0714e42d6b4f832a521557bf2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235997"
---
# <a name="mfpkey_noiseedgeremoval-property"></a>MFPKEY \_ propriété NOISEEDGEREMOVAL

Spécifie si le codec doit tenter de détecter les bords bruyants du cadre et les supprimer.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCNoiseEdgeRemoval g

## <a name="data-type"></a>Type de données

VT \_ bool

## <a name="default-value"></a>Valeur par défaut

FALSE

## <a name="remarks"></a>Notes

En règle générale, un bord de cadre bruyant est le nombre de données de l’intervalle de occultation verticale (VBI) d’une image de télévision. Le VBI correspond aux 21 premières lignes de balayage du cadre de télévision. Ces lignes de numérisation ne contiennent pas de données vidéo, elles contiennent des données sur la diffusion. Lorsqu’un signal de télévision est enregistré par une carte de capture, le VBI est généralement supprimé du cadre. La détection et la correction des bords bruyants effectuées par le codec peuvent uniquement corriger une arête qui a au moins trois lignes de bruit. Si la vidéo capturée contient plus de trois lignes bruyantes, il y a un problème avec le matériel utilisé pour capturer la vidéo.

Si le codec est défini pour supprimer les bords bruyants, il duplique les lignes adjacentes à la périphérie bruyante pour remplir le cadre.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




