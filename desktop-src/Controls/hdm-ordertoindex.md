---
title: Message HDM_ORDERTOINDEX (commctrl. h)
description: Récupère une valeur d’index pour un élément en fonction de son ordre dans le contrôle d’en-tête. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ OrderToIndex.
ms.assetid: vs|controls|~\controls\header\messages\hdm_ordertoindex.htm
keywords:
- HDM_ORDERTOINDEX les contrôles de Windows de message
topic_type:
- apiref
api_name:
- HDM_ORDERTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b65d10fb27c9a07639ebbd5770a53d72cbf0aba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006269"
---
# <a name="hdm_ordertoindex-message"></a>\_Message HDM ORDERTOINDEX

Récupère une valeur d’index pour un élément en fonction de son ordre dans le contrôle d’en-tête. Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ OrderToIndex**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ordre dans lequel l’élément apparaît dans le contrôle d’en-tête, de gauche à droite. Par exemple, la valeur d’index de l’élément dans la colonne la plus à gauche serait 0. La valeur de l’élément suivant à droite est 1, et ainsi de suite.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne INT qui indique l’index de l’élément. Si *wParam* n’est pas valide (valeur négative ou trop grande), le retour est égal à *wParam*.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





