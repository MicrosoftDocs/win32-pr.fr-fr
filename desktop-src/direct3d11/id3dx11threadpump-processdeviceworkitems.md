---
title: Méthode ID3DX11ThreadPump ProcessDeviceWorkItems (D3DX11core. h)
description: 'remarque : la bibliothèque de l’utilitaire d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Définit les éléments de travail sur l’appareil une fois qu’ils ont terminé le chargement et le traitement.'
ms.assetid: 154e6ea5-0a88-4c8a-9c20-e7fbf95f1946
keywords:
- Méthode ProcessDeviceWorkItems Direct3D 11
- Méthode ProcessDeviceWorkItems Direct3D 11, interface ID3DX11ThreadPump
- Interface ID3DX11ThreadPump Direct3D 11, méthode ProcessDeviceWorkItems
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.ProcessDeviceWorkItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ad570785ac7dc36fb5dd9d464e97ef46f52ca93
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414476"
---
# <a name="id3dx11threadpumpprocessdeviceworkitems-method"></a>ID3DX11ThreadPump ::P méthode rocessDeviceWorkItems

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.

 

Définit les éléments de travail sur l’appareil une fois qu’ils ont terminé le chargement et le traitement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*iWorkItemCount* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre d’éléments de travail à définir sur l’appareil.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Notes

Lorsque la pompe de thread a terminé le chargement et le traitement d’une ressource ou d’un nuanceur, elle le contiendra dans une file d’attente jusqu’à ce que cette API soit appelée, auquel cas les éléments traités seront définis sur l’appareil. Cela est utile pour contrôler la quantité de traitement consacrée à la liaison de ressources à l’appareil pour chaque trame.

En guise d’exemple de l’utilisation de cette API, imaginons que vous approchez de la fin d’un niveau de votre jeu et que vous souhaitez commencer à précharger les textures, les nuanceurs et les autres ressources pour le niveau suivant. La pompe de threads démarre le chargement, la décompression et le traitement des ressources et des nuanceurs sur un thread séparé jusqu’à ce qu’ils soient prêts à être définis sur l’appareil. à partir de là, il les laisse dans une file d’attente. Il se peut que vous ne souhaitiez pas définir l’ensemble des ressources et des nuanceurs sur l’appareil en une seule fois, car cela peut entraîner un ralentissement de la vitesse d’exécution d’un jeu. Par conséquent, cette API peut être appelée une fois par frame afin que seuls les petits éléments de travail soient définis sur le périphérique de chaque trame, répartissant ainsi la charge de travail des ressources de liaison sur le périphérique sur plusieurs frames.

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

 

