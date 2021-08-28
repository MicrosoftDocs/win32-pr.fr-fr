---
title: IWMPMedia. isIdentical (VB et C)
description: La propriété isIdentical (méthode obtenir \_ isIdentical dans C \) obtient une valeur indiquant si l’élément multimédia spécifié est le même que celui actuel.
ms.assetid: 1406a0ff-2dc8-4cde-8b71-4a39b8608fb1
keywords:
- IWMPMedia. isIdentical (VB et C) Lecteur Windows Media
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
ms.openlocfilehash: 24e8de133003bdddcf0438e5a13dc3fa74227ede7bf42350e2b7c3c96f2c197e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003579"
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

## <a name="remarks"></a>Remarques

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

 

 





