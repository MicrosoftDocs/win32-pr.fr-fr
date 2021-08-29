---
description: Spécifie la bande passante de lien pour la source réseau, en bits par seconde.
ms.assetid: 1b71dce1-8744-4114-9629-2a9d0afb7c43
title: MFNETSOURCE_CONNECTIONBANDWIDTH, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd12a36db2529001d96729c2f019c017b333585c215106b4051a4deb7995a9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113559"
---
# <a name="mfnetsource_connectionbandwidth-property"></a>MFNETSOURCE \_ propriété CONNECTIONBANDWIDTH

Spécifie la bande passante de lien pour la source réseau, en bits par seconde.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**DWORD** (stocké en tant que **long**)

VT \_

**lVal**



## <a name="remarks"></a>Remarques

La constante **MFNETSOURCE \_ CONNECTIONBANDWIDTH** définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

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

[Fonctionnalités de la source réseau](network-source-features.md)
</dt> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




