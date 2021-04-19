---
title: IWMPDVD méthode back
description: La méthode back remplace l’affichage d’un sous-menu par son menu parent.
ms.assetid: 81d033d4-f570-44a5-898a-e419101c04fa
keywords:
- méthode back du lecteur Windows Media
- méthode back du lecteur Windows Media, interface IWMPDVD
- Interface IWMPDVD lecteur Windows Media, méthode back
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
ms.openlocfilehash: 4cd31cd6365843a6905760c4447ea679e15e70ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542742"
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

## <a name="remarks"></a>Notes

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

 

 





