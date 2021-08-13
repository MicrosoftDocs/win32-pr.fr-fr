---
title: IWMPDVD méthode back
description: La méthode back remplace l’affichage d’un sous-menu par son menu parent.
ms.assetid: 81d033d4-f570-44a5-898a-e419101c04fa
keywords:
- Lecteur Windows Media de la méthode back
- Lecteur Windows Media de la méthode back, interface IWMPDVD
- Lecteur Windows Media de l’interface IWMPDVD, méthode back
topic_type:
- apiref
api_name:
- IWMPDVD.back
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483e8e36f8ac5e539925306a53c04d144fb6de1281878840fc598c96c814f002
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414559"
---
# <a name="iwmpdvdback-method"></a>IWMPDVD :: Back, méthode

La méthode **Back** remplace l’affichage d’un sous-menu par son menu parent.

## <a name="syntax"></a>Syntaxe


```CSharp
public void back();
```


```VB

Public Sub back()
Implements IWMPDVD.back
```





## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Chaque DVD est créé différemment. Certains DVD sont créés afin que la `back` méthode soit disponible dans le menu racine, mais lorsqu’elle est appelée, elle ne fait rien.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPDVD (VB et C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





