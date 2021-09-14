---
title: Méthode IWMPNetwork getProxySettings
description: La méthode getProxySettings retourne des informations sur les paramètres de proxy pour un protocole.
ms.assetid: eda4829a-4869-4557-8fe9-8061a1e0f586
keywords:
- Lecteur Windows Media de la méthode getProxySettings
- méthode getProxySettings Lecteur Windows Media, interface IWMPNetwork
- Lecteur Windows Media de l’interface IWMPNetwork, méthode getProxySettings
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxySettings
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d970160c07c90e84585c87ed1abf740fbe3c6318
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232853"
---
# <a name="iwmpnetworkgetproxysettings-method"></a>IWMPNetwork :: getProxySettings, méthode

La méthode **getProxySettings** retourne des informations sur les paramètres de proxy pour un protocole.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 getProxySettings(
  System.String bstrProtocol
);
```


```VB

Public Function getProxySettings( _
  ByVal bstrProtocol As System.String _
) As System.Int32
Implements IWMPNetwork.getProxySettings
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrProtocol* \[ dans\]
</dt> <dd>

**System. String** qui est le nom de protocole. Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

**System. Int32** qui est l’une des valeurs suivantes.



| Valeur | Description                                                                      |
|-------|----------------------------------------------------------------------------------|
| 0     | Aucun serveur proxy n’est utilisé.                                                |
| 1     | Les paramètres de proxy pour le navigateur actuel sont utilisés (valides uniquement pour le protocole HTTP). |
| 2     | Les paramètres de proxy spécifiés manuellement sont utilisés.                            |
| 3     | Les paramètres de proxy sont détectés automatiquement.                                      |



 

## <a name="remarks"></a>Notes

Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.

## <a name="examples"></a>Exemples

L’exemple de code suivant utilise **getProxySettings** pour afficher un message qui fournit des informations sur les paramètres de proxy actuels du lecteur, dans une étiquette. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Retrieve a number representing the current proxy settings.
int proxySetting = player.network.getProxySettings("MMS");

// Display the message that corresponds to the current settings.
switch(proxySetting)
{
    case 0:
    proxySettingsLabel.Text = "A proxy server is not being used";
    break;

    case 1: 
    proxySettingsLabel.Text = "The proxy settings for the current browser are being used.";
    break;

    case 2:
    proxySettingsLabel.Text = "The manually specified proxy settings are being used.";
    break;

    case 3:
    proxySettingsLabel.Text = "The proxy settings are being auto-detected.";
    break;

    default:
    proxySettingsLabel.Text = "Unable to determine proxy setting, try again.";
    break;
}
```


```VB

' Retrieve a number representing the current proxy settings.
Dim proxySetting As Integer = player.network.getProxySettings(&quot;MMS&quot;)

&#39; Display the message that corresponds to the current settings.
Select Case proxySetting

    Case 0
        proxySettingsLabel.Text = &quot;A proxy server is not being used&quot;

    Case 1
        proxySettingsLabel.Text = &quot;The proxy settings for the current browser are being used.&quot;

    Case 2
        proxySettingsLabel.Text = &quot;The manually specified proxy settings are being used.&quot;

    Case 3
        proxySettingsLabel.Text = &quot;The proxy settings are being auto-detected.&quot;

    Case Else
        proxySettingsLabel.Text = &quot;Unable to determine proxy setting, try again.&quot;

End Select
```





## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPNetwork (VB et C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. setproxysettings n' (VB et C#)**](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)
</dt> </dl>

 

 





