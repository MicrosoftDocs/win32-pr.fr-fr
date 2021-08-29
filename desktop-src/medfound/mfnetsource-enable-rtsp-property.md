---
description: Spécifie si le transport RTSP (Real-Time Streaming Protocol) est activé dans la source réseau.
ms.assetid: 299393d2-7949-48ef-a36d-19bb8760fc4e
title: MFNETSOURCE_ENABLE_RTSP, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba4c41315465718458cb74697057a45dfbaeb5215c3c9bf5a8958231360921a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113529"
---
# <a name="mfnetsource_enable_rtsp-property"></a>MFNETSOURCE \_ activer la \_ propriété RTSP

Spécifie si le transport RTSP (Real-Time Streaming Protocol) est activé dans la source réseau.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

Boolean (**long**)

VT \_

**lVal**



## <a name="remarks"></a>Remarques

La constante **MFNETSOURCE \_ Enable \_ RTSP** définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

Les applications peuvent utiliser cette propriété pour configurer la source réseau. Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Protocoles pris en charge](supported-protocols.md)
</dt> </dl>

 

 




