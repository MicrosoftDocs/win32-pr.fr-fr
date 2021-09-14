---
description: Active ou désactive le mode aperçu, ce qui permet à l’application de remplacer la logique de mise en mémoire tampon initiale.
ms.assetid: 8aa8c6ac-8746-4bf6-9f57-b1426495a275
title: MFNETSOURCE_PREVIEWMODEENABLED, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1170135b0feb90a79bf5e26d36a02e262fdc1977
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127236105"
---
# <a name="mfnetsource_previewmodeenabled-property"></a>MFNETSOURCE \_ propriété PREVIEWMODEENABLED

Active ou désactive le mode aperçu, ce qui permet à l’application de remplacer la logique de mise en mémoire tampon initiale.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**Boolean**

VT \_ bool

**lVal**



## <a name="remarks"></a>Notes

La constante **MFNETSOURCE \_ PREVIEWMODEENABLED** définit le GUID de la clé de propriété. L’identificateur de propriété (PID) est égal à zéro. Cette propriété est définie sur la source réseau en passant un pointeur **IPropertyStore** vers le programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

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

 

 




