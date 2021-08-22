---
description: Active ou désactive le mode aperçu, ce qui permet à l’application de remplacer la logique de mise en mémoire tampon initiale.
ms.assetid: 8aa8c6ac-8746-4bf6-9f57-b1426495a275
title: MFNETSOURCE_PREVIEWMODEENABLED, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e03940828c6fa32b9e0367a03f960d4d64d88edf691100817ed31883013ce1b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663859"
---
# <a name="mfnetsource_previewmodeenabled-property"></a>MFNETSOURCE \_ propriété PREVIEWMODEENABLED

Active ou désactive le mode aperçu, ce qui permet à l’application de remplacer la logique de mise en mémoire tampon initiale.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**Boolean**

VT \_ bool

**lVal**



## <a name="remarks"></a>Remarques

La constante **MFNETSOURCE \_ PREVIEWMODEENABLED** définit le GUID de la clé de propriété. L’identificateur de propriété (PID) est égal à zéro. Cette propriété est définie sur la source réseau en passant un pointeur **IPropertyStore** vers le programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

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

 

 




