---
description: Envoyé par un flux d’octets lorsque les caractéristiques du flux d’octets ont changé.
ms.assetid: EC34A7A3-BF01-4F9E-BA79-131B76D4C58F
title: Événement MEByteStreamCharacteristicsChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e626f510927970aad3c51182fca3a6dfddb0009
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531841"
---
# <a name="mebytestreamcharacteristicschanged-event"></a>Événement MEByteStreamCharacteristicsChanged

Envoyé par un flux d’octets lorsque les caractéristiques du flux d’octets ont changé.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE               | Description                           |
|-----------------------|---------------------------------------|
| VT \_ vide <br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="remarks"></a>Notes

Cet événement indique qu’une ou plusieurs des caractéristiques suivantes ont été modifiées :

-   Indicateurs de capacité ([**IMFByteStream :: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities))
-   Indicateur de fin de flux ([**IMFByteStream :: IsEndOfStream**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-isendofstream))
-   Longueur ([**IMFByteStream :: GetLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getlength))

Toutes les implémentations de [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) ne prennent pas en charge cet événement. Pour recevoir l’événement, interrogez l’objet de flux d’octets de l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




