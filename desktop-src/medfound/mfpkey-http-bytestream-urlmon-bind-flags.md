---
description: Définit les indicateurs de liaison du moniker pour le flux d’octets HTTP Microsoft Media Foundation.
ms.assetid: 9426D235-65E1-40BA-94E9-CF0C49263E6F
title: MFPKEY_HTTP_ByteStream_Urlmon_Bind_Flags, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aafbc2c32491caa327b1f7a54d4c9738dddf9dde3ad08efcd4eb075cd37995d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117690134"
---
# <a name="mfpkey_http_bytestream_urlmon_bind_flags-property"></a>MFPKEY \_ http \_ ByteStream \_ urlmon \_ - \_ propriété indicateurs de liaison

Définit les indicateurs de liaison du moniker pour le flux d’octets HTTP Microsoft Media Foundation.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Remarques

Utilisez cette propriété pour configurer le flux d’octets HTTP Media Foundation. Pour définir la propriété, transmettez un pointeur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

La valeur de cette propriété est une opération **or au niveau du** bit de l’énumération **BINDF** . Cette propriété s’applique uniquement lorsque la propriété [MFPKEY \_ http \_ ByteStream \_ Enable \_ urlmon](mfpkey-http-bytestream-enable-urlmon.md) a la valeur **Variant \_ true**.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
