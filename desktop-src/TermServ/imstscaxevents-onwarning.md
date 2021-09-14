---
title: Méthode IMsTscAxEvents OnWarning
description: Appelé lorsque le contrôle client rencontre une condition d’erreur qui n’est pas irrécupérable.
ms.assetid: af43d3aa-0ae8-4721-b85d-bb043b20dc40
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnWarning
- Méthode OnWarning Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnWarning
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnWarning
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aadc7013f34c93406f93841896a9041bbb1b7cfb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228599"
---
# <a name="imstscaxeventsonwarning-method"></a>IMsTscAxEvents :: OnWarning, méthode

Appelé lorsque le contrôle client rencontre une condition d’erreur qui n’est pas irrécupérable.

## <a name="syntax"></a>Syntaxe


```C++
void OnWarning(
  [in] long warningCode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*WarningCode* \[ dans\]
</dt> <dd>

Code d'erreur.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Le cache bitmap est endommagé.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Spécifications



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

 

 





