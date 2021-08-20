---
title: Propriété Count IWMPCdromCollection
description: La propriété Count obtient le nombre de lecteurs CD et DVD disponibles sur le système.
ms.assetid: 1359ab7e-fbe3-461c-801b-7c986f6e5687
keywords:
- Lecteur Windows Media de la propriété count
- Lecteur Windows Media de la propriété count, interface IWMPCdromCollection
- Lecteur Windows Media de l’interface IWMPCdromCollection, propriété count
topic_type:
- apiref
api_name:
- IWMPCdromCollection.count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e042e2a1d84d9e654cd4b50c5e5d726cc0306d64261e3e7d750bb6db73c77a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930629"
---
# <a name="iwmpcdromcollectioncount-property"></a>IWMPCdromCollection :: Count, propriété

La propriété **Count** obtient le nombre de lecteurs CD et DVD disponibles sur le système.

## <a name="syntax"></a>Syntaxe


```CSharp
public System.Int32 count {get; set;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a>Valeur de la propriété

**System. Int32** qui correspond au nombre de lecteurs disponibles.

## <a name="remarks"></a>Remarques

Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

Les lecteurs de DVD sont comptabilisés exactement comme les lecteurs de CD. toutefois, le contrôle de ActiveX Lecteur Windows Media prend en charge uniquement les fonctionnalités de DVD pour Windows XP ou version ultérieure. En règle générale, les lecteurs de DVD peuvent lire des CD, mais les lecteurs de CD ne peuvent pas lire les DVD.

## <a name="examples"></a>Exemples

L’exemple suivant utilise Count pour afficher le nombre de lecteurs de CD et de DVD disponibles dans une boîte de message. L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show("Number of available CD and DVD drives:  " + numDrives.ToString());
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show(&quot;Number of available CD and DVD drives:  &quot; + numDrives.ToString())
```





## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPCdromCollection (VB et C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB et C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB et C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





