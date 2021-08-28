---
title: Méthode ID3DX11ThreadPump GetQueueStatus (D3DX11core. h)
description: 'remarque : la bibliothèque de l’utilitaire d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Obtient le nombre d’éléments dans chacune des trois files d’attente à l’intérieur de la pompe de thread.'
ms.assetid: 69e1c786-6c7d-4432-bf34-3bf7606a07f6
keywords:
- Méthode GetQueueStatus Direct3D 11
- Méthode GetQueueStatus Direct3D 11, interface ID3DX11ThreadPump
- Interface ID3DX11ThreadPump Direct3D 11, méthode GetQueueStatus
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.GetQueueStatus
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41535dba7c5abb96c132714ecbc6ee4e02f1f42fcb6a45ebe8795286d8613c66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851499"
---
# <a name="id3dx11threadpumpgetqueuestatus-method"></a>ID3DX11ThreadPump :: GetQueueStatus, méthode

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.

 

Obtient le nombre d’éléments dans chacune des trois files d’attente à l’intérieur de la pompe de thread.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pIoQueue* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***

Nombre d’éléments dans la file d’attente d’e/s.

</dd> <dt>

*pProcessQueue* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***

Nombre d’éléments dans la file d’attente de traitement.

</dd> <dt>

*pDeviceQueue* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***

Nombre d’éléments dans la file d’attente de l’appareil.

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

 

