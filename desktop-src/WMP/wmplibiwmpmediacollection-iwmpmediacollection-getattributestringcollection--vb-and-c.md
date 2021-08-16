---
title: Méthode IWMPMediaCollection getAttributeStringCollection
description: La méthode getAttributeStringCollection retourne une interface IWMPStringCollection qui représente l’ensemble de toutes les valeurs d’un attribut spécifié dans un type de média.
ms.assetid: 5ac19c04-75db-4618-9c4e-b20e2f709024
keywords:
- Lecteur Windows Media de la méthode getAttributeStringCollection
- méthode getAttributeStringCollection Lecteur Windows Media, interface IWMPMediaCollection
- Lecteur Windows Media de l’interface IWMPMediaCollection, méthode getAttributeStringCollection
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAttributeStringCollection
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 508630ee8a377e1542f823c1afb21521206369aa3ce489c58afae47efa268880
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331941"
---
# <a name="iwmpmediacollectiongetattributestringcollection-method"></a>IWMPMediaCollection :: getAttributeStringCollection, méthode

La méthode **getAttributeStringCollection** retourne une interface **IWMPStringCollection** qui représente l’ensemble de toutes les valeurs d’un attribut spécifié dans un type de média.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPStringCollection getAttributeStringCollection(
  System.String bstrAttribute,
  System.String bstrMediaType
);
```


```VB

Public Function getAttributeStringCollection( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPStringCollection
Implements IWMPMediaCollection.getAttributeStringCollection
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrAttribute* \[ dans\]
</dt> <dd>

**System. String** qui est l’attribut pour lequel les valeurs sont récupérées.

</dd> <dt>

*bstrMediaType* \[ dans\]
</dt> <dd>

**System. String** qui est le type de média pour lequel les valeurs sont récupérées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Interface **wmplib. IWMPStringCollection** pour les valeurs récupérées.

## <a name="remarks"></a>Remarques

Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

pour plus d’informations sur les attributs pris en charge par Lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md).

## <a name="examples"></a>Exemples

L’exemple suivant utilise **getAttributeStringCollection** pour afficher une liste de valeurs qui correspondent à un attribut particulier pour les éléments audio de la collection de supports. Une zone de liste permet à l’utilisateur de sélectionner un attribut, tel qu’un artiste, un genre ou un album, et une zone de texte multiligne affiche le résultat. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
private void audioAttributes_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Retrieve the attribute type from the ListBox
    string attributeType = (string)((System.Windows.Forms.ListBox)sender).SelectedItem;

    // Get an interface to the mediaCollection.  
    WMPLib.IWMPMediaCollection2 library = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

    // Get an interface to the string collection for the attribute type the user selects.
    WMPLib.IWMPStringCollection2 all = (WMPLib.IWMPStringCollection2)library.getAttributeStringCollection(attributeType, "Audio");

    // Clear the text box of previous results.
    attributeValues.Clear();

    // Create an array to hold the attribute values.
    string[] attributeArray = new string[all.count];
    
    // Loop through the string collection.
    for (int i = 0; i < all.count; i++)
    {
        // Store the items in the array.
        attributeArray[i] = all.Item(i);
    }

    // Display the items in the text box.
    attributeValues.Lines = attributeArray;
}
```


```VB

Public Sub audioAttributes_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles audioAttributes.SelectedIndexChanged

    &#39; Retrieve the attribute type from the ListBox
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim attributeType As String = lb.SelectedItem

    &#39; Get an interface to the mediaCollection.  
    Dim library As WMPLib.IWMPMediaCollection2 = player.mediaCollection

    &#39; Get an interface to the string collection for the attribute type the user selects.
    Dim all As WMPLib.IWMPStringCollection2 = library.getAttributeStringCollection(attributeType, &quot;Audio&quot;)

    &#39; Clear the text box of previous results.
    attributeValues.Clear()

    &#39; Create an array to hold the attribute values.
    Dim attributeArray(all.count) As String

    &#39; Loop through the string collection.
    For i As Integer = 0 To (all.count - 1)

        &#39; Store the items in the array.
        attributeArray(i) = all.Item(i)

    Next i

    &#39; Display the items in the text box.
    attributeValues.Lines = attributeArray

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

[**Interface IWMPMediaCollection (VB et C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPStringCollection (VB et C#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





