---
description: Identificateur unique par lequel le serveur identifie le client.
ms.assetid: 490a2b03-aba8-4510-80c5-ca12f4037747
title: MFNETSOURCE_CLIENTGUID, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9585f5ac9cd69148272cb986746f6849aad4c3aa048b46baf2f75aeaba77c092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738988"
---
# <a name="mfnetsource_clientguid-property"></a>MFNETSOURCE \_ propriété CLIENTGUID

Identificateur unique par lequel le serveur identifie le client.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**GUID**

\_CLSID VT

**puuid**



## <a name="remarks"></a>Remarques

La constante **MFNETSOURCE \_ CLIENTGUID** définit le GUID de la clé de propriété. L’identificateur de propriété (PID) est égal à zéro. Pour définir cette propriété sur la source réseau, transmettez un pointeur **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

Si la valeur n’est pas définie ou définie en tant que **GUID \_ NULL**, Microsoft Media Foundation génère un GUID anonyme par session qui garantit la confidentialité de l’utilisateur.

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
</dt> </dl>

 

 




