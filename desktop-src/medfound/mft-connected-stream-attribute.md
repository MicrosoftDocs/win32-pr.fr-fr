---
description: Contient un pointeur vers les attributs de flux du flux connecté sur une table de Media Foundation matérielle (MFT).
ms.assetid: 7e14a02e-4cbf-45aa-a6f5-2c53b2437127
title: Attribut MFT_CONNECTED_STREAM_ATTRIBUTE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b182cbed78f5f9851b621de72bf691bf698b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863962"
---
# <a name="mft_connected_stream_attribute-attribute"></a>Attribut de l' \_ \_ attribut de flux connecté MFT \_

Contient un pointeur vers les attributs de flux du flux connecté sur une table de Media Foundation matérielle (MFT).

## <a name="data-type"></a>Type de données

**IMFAttributes \** _ stocké en tant que _*IUnknown \**_

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetUnknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Notes

En général, les applications n’utilisent pas cet attribut.

Cet attribut est utilisé pour les MFTs qui agissent en tant que proxys sur un périphérique matériel. Pour plus d’informations, consultez [Hardware MFTS](hardware-mfts.md).

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFT \_ connecté \_ au \_ flux de matériel \_](mft-connected-to-hw-stream.md)
</dt> <dt>

[Matériel MFTs](hardware-mfts.md)
</dt> <dt>

[Attributs de transformation](transform-attributes.md)
</dt> </dl>

 

 




