---
description: Définit une fenêtre pour le flux d’octets HTTP Microsoft Media Foundation.
ms.assetid: 52761AC1-4974-4087-B5EE-A797F5BAD86D
title: MFPKEY_HTTP_ByteStream_Urlmon_Window, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df398d2c6d7655a68a139545d84cee48f9cf7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526656"
---
# <a name="mfpkey_http_bytestream_urlmon_window-property"></a>MFPKEY \_ http \_ ByteStream \_ urlmon, propriété de la \_ fenêtre

Définit une fenêtre pour le flux d’octets HTTP Microsoft Media Foundation. La fenêtre est utilisée pour présenter des informations dans l’interface utilisateur pendant une opération de liaison.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**IUnknown\***

VT \_ inconnu

**punkVal**



## <a name="remarks"></a>Notes

Utilisez cette propriété pour configurer le flux d’octets HTTP Media Foundation. Pour définir la propriété, transmettez un pointeur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

La valeur de cette propriété est un pointeur vers l’interface **IWindowForBindingUI** . Cette propriété s’applique uniquement lorsque la propriété [MFPKEY \_ http \_ ByteStream \_ Enable \_ urlmon](mfpkey-http-bytestream-enable-urlmon.md) a la valeur **Variant \_ true**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
