---
title: IMsRdpClientTransportSettings2 propriété GatewayPassword
description: Spécifie le mot de passe qu’un utilisateur fournit pour se connecter au serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: f29078e5-49ab-45a0-8d79-4b57d7c35e3a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayPassword
- Services Bureau à distance de la propriété GatewayPassword, interface IMsRdpClientTransportSettings2
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings2, propriété GatewayPassword
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPassword
- IMsRdpClientTransportSettings2.put_GatewayPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977ac8114a8be4f4f5ef8aa21a4a00f48aead31ee18f7fe41f789ff2a3c9b478
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959349"
---
# <a name="imsrdpclienttransportsettings2gatewaypassword-property"></a>IMsRdpClientTransportSettings2 :: GatewayPassword, propriété

Spécifie le mot de passe qu’un utilisateur fournit pour se connecter au serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).

Cette propriété est en écriture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_GatewayPassword(
  [in] BSTR proxyPassword
);
```



## <a name="property-value"></a>Valeur de la propriété

Mot de passe fourni par l’utilisateur pour se connecter au serveur de passerelle Bureau à distance.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista avec SP1<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                    |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 est défini comme 67341688-D606-4C73-A5D2-2E0489009319<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





