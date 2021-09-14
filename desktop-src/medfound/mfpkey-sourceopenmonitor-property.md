---
description: Contient un pointeur vers l’interface IMFSourceOpenMonitor de l’application.
ms.assetid: 5b94ae87-91fc-49d6-9355-83327cfdb3f3
title: MFPKEY_SourceOpenMonitor, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a49826ee16a733993b9052e12d9e6fcd5003410
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313794"
---
# <a name="mfpkey_sourceopenmonitor-property"></a>MFPKEY \_ propriété SourceOpenMonitor

Contient un pointeur vers l’interface [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) de l’application.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**IUnknown** , pointeur

VT \_ inconnu

**punkVal**



## <a name="remarks"></a>Notes

Les applications peuvent passer cette propriété au programme de résolution source pour recevoir des notifications d’événements à partir de la source réseau.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




