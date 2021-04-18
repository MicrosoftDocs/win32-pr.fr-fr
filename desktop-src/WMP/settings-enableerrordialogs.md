---
title: Paramètres. enableErrorDialogs
description: La propriété enableErrorDialogs spécifie ou récupère une valeur indiquant si les boîtes de dialogue d’erreur s’affichent automatiquement.
ms.assetid: 16b10bea-4b3e-469f-a903-02f19ffcdf31
keywords:
- Settings. enableErrorDialogs Windows Media Player
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
ms.openlocfilehash: c5746bb68da71ca827da3923e4956b613eabdb50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540340"
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

Cette propriété présente un comportement spécifique pour les instances distantes du contrôle du lecteur. Pour plus d’informations, consultez [communication à distance du contrôle du lecteur Windows Media](remoting-the-windows-media-player-control.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Settings (objet)**](settings-object.md)
</dt> </dl>

 

 





