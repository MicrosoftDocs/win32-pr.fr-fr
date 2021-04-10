---
title: Méthode IMsTscAxEvents OnConfirmClose
description: Appelée lorsque le client appelle la méthode IMsRdpClient RequestClose.
ms.assetid: fb149fbc-9415-4c4c-8d4b-e22214ac38cb
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnConfirmClose
- Méthode OnConfirmClose Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnConfirmClose
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConfirmClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623196033e23a964857a6a604c7eca3904f32c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106486"
---
# <a name="imstscaxeventsonconfirmclose-method"></a>IMsTscAxEvents :: OnConfirmClose, méthode

Appelée lorsque le client appelle la méthode [**IMsRdpClient :: RequestClose**](imsrdpclient-requestclose.md) . En réponse à cet événement, l’utilisateur doit être invité à confirmer la fermeture de la connexion. Pour plus d'informations, consultez la section Notes qui suit.

## <a name="syntax"></a>Syntaxe


```C++
void OnConfirmClose(
  [out] VARIANT_BOOL *pfAllowClose
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pfAllowClose* \[ à\]
</dt> <dd>

Si **la \_ valeur de type Variant est true**, la valeur par défaut indique que l’utilisateur souhaite fermer la connexion. Si la **valeur de type Variant est \_ false**, indique que l’utilisateur ne souhaite pas fermer la connexion. Pour plus d'informations, consultez la section Notes qui suit.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Quand une application conteneur appelle la méthode [**IMsRdpClient :: RequestClose**](imsrdpclient-requestclose.md) , cette méthode retourne une valeur indiquant si le conteneur doit attendre qu’un événement **OnConfirmClose** se produise avant de fermer la connexion de contrôle. Si **RequestClose** retourne **controlCloseWaitForEvents**, et que l’utilisateur est connecté et connecté à sa session services Bureau à distance, l’événement **OnConfirmClose** se déclenche. À ce stade, l’application conteneur peut demander à l’utilisateur s’il souhaite fermer la connexion. Si l’utilisateur souhaite fermer la connexion, l’application doit définir le paramètre *pfAllowClose* sur la **\_ valeur variant true** et procéder à la fermeture de la connexion. Si l’utilisateur ne souhaite pas fermer, l’application doit affecter à *pfAllowClose* la valeur **Variant \_ false** et conserver la connexion ouverte.

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

 

 





