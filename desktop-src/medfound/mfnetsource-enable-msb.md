---
description: Spécifie si le protocole de multidiffusion de diffusion multimédia en continu (MSB) est activé dans la source réseau.
ms.assetid: a46e3b4c-60be-4470-b9dc-041902c2563c
title: MFNETSOURCE_ENABLE_MSB, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1054b4a94bf966457ddeccc606fbd2fd2c8a1d5b3978b830b5e3c48f0f93b5ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243816"
---
# <a name="mfnetsource_enable_msb-property"></a>MFNETSOURCE \_ activer la \_ propriété MSB

Spécifie si le protocole de multidiffusion de diffusion multimédia en continu (MSB) est activé dans la source réseau.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**LONG**

VT \_

**lVal**



## <a name="remarks"></a>Notes

La constante **MFNETSOURCE \_ Enable \_ MSB** définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

Les applications peuvent utiliser cette propriété pour configurer la source réseau. Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

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
</dt> <dt>

[Protocoles pris en charge](supported-protocols.md)
</dt> </dl>

 

 




