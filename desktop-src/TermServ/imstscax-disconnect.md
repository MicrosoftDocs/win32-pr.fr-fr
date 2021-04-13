---
title: Méthode de déconnexion IMsTscAx
description: Déconnecte la connexion active.
ms.assetid: 9fcffd45-b293-4650-be8f-1b0d01d592a2
ms.tgt_platform: multiple
keywords:
- Méthode Disconnect Services Bureau à distance
- Méthode Disconnect Services Bureau à distance, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, méthode Disconnect
- Méthode Disconnect Services Bureau à distance, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, méthode Disconnect
- Méthode Disconnect Services Bureau à distance, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, méthode Disconnect
- Méthode Disconnect Services Bureau à distance, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, méthode Disconnect
- Méthode Disconnect Services Bureau à distance, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, méthode Disconnect
- Méthode Disconnect Services Bureau à distance, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, méthode Disconnect
- Méthode Disconnect Services Bureau à distance, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, méthode Disconnect
- Méthode Disconnect Services Bureau à distance, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, méthode Disconnect
- Méthode Disconnect Services Bureau à distance, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, méthode Disconnect
- Méthode Disconnect Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, méthode Disconnect
topic_type:
- apiref
api_name:
- IMsTscAx.Disconnect
- IMsRdpClient.Disconnect
- IMsRdpClient2.Disconnect
- IMsRdpClient3.Disconnect
- IMsRdpClient4.Disconnect
- IMsRdpClient5.Disconnect
- IMsRdpClient6.Disconnect
- IMsRdpClient7.Disconnect
- IMsRdpClient8.Disconnect
- IMsRdpClient9.Disconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4f1545a8244209c0b4fa8267fcc8ce2a41e090
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508842"
---
# <a name="imstscaxdisconnect-method"></a>IMsTscAx ::D méthode éconnecter

Déconnecte la connexion active.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

Cette méthode retourne une valeur d’erreur d’échec si elle est appelée lorsque le contrôle n’est pas connecté.

Il est également possible de déconnecter le contrôle en fermant sa fenêtre principale. Par exemple, si le contrôle est hébergé dans une page Web, il n’est pas nécessaire d’appeler cette méthode avant de quitter la page ; la fermeture du contrôle déclenche une déconnexion.

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**Se connecter**](imstscax-connect.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





