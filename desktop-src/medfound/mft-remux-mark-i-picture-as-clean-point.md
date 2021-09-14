---
description: Spécifie si la table MFT REMUX vidéo H. 264 doit marquer I images comme point de nettoyage pour améliorer la capacité de recherche. Cela risque d’endommager les recherches dans des fichiers MP4 finaux non conformes.
ms.assetid: BB521E13-40A4-4643-B071-76B8CBC62074
title: Attribut MFT_REMUX_MARK_I_PICTURE_AS_CLEAN_POINT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c9fe8398507f6d7af5d0e4bf45a36a4454f220
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313726"
---
# <a name="mft_remux_mark_i_picture_as_clean_point-attribute"></a>\_ \_ Image de la marque REMUX MFT \_ \_ \_ comme \_ point de nettoyage \_

Spécifie si la table MFT REMUX vidéo H. 264 doit marquer I images comme point de nettoyage pour améliorer la capacité de recherche. Cela risque d’endommager les recherches dans des fichiers MP4 finaux non conformes.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Notes

L’image de point de nettoyage doit être compressée pour les images par définition.

Cela n’est pas recommandé pour l’enregistrement ou la remuxing des fichiers MP4, sauf si un tel exercice consiste à produire des fichiers Pseudo-MP4 intermédiaires pour la modification vidéo.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Mftransform. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




