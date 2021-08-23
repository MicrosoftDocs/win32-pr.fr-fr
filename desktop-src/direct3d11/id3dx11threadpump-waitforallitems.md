---
title: Méthode ID3DX11ThreadPump WaitForAllItems (D3DX11core. h)
description: 'remarque : la bibliothèque de l’utilitaire d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Attend la fin de l’exécution de tous les éléments de travail de la pompe de thread.'
ms.assetid: 6dfdaee8-e563-4c37-a2c1-4b115e29c434
keywords:
- Méthode WaitForAllItems Direct3D 11
- Méthode WaitForAllItems Direct3D 11, interface ID3DX11ThreadPump
- Interface ID3DX11ThreadPump Direct3D 11, méthode WaitForAllItems
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.WaitForAllItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b3dcb5be664e81a479c0459808456fc1417bec78043ae0376f125c62c65a208
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729100"
---
# <a name="id3dx11threadpumpwaitforallitems-method"></a>ID3DX11ThreadPump :: WaitForAllItems, méthode

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.

 

Attend la fin de l’exécution de tous les éléments de travail de la pompe de thread.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WaitForAllItems();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11ThreadPump](id3dx11threadpump.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





