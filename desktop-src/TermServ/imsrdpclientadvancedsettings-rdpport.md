---
title: IMsRdpClientAdvancedSettings propriété RDPPort
description: Spécifie le port de connexion.
ms.assetid: 15be7ef8-8ed2-46e0-8cc5-d5cf1642b79e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RDPPort
- Services Bureau à distance de la propriété RDPPort, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété RDPPort
- Services Bureau à distance de la propriété RDPPort, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété RDPPort
- Services Bureau à distance de la propriété RDPPort, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété RDPPort
- Services Bureau à distance de la propriété RDPPort, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété RDPPort
- Services Bureau à distance de la propriété RDPPort, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété RDPPort
- Services Bureau à distance de la propriété RDPPort, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété RDPPort
- Services Bureau à distance de la propriété RDPPort, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété RDPPort
- Services Bureau à distance de la propriété RDPPort, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété RDPPort
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RDPPort
- IMsRdpClientAdvancedSettings.get_RDPPort
- IMsRdpClientAdvancedSettings.put_RDPPort
- IMsRdpClientAdvancedSettings2.RDPPort
- IMsRdpClientAdvancedSettings2.get_RDPPort
- IMsRdpClientAdvancedSettings2.put_RDPPort
- IMsRdpClientAdvancedSettings3.RDPPort
- IMsRdpClientAdvancedSettings3.get_RDPPort
- IMsRdpClientAdvancedSettings3.put_RDPPort
- IMsRdpClientAdvancedSettings4.RDPPort
- IMsRdpClientAdvancedSettings4.get_RDPPort
- IMsRdpClientAdvancedSettings4.put_RDPPort
- IMsRdpClientAdvancedSettings5.RDPPort
- IMsRdpClientAdvancedSettings5.get_RDPPort
- IMsRdpClientAdvancedSettings5.put_RDPPort
- IMsRdpClientAdvancedSettings6.RDPPort
- IMsRdpClientAdvancedSettings6.get_RDPPort
- IMsRdpClientAdvancedSettings6.put_RDPPort
- IMsRdpClientAdvancedSettings7.RDPPort
- IMsRdpClientAdvancedSettings7.get_RDPPort
- IMsRdpClientAdvancedSettings7.put_RDPPort
- IMsRdpClientAdvancedSettings8.RDPPort
- IMsRdpClientAdvancedSettings8.get_RDPPort
- IMsRdpClientAdvancedSettings8.put_RDPPort
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c8eafb3521d6338a0a2d469c813ff7ffa447a20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106174"
---
# <a name="imsrdpclientadvancedsettingsrdpport-property"></a>IMsRdpClientAdvancedSettings :: RDPPort, propriété

Spécifie le port de connexion.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_RDPPort(
  [in]  LONG rdpPort
);

HRESULT get_RDPPort(
  [out] LONG *prdpPort
);
```



## <a name="property-value"></a>Valeur de la propriété

Le nouveau port. La valeur par défaut est 3389.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                  |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





