---
title: Méthode IMsTscAxEvents OnFocusReleased
description: Appelé lorsque la combinaison de touches de focus de mise en sortie est enfoncée. Par exemple, cet événement est appelé quand l’utilisateur appuie sur la touche CTRL + ALT + gauche ou sur la combinaison de touches CTRL + ALT + flèche droite.
ms.assetid: f5d755b0-4b8f-4d62-8dc4-f6b63e3819e5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnFocusReleased
- Méthode OnFocusReleased Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnFocusReleased
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFocusReleased
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eff03f95d4ebbb068bccbfd9f68a930c00f0b00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513794"
---
# <a name="imstscaxeventsonfocusreleased-method"></a>IMsTscAxEvents :: OnFocusReleased, méthode

Appelé lorsque la combinaison de touches de focus de mise en sortie est enfoncée. Par exemple, cet événement est appelé quand l’utilisateur appuie sur la touche CTRL + ALT + gauche ou sur la combinaison de touches CTRL + ALT + flèche droite.

Cet événement permet au conteneur de contrôles ActiveX de retirer le contrôle du contrôle ActiveX. Par exemple, cela est utile dans un scénario où vous n’avez pas de souris, et les combinaisons de touches spéciales, telles que ALT + TAB, sont redirigées vers le serveur. Dans ce cas, vous n’avez pas de moyen de ramener le focus clavier sur le bureau local. Toutefois, avec la combinaison de touches CTRL + ALT + gauche ou CTRL + ALT + flèche droite, le conteneur ActiveX peut écouter cet événement et y répondre en désoccupant le focus du contrôle ActiveX.

## <a name="syntax"></a>Syntaxe


```C++
void OnFocusReleased(
  [in] INT iDirection
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*iDirection* \[ dans\]
</dt> <dd>

Paramètre de direction de 1 (CTRL + ALT + flèche droite) ou 1 (CTRL + ALT + flèche gauche).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cet événement est disponible lorsque Connexion Bureau à distance 6,0 est utilisé sur le client.

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

 

 





