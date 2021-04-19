---
description: Spécifie les coefficients de repli pour le décodage de l’audio multicanaux pour un nombre de canaux inférieur à celui contenu dans le flux encodé.
ms.assetid: f6737c05-4b39-4209-9985-9402b28cf316
title: MFPKEY_WMADEC_FOLDDOWN_MATRIX, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92cb2495863d319c7f755d7d72f475ccf1eda75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524947"
---
# <a name="mfpkey_wmadec_folddown_matrix-property"></a>MFPKEY \_ WMADEC \_ FOLDDOWN, propriété de la \_ matrice

Spécifie les coefficients de repli pour le décodage de l’audio multicanaux pour un nombre de canaux inférieur à celui contenu dans le flux encodé.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMACFoldDownXToYChannels g

\_wszWMACFoldXToYChannelsZ g

## <a name="data-type"></a>Type de données

**Tableau VT de \_ groupe VT \| \_**

## <a name="remarks"></a>Notes

Un décodeur audio peut agir en tant qu’objet de média DirectX (DMO) ou en tant que transformation de Media Foundation (MFT). Pour plus d’informations sur le moment où un décodeur agit comme DMO ou MFT, consultez les pages de référence des codecs individuels sous [objets codec](codecobjects.md).

Quand vous utilisez un décodeur en tant qu’DMO, le décodeur peut effectuer un repli de canal vers le dessous, et vous pouvez énumérer les types de média de sortie repliés en appelant [**IMediaObject :: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).

Lorsque vous utilisez un décodeur en tant que MFT, le décodeur par défaut n’effectue pas de repli et n’offre pas de types de média de sortie pliés. Un décodeur agissant en tant que MFT effectue un repli uniquement si les coefficients de repli personnalisé sont définis à l’aide de la propriété de **\_ \_ \_ matrice MFPKEY WMADEC FOLDDOWN** .

Si la propriété de la **\_ \_ \_ matrice MFPKEY WMADEC FOLDDOWN** n’est pas définie sur la MFT du décodeur audio et que vous souhaitez effectuer un repli, vous pouvez utiliser (en tant que MFT) le processeur de signal numérique de reéchantillonneur audio.

La valeur de cette propriété est une chaîne contenant des coefficients de repli dans une liste séparée par des virgules de valeurs entières. La liste doit contenir un nombre d’entiers pour chaque canal dans le contenu encodé égal au nombre de canaux dans le contenu décodé.

Si le coefficient est égal à zéro, la valeur à utiliser dans la chaîne doit être « -2147483648 »; dans le cas contraire, la valeur est calculée à l’aide de l’équation : 20 \* 65536 \* log10 (x).

Les coefficients sont répertoriés dans l’ordre de masque de canal, comme défini par les constantes de masque de canal incluses dans le fichier d’en-tête mmreg. h. Par conséquent, les deux premières valeurs dans un pli de canal 6-à-2 représentent les portions du canal de sortie de gauche et le canal de sortie de droite qui sont constitués du canal de gauche central dans le flux de 6 canaux.

Vous devez définir cette propriété uniquement si les valeurs de repli fournies par l’auteur sont conservées avec le contenu encodé. Dans le cas contraire, laissez le décodeur effectuer ses propres calculs.

Le codec Windows Media Audio 10 Professional prend actuellement en charge le repli sur deux canaux uniquement.

Si la propriété [MFPKEY \_ WMADEC \_ SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md) est définie sur **DSSPEAKER \_ surround**, le codec ignore les coefficients de repli et de repli fournis par l’auteur jusqu’à un signal à 2 canaux qui peut être traité par le décodeur de matrice du récepteur. Cela permet à l’équipement surround d’offrir quatre canaux. Ce mode est pris en charge uniquement si la source est 5,1. Le codec peut uniquement plier 8 canaux à 2 canaux.

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

 

 
