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
ms.openlocfilehash: 4cd31cd6365843a6905760c4447ea679e15e70ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193064"
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

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Chaque DVD est créé différemment. Certains DVD sont créés afin que la `back` méthode soit disponible dans le menu racine, mais lorsqu’elle est appelée, elle ne fait rien.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPDVD (VB et C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





