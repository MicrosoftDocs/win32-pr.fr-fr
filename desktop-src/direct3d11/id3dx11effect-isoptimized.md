---
title: Méthode ID3DX11Effect IsOptimized (D3dx11effect. h)
description: Testez un effet pour voir si les métadonnées de réflexion ont été supprimées de la mémoire.
ms.assetid: fb0a876b-7419-45b7-97fe-8352dd97d8c5
keywords:
- Méthode IsOptimized Direct3D 11
- Méthode IsOptimized Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode IsOptimized
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsOptimized
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd04bf43869f23bfec38db34be1b83b2c4f3953c7017120ebe2f0c985504b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124504"
---
# <a name="id3dx11effectisoptimized-method"></a>ID3DX11Effect :: IsOptimized, méthode

Testez un effet pour voir si les métadonnées de réflexion ont été supprimées de la mémoire.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsOptimized();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

**True** si l’effet est optimisé ; Sinon, **false**.

## <a name="remarks"></a>Remarques

Un effet utilise l’espace mémoire de deux façons différentes : pour stocker les informations requises par le runtime pour exécuter un effet, et pour stocker les métadonnées requises pour répercuter les informations dans une application à l’aide de l’API. Vous pouvez réduire la quantité de mémoire requise par un effet en appelant [**ID3DX11Effect :: Optimize**](id3dx11effect-optimize.md) , qui supprime les métadonnées de réflexion de la mémoire. Bien entendu, les méthodes d’API pour lire des variables ne fonctionnent plus une fois que les données de réflexion ont été supprimées.

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

