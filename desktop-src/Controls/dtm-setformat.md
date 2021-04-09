---
title: Message DTM_SETFORMAT (commctrl. h)
description: Définit l’affichage d’un contrôle de sélecteur de date et heure (PAO) basé sur une chaîne de format donnée. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime SetFormat.
ms.assetid: a89fa3ad-9894-4c52-ab56-fb62208e39b3
keywords:
- DTM_SETFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- DTM_SETFORMAT
- DTM_SETFORMATA
- DTM_SETFORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17669ed2e1ed23e3b090b77701bbe05d23a5ccb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033061"
---
# <a name="dtm_setformat-message"></a>\_Message DTM SETFORMAT

Définit l’affichage d’un contrôle de sélecteur de date et heure (PAO) basé sur une chaîne de format donnée. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une [chaîne de format](date-and-time-picker-controls.md) se terminant par zéro qui définit l’affichage souhaité. Si ce paramètre a la **valeur null** , le contrôle est réinitialisé à la chaîne de format par défaut pour le style actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Notes

Il est acceptable d’inclure des caractères supplémentaires dans la chaîne de format pour produire un affichage plus riche. Toutefois, tous les caractères sans format doivent être placés entre guillemets simples. Par exemple, la chaîne de format « » aujourd’hui est : «HH » : « m » : « ddddMMMdd », « yyy » produirait une sortie telle que « Today is : 04:22:31 mardi Mar 23, 1996 ».

> [!Note]  
> Un contrôle de PAO effectue le suivi des modifications de paramètres régionaux lorsqu’il utilise la chaîne de format par défaut. Si vous définissez une chaîne de format personnalisée, elle ne sera pas mise à jour en réponse aux modifications des paramètres régionaux.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **DTM \_ SETFORMATW** (Unicode) et **DTM \_ SETFORMATA** (ANSI)<br/>               |



 

 





