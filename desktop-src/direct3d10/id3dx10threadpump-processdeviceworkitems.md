---
description: Définissez les éléments de travail sur l’appareil une fois qu’ils ont terminé le chargement et le traitement.
ms.assetid: 67a9fcb2-3513-413d-ac3d-9988ef7b5a1f
title: ID3DX10ThreadPump ::P méthode rocessDeviceWorkItems (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.ProcessDeviceWorkItems
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 88b98d68e4e0e47b2c8e7f9a2e095565c53e2561
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116299"
---
# <a name="id3dx10threadpumpprocessdeviceworkitems-method"></a>ID3DX10ThreadPump ::P méthode rocessDeviceWorkItems

Définissez les éléments de travail sur l’appareil une fois qu’ils ont terminé le chargement et le traitement. Lorsque la pompe de thread a terminé le chargement et le traitement d’une ressource ou d’un nuanceur, elle le contiendra dans une file d’attente jusqu’à ce que cette API soit appelée, auquel cas les éléments traités seront définis sur l’appareil. Cela est utile pour contrôler la quantité de traitement consacrée à la liaison de ressources à l’appareil pour chaque trame. Consultez la section Remarques.

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

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre d’éléments de travail à définir sur l’appareil. ProcessDeviceObjectCreation va créer au maximum objets iWorkItemCount. S’il n’y a pas assez d’éléments de travail dans la file d’attente pour traiter les objets iWorkItemCount, ProcessDeviceObjectCreation créera autant d’objets d’appareil qu’il y a d’éléments dans la file d’attente.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Notes

En guise d’exemple de l’utilisation de cette API, imaginons que vous approchez de la fin d’un niveau de votre jeu et que vous souhaitez commencer à précharger les textures, les nuanceurs et les autres ressources pour le niveau suivant. La pompe de threads démarre le chargement, la décompression et le traitement des ressources et des nuanceurs sur un thread séparé jusqu’à ce qu’ils soient prêts à être définis sur l’appareil. à partir de là, il les laisse dans une file d’attente. Il se peut que vous ne souhaitiez pas définir toutes les ressources et tous les nuanceurs sur l’appareil en même temps, car cela peut entraîner un ralentissement temporaire pouvant être remarqué dans les performances du jeu. Par conséquent, cette API peut être appelée une fois par frame afin que seuls les petits éléments de travail soient définis sur le périphérique de chaque trame, répartissant ainsi la charge de travail des ressources de liaison sur l’appareil sur plusieurs trames et minimisant la probabilité d’un ralentissement des performances du jeu.

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

 

 
