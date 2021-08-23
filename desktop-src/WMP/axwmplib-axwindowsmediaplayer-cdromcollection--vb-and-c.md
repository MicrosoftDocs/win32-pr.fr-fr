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
ms.openlocfilehash: dec885de319153383b82359e35208d19031fa7378749b39033402aba11f8dbd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055011"
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

## <a name="remarks"></a>Remarques

Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

## <a name="requirements"></a>Configuration requise



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

 

 





