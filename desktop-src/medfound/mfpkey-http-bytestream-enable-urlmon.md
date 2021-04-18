---
description: Permet à l’Microsoft Media Foundation flux d’octets HTTP d’utiliser des monikers d’URL (également appelé urlmon).
ms.assetid: 8B7D2FF7-D8A8-49E9-8CED-D37853B97A8F
title: MFPKEY_HTTP_ByteStream_Enable_Urlmon, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1858f34a5f719caba1a48f049b95f2031b400240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525984"
---
# <a name="mfpkey_http_bytestream_enable_urlmon-property"></a>MFPKEY \_ http \_ ByteStream \_ Enable \_ urlmon, propriété

Permet à l’Microsoft Media Foundation flux d’octets HTTP d’utiliser des monikers d’URL (également appelé *urlmon*).



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**VARIANT \_ booléen**

VT \_ bool

**boolVal**



## <a name="remarks"></a>Notes

Utilisez cette propriété pour configurer le flux d’octets HTTP Media Foundation. Pour définir la propriété, transmettez un pointeur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

Si la valeur est **\_ true**, le flux d’octets http utilise urlmon pour le transport http. Dans le cas contraire, si la valeur est **\_ false**, le flux d’octets utilise WinHTTP.

La valeur par défaut **est \_ true** pour les applications du Windows Store et la **variante \_ false** pour l’application de bureau Windows.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
