---
title: IMsRdpExtendedSettings Property, propriété
description: Contient une propriété nommée.
ms.assetid: 3acaeff9-1617-46c3-80c3-b87496b83670
ms.tgt_platform: multiple
keywords:
- Propriété Property Services Bureau à distance
- Propriété Property Services Bureau à distance, IMsRdpExtendedSettings, interface
- Services Bureau à distance de l’interface IMsRdpExtendedSettings, propriété Property
topic_type:
- apiref
api_name:
- IMsRdpExtendedSettings.Property
- IMsRdpExtendedSettings.get_Property
- IMsRdpExtendedSettings.put_Property
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eadc8ce59e5a2bd50a4e61ad75b5124b24c21b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "103745349"
---
# <a name="imsrdpextendedsettingsproperty-property"></a>IMsRdpExtendedSettings ::P propriété opriétés

Contient une propriété nommée.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Property(
  [in]          BSTR    bstrPropertyName,
  [in]          VARIANT *pValue
);

HRESULT get_Property(
  [in]          BSTR    bstrPropertyName,
  [out, retval] VARIANT *pValue
);
```



## <a name="property-value"></a>Valeur de la propriété

Valeur de la propriété nommée.

| Nom de la propriété | Type de données | Accès | Peut être modifié après le démarrage de la connexion | Description |
|----------|-----------|--------|-----------------------------------------|-------------|
| ConnectToChildSession | **VT \_ bool** | Lecture/écriture | Oui | Si vous affectez la **valeur true** à cette propriété, le contrôle client se connecte à la session enfant sur l’ordinateur local au lieu d’un serveur distant. Si cette propriété est définie sur **true**, vous ne pouvez pas vous connecter à un serveur distant, car toutes les connexions sont redirigées vers localhost. Pour plus d’informations sur les sessions enfants, consultez [sessions enfants](child-sessions.md). |
| DisableCredentialsDelegation | **VT \_ bool** | Lecture/écriture | Non | Si la **valeur est true**, les informations d’identification ne sont pas envoyées au serveur distant. |
| EnableFrameBufferRedirection | **VT \_ bool** | Lecture/écriture | Non | Si la **valeur est true**, la redirection de la mémoire tampon de frame est tentée. Pour une connexion de bouclage (le même ordinateur étant à la fois client et serveur), la redirection de la mémoire tampon de trame permet de partager la mémoire de la mémoire tampon de trame entre les sessions. |
| EnableHardwareMode | **VT \_ bool**  | Écriture seule | Non | Si la **valeur est true**, l’assistance matérielle au décodage graphique est tentée. |
| IgnoreCursors | **VT \_ bool** | Écriture seule | Non | Si la **valeur est true**, les curseurs envoyés par le serveur distant sont ignorés. |
| ManualClipboardSyncEnabled | **VT \_ bool** | Lecture/écriture | Oui | Si cette propriété a la **valeur true** , cela signifie que les presse-papiers locaux et distants ne seront pas synchronisés automatiquement. Au lieu de cela, l’interface [**IMsRdpClipboard**](imsrdpclipboard.md) doit être utilisée pour synchroniser les formats du presse-papiers du presse-papiers local vers le presse-papiers distant et le presse-papiers distant vers le presse-papiers local. |
| ZoomLevel | **_VT \_ UI4_* | Lecture/écriture | Oui | Implémente la fonctionnalité de zoom à l’aide du contrôle ActiveX RDP. La fonctionnalité de zoom est disponible dans le menu **système** de RDP. La propriété **zoomLevel** n’a aucun effet en mode RemoteApp et en mode plein écran. [**IMsRdpClientAdvancedSettings :: SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md) et **zoomLevel** s’excluent mutuellement. |

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                                                                                                                                                                                                                           |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                                                                                                                                                                                                                                 |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                         |
| CLSID<br/>                    | Le CLSID \_ MsRdpClient7NotSafeForScripting est défini en tant que 54d38bf7-b1ef-4479-9674-1bd6ea465258<br/> Le CLSID \_ MsRdpClient8NotSafeForScripting est défini en tant que A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> Le CLSID \_ MsRdpClient9NotSafeForScripting est défini en tant que 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpExtendedSettings est défini en tant que 302D8188-0052-4807-806A-362B628F9AC5<br/>                                                                                                                                                                                                                      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpExtendedSettings**](imsrdpextendedsettings.md)
</dt> </dl>

 

 





