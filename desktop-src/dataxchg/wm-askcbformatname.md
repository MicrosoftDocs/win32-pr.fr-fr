---
title: Message WM_ASKCBFORMATNAME (winuser. h)
description: Envoyé au propriétaire du presse-papiers par une fenêtre de la visionneuse du presse-papiers pour demander le nom d’un \_ format de presse-papiers CF OWNERDISPLAY.
ms.assetid: eee026ec-58db-41b3-9705-30a17eebbd70
keywords:
- WM_ASKCBFORMATNAME des données de message Exchange
topic_type:
- apiref
api_name:
- WM_ASKCBFORMATNAME
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe96a2ddf4e6767c083ec2e3f4e3fc61bdde902ff93ce9a162ec7e93eb5bef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991239"
---
# <a name="wm_askcbformatname-message"></a>\_Message WM ASKCBFORMATNAME

Envoyé au propriétaire du presse-papiers par une fenêtre de la visionneuse du presse-papiers pour demander le nom d’un format de presse-papiers [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) .

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_ASKCBFORMATNAME              0x030C
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Taille, en caractères, de la mémoire tampon vers laquelle pointe le paramètre *lParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la mémoire tampon qui doit recevoir le nom du format du presse-papiers.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Remarques

En réponse à ce message, le propriétaire du presse-papiers doit copier le nom du format d’affichage du propriétaire dans la mémoire tampon spécifiée, sans dépasser la taille de la mémoire tampon spécifiée par le paramètre *wParam* .

Une fenêtre de la visionneuse du presse-papiers envoie ce message au propriétaire du presse-papiers pour déterminer le nom du format [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) , par exemple, pour initialiser un menu répertoriant les formats disponibles.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du presse-papiers](clipboard.md)
</dt> </dl>

 

