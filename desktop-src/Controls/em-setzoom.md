---
title: Message EM_SETZOOM (RichEdit. h)
description: Définit le facteur de zoom. Le ratio doit être une valeur comprise entre 1/64 et 64. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.
ms.assetid: 6cdec5b8-4ce7-4fd5-8083-4daa63d17f63
keywords:
- EM_SETZOOM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecf6541bc018df253a3ed45f8bced42e2f19938449d7fc35bf7f309909d53a3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437179"
---
# <a name="em_setzoom-message"></a>\_Message SETZOOM em

Définit le taux de zoom pour un contrôle d’édition multiligne ou un contrôle RichEdit. Le ratio doit être une valeur comprise entre 1/64 et 64. Le contrôle d’édition doit avoir le jeu de styles étendus **es \_ ex \_ zoomable** . pour que ce message ait un effet, consultez [modifier les styles étendus de contrôle](edit-control-window-extended-styles.md).

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Numérateur du rapport de zoom.

</dd> <dt>

*lParam* 
</dt> <dd>

Dénominateur du rapport de zoom. Ces paramètres peuvent avoir les valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                              | Signification                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Both_0"></span><span id="both_0"></span><span id="BOTH_0"></span><dl> <dt>**Les deux**</dt> </dl>                                                                                                   | Désactive le zoom à l’aide du **message \_ SETZOOM em** (le zoom peut encore se produire à l’aide de [**TxGetExtent**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)).<br/> |
| <span id="1_64____wParam___lParam____64"></span><span id="1_64____wparam___lparam____64"></span><span id="1_64____WPARAM___LPARAM____64"></span><dl> <dt>**1/64 < (wParam/lParam) < 64**</dt> </dl> | Zooms affichés par le numérateur/dénominateur du rapport de zoom<br/>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le nouveau paramètre de zoom est accepté, la valeur de retour est **true**.

Si le nouveau paramètre de zoom n’est pas accepté, la valeur de retour est **false**.

## <a name="remarks"></a>Remarques

**Modifier :** pris en charge dans Windows 10 1809 et versions ultérieures. Le contrôle d’édition doit avoir le jeu de styles étendus **es \_ ex \_ zoomable** . pour que ce message ait un effet, consultez [modifier les styles étendus de contrôle](edit-control-window-extended-styles.md). Pour plus d’informations sur le contrôle d’édition, consultez [modifier des contrôles](about-edit-controls.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | Édition enrichie 3,0<br/>                                                              |
| En-tête<br/>                   | <dl> <dt>RichEdit. h/commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETZOOM em**](em-getzoom.md)
</dt> </dl>

 

 





