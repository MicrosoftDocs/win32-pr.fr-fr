---
title: Message TB_HITTEST (commctrl. h)
description: Détermine où un point se trouve dans un contrôle de barre d’outils.
ms.assetid: d08f3805-2042-470e-8f5a-8a6a681d1189
keywords:
- TB_HITTEST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6264bc0191f091d3819081ddd67e428b64c84570
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116682"
---
# <a name="tb_hittest-message"></a>TO \_ message HITTEST

Détermine où un point se trouve dans un contrôle de barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure de [**points**](/previous-versions//dd162805(v=vs.85)) qui contient la coordonnée x du test d’atteinte dans le membre **x** et la coordonnée y du test de positionnement dans le membre **y** . Les coordonnées sont relatives à la zone cliente de la barre d’outils.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur entière. Si la valeur de retour est zéro ou une valeur positive, il s’agit de l’index de base zéro de l’élément de non-séparateur dans lequel se trouve le point. Si la valeur de retour est négative, le point ne se situe pas dans un bouton. La valeur absolue de la valeur de retour est l’index d’un élément de séparateur ou de l’élément de non-séparateur le plus proche.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

