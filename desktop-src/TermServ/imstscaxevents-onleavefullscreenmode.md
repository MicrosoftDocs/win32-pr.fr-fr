---
title: Méthode IMsTscAxEvents OnLeaveFullScreenMode
description: Appelé lorsque le client quitte le mode plein écran. Par exemple, cet événement est appelé quand l’utilisateur appuie sur la combinaison de touches de raccourci du mode plein écran (CTRL + ALT + ATTN).
ms.assetid: 95c5d427-b6e2-4a42-9816-b130ab533ac0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnLeaveFullScreenMode
- Méthode OnLeaveFullScreenMode Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnLeaveFullScreenMode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLeaveFullScreenMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4ee414f2dceba35a17ff86bce03c83d75aab48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033003"
---
# <a name="imstscaxeventsonleavefullscreenmode-method"></a>IMsTscAxEvents :: OnLeaveFullScreenMode, méthode

Appelé lorsque le client quitte le mode plein écran. Par exemple, cet événement est appelé quand l’utilisateur appuie sur la combinaison de touches de [raccourci](terminal-services-shortcut-keys.md) du mode plein écran (Ctrl + Alt + Attn).

## <a name="syntax"></a>Syntaxe


```C++
void OnLeaveFullScreenMode();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





