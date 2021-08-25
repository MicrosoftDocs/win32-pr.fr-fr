---
title: IMsRdpClientTransportSettings2 propriété GatewaySupportUrl
description: Spécifie ou récupère l’adresse Web du site qui fournit le support technique pour ce serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: e9c0f5ec-1b2f-4e09-8169-4316fd394443
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewaySupportUrl
- Services Bureau à distance de la propriété GatewaySupportUrl, interface IMsRdpClientTransportSettings2
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings2, propriété GatewaySupportUrl
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewaySupportUrl
- IMsRdpClientTransportSettings2.get_GatewaySupportUrl
- IMsRdpClientTransportSettings2.put_GatewaySupportUrl
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2833962f66fb6fab2597629877c5990c9234eb5b2dfe076073bedc2ceab9fd65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770689"
---
# <a name="imsrdpclienttransportsettings2gatewaysupporturl-property"></a>IMsRdpClientTransportSettings2 :: GatewaySupportUrl, propriété

Spécifie ou récupère l’adresse Web du site qui fournit le support technique pour ce serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_GatewaySupportUrl(
  [in]  BSTR bstrProxySupportUrl
);

HRESULT get_GatewaySupportUrl(
  [out] BSTR *pbstrProxySupportUrl
);
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie ou récupère l’adresse Web du site qui fournit le support technique pour ce serveur de passerelle Bureau à distance.

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

 

 





