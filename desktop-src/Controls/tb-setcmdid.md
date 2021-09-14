---
title: Message TB_SETCMDID (commctrl. h)
description: Définit l’identificateur de commande d’un bouton de barre d’outils.
ms.assetid: 0674c905-2d9d-45d3-b565-2f3bcd7d6383
keywords:
- TB_SETCMDID les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_SETCMDID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f91cc4fd4d70e912bed3163cdf783e8e17ab463
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116594"
---
# <a name="tb_setcmdid-message"></a>TO \_ SETCMDID message

Définit l’identificateur de commande d’un bouton de barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro du bouton dont l’identificateur de commande doit être défini.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificateur de commande.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





