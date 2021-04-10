---
title: IMsRdpClientAdvancedSettings6 AuthenticationType, propriété
description: Spécifie le type d’authentification utilisé pour cette connexion.
ms.assetid: A6DAAE0A-5045-4C2C-B065-AB5BFB39F955
ms.tgt_platform: multiple
keywords:
- Propriété AuthenticationType Services Bureau à distance
- AuthenticationType, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings6, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété AuthenticationType
- AuthenticationType, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings7, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété AuthenticationType
- AuthenticationType, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings8, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété AuthenticationType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationType
- IMsRdpClientAdvancedSettings6.get_AuthenticationType
- IMsRdpClientAdvancedSettings7.AuthenticationType
- IMsRdpClientAdvancedSettings7.get_AuthenticationType
- IMsRdpClientAdvancedSettings8.AuthenticationType
- IMsRdpClientAdvancedSettings8.get_AuthenticationType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c59239570538b690866e499ee942b6635055c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103690"
---
# <a name="imsrdpclientadvancedsettings6authenticationtype-property"></a>IMsRdpClientAdvancedSettings6 :: AuthenticationType, propriété

Spécifie le type d’authentification utilisé pour cette connexion.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_AuthenticationType(
  [out] UINT *puiAuthType
);
```



## <a name="property-value"></a>Valeur de la propriété

Reçoit une valeur qui spécifie le type d’authentification utilisé pour cette connexion. Il peut s’agir de l’une des valeurs suivantes.

<dt>

0
</dt> <dd>

Aucune authentification n’est utilisée.

</dd> <dt>

1
</dt> <dd>

L’authentification par certificat est utilisée.

</dd> <dt>

2
</dt> <dd>

L’authentification Kerberos est utilisée.

</dd> <dt>

3
</dt> <dd>

Le certificat et l’authentification Kerberos sont utilisés.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                   |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 est défini en tant que 222c4b5d-45d9-4DF0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





