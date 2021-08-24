---
description: Indique si un récepteur multimédia prend en charge le workflow de données matérielles.
ms.assetid: 15838467-D253-4ECE-B9E7-AFD3A21B3AF2
title: Attribut MF_STREAM_SINK_SUPPORTS_HW_CONNECTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9f663c492e5ae15590cc9240762e90298122790fa350fae51d09dd1199f6d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714373"
---
# <a name="mf_stream_sink_supports_hw_connection-attribute"></a>Le \_ récepteur de flux MF \_ \_ prend en charge l' \_ attribut de \_ connexion matérielle

Indique si un récepteur multimédia prend en charge le workflow de données matérielles.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Remarques

Cet attribut est utilisé lorsqu’un récepteur multimédia transmet un périphérique matériel et est en mesure de recevoir des données sur un bus matériel. Par exemple, un décodeur audio matériel peut envoyer des données audio directement au matériel de rendu audio.

Dans ce scénario, le décodeur et le récepteur sont toujours représentés dans le Microsoft Media Foundation par une [transformation de Media Foundation](media-foundation-transforms.md) (MFT) et un récepteur multimédia. Toutefois, il n’y a pas de flux de données entre ces deux objets au niveau de la couche de pipeline, uniquement au niveau de la couche matérielle, comme indiqué dans le diagramme suivant.

![diagramme qui montre une source de proxy matériel.](images/proxy-mft4.png)

La connexion entre la table MFT et le récepteur multimédia est négociée comme suit.

1.  Le pipeline vérifie si la MFT est un proxy matériel, en vérifiant l’attribut d' [ \_ \_ \_ \_ attribut d’URL matériel de l’énumération MFT](mft-enum-hardware-url-attribute.md) sur la table MFT. Pour plus d’informations, consultez [Hardware MFTS](hardware-mfts.md).
2.  Le pipeline obtient un pointeur vers l’interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) du récepteur de flux sur le récepteur multimédia.
3.  Le pipeline utilise le pointeur [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pour interroger le \_ récepteur de flux MF \_ \_ prend en charge l' \_ attribut de \_ connexion matérielle. Si cet attribut est présent et qu’il est égal à **true**, la source du média prend en charge les connexions matérielles.
4.  Le pipeline définit l’attribut d' [ \_ \_ \_ attribut de flux connecté MFT](mft-connected-stream-attribute.md) sur le récepteur de flux. La valeur de cet attribut est le pointeur [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) à partir de la table MFT.
5.  Le pipeline affecte la **valeur true** à l’attribut [MFT \_ Connected \_ to \_ HW \_ Stream](mft-connected-to-hw-stream.md) à la fois dans le récepteur de flux et dans la table MFT.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




