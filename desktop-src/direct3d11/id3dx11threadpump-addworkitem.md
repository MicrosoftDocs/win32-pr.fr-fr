---
title: Méthode ID3DX11ThreadPump AddWorkItem (D3DX11core. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Ajoute un élément de travail à la pompe de thread.'
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
ms.openlocfilehash: ebf249405bd71287f93444ae8d23dab694027360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322686"
---
# <a name="id3dx11threadpumpaddworkitem-method"></a>ID3DX11ThreadPump :: AddWorkItem, méthode

> [!Note]  
> La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.

 

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

## <a name="requirements"></a>Spécifications



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

 

 





