---
title: Méthode IWMPNetwork setProxyPort
description: La méthode setProxyPort spécifie le port du proxy à utiliser. | Méthode IWMPNetwork setProxyPort
ms.assetid: df4b33f6-52b5-437f-ade2-0d08ca2878a9
keywords:
- Lecteur Windows Media de la méthode setProxyPort
- méthode setProxyPort Lecteur Windows Media, interface IWMPNetwork
- Lecteur Windows Media de l’interface IWMPNetwork, méthode setProxyPort
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyPort
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e79453ee2d69a0c6b227006416e49b4d4c24b99b3b02dd2bd00cd3bafafc5b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734839"
---
# <a name="iwmpnetworksetproxyport-method"></a>IWMPNetwork :: setProxyPort, méthode

La méthode **setProxyPort** spécifie le port du proxy à utiliser.

## <a name="syntax"></a>Syntaxe


```CSharp
public void setProxyPort(
  System.String bstrProtocol,
  System.Int32 lProxyPort
);
```


```VB

Public Sub setProxyPort( _
  ByVal bstrProtocol As System.String, _
  ByVal lProxyPort As System.Int32 _
)
Implements IWMPNetwork.setProxyPort
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrProtocol* \[ dans\]
</dt> <dd>

**System. String** qui est le nom de protocole. Pour obtenir la liste des protocoles pris en charge, consultez [protocoles et types de fichiers pris en charge](supported-protocols-and-file-types.md).

</dd> <dt>

*lProxyPort* \[ dans\]
</dt> <dd>

**System. Int32** qui est le port proxy à utiliser.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode n’a aucun effet, sauf si la valeur récupérée à partir de **IWMPNetwork. getProxySettings** est 2 (utiliser des paramètres manuels).

Cette méthode échoue sauf si l’application appelante est en cours d’exécution sur l’ordinateur local ou sur l’intranet.

## <a name="examples"></a>Exemples

l’exemple de code suivant utilise **setProxyPort** pour spécifier le numéro de port du proxy Lecteur Windows Media pour le protocole MMS. Le numéro de port est récupéré à partir d’une zone de texte lorsque l’utilisateur clique sur un bouton. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
private void setProxyPort_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new proxy port number.
        int portnumber = System.Convert.ToInt32(portText.Text);

        // Set the proxy port.
        player.network.setProxyPort("MMS", portnumber);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setProxyPort_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setProxyPort.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new proxy port number.
        Dim portnumber As Integer = System.Convert.ToInt32(portText.Text)

        &#39; Set the proxy port.
        player.network.setProxyPort(&quot;MMS&quot;, portnumber)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPNetwork (VB et C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. getProxyPort (VB et C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. getProxySettings (VB et C#)**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





