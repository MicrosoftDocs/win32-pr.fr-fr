---
description: Spécifie si un gestionnaire de flux d’octets peut utiliser un flux d’octets ouvert pour l’écriture par un autre thread.
ms.assetid: d9d97880-a563-420c-b598-c3ebd1ae8b74
title: Attribut MF_BYTESTREAMHANDLER_ACCEPTS_SHARE_WRITE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b46a3402585cbce9c1d1464ceb9fb161527673c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414227"
---
# <a name="mf_bytestreamhandler_accepts_share_write-attribute"></a>MF \_ BYTESTREAMHANDLER \_ accepte \_ l' \_ attribut d’écriture de partage

Spécifie si un gestionnaire de flux d’octets peut utiliser un flux d’octets ouvert pour l’écriture par un autre thread.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Notes

Les gestionnaires de flux d’octets peuvent prendre en charge cet attribut. Pour obtenir ou définir l’attribut, interrogez d’abord le gestionnaire de flux d’octets de l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Appelez ensuite [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) ou [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

Si cet attribut a la **valeur true**, cela signifie que le gestionnaire de flux d’octets peut lire à partir d’un flux, tandis qu’un autre thread écrit dans le même flux. Lorsqu’un flux est ouvert en écriture par un autre thread, la méthode [**IMFByteStream :: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) retourne l’indicateur d' **\_ \_ écriture de partage MFBYTESTREAM** .

Cet attribut affecte la résolution de la source. Si l’indicateur **MFBYTESTREAM \_ share \_ Write** est défini pour un flux d’octets, le programme de [résolution source](source-resolver.md) ne passe pas ce flux à un gestionnaire de flux d’octets, à moins que le gestionnaire MF \_ BYTESTREAMHANDLER \_ accepte l' \_ \_ attribut share Write défini sur **true**.

L’indicateur **MFBYTESTREAM \_ share \_ Write** indique que la longueur du flux peut changer pendant que le gestionnaire la lit.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Gestionnaires de schémas et gestionnaires de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)
</dt> </dl>

 

 




