---
description: Spécifie si tous les protocoles de téléchargement sont activés.
ms.assetid: c178693f-44ea-481e-b7f2-2ec94eea1994
title: MFNETSOURCE_ENABLE_DOWNLOAD, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1b57d8ab984f7c198d1c1b43455f2d0d5dda68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034103"
---
# <a name="mfnetsource_enable_download-property"></a>MFNETSOURCE \_ activer la \_ propriété de téléchargement

Spécifie si tous les protocoles de téléchargement sont activés.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

Boolean (**long**)

VT \_

**lVal**



## <a name="remarks"></a>Notes

La constante **MFNETSOURCE \_ Enable \_ Download** définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

Les applications peuvent utiliser cette propriété pour configurer la source réseau. Pour définir la propriété, transmettez un pointeur **IPropertyStore** à la [configuration d’une source de média](configuring-a-media-source.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Protocoles pris en charge](supported-protocols.md)
</dt> </dl>

 

 




