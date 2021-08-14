---
description: Contient un pointeur vers l’interface IMFSourceOpenMonitor de l’application.
ms.assetid: 5b94ae87-91fc-49d6-9355-83327cfdb3f3
title: MFPKEY_SourceOpenMonitor, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45594e1929e66982d3e518c4ba098d2ca4b22e854e033dc69025aaf3ec5d5cc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872987"
---
# <a name="mfpkey_sourceopenmonitor-property"></a>MFPKEY \_ propriété SourceOpenMonitor

Contient un pointeur vers l’interface [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) de l’application.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**IUnknown** , pointeur

VT \_ inconnu

**punkVal**



## <a name="remarks"></a>Remarques

Les applications peuvent passer cette propriété au programme de résolution source pour recevoir des notifications d’événements à partir de la source réseau.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




