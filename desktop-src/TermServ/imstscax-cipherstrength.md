---
title: IMsTscAx propriété CipherStrength
description: Récupère la force de chiffrement maximale du contrôle actuel.
ms.assetid: 94efe3e5-4074-4187-b58a-b812f37f3622
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété CipherStrength
- Services Bureau à distance de la propriété CipherStrength, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété CipherStrength
- Services Bureau à distance de la propriété CipherStrength, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété CipherStrength
- Services Bureau à distance de la propriété CipherStrength, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété CipherStrength
- Services Bureau à distance de la propriété CipherStrength, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété CipherStrength
- Services Bureau à distance de la propriété CipherStrength, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété CipherStrength
- Services Bureau à distance de la propriété CipherStrength, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété CipherStrength
- Services Bureau à distance de la propriété CipherStrength, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété CipherStrength
- Services Bureau à distance de la propriété CipherStrength, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété CipherStrength
- Services Bureau à distance de la propriété CipherStrength, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété CipherStrength
- Services Bureau à distance de la propriété CipherStrength, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété CipherStrength
topic_type:
- apiref
api_name:
- IMsTscAx.CipherStrength
- IMsTscAx.get_CipherStrength
- IMsRdpClient.CipherStrength
- IMsRdpClient.get_CipherStrength
- IMsRdpClient2.CipherStrength
- IMsRdpClient2.get_CipherStrength
- IMsRdpClient3.CipherStrength
- IMsRdpClient3.get_CipherStrength
- IMsRdpClient4.CipherStrength
- IMsRdpClient4.get_CipherStrength
- IMsRdpClient5.CipherStrength
- IMsRdpClient5.get_CipherStrength
- IMsRdpClient6.CipherStrength
- IMsRdpClient6.get_CipherStrength
- IMsRdpClient7.CipherStrength
- IMsRdpClient7.get_CipherStrength
- IMsRdpClient8.CipherStrength
- IMsRdpClient8.get_CipherStrength
- IMsRdpClient9.CipherStrength
- IMsRdpClient9.get_CipherStrength
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b66418f2e956afcf6c5b9f1f9a0d5971119e7fddae1c1d46d115f4bbe0e6391
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125439"
---
# <a name="imstscaxcipherstrength-property"></a>IMsTscAx :: CipherStrength, propriété

Récupère la force de chiffrement maximale du contrôle actuel.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_CipherStrength(
  [out] LONG *pCipherStrength
);
```



## <a name="property-value"></a>Valeur de la propriété

Force de chiffrement.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Remarques

par Connexion Bureau à distance par le Web, la puissance de chiffrement est toujours 128, car le contrôle de ActiveX Bureau à distance prend en charge le chiffrement jusqu’à 128 bits inclus. Le contrôle 128 bits peut toujours se connecter à des serveurs de chiffrement 56 bits Bureau à distance des serveurs hôtes de session Bureau à distance.

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

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





