---
description: Ajoutez un élément de travail à la pompe de thread.
ms.assetid: f07789dc-a3d5-4bad-9768-527e701271b8
title: 'ID3DX10ThreadPump :: AddWorkItem, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.AddWorkItem
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 43602019018a9751453eb93f4ffb9b1c29eada6caf120a6721522982c3355dfc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609319"
---
# <a name="id3dx10threadpumpaddworkitem-method"></a>ID3DX10ThreadPump :: AddWorkItem, méthode

Ajoutez un élément de travail à la pompe de thread.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddWorkItem(
  [in]  ID3DX10DataLoader    *pDataLoader,
  [in]  ID3DX10DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDataLoader* \[ dans\]
</dt> <dd>

Type : **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\***

Chargeur que la pompe de threads utilisera lorsqu’un élément de travail nécessite le chargement de données.

</dd> <dt>

*pDataProcessor* \[ dans\]
</dt> <dd>

Type : **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***

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

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX10ThreadPump](id3dx10threadpump.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




