---
title: Méthode IWMPMedia getAttributeName
description: La méthode getAttributeName retourne le nom de l’attribut correspondant à l’index spécifié.
ms.assetid: d2496484-34cc-4222-9bc3-1d3ebb9a4173
keywords:
- Lecteur Windows Media de la méthode getAttributeName
- méthode getAttributeName Lecteur Windows Media, interface IWMPMedia
- Lecteur Windows Media de l’interface IWMPMedia, méthode getAttributeName
topic_type:
- apiref
api_name:
- IWMPMedia.getAttributeName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb40ef8c0c984258dc11dd00c80807db2f4eb64a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414557"
---
# <a name="iwmpmediagetattributename-method"></a>IWMPMedia :: getAttributeName, méthode

La méthode **getAttributeName** retourne le nom de l’attribut correspondant à l’index spécifié.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.String getAttributeName(
  System.Int32 lIndex
);
```


```VB

Public Function getAttributeName( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPMedia.getAttributeName
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*Lindex* \[ dans\]
</dt> <dd>

**System. Int32** qui est l’index.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

**System. String** qui est le nom de l’attribut.

## <a name="remarks"></a>Notes

Le nom d’attribut retourné peut être utilisé conjointement avec **getItemInfo** pour récupérer la valeur d’un attribut nommé spécifique.

Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

pour plus d’informations sur les attributs pris en charge par Lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md).

## <a name="examples"></a>Exemples

L’exemple suivant utilise **getAttributeName** pour remplir une zone de texte multiligne avec l’index et le nom de chaque attribut de l’élément multimédia en cours. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
// Store an IWMPMedia3 interface for the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes for the current media item. 
int attCount = cm.attributeCount;

// Create an array of strings to hold the index and name for each attribute.
string[] attInfo = new string[attCount];

// Loop through the attribute list.
for (int i = 0; i < attCount; i++)
{
    // Store the attribute index and name in the array.
    attInfo[i] = ("Attribute " + i + ": " + cm.getAttributeName(i));
}

// Display the attribute information in the text box.
attributeNames.Lines = attInfo;
```


```VB

' Store an IWMPMedia3 interface for the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes for the current media. 
Dim attCount As Integer = cm.attributeCount

&#39; Create an array of strings to hold the index and name for each attribute.
Dim attInfo(attCount) As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (attCount - 1)

    &#39; Store the attribute index and name in the array.
    attInfo(i) = (&quot;Attribute &quot; + i.ToString() + &quot;: &quot; + cm.getAttributeName(i))

Next i

&#39; Display the attribute information in the text box.
attributeNames.Lines = attInfo
```





## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getItemInfo (VB et C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





