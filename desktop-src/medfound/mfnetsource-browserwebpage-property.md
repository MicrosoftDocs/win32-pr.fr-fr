---
description: Valeur de la &\# 0034 ; CS (référant) &\# 0034 ; champ que la source réseau utilise pour la journalisation.
ms.assetid: 328544b3-0d5f-4d1a-9ad1-ac38402d5898
title: MFNETSOURCE_BROWSERWEBPAGE, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6be6d64682f0f8d607e813927059360ff1273a33d87791fb7eab55ff10261e3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739034"
---
# <a name="mfnetsource_browserwebpage-property"></a>MFNETSOURCE \_ propriété BROWSERWEBPAGE

Valeur du champ « cs (référant) » que la source réseau utilise pour la journalisation. Les applications peuvent définir cette propriété sur l’URL de la page Web dans laquelle l’application a été incorporée.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

Chaîne de caractères larges (**WCHAR** \* )

\_LPWStr VT

**pwszVal**



## <a name="remarks"></a>Remarques

La constante **MFNETSOURCE \_ BROWSERWEBPAGE** définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

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

 

 




