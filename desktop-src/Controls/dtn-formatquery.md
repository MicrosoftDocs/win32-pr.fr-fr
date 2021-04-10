---
title: DTN_FORMATQUERY le code de notification (commctrl. h)
description: Envoyé par un contrôle de sélecteur de date et heure (PAO) pour récupérer la taille maximale autorisée de la chaîne qui s’affichera dans un champ de rappel. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0f00086a-0ab8-4f6f-9c3e-6e77008aa088
keywords:
- Contrôles Windows de code de notification DTN_FORMATQUERY
topic_type:
- apiref
api_name:
- DTN_FORMATQUERY
- DTN_FORMATQUERYA
- DTN_FORMATQUERYW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69e9653f369f13e0ef4a775265d763e854db4de7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941716"
---
# <a name="dtn_formatquery-notification-code"></a>\_Code de notification DTN FORMATQUERY

Envoyé par un contrôle de sélecteur de date et heure (PAO) pour récupérer la taille maximale autorisée de la chaîne qui s’affichera dans un champ de rappel. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
DTN_FORMATQUERY

    lpDTFormatQuery = (LPNMDATETIMEFORMATQUERY) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) contenant des informations sur le champ de rappel. La structure contient une sous-chaîne qui définit un champ de rappel et reçoit la taille maximale autorisée de la chaîne qui s’affichera dans le champ de rappel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Le propriétaire du contrôle doit calculer la largeur maximale possible du texte qui sera affiché dans le champ de rappel, définir le membre **szMax** de la structure [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) et retourner zéro.

## <a name="remarks"></a>Notes

La gestion de ce code de notification prépare le contrôle pour la taille maximale de la chaîne qui s’affiche dans un champ de rappel particulier. Cela permet au contrôle d’afficher correctement la sortie à tout moment, ce qui réduit le scintillement dans l’affichage du contrôle. (Pour plus d’informations sur les champs de rappel, consultez [champs de rappel](date-and-time-picker-controls.md).)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **DTN \_ FORMATQUERYW** (Unicode) et **DTN \_ FORMATQUERYA** (ANSI)<br/>           |



 

 





