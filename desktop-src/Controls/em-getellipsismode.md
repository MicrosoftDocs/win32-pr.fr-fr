---
title: Message EM_GETELLIPSISMODE (RichEdit. h)
description: Récupère le mode de sélection en cours.
ms.assetid: 01A755F3-6C6E-4974-9866-76BF15E0F3AD
keywords:
- EM_GETELLIPSISMODE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6706c2b6ee75852fd0b3ee7a1a9d18b25d20d242d72068ba073d1bb025ff8ed5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019697"
---
# <a name="em_getellipsismode-message"></a>\_Message GETELLIPSISMODE em

Récupère le mode de sélection en cours. Quand cette option est activée, des points de suspension () s’affichent pour le texte qui ne tient pas dans la fenêtre d’affichage. Les points de suspension sont utilisés uniquement lorsque le contrôle n’est pas actif. Lorsqu’elles sont actives, les barres de défilement sont utilisées pour révéler le texte qui ne tient pas dans la fenêtre d’affichage.


```C++
#define EM_GETELLIPSISMODE       (WM_USER + 305)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une valeur DWORD qui reçoit l’une des valeurs suivantes.



| Valeur                                                                                                                                                         | Signification                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <dt>**POINTS de suspension \_ aucun**</dt> </dl> | Aucun bouton de sélection n’est utilisé.<br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <dt>**fin des points de suspension \_**</dt> </dl>    | Points de suspension à la fin (arrêt forcé).<br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <dt>**mot de points de suspension \_**</dt> </dl> | Points de suspension à la fin (saut de mot).<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si wParam est 0 et lParam n’est pas NULL, la valeur de retour est égale à TRUE ; Sinon, la valeur de retour est FALSe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETELLIPSISMODE em**](em-setellipsismode.md)
</dt> <dt>

[**\_GETELLIPSISSTATE em**](em-getellipsisstate.md)
</dt> </dl>

 

 





