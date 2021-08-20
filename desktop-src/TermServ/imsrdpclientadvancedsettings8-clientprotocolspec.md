---
title: IMsRdpClientAdvancedSettings8 propriété ClientProtocolSpec
description: Spécifie le Protocole Bureau à distance utilisé entre le client et le serveur.
ms.assetid: DD607D54-CAEA-43EE-94EB-F983AEA0CC1E
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ClientProtocolSpec
- Services Bureau à distance de la propriété ClientProtocolSpec, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété ClientProtocolSpec
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings8.ClientProtocolSpec
- IMsRdpClientAdvancedSettings8.get_ClientProtocolSpec
- IMsRdpClientAdvancedSettings8.put_ClientProtocolSpec
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7e0cc7b45e457a2e0300e5e59ac1780a4ac4cd9ef023f10b6a73986a960574
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130130"
---
# <a name="imsrdpclientadvancedsettings8clientprotocolspec-property"></a>IMsRdpClientAdvancedSettings8 :: ClientProtocolSpec, propriété

Spécifie le Protocole Bureau à distance utilisé entre le client et le serveur.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_ClientProtocolSpec(
  [in]  ClientSpec ClientMode
);

HRESULT get_ClientProtocolSpec(
  [out] ClientSpec *pClientMode
);
```



## <a name="property-value"></a>Valeur de la propriété

Valeur de l’énumération [**ClientSpec**](clientspec.md) qui spécifie le Protocole Bureau à distance utilisé entre le client et le serveur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ClientSpec**](clientspec.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





