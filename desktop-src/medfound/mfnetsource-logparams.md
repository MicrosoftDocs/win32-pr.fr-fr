---
description: Tableau de chaînes avec les paramètres à envoyer au serveur de journal.
ms.assetid: 36d711c7-a1ff-4ef2-b633-5f9f1662801e
title: MFNETSOURCE_LOGPARAMS, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec30f3f4d85f44905288601ba73ee6c246d8a9db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414113"
---
# <a name="mfnetsource_logparams-property"></a>MFNETSOURCE \_ propriété LOGPARAMS

Tableau de chaînes avec les paramètres à envoyer au serveur de journal.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**WCHAR\***

\_LPWStr VT

**pwszVal**



## <a name="remarks"></a>Notes

La constante **MFNETSOURCE \_ LOGPARAMS** définit le GUID de la clé de propriété. L’identificateur de propriété (PID) est égal à zéro. Pour définir cette propriété sur la source réseau, transmettez un pointeur **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

## <a name="requirements"></a>Spécifications



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
</dt> </dl>

 

 




