---
title: IWMPPlaylist propriété attributeCount
description: La propriété attributeCount obtient le nombre d’attributs associés à une sélection.
ms.assetid: 0713ec4e-7e06-4ad2-8f7c-17ed5a92d5ee
keywords:
- propriété attributeCount lecteur Windows Media
- propriété attributeCount lecteur Windows Media, interface IWMPPlaylist
- Interface IWMPPlaylist lecteur Windows Media, propriété attributeCount
topic_type:
- apiref
api_name:
- IWMPPlaylist.attributeCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4107eb1ad302415715b573b55d2dee1d7155128d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540600"
---
# <a name="iwmpplaylistattributecount-property"></a>IWMPPlaylist :: attributeCount, propriété

La propriété **attributeCount** obtient le nombre d’attributs associés à une sélection.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 attributeCount {get; set;}
```


```VB

Public ReadOnly Property attributeCount As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui correspond au nombre d’attributs associés à la sélection.

## <a name="remarks"></a>Notes

Étant donné que les sélections peuvent provenir de nombreuses sources différentes, elles peuvent avoir plusieurs ensembles différents d’attributs. Cette propriété obtient le nombre total d’attributs associés à une sélection particulière afin que d’autres membres de l’interface **IWMPPlaylist** puissent y accéder.

Avant d’utiliser cette propriété, vous devez disposer d’un accès en lecture à la bibliothèque. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la [référence des attributs](attribute-reference.md).

## <a name="examples"></a>Exemples

L’exemple suivant illustre la façon dont différentes propriétés et méthodes des interfaces **IWMPPlaylist** et **IWMPMedia** sont utilisées en remplissant un contrôle TreeView avec des nœuds pour la sélection actuelle, les attributs de sélection, les éléments multimédias dans la sélection et les attributs d’élément multimédia. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
WMPLib.IWMPPlaylist playlist = player.currentPlaylist;
WMPLib.IWMPMedia media;
string name;

// Demonstrates setItemInfo()
playlist.setItemInfo("custom playlist attribute", "changed");
playlist.get_Item(0).setItemInfo("new custom attribute", "5");

// Create a tree node for each playlist attribute and a subnode for the item info of that attribute.
System.Windows.Forms.TreeNode playlistRootNode = new System.Windows.Forms.TreeNode("Playlist Attributes");

for (int i = 0; i < playlist.attributeCount; ++i)
{
    // Add a tree node for each playlist attribute.
    string attribute = playlist.get_attributeName(i);
    playlistRootNode.Nodes.Add(new System.Windows.Forms.TreeNode(attribute));

    // Add a subnode for the item info for that attribute.
    string info = playlist.getItemInfo(attribute);
    playlistRootNode.Nodes[i].Nodes.Add(new System.Windows.Forms.TreeNode(info));
}

// Add the playlist root node to the tree
displayAttributes.Nodes.Add(playlistRootNode);

// Add nodes for each media item and subnodes for each attribute of that item.
System.Windows.Forms.TreeNode mediaRootNode = new System.Windows.Forms.TreeNode("Media Items in the Playlist");
for(int i = 0; i < playlist.count; i++)
{
    // Get the media item
    media = playlist.get_Item(i);

    // Add a tree node for each media item in the playlist.
    mediaRootNode.Nodes.Add(new System.Windows.Forms.TreeNode(media.name));

    // Add a child node for each attribute of the media item
    for(int j = 0; j < media.attributeCount; j++)
    {
        name = media.getAttributeName(j);
        mediaRootNode.Nodes[i].Nodes.Add(new System.Windows.Forms.TreeNode(name + ": " + media.getItemInfo(name)));
    }
}

// Add the media root node to the tree
displayAttributes.Nodes.Add(mediaRootNode);
```


```VB

Dim playlist As WMPLib.IWMPPlaylist = player.currentPlaylist
Dim Media As WMPLib.IWMPMedia
Dim name As String

&#39; Demonstrates setItemInfo()
playlist.setItemInfo(&quot;custom playlist attribute&quot;, &quot;changed&quot;)
playlist.Item(0).setItemInfo(&quot;new custom attribute&quot;, &quot;5&quot;)

&#39; Create a tree node for each playlist attribute and a subnode for the item info of that attribute.
Dim playlistRootNode As System.Windows.Forms.TreeNode = New System.Windows.Forms.TreeNode(&quot;Playlist Attributes&quot;)

For i As Integer = 0 To (playlist.attributeCount - 1) Step 1

    &#39; Add a tree node for each playlist attribute.
    Dim attribute As String = playlist.attributeName(i)
    playlistRootNode.Nodes.Add(New System.Windows.Forms.TreeNode(attribute))

    &#39; Add a subnode for the item info for that attribute.
    Dim info As String = playlist.getItemInfo(attribute)
    playlistRootNode.Nodes(i).Nodes.Add(New System.Windows.Forms.TreeNode(info))

Next i

&#39; Add the playlist root node to the tree
displayAttributes.Nodes.Add(playlistRootNode)

&#39; Add nodes for each media item and subnodes for each attribute of that item.
Dim mediaRootNode As System.Windows.Forms.TreeNode = New System.Windows.Forms.TreeNode(&quot;Media Items in the Playlist&quot;)

For i As Integer = 0 To (playlist.count - 1) Step 1

    &#39; Get the media item
    Media = playlist.Item(i)

    &#39; Add a tree node for each media item in the playlist.
    mediaRootNode.Nodes.Add(New System.Windows.Forms.TreeNode(Media.name))

    &#39; Add a child node for each attribute of the media item
    For j As Integer = 0 To (Media.attributeCount - 1) Step 1

        name = Media.getAttributeName(j)
        mediaRootNode.Nodes(i).Nodes.Add(New System.Windows.Forms.TreeNode(name + &quot;: &quot; + Media.getItemInfo(name)))

    Next j

Next i

&#39; Add the media root node to the tree
displayAttributes.Nodes.Add(mediaRootNode)
```





## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPPlaylist (VB et C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





