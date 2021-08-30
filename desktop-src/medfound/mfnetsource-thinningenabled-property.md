---
description: Spécifie si le basculement de flux est activé sur la source réseau.
ms.assetid: 691a3549-eaf8-4e3d-ad0e-e5b013658f78
title: MFNETSOURCE_THINNINGENABLED, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cfe92e09e9f772d7506cf944a8b2de793048d71e3ed8d893f534e919d4877ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940195"
---
# <a name="mfnetsource_thinningenabled-property"></a>MFNETSOURCE \_ propriété THINNINGENABLED

Spécifie si le basculement de flux est activé sur la source réseau. Le basculement de flux permet au serveur multimédia de modifier les flux dans un fichier à débit binaire multiple (MBR), en fonction de la bande passante disponible.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

Boolean (**long**)

VT \_

**lVal**



## <a name="remarks"></a>Remarques

La constante **MFNETSOURCE \_ THINNINGENABLED** définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

Les applications peuvent utiliser cette propriété pour configurer la source réseau. Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

La valeur par défaut de cette propriété est **true**.

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
</dt> </dl>

 

 




