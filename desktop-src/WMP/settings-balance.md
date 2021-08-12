---
title: Paramètres. solde
description: La propriété balance spécifie ou récupère le solde stéréo actuel.
ms.assetid: 26f04989-a1b1-4aec-8a15-c4e3737a4e62
keywords:
- Paramètres. balance Lecteur Windows Media
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
ms.openlocfilehash: e569c40214655fc643762da8580bd8d6a16e098b99c649bb27e1a1485d498931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569574"
---
# <a name="settingsbalance"></a>Paramètres. solde

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

[**Paramètres Dessin**](settings-object.md)
</dt> </dl>

 

 





