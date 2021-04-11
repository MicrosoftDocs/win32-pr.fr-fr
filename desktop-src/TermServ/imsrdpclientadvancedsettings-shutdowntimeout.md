---
title: IMsRdpClientAdvancedSettings shutdownTimeout, propriété
description: Spécifie la durée, en secondes, à attendre que le serveur réponde à une demande de déconnexion.
ms.assetid: 3fa935dc-d4b0-433b-ab67-a644fcf09006
ms.tgt_platform: multiple
keywords:
- shutdownTimeout, propriété Services Bureau à distance
- shutdownTimeout, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété shutdownTimeout
- shutdownTimeout, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings2, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété shutdownTimeout
- shutdownTimeout, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings3, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété shutdownTimeout
- shutdownTimeout, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings4, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété shutdownTimeout
- shutdownTimeout, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings5, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété shutdownTimeout
- shutdownTimeout, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings6, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété shutdownTimeout
- shutdownTimeout, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings7, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété shutdownTimeout
- shutdownTimeout, propriété Services Bureau à distance, IMsRdpClientAdvancedSettings8, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété shutdownTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.shutdownTimeout
- IMsRdpClientAdvancedSettings.get_shutdownTimeout
- IMsRdpClientAdvancedSettings.put_shutdownTimeout
- IMsRdpClientAdvancedSettings2.shutdownTimeout
- IMsRdpClientAdvancedSettings2.get_shutdownTimeout
- IMsRdpClientAdvancedSettings2.put_shutdownTimeout
- IMsRdpClientAdvancedSettings3.shutdownTimeout
- IMsRdpClientAdvancedSettings3.get_shutdownTimeout
- IMsRdpClientAdvancedSettings3.put_shutdownTimeout
- IMsRdpClientAdvancedSettings4.shutdownTimeout
- IMsRdpClientAdvancedSettings4.get_shutdownTimeout
- IMsRdpClientAdvancedSettings4.put_shutdownTimeout
- IMsRdpClientAdvancedSettings5.shutdownTimeout
- IMsRdpClientAdvancedSettings5.get_shutdownTimeout
- IMsRdpClientAdvancedSettings5.put_shutdownTimeout
- IMsRdpClientAdvancedSettings6.shutdownTimeout
- IMsRdpClientAdvancedSettings6.get_shutdownTimeout
- IMsRdpClientAdvancedSettings6.put_shutdownTimeout
- IMsRdpClientAdvancedSettings7.shutdownTimeout
- IMsRdpClientAdvancedSettings7.get_shutdownTimeout
- IMsRdpClientAdvancedSettings7.put_shutdownTimeout
- IMsRdpClientAdvancedSettings8.shutdownTimeout
- IMsRdpClientAdvancedSettings8.get_shutdownTimeout
- IMsRdpClientAdvancedSettings8.put_shutdownTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 868a011a0ce484f5bb2dd7d1ec610f4e3a436898
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383895"
---
# <a name="imsrdpclientadvancedsettingsshutdowntimeout-property"></a>IMsRdpClientAdvancedSettings :: shutdownTimeout, propriété

Spécifie la durée, en secondes, à attendre que le serveur réponde à une demande de déconnexion.

Si le serveur ne répond pas dans le délai spécifié, le contrôle client se déconnecte.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_shutdownTimeout(
  [in]  LONG shutdownTimeout
);

HRESULT get_shutdownTimeout(
  [out] LONG *pshutdownTimeout
);
```



## <a name="property-value"></a>Valeur de la propriété

Nouvelle durée, en secondes. La valeur par défaut de la propriété est 10. La valeur maximale est 600, qui représente 10 minutes.

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

 

 





