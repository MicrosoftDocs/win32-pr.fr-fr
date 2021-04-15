---
description: Valeur de la &\# 0034 ; c-hostexever&\# 0034 ; le champ que la source réseau utilise pour la journalisation.
ms.assetid: eee93457-483d-41dc-91c5-c12382d03152
title: MFNETSOURCE_HOSTVERSION, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f10c1a66bc2ab52455140733a6b60f25863c8f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485201"
---
# <a name="mfnetsource_hostversion-property"></a>MFNETSOURCE \_ propriété HOSTVERSION

Valeur du champ « c-hostexever » que la source réseau utilise pour la journalisation. Les applications peuvent affecter à cette propriété le numéro de version de l’application hôte. L’application hôte est le fichier. exe identifié par le champ c-hostexe.



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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Journalisation du client](client-logging.md)
</dt> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




