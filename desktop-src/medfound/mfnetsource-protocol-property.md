---
description: Spécifie le protocole de contrôle utilisé par la source réseau.
ms.assetid: 4de8b8ba-97d9-4269-a16c-1853dc02f674
title: MFNETSOURCE_PROTOCOL, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae15ce40e7c049552cbb0f4916f5f4ff70ef6e55746528ebe0083eee69b22a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243321"
---
# <a name="mfnetsource_protocol-property"></a>\_Propriété de protocole MFNETSOURCE

Spécifie le protocole de contrôle utilisé par la source réseau. La valeur de cette propriété est un membre de l’énumération du [**\_ \_ type de protocole MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**LONG**

VT \_

**lVal**



## <a name="remarks"></a>Notes

Le **\_ protocole MFNETSOURCE** constant définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

Cette propriété est en lecture seule. Pour récupérer cette propriété, interrogez la source réseau de l’interface **IPropertyStore** et appelez **IPropertyStore :: GetValue**.

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

 

 




