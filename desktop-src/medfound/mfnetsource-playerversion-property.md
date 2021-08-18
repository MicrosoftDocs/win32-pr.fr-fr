---
description: Valeur de la &\# 0034 ; c-playerversion&\# 0034 ; le champ que la source réseau utilise pour la journalisation.
ms.assetid: 7bc485de-345b-475c-bbae-0776aa63c93a
title: MFNETSOURCE_PLAYERVERSION, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71828db44eca7c4318dbdb11e7934871911b06dbc4547f83723a9944f139ae26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738968"
---
# <a name="mfnetsource_playerversion-property"></a>MFNETSOURCE \_ propriété PLAYERVERSION

Valeur du champ « c-playerversion » que la source réseau utilise pour la journalisation. Les applications peuvent affecter à cette propriété le numéro de version de l’application.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**LONGLONG**

Le \_ i8 VT

**hVal**



## <a name="remarks"></a>Remarques

La constante **MFNETSOURCE \_ PLAYERVERSION** définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

Les applications peuvent utiliser cette propriété pour configurer la source réseau. Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez la page programme de [résolution source](source-resolver.md).

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

 

 




