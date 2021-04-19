---
description: Le \_ message WM CTLCOLOR est utilisé dans les versions 16 bits de Windows pour modifier le jeu de couleurs des zones de liste, les zones de liste des zones de liste déroulante, les boîtes de message, les contrôles de bouton, les contrôles d’édition, les contrôles statiques et les boîtes de dialogue. Remarque pour plus d’informations sur ce message et les versions 32 bits de Windows, consultez la section Notes.
ms.assetid: e654cf48-550f-4210-9952-20470b9a397a
title: Message WM_CTLCOLOR (WindowsX. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8166979c17b7d2eef50af062e5df13712e9d32ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528756"
---
# <a name="wm_ctlcolor-message"></a>\_Message WM CTLCOLOR

Le message **WM \_ CTLCOLOR** est utilisé dans les versions 16 bits de Windows pour modifier le jeu de couleurs des zones de liste, les zones de liste des zones de liste déroulante, les boîtes de message, les contrôles de bouton, les contrôles d’édition, les contrôles statiques et les boîtes de dialogue.

> [!Note]  
> Pour plus d’informations sur ce message et les versions 32 bits de Windows, consultez la section Notes.

 


```C++
  WM_CTLCOLOR

  WPARAM wParam;
  LPARAM lParam;
    
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de la fenêtre de destination.

</dd> <dt>

*wParam* 
</dt> <dd>

Handle d’un contexte d’affichage (DC).

</dd> <dt>

*lParam* 
</dt> <dd>

Handle d’une fenêtre enfant (contrôle).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle retourne un handle à un pinceau. Le système utilise le pinceau pour peindre l’arrière-plan du contrôle.

## <a name="remarks"></a>Notes

Le message **WM \_ CTLCOLOR** de Windows 16 bits a été remplacé par des notifications plus spécifiques. Ces remplacements sont les suivants :

-   [**\_CTLCOLORBTN WM**](../controls/wm-ctlcolorbtn.md)
-   [**\_CTLCOLOREDIT WM**](../controls/wm-ctlcoloredit.md)
-   [**\_CTLCOLORDLG WM**](../dlgbox/wm-ctlcolordlg.md)
-   [**\_CTLCOLORLISTBOX WM**](../controls/wm-ctlcolorlistbox.md)
-   [**\_CTLCOLORSCROLLBAR WM**](../controls/wm-ctlcolorscrollbar.md)
-   [**\_CTLCOLORSTATIC WM**](../controls/wm-ctlcolorstatic.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WindowsX. h</dt> </dl> |



 

 
