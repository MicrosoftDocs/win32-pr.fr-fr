---
title: IMsRdpClientAdvancedSettings propriété RedirectSmartCards
description: Spécifie si la redirection des cartes à puce est autorisée.
ms.assetid: 53b6b483-ccba-41eb-a417-241a4430958e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RedirectSmartCards
- Services Bureau à distance de la propriété RedirectSmartCards, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété RedirectSmartCards
- Services Bureau à distance de la propriété RedirectSmartCards, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété RedirectSmartCards
- Services Bureau à distance de la propriété RedirectSmartCards, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété RedirectSmartCards
- Services Bureau à distance de la propriété RedirectSmartCards, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété RedirectSmartCards
- Services Bureau à distance de la propriété RedirectSmartCards, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété RedirectSmartCards
- Services Bureau à distance de la propriété RedirectSmartCards, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété RedirectSmartCards
- Services Bureau à distance de la propriété RedirectSmartCards, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété RedirectSmartCards
- Services Bureau à distance de la propriété RedirectSmartCards, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété RedirectSmartCards
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectSmartCards
- IMsRdpClientAdvancedSettings.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings2.RedirectSmartCards
- IMsRdpClientAdvancedSettings2.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings2.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings3.RedirectSmartCards
- IMsRdpClientAdvancedSettings3.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings3.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings4.RedirectSmartCards
- IMsRdpClientAdvancedSettings4.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings4.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings5.RedirectSmartCards
- IMsRdpClientAdvancedSettings5.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings5.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings6.RedirectSmartCards
- IMsRdpClientAdvancedSettings6.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings6.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings7.RedirectSmartCards
- IMsRdpClientAdvancedSettings7.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings7.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings8.RedirectSmartCards
- IMsRdpClientAdvancedSettings8.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings8.put_RedirectSmartCards
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ba58a492ede5371c0f43d996f46ed7a898df7f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509504"
---
# <a name="imsrdpclientadvancedsettingsredirectsmartcards-property"></a>IMsRdpClientAdvancedSettings :: RedirectSmartCards, propriété

Spécifie si la redirection des cartes à puce est autorisée.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_RedirectSmartCards(
  [in]  VARIANT_BOOL redirectSmartCards
);

HRESULT get_RedirectSmartCards(
  [out] VARIANT_BOOL *predirectSmartCards
);
```



## <a name="property-value"></a>Valeur de la propriété

Affectez à ce paramètre la valeur **Variant \_ true** pour autoriser la redirection ou la **variante \_ false** dans le cas contraire. **Variante \_ TRUE** demande à l’utilisateur de confirmer l’autorisation de la redirection au moment de la connexion, pour des raisons de sécurité.

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

 

 





