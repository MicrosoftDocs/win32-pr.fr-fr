---
title: Settings. balance
description: La propriété balance spécifie ou récupère le solde stéréo actuel.
ms.assetid: 26f04989-a1b1-4aec-8a15-c4e3737a4e62
keywords:
- Settings. balance du lecteur Windows Media
topic_type:
- apiref
api_name:
- Settings.balance
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 248cd3b2bbf735ef54382fb5b1be52755cad3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541010"
---
# <a name="settingsbalance"></a>Settings. balance

La propriété **balance** spécifie ou récupère le solde stéréo actuel.

## <a name="syntax"></a>Syntaxe

Player. Settings. balance

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture/écriture (**long**). Les valeurs sont comprises entre 100 et 100, avec une valeur par défaut de zéro.

## <a name="remarks"></a>Notes

La valeur zéro indique que le son est lu à un volume égal sur les canaux gauche et droit. Une valeur de 100 indique que l’audio est lu uniquement sur le canal de gauche. Une valeur de 100 indique que l’audio est lu uniquement sur le canal approprié.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Settings (objet)**](settings-object.md)
</dt> </dl>

 

 





