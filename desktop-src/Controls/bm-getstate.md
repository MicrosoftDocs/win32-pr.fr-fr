---
title: Message BM_GETSTATE (winuser. h)
description: Récupère l’état d’un bouton ou d’une case à cocher. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ GetState macro.
ms.assetid: ca4c2f1a-b657-490a-ac8b-5f0cfef64d76
keywords:
- BM_GETSTATE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- BM_GETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd44921c61477e26cd5570fcbaa6f96a4e61f96ee22ad1c705bf553788d8cfba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674839"
---
# <a name="bm_getstate-message"></a>\_Message GETSTATE BM

Récupère l’état d’un bouton ou d’une case à cocher. Vous pouvez envoyer ce message de manière explicite ou utiliser le [**bouton \_ GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) macro.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour spécifie l’état actuel du bouton. Il s’agit d’une combinaison des valeurs suivantes.



| Code de retour                                                                                        | Description                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BST \_ vérifié**</dt> </dl>        | Le bouton est activé.<br/>                                                                                                                                                                                        |
| <dl> <dt>**BST \_ DROPDOWNPUSHED**</dt> </dl> | [Windows Vista](common-control-versions.md). Le bouton est dans l’État déroulant. S’applique uniquement si le bouton a le style de [**\_ liste déroulante TBSTYLE**](toolbar-control-and-button-styles.md) .<br/> |
| <dl> <dt>**\_focus BST**</dt> </dl>          | Le bouton a le focus clavier.<br/>                                                                                                                                                                            |
| <dl> <dt>**BST \_ chaud**</dt> </dl>            | Le bouton est actif ; autrement dit, la souris pointe dessus.<br/>                                                                                                                                                    |
| <dl> <dt>**BST \_ indéterminé**</dt> </dl>  | L’état du bouton est indéterminé. S’applique uniquement si le bouton a le style [**BS \_ 3STATE**](button-styles.md) ou [**BS \_ AUTO3STATE**](button-styles.md) .<br/>                    |
| <dl> <dt>**BST \_ poussé**</dt> </dl>         | Le bouton est affiché dans l’État pushd.<br/>                                                                                                                                                                |
| <dl> <dt>**BST \_ désactivé**</dt> </dl>      | Aucun état spécial. Équivalent à zéro.<br/>                                                                                                                                                                         |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETCHECK BM**](bm-getcheck.md)
</dt> <dt>

[**BM \_ SETSTATE**](bm-setstate.md)
</dt> </dl>

 

 





