---
title: Message TB_INSERTMARKHITTEST (commctrl. h)
description: Récupère les informations sur les marques d’insertion pour un point dans une barre d’outils.
ms.assetid: 65c64fd0-f089-4b1a-84e5-1a3e10aa7f5e
keywords:
- TB_INSERTMARKHITTEST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5237d5a13250c3eb95bfe741415a9da245585c78
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116673"
---
# <a name="tb_insertmarkhittest-message"></a>TO \_ INSERTMARKHITTEST message

Récupère les informations sur les marques d’insertion pour un point dans une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Pointeur vers une structure de [**points**](/previous-versions//dd162805(v=vs.85)) qui contient les coordonnées de test de positionnement par rapport à la zone cliente de la barre d’outils.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) qui reçoit les informations sur les marques d’insertion.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur différente de zéro si le point est une marque d’insertion, ou zéro dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

