---
title: IMsRdpClientAdvancedSettings propriété RedirectPrinters
description: Spécifie si la redirection des imprimantes est autorisée.
ms.assetid: 7d4f28a7-a99d-4d0b-ab51-832a78881900
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RedirectPrinters
- Services Bureau à distance de la propriété RedirectPrinters, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété RedirectPrinters
- Services Bureau à distance de la propriété RedirectPrinters, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété RedirectPrinters
- Services Bureau à distance de la propriété RedirectPrinters, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété RedirectPrinters
- Services Bureau à distance de la propriété RedirectPrinters, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété RedirectPrinters
- Services Bureau à distance de la propriété RedirectPrinters, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété RedirectPrinters
- Services Bureau à distance de la propriété RedirectPrinters, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété RedirectPrinters
- Services Bureau à distance de la propriété RedirectPrinters, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété RedirectPrinters
- Services Bureau à distance de la propriété RedirectPrinters, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété RedirectPrinters
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectPrinters
- IMsRdpClientAdvancedSettings.get_RedirectPrinters
- IMsRdpClientAdvancedSettings.put_RedirectPrinters
- IMsRdpClientAdvancedSettings2.RedirectPrinters
- IMsRdpClientAdvancedSettings2.get_RedirectPrinters
- IMsRdpClientAdvancedSettings2.put_RedirectPrinters
- IMsRdpClientAdvancedSettings3.RedirectPrinters
- IMsRdpClientAdvancedSettings3.get_RedirectPrinters
- IMsRdpClientAdvancedSettings3.put_RedirectPrinters
- IMsRdpClientAdvancedSettings4.RedirectPrinters
- IMsRdpClientAdvancedSettings4.get_RedirectPrinters
- IMsRdpClientAdvancedSettings4.put_RedirectPrinters
- IMsRdpClientAdvancedSettings5.RedirectPrinters
- IMsRdpClientAdvancedSettings5.get_RedirectPrinters
- IMsRdpClientAdvancedSettings5.put_RedirectPrinters
- IMsRdpClientAdvancedSettings6.RedirectPrinters
- IMsRdpClientAdvancedSettings6.get_RedirectPrinters
- IMsRdpClientAdvancedSettings6.put_RedirectPrinters
- IMsRdpClientAdvancedSettings7.RedirectPrinters
- IMsRdpClientAdvancedSettings7.get_RedirectPrinters
- IMsRdpClientAdvancedSettings7.put_RedirectPrinters
- IMsRdpClientAdvancedSettings8.RedirectPrinters
- IMsRdpClientAdvancedSettings8.get_RedirectPrinters
- IMsRdpClientAdvancedSettings8.put_RedirectPrinters
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91bb51e0701a57070e4a71d275ff419971a2ec81a0e1b6664157e40972dc92a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757456"
---
# <a name="imsrdpclientadvancedsettingsredirectprinters-property"></a>IMsRdpClientAdvancedSettings :: RedirectPrinters, propriété

Spécifie si la redirection des imprimantes est autorisée.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_RedirectPrinters(
  [in]  VARIANT_BOOL redirectPrinters
);

HRESULT get_RedirectPrinters(
  [out] VARIANT_BOOL *predirectPrinters
);
```



## <a name="property-value"></a>Valeur de la propriété

Affectez à ce paramètre la valeur **Variant \_ true** pour autoriser la redirection ou la **variante \_ false** dans le cas contraire.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Remarques

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

 

 





