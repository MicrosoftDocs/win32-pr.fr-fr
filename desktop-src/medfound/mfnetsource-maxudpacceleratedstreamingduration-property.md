---
description: Durée maximale de la diffusion en continu accélérée, en millisecondes, lorsque la source réseau utilise le transport UDP.
ms.assetid: d5f3064a-b222-4f72-b889-cd88c14a239c
title: MFNETSOURCE_MAXUDPACCELERATEDSTREAMINGDURATION, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2621e01203ba81b54e565f86953df64304c9bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035189"
---
# <a name="mfnetsource_maxudpacceleratedstreamingduration-property"></a>MFNETSOURCE \_ propriété MAXUDPACCELERATEDSTREAMINGDURATION

Durée maximale de la diffusion en continu accélérée, en millisecondes, lorsque la source réseau utilise le transport UDP.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**DWORD** (stocké en tant que **long**)

VT \_

**lVal**



## <a name="remarks"></a>Notes

La constante **MFNETSOURCE \_ MAXUDPACCELERATEDSTREAMINGDURATION** définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

Pour le transport UDP, cette propriété remplace la propriété [**MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) si la valeur de cette propriété est inférieure.

Les applications peuvent utiliser cette propriété pour configurer la source réseau. Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

La valeur par défaut de cette propriété est 8 000 millisecondes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Fonctionnalités de la source réseau](network-source-features.md)
</dt> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




