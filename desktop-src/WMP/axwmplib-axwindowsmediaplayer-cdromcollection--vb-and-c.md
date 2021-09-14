---
title: AxWindowsMediaPlayer. cdromCollection, propriété
description: La propriété cdromCollection obtient une interface IWMPCdromCollection qui fournit l’accès à une collection de lecteurs de CD ou DVD.
ms.assetid: 03f4e7d1-4376-4112-993e-943d29aca049
keywords:
- Lecteur Windows Media de la propriété cdromCollection
- Lecteur Windows Media de la propriété cdromCollection, classe AxWindowsMediaPlayer
- Lecteur Windows Media de la classe AxWindowsMediaPlayer, propriété cdromCollection
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.cdromCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4ba3bb5df95e9ee53e2a6c3aecbd1e9a355882
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856035"
---
# <a name="axwindowsmediaplayercdromcollection-property"></a>AxWindowsMediaPlayer. cdromCollection, propriété

La propriété cdromCollection obtient une interface **IWMPCdromCollection** qui fournit l’accès à une collection de lecteurs de CD ou DVD.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```CSharp
public IWMPCdromCollection cdromCollection {get;}
```


```VB

Public ReadOnly Property cdromCollection As IWMPCdromCollection
```





## <a name="property-value"></a>Valeur de la propriété

Interface WMPLib. IWMPCdromCollection.

## <a name="remarks"></a>Notes

Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                          |
| Espace de noms<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**objet AxWindowsMediaPlayer (VB et C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interface IWMPCdromCollection (VB et C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB et C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB et C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





