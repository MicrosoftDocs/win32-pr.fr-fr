---
description: Valeur de la &\# 0034 ; c-hostexever&\# 0034 ; le champ que la source réseau utilise pour la journalisation.
ms.assetid: eee93457-483d-41dc-91c5-c12382d03152
title: MFNETSOURCE_HOSTVERSION, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5f78a277de4fc5b0609be31f21f684357806dbb8609657a930cdc4816b1e43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243459"
---
# <a name="mfnetsource_hostversion-property"></a>MFNETSOURCE \_ propriété HOSTVERSION

Valeur du champ « c-hostexever » que la source réseau utilise pour la journalisation. Les applications peuvent affecter à cette propriété le numéro de version de l’application hôte. L’application hôte est le fichier .exe identifié par le champ c-hostexe.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**LONGLONG**

Le \_ i8 VT

**hVal**



## <a name="remarks"></a>Notes

La constante **MFNETSOURCE \_ HOSTVERSION** définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

Les applications peuvent utiliser cette propriété pour configurer la source réseau. Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Journalisation du client](client-logging.md)
</dt> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




