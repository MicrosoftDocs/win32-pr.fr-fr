---
title: Message EM_SETELLIPSISMODE (RichEdit. h)
description: Ce message définit le mode de sélection en cours.
ms.assetid: C77263E8-424B-4EDE-ACBF-BA85248FC31F
keywords:
- EM_SETELLIPSISMODE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3445172ea0a4ed4ef49e9a131db8d4357faaa5f7fef553169b7a8e1e795fd01c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019477"
---
# <a name="em_setellipsismode-message"></a>\_Message SETELLIPSISMODE em

Ce message définit le mode de sélection en cours. Quand cette option est activée, des points de suspension () s’affichent pour le texte qui ne tient pas dans la fenêtre d’affichage. Les points de suspension sont utilisés uniquement lorsque le contrôle n’est pas actif. Lorsqu’elles sont actives, les barres de défilement sont utilisées pour révéler le texte qui ne tient pas dans la fenêtre d’affichage.


```C++
#define EM_SETELLIPSISMODE       (WM_USER + 306)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur DWORD qui reçoit l’une des valeurs suivantes.



| Valeur                                                                                                                                                         | Signification                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <dt>**POINTS de suspension \_ aucun**</dt> </dl> | Aucun bouton de sélection n’est utilisé.<br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <dt>**fin des points de suspension \_**</dt> </dl>    | Points de suspension à la fin (arrêt forcé).<br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <dt>**mot de points de suspension \_**</dt> </dl> | Points de suspension à la fin (saut de mot).<br/>   |



 

Les bits de ces valeurs tiennent tous dans le **\_ masque des points de suspension**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si wParam est 0 et lParam est l’une des valeurs du tableau ci-dessus, la valeur de retour est égale à TRUE ; Sinon, la valeur de retour est FALSe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETELLIPSISMODE em**](em-getellipsismode.md)
</dt> <dt>

[**\_GETELLIPSISSTATE em**](em-getellipsisstate.md)
</dt> </dl>

 

 





