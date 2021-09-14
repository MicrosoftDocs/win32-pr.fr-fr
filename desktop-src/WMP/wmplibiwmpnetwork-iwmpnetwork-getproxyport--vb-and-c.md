---
title: Méthode IWMPNetwork getProxyPort
description: La méthode getProxyPort retourne le port proxy utilisé.
ms.assetid: fc94f3a9-458d-410c-98e9-a34be6e08c52
keywords:
- Lecteur Windows Media de la méthode getProxyPort
- méthode getProxyPort Lecteur Windows Media, interface IWMPNetwork
- Lecteur Windows Media de l’interface IWMPNetwork, méthode getProxyPort
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyPort
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46fb388c2740e709e75579c01d216af677a826c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232854"
---
# <a name="iwmpnetworkgetproxyport-method"></a>IWMPNetwork :: getProxyPort, méthode

La méthode **getProxyPort** retourne le port proxy utilisé.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 getProxyPort(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyPort( _
  ByVal bstrProtocol As System.String _
) As System.Int32
Implements IWMPNetwork.getProxyPort
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrProtocol* \[ dans\]
</dt> <dd>

**System. String** qui est le nom de protocole. Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

**System. Int32** qui est le port proxy utilisé. La valeur est significative uniquement lorsque **IWMPNetwork. getProxySettings** retourne la valeur 2 (utiliser des paramètres manuels).

## <a name="remarks"></a>Notes

Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.

## <a name="examples"></a>Exemples

l’exemple de code suivant utilise **getProxyPort** pour afficher les numéros de port de proxy Lecteur Windows Media actuels pour les protocoles MMS et HTTP. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Variables to hold the results of calls to getProxyPort. 
int proxyPortHTTP = 0;
int proxyPortMMS = 0;

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyPortHTTP = player.network.getProxyPort("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyPortMMS = player.network.getProxyPort("MMS");
}

// Store the proxy port numbers in a string array and display them using a multi-line
// text box. Unavailable proxy port numbers will display as "undefined".
proxyPorts[0] = ("The current HTTP proxy port is: " + proxyPortHTTP.ToString());
proxyPorts[1] = ("The current MMS proxy port is: " + proxyPortMMS.ToString());
proxyPortText.Lines = proxyPorts;
```


```VB

' Variables to hold the results of calls to getProxyPort. 
Dim proxyPortHTTP As Integer = 0
Dim proxyPortMMS As Integer = 0

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyPortHTTP = player.network.getProxyPort(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyPortMMS = player.network.getProxyPort(&quot;MMS&quot;)

End If

&#39; Store the proxy port numbers in a string array and display them using a multi-line
&#39; text box. Unavailable proxy port numbers will display as &quot;undefined&quot;.
proxyPorts(0) = (&quot;The current HTTP proxy port is: &quot; + proxyPortHTTP.ToString())
proxyPorts(1) = (&quot;The current MMS proxy port is: &quot; + proxyPortMMS.ToString())
proxyPortText.Lines = proxyPorts
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

[**IWMPNetwork. getProxySettings (VB et C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. setProxyPort (VB et C#)**](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)
</dt> </dl>

 

 





