---
description: Stocke la chaîne envoyée dans l’en-tête Accept-Language.
ms.assetid: b6ac613c-099b-4415-84ad-c0f8ad5f667b
title: MFNETSOURCE_STREAM_LANGUAGE, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c44b6f55fd2f5652a41d9aa5eed76e60e73152343d2baf6c577be56bc462c94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344539"
---
# <a name="mfnetsource_stream_language-property"></a>MFNETSOURCE \_ , \_ propriété de langage de flux

Stocke la chaîne envoyée dans l’en-tête Accept-Language.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**WCHAR\***

\_LPWStr VT

**pwszVal**



## <a name="remarks"></a>Remarques

La \_ constante MFNETSOURCE Stream \_ Language définit le GUID de la clé de propriété. L’identificateur de propriété (PID) est égal à zéro. Pour définir cette propriété sur la source réseau, transmettez un pointeur **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




