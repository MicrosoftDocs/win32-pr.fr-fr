---
title: Propriété de serveur IMsTscAx (Asptlb. h)
description: Spécifie le nom du serveur auquel le contrôle actuel est connecté.
ms.assetid: 81118ddd-2662-47f5-8e9d-9c2a5056820b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriétés de serveur
- Services Bureau à distance de propriétés de serveur, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété de serveur
- Services Bureau à distance de propriétés de serveur, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété de serveur
- Services Bureau à distance de propriétés de serveur, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété de serveur
- Services Bureau à distance de propriétés de serveur, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété de serveur
- Services Bureau à distance de propriétés de serveur, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété de serveur
- Services Bureau à distance de propriétés de serveur, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété de serveur
- Services Bureau à distance de propriétés de serveur, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété de serveur
- Services Bureau à distance de propriétés de serveur, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété de serveur
- Services Bureau à distance de propriétés de serveur, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété de serveur
- Services Bureau à distance de propriétés de serveur, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété de serveur
topic_type:
- apiref
api_name:
- IMsTscAx.Server
- IMsTscAx.get_Server
- IMsTscAx.put_Server
- IMsRdpClient.Server
- IMsRdpClient.get_Server
- IMsRdpClient.put_Server
- IMsRdpClient2.Server
- IMsRdpClient2.get_Server
- IMsRdpClient2.put_Server
- IMsRdpClient3.Server
- IMsRdpClient3.get_Server
- IMsRdpClient3.put_Server
- IMsRdpClient4.Server
- IMsRdpClient4.get_Server
- IMsRdpClient4.put_Server
- IMsRdpClient5.Server
- IMsRdpClient5.get_Server
- IMsRdpClient5.put_Server
- IMsRdpClient6.Server
- IMsRdpClient6.get_Server
- IMsRdpClient6.put_Server
- IMsRdpClient7.Server
- IMsRdpClient7.get_Server
- IMsRdpClient7.put_Server
- IMsRdpClient8.Server
- IMsRdpClient8.get_Server
- IMsRdpClient8.put_Server
- IMsRdpClient9.Server
- IMsRdpClient9.get_Server
- IMsRdpClient9.put_Server
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8ce72d7cc26dc3fd7b60b7f1d4f26d2737980dfde88a1b31c79a59fb4335f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770999"
---
# <a name="imstscaxserver-property"></a>IMsTscAx :: Server, propriété

Spécifie le nom du serveur auquel le contrôle actuel est connecté.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Server(
  [in]  BSTR newVal
);

HRESULT get_Server(
  [out] BSTR *pServer
);
```



## <a name="property-value"></a>Valeur de la propriété

Nouveau nom du serveur. Ce paramètre peut être un nom DNS ou une adresse IP.

## <a name="error-codes"></a>Codes d’erreur

Si les méthodes sont correctement exécutées, la méthode **S \_ OK** est retournée. Toute autre valeur **HRESULT** indique que l’appel a échoué.

## <a name="remarks"></a>Remarques

cette propriété doit être définie avant d’appeler la méthode [**Connecter**](imstscax-connect.md) . Il s’agit de la seule propriété qui doit être définie avant la connexion.

Cette propriété ne peut être définie que si le contrôle n’est pas dans l’état connecté. Cette propriété retourne **E \_ Fail** si elle est appelée lorsque le contrôle est connecté. Vous pouvez vérifier l’état connecté à l’aide de la propriété [**Connected**](imstscax-connected.md) .

Cette méthode alloue la mémoire requise pour la mémoire tampon vers laquelle pointe le paramètre *pserver* . L’appel d’applications C/C++ doit libérer la mémoire avec un appel à la fonction [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) . cela n’est pas nécessaire pour les Visual Basic et les clients de script.

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| En-tête<br/>                   | <dl> <dt>Asptlb. h</dt> </dl>    |
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

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

