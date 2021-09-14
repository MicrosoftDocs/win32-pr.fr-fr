---
title: IWMPSettings. isAvailable (VB et C)
description: La propriété isAvailable (la \_ méthode obtenir IsAvailable dans C \) obtient une valeur qui indique si une action spécifiée peut être exécutée.
ms.assetid: 9db1fc50-5c2a-4d2d-b1ed-02b8e6571372
keywords:
- IWMPSettings. isAvailable (VB et C) Lecteur Windows Media
topic_type:
- apiref
api_name:
- IWMPSettings.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e932f0adb325c4c2f9f88e9f80d75ecaecd3ca85
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013270"
---
# <a name="iwmpsettingsisavailable-vb-and-c"></a>IWMPSettings. isAvailable (VB et C#)

La propriété **isAvailable** (la méthode **obtenir \_ isAvailable** en C#) obtient une valeur qui indique si une action spécifiée peut être exécutée.


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a>Paramètres

*bstrItem*

**System. String** qui est l’une des valeurs suivantes.



| Valeur              | Description                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| démarrage automatique          | détecte si la propriété autostart peut être définie pour spécifier que Lecteur Windows Media démarre automatiquement la lecture. |
| Balance            | Détecte si la propriété de balance peut être utilisée pour définir le solde stéréo.                                           |
| BaseURL            | Détecte si la propriété baseURL peut être définie pour spécifier une URL de base.                                                |
| DefaultFrame       | Détecte si la propriété defaultFrame peut être définie pour spécifier le frame par défaut.                                    |
| EnableErrorDialogs | Détecte si la propriété enableErrorDialogs peut être définie pour activer ou désactiver l’affichage des boîtes de dialogue d’erreur.        |
| GetMode            | Détecte si la méthode getMode peut être utilisée pour récupérer la boucle en cours ou le mode de lecture aléatoire.                          |
| InvokeURLs         | Détecte si la propriété invokeURLs peut être définie pour spécifier si les événements d’URL doivent lancer un navigateur Web.         |
| Désactiver le son               | Détecte si la propriété muet peut être définie pour spécifier si la sortie audio est activée ou désactivée.                        |
| PlayCount          | Détecte si la propriété playCount peut être définie pour spécifier le nombre de fois qu’un élément multimédia doit être lu.                 |
| Tarif               | Détecte si la propriété rate peut être définie pour contrôler la vitesse de lecture.                                            |
| SetMode            | Détecte si la méthode setMode peut être utilisée pour spécifier la boucle actuelle ou le mode de lecture aléatoire.                           |
| Volume             | Détecte si la propriété de volume peut être définie pour spécifier le volume audio.                                           |



 

## <a name="property-value"></a>Valeur de propriété

Valeur **System. Boolean** indiquant si l’action spécifiée peut être exécutée.

## <a name="remarks"></a>Remarques

**IWMPSettings. isIdentical** est une propriété de Visual Basic qui accepte un paramètre. En C#, on parle de méthode **IWMPSettings. obten \_ isIdentical** .

## <a name="examples"></a>Exemples

L’exemple suivant teste chacune des propriétés **IWMPSettings** à l’aide de la propriété **isAvailable** (méthode d’extraction de la méthode **\_ IsAvailable** en C#). Le nom de la propriété et le résultat de chaque test sont affichés dans une zone de texte multiligne. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Create a string array that contains a list of IWMPSettings properties.
string[] propertyList = new string[12]{
    "AutoStart", "Balance", "BaseURL", "DefaultFrame", "EnableErrorDialogs",
    "GetMode", "InvokeURLs", "Mute", "PlayCount", "Rate", "SetMode", "Volume"
};

// Create another string array of the same size to hold the result of each
// call to get_isAvailable.
string[] results = new string[12];

// Test each property using get_isAvailable and add the name of the property
// and the result of the test to the results array.
for (int i = 0; i < propertyList.Length; i++)
{
    bool isAvailable = player.settings.get_isAvailable(propertyList[i]);

    results[i] = (propertyList[i] + " = " + isAvailable.ToString());
}

// Display the results in a multi-line text box.
playerSettings.Lines = results;
```


```VB

'  Create a string array that contains a list of IWMPSettings properties.
Dim propertyList As String() = New String(11) { _
    &quot;AutoStart&quot;, &quot;Balance&quot;, &quot;BaseURL&quot;, &quot;DefaultFrame&quot;, &quot;EnableErrorDialogs&quot;, _
    &quot;GetMode&quot;, &quot;InvokeURLs&quot;, &quot;Mute&quot;, &quot;PlayCount&quot;, &quot;Rate&quot;, &quot;SetMode&quot;, &quot;Volume&quot; _
}

&#39;  Create another string array of the same size to hold the result of each
&#39;  call to get_isAvailable.
Dim results(12) As String

&#39;  Test each property using isAvailable and add the name of the property
&#39;  and the result of the test to the results array.
For i As Integer = 0 To (propertyList.Length - 1)

    Dim isAvailable As Boolean = player.settings.isAvailable(propertyList(i))
    results(i) = (propertyList(i) + &quot; = &quot; + isAvailable.ToString())

Next i

&#39;  Display the results in a multi-line text box.
playerSettings.Lines = results
```





## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPSettings (VB et C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. autostart (VB et C#)**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. balance (VB et C#)**](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. baseURL (VB et C#)**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. defaultFrame (VB et C#)**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. enableErrorDialogs (VB et C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. getMode (VB et C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. invokeURLs (VB et C#)**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. muet (VB et C#)**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. playCount (VB et C#)**](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. rate (VB et C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. setMode (VB et C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. volume (VB et C#)**](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)
</dt> </dl>

 

 





