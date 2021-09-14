---
title: IWMPControls2 Step, méthode
description: La méthode STEP fait passer l’élément multimédia vidéo actuel au frame suivant ou au frame précédent et fige la lecture.
ms.assetid: c5cb720f-527f-45b6-ae8a-4da0e3e34618
keywords:
- step, méthode Lecteur Windows Media
- step, méthode Lecteur Windows Media, IWMPControls2, interface
- Lecteur Windows Media de l’interface IWMPControls2, méthode step
topic_type:
- apiref
api_name:
- IWMPControls2.step
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cfb65dd20de506a8f303121b23668e2fbf14dc4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010747"
---
# <a name="iwmpcontrols2step-method"></a>IWMPControls2 :: Step, méthode

La méthode **Step** fait passer l’élément multimédia vidéo actuel au frame suivant ou au frame précédent et fige la lecture.

## <a name="syntax"></a>Syntaxe


```CSharp
public void step(
  System.Int32 lStep
);
```


```VB

Public Sub step( _
  ByVal lStep As System.Int32 _
)
Implements IWMPControls2.step
```





## <a name="parameters"></a>Paramètres

<dl> <dt>

*lStep* \[ dans\]
</dt> <dd>

Valeur **System. Int32** indiquant le nombre de frames à exécuter avant le gel. Doit avoir la valeur 1 ou-1.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode ne prend actuellement en charge que les paramètres 1 ou-1, de sorte que vous ne pouvez exécuter qu’un seul Frame à la fois.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Lecteur Windows Media série 9 ou version ultérieure<br/>                                                                      |
| Espace de noms<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPControls2 (VB et C#)**](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[**Interface IWMPDVD (VB et C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





