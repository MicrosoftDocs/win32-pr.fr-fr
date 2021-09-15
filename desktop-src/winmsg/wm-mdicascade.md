---
description: Une application envoie le \_ message WM MDICASCADE à une fenêtre cliente d’interface multidocument (MDI) pour réorganiser toutes ses fenêtres enfants dans un format en cascade.
ms.assetid: 33d04859-4220-40a6-be46-74a812a44ca8
title: Message WM_MDICASCADE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6208ce924ab6185399f3f673a435e1fbaca2741
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404490"
---
# <a name="wm_mdicascade-message"></a>\_Message WM MDICASCADE

Une application envoie le message **WM \_ MDICASCADE** à une fenêtre cliente d’interface multidocument (MDI) pour réorganiser toutes ses fenêtres enfants dans un format en cascade.


```C++
#define WM_MDICASCADE                   0x0227
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Comportement en cascade. Ce paramètre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                          | Signification                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="MDITILE_SKIPDISABLED"></span><span id="mditile_skipdisabled"></span><dl> <dt>**MDITILE \_ SKIPDISABLED**</dt> <dt>0x0002</dt> </dl> | Empêche la mise en cascade des fenêtres enfants MDI désactivées. <br/> |
| <span id="MDITILE_ZORDER"></span><span id="mditile_zorder"></span><dl> <dt>**MDITILE \_ ZORDER**</dt> , <dt>0x0004</dt> </dl>                   | Réorganise les fenêtres dans l’ordre de plan.<br/>                          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **bool**

Si le message est correctement exécuté, la valeur de retour est **true**.

Si le message échoue, la valeur de retour est **false**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_MDIICONARRANGE WM**](wm-mdiiconarrange.md)
</dt> <dt>

[**\_MDITILE WM**](wm-mditile.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Interface multidocument](multiple-document-interface.md)
</dt> </dl>

 

 




