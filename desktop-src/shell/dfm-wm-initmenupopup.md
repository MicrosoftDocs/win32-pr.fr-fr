---
description: DFM_WM_INITMENUPOPUP message-envoyé quand un menu déroulant ou un sous-menu est sur le paragraphe actif. Cela permet à une application de modifier le menu avant qu’il ne soit affiché, sans modifier le menu entier.
title: Message DFM_WM_INITMENUPOPUP (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 314e83f7-839d-4ca0-b5c1-842c5bf14923
api_name:
- DFM_WM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4cb68b8251fa383ae9386eae3e6753158330c4be7566f02a8758a72dfe05de03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943149"
---
# <a name="dfm_wm_initmenupopup-message"></a>\_Message DFM WM \_ INITMENUPOPUP

Envoyé lorsqu’un menu déroulant ou un sous-menu est sur le paragraphe actif. Cela permet à une application de modifier le menu avant qu’il ne soit affiché, sans modifier le menu entier.


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Handle vers le menu ou le sous-menu déroulant.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Le mot de poids faible spécifie la position relative de base zéro de l’élément de menu qui ouvre le menu déroulant ou le sous-menu.

Le mot de poids fort indique si le menu déroulant est le menu fenêtre. Si le menu est le menu fenêtre, ce paramètre a la **valeur true**; Sinon, la **valeur est false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




