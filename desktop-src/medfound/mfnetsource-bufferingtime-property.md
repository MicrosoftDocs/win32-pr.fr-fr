---
description: Nombre de secondes de données que la source réseau met en mémoire tampon au démarrage.
ms.assetid: 186b55fc-d1b1-4187-a748-efaee114eca9
title: MFNETSOURCE_BUFFERINGTIME, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b6de79344913d77a30dc05dcad4e4f8dd3608e0d35009b1d8e5254e08790993
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243806"
---
# <a name="mfnetsource_bufferingtime-property"></a>MFNETSOURCE \_ propriété BUFFERINGTIME

Nombre de secondes de données que la source réseau met en mémoire tampon au démarrage.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**DWORD** (stocké en tant que **long**)

VT \_

**lVal**



## <a name="remarks"></a>Notes

La constante **MFNETSOURCE \_ BUFFERINGTIME** définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

Les applications peuvent utiliser cette propriété pour configurer la source réseau. Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

La valeur par défaut de cette propriété est de 5 secondes.

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

[Fonctionnalités de la source réseau](network-source-features.md)
</dt> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




