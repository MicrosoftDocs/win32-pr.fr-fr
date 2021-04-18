---
description: Spécifie le degré auquel le codec doit réduire la plage de couleurs effectives de la vidéo.
ms.assetid: 7227957b-59c9-4dd9-ad2b-a383e888cd46
title: MFPKEY_RANGEREDUX, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ec326e5d21a72792aab38f08d8c8c9207ab867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519642"
---
# <a name="mfpkey_rangeredux-property"></a>MFPKEY \_ propriété RANGEREDUX

Spécifie le degré auquel le codec doit réduire la plage de couleurs effectives de la vidéo.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCRangeRedux g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="remarks"></a>Notes

La réduction de plage spécifie le degré auquel le codec doit réduire la luminance et la plage de chrominance de la vidéo. La réduction de la plage réduit la taille des images vidéo encodées, mais réduit également le détail des couleurs de la vidéo.

La réduction de plage se compose d’une réduction lors du décodage et de l’extension. Il est possible de faire en sorte que les facteurs d’expansion ne soient pas les mêmes que les facteurs de réduction, mais cela n’est pas recommandé dans la plupart des scénarios où le remappage de plage est utile.

La réduction de la plage et l’expansion sont effectuées séparément sur les canaux de luminance et de chrominance. La réduction de la plage peut être un moyen efficace de réduire la complexité de la vidéo à faible vitesse de transmission sans sacrifier les détails de l’image. En définissant les quatre valeurs sur 8, vous réduisez la quantité d’informations de luminance et de chrominance de moitié, en laissant plus de bits à rediriger pour conserver les détails de l’image.

Le codec peut choisir d’utiliser automatiquement la réduction de plage lors de l’encodage de vidéos à des débits binaires très faibles. Si vous affectez la valeur 0 à ces quatre valeurs, vous désactivez complètement la réduction de plage, même dans les scénarios de faible débit.

La réduction de la plage de couleurs réduit la taille encodée des images vidéo, mais peut introduire un flou dans les frames décodés.

Si cette propriété n’est pas définie, le codec détermine s’il faut utiliser la réduction de plage au moment de l’encodage. En règle générale, cette option est sélectionnée par le codec uniquement aux taux de bits faibles.

La valeur de cette propriété est une combinaison de quatre composants, séparés par des zéros, mis en forme en tant que 0x0M0m0N0n, où :

-   M est le facteur de réduction de plage d’encodage pour le composant Y.
-   m est le facteur d’extension de la plage de décodage pour le composant Y (généralement le même que M).
-   N est le facteur de réduction de la plage d’encodage pour le composant UV.
-   n est le facteur d’extension de la plage de décodage pour le composant UV (généralement identique à N).

Chaque facteur est un chiffre compris entre 0 et 8, où 0 n’est pas une réduction ou une expansion et 8 est la réduction ou l’expansion maximale.

Si vous définissez la valeur sur 0x00000000, la réduction de plage est complètement désactivée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




