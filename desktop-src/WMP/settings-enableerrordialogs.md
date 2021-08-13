---
title: Paramètres. enableErrorDialogs
description: La propriété enableErrorDialogs spécifie ou récupère une valeur indiquant si les boîtes de dialogue d’erreur s’affichent automatiquement.
ms.assetid: 16b10bea-4b3e-469f-a903-02f19ffcdf31
keywords:
- Paramètres. enableErrorDialogs Lecteur Windows Media
topic_type:
- apiref
api_name:
- Settings.enableErrorDialogs
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa786606a97edcfca22512dd0b3188a06a7851f8bab2401e139d7ead2c3495ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569371"
---
# <a name="settingsenableerrordialogs"></a>Paramètres. enableErrorDialogs

La propriété **enableErrorDialogs** spécifie ou récupère une valeur indiquant si les boîtes de dialogue d’erreur s’affichent automatiquement.

## <a name="syntax"></a>Syntaxe

Player. Settings. enableErrorDialogs

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                                     |
|-------|-------------------------------------------------|
| true  | Par défaut. Les boîtes de dialogue d’erreur s’affichent automatiquement. |
| false | Les boîtes de dialogue d’erreur ne s’affichent pas automatiquement.      |



 

## <a name="remarks"></a>Notes

Cette propriété présente un comportement spécifique pour les instances distantes du contrôle du lecteur. pour plus d’informations, consultez [communication à distance du contrôle Lecteur Windows Media](remoting-the-windows-media-player-control.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Paramètres Dessin**](settings-object.md)
</dt> </dl>

 

 





