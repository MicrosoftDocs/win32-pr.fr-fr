---
title: IWMPMedia. isIdentical (VB et C)
description: La propriété isIdentical (méthode obtenir \_ isIdentical dans C \) obtient une valeur indiquant si l’élément multimédia spécifié est le même que celui actuel.
ms.assetid: 1406a0ff-2dc8-4cde-8b71-4a39b8608fb1
keywords:
- IWMPMedia. isIdentical (VB et C) lecteur Windows Media
topic_type:
- apiref
api_name:
- IWMPMedia.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a488ad300362c1f8dccfd0fa6f6c7e4dee7676
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545599"
---
# <a name="iwmpmediaisidentical-vb-and-c"></a>IWMPMedia. isIdentical (VB et C#)

La propriété **isIdentical** (méthode **obtenir \_ isIdentical** en C#) obtient une valeur indiquant si l’élément multimédia spécifié est le même que celui actuel.


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPMedia As IWMPMedia
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPMedia pIWMPMedia
);
```



## <a name="parameters"></a>Paramètres

*pIWMPMedia*

Interface **wmplib. IWMPMedia** de l’élément multimédia à comparer avec l’élément multimédia actuel.

## <a name="property-value"></a>Valeur de propriété

Valeur **System. Boolean** qui indique si les deux éléments multimédias sont identiques.

## <a name="remarks"></a>Notes

**IWMPMedia. isIdentical** est une propriété de Visual Basic qui accepte un paramètre. En C#, on parle de méthode **IWMPMedia. obten \_ isIdentical** .

## <a name="examples"></a>Exemples

L’exemple suivant utilise la propriété **isIdentical** (méthode **obtenir \_ isIdentical** en C#) pour vérifier si un élément multimédia nommé newMedia est le même que l’élément multimédia en cours. Si ce n’est pas le cas, le nouvel élément multimédia est lu. Dans le cas contraire, le média actuel continue de s’exécuter sans interruption. L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.


```CSharp
if (newMedia.get_isIdentical(player.currentMedia) != true)
{
    // Change the current media to the new media item.
    player.currentMedia = newMedia;

    // Play the new media item.
    player.Ctlcontrols.play();
}
```


```VB

If (newMedia.isIdentical(player.currentMedia) <> True) Then

    &#39; Change the current media to the new media item.
    player.currentMedia = newMedia

    &#39; Play the new media item.
    player.Ctlcontrols.play()

End If
```





## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPMedia (VB et C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





