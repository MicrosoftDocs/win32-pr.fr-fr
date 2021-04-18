---
description: Spécifie si la source réseau envoie des demandes de renvoi UDP en réponse à des paquets perdus.
ms.assetid: 7956536d-9f3d-4875-8006-17e2cd577b61
title: MFNETSOURCE_RESENDSENABLED, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2646a9ef3e23fbcc9b3dff205f87d268115177
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519805"
---
# <a name="mfnetsource_resendsenabled-property"></a>MFNETSOURCE \_ propriété RESENDSENABLED

Spécifie si la source réseau envoie des demandes de renvoi UDP en réponse à des paquets perdus.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

Boolean (**long**)

VT \_

**lVal**



## <a name="remarks"></a>Notes

La constante **MFNETSOURCE \_ RESENDSENABLED** définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

Les applications peuvent utiliser cette propriété pour configurer la source réseau. Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

La valeur par défaut de cette propriété est **true**.

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

 

 




