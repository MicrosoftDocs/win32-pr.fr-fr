---
description: Liste des URL auxquelles la source réseau enverra les informations de journalisation.
ms.assetid: 772c5b57-273d-4289-9229-ef7a199c6473
title: MFNETSOURCE_LOGURL, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b855475e17264682ffc49a391894bb6acc6a721712b8ce6e4c01d98b1d216d48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874633"
---
# <a name="mfnetsource_logurl-property"></a>MFNETSOURCE \_ propriété LOGURL

Liste des URL auxquelles la source réseau enverra les informations de journalisation.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

Tableau de chaînes de caractères larges (**CALPWSTR**)

\_LPWStr VT Vector \| VT \_

**calpwstr**



## <a name="remarks"></a>Remarques

La constante **MFNETSOURCE \_ LOGURL** définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

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

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




