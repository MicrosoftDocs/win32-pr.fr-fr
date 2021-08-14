---
title: Message TB_SETHOTITEM (commctrl. h)
description: 'TB_SETHOTITEM message : définit l’élément réactif dans une barre d’outils.'
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- TB_SETHOTITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a48de58e07d877d999c2d0388bf32845fce349511da563c3a6b1fa9f9c7b3d20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318839"
---
# <a name="tb_sethotitem-message"></a>TO \_ SETHOTITEM message

Définit l’élément réactif dans une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’élément qui sera rendu chaud. Si cette valeur est-1, aucun des éléments n’est chaud.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index de l’élément réactif précédent, ou-1 s’il n’y a pas d’élément réactif.

## <a name="remarks"></a>Remarques

Le comportement de ce message n’est pas défini pour les barres d’outils qui n’ont pas le style [**\_ plat TBSTYLE**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





