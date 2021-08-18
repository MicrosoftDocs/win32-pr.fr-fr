---
title: Méthode IWMPNetwork getProxyBypassForLocal
description: La méthode getProxyBypassForLocal retourne une valeur qui indique si le serveur proxy est contourné si le serveur d’origine se trouve sur un réseau local.
ms.assetid: 150a05f3-6979-4a88-a617-472f07d38807
keywords:
- Lecteur Windows Media de la méthode getProxyBypassForLocal
- méthode getProxyBypassForLocal Lecteur Windows Media, interface IWMPNetwork
- Lecteur Windows Media de l’interface IWMPNetwork, méthode getProxyBypassForLocal
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyBypassForLocal
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50d23307ab8872fb49b2b4797d54b78a71a04adba350287fa23cb8e5ab90541c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996479"
---
# <a name="iwmpnetworkgetproxybypassforlocal-method"></a>IWMPNetwork :: getProxyBypassForLocal, méthode

La méthode **getProxyBypassForLocal** retourne une valeur qui indique si le serveur proxy est contourné si le serveur d’origine se trouve sur un réseau local.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Boolean getProxyBypassForLocal(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyBypassForLocal( _
  ByVal bstrProtocol As System.String _
) As System.Boolean
Implements IWMPNetwork.getProxyBypassForLocal
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrProtocol* 
</dt> <dd>

**System. String** qui est le nom de protocole.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Valeur **System. Boolean** qui indique si le serveur proxy est contourné. La valeur est significative uniquement lorsque **IWMPNetwork. getProxySettings** retourne la valeur 2 (utiliser des paramètres manuels).

## <a name="remarks"></a>Remarques

Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.

## <a name="examples"></a>Exemples

l’exemple de code suivant utilise **getProxyBypassForLocal** pour indiquer si Lecteur Windows Media est défini pour ignorer le serveur proxy pour les adresses locales. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```VB
' Boolean values to hold the results of calls to getProxyBypassForLocal. 
Dim proxyBypassForLocalHTTP As Boolean = False
Dim proxyBypassForLocalMMS As Boolean = False

' Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings("HTTP") = 2) Then

    proxyBypassForLocalHTTP = player.network.getProxyBypassForLocal("HTTP")

End If

' Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings("MMS") = 2) Then

    proxyBypassForLocalMMS = player.network.getProxyBypassForLocal("MMS")

End If

' Store the proxy bypass for local values in a string array and display them
' using a multi-line text box. Unavailable proxy bypass for local values will display
' as "undefined".
proxyInfo(0) = ("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP.ToString())
proxyInfo(1) = ("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS.ToString())
proxyBypassText.Lines = proxyInfo
```


```CSharp

// Boolean values to hold the results of calls to getProxyBypassForLocal. 
bool proxyBypassForLocalHTTP = false;
bool proxyBypassForLocalMMS = false;

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings(&quot;HTTP&quot;) == 2)
{
    proxyBypassForLocalHTTP = player.network.getProxyBypassForLocal(&quot;HTTP&quot;);
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings(&quot;MMS&quot;) == 2)
{
   proxyBypassForLocalMMS = player.network.getProxyBypassForLocal(&quot;MMS&quot;);
}

// Store the proxy bypass for local values in a string array and display them
// using a multi-line text box. Unavailable proxy bypass for local values will display
// as &quot;undefined&quot;.
proxyInfo[0] = (&quot;The current HTTP proxy bypass for local value: &quot; + proxyBypassForLocalHTTP.ToString());
proxyInfo[1] = (&quot;The current MMS proxy bypass for local value: &quot; + proxyBypassForLocalMMS.ToString());
proxyBypassText.Lines = proxyInfo;
```





## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|-----------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                             |
| Espace de noms<br/> | **WMPLib**<br/>                                                                         |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPNetwork (VB et C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. getProxySettings (VB et C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. setProxyBypassForLocal (VB et C#)**](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md)
</dt> </dl>

 

 





