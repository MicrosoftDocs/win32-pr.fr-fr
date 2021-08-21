---
title: Méthode IMsTscAxEvents OnFatalError
description: Appelé lorsque le contrôle client rencontre une erreur irrécupérable.
ms.assetid: 13a5eb2e-d847-4561-b30b-3f23a0579b4d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnFatalError
- Méthode OnFatalError Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnFatalError
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFatalError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a10315eca4fcbf96edf123699614d29a2c0b8974f563c52148b5de75310fc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000679"
---
# <a name="imstscaxeventsonfatalerror-method"></a>IMsTscAxEvents :: OnFatalError, méthode

Appelé lorsque le contrôle client rencontre une erreur irrécupérable.

## <a name="syntax"></a>Syntaxe


```C++
void OnFatalError(
  [in] long errorCode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ErrorCode* \[ dans\]
</dt> <dd>

Indique le code d’erreur.

<dt>

<span id="0"></span>

<span id="0"></span>**entre**


</dt> <dd>

Une erreur inconnue s’est produite.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Code d’erreur interne 1.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Une erreur de mémoire insuffisante s’est produite.

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**1,3**


</dt> <dd>

Une erreur de création de fenêtre s’est produite.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Code d’erreur interne 2.

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5,5**


</dt> <dd>

Code d’erreur interne 3. Cet État n’est pas valide.

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**6,3**


</dt> <dd>

Code d’erreur interne 4.

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**Commission(7**


</dt> <dd>

Une erreur irrécupérable s’est produite lors de la connexion du client.

</dd> <dt>

<span id="100"></span>

<span id="100"></span>**100**


</dt> <dd>

Erreur d’initialisation Winsock.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

En réponse à cet événement, le conteneur affiche un message d’erreur et s’arrête.

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

 

 





