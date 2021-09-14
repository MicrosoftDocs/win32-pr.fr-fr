---
title: Message TB_GETHOTITEM (commctrl. h)
description: Récupère l’index de l’élément réactif dans une barre d’outils.
ms.assetid: a87dbfc3-c6be-4a0a-9b6a-301b900d7929
keywords:
- TB_GETHOTITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829864cc9223ba15b49b1ecc623f294fd4a6b4fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116773"
---
# <a name="tb_gethotitem-message"></a>TO \_ GETHOTITEM message

Récupère l’index de l’élément réactif dans une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’index de l’élément réactif, ou-1 si aucun élément réactif n’est défini. Les contrôles Toolbar qui n’ont pas le style [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) n’ont pas d’éléments chauds.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





