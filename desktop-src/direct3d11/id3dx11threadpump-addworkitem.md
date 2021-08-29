---
title: Méthode ID3DX11ThreadPump AddWorkItem (D3DX11core. h)
description: 'remarque : la bibliothèque de l’utilitaire d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Ajoute un élément de travail à la pompe de thread.'
ms.assetid: 2578506c-6175-457a-bf10-94929bb3c0c4
keywords:
- Méthode AddWorkItem Direct3D 11
- Méthode AddWorkItem Direct3D 11, interface ID3DX11ThreadPump
- Interface ID3DX11ThreadPump Direct3D 11, méthode AddWorkItem
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.AddWorkItem
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbf0fda0ef2410ea7bd2e08a350d1e56e85c1beb999568ccfa4a653db1e22212
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119659"
---
# <a name="id3dx11threadpumpaddworkitem-method"></a>ID3DX11ThreadPump :: AddWorkItem, méthode

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.

 

Ajoute un élément de travail à la pompe de thread.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddWorkItem(
  [in]  ID3DX11DataLoader    *pDataLoader,
  [in]  ID3DX11DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDataLoader* \[ dans\]
</dt> <dd>

Type : **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\***

Chargeur que la pompe de threads utilisera lorsqu’un élément de travail nécessite le chargement de données.

</dd> <dt>

*pDataProcessor* \[ dans\]
</dt> <dd>

Type : **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\***

Processeur que la pompe de threads utilisera lorsqu’un élément de travail nécessitera un traitement des données.

</dd> <dt>

*pHResult* \[ dans\]
</dt> <dd>

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Pointeur vers la valeur de retour. Peut avoir la **valeur null**.

</dd> <dt>

*ppDeviceObject* \[ à\]
</dt> <dd>

Type : **void \* \***

Périphérique qui utilise l’objet.

</dd> </dl>

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

 

 





