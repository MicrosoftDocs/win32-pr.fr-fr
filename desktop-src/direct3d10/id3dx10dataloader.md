---
description: Objet chargeant des données utilisé par l’interface ID3DX10ThreadPump pour le chargement des données de façon asynchrone.
ms.assetid: bda2414c-bbab-47ac-b23a-f58fb86e732d
title: Interface ID3DX10DataLoader (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 86da40dd581c10d9f567f6011cd3987710a9aa36e41f360dc4ffc2662f909c18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128356"
---
# <a name="id3dx10dataloader-interface"></a>Interface ID3DX10DataLoader

Objet chargeant des données utilisé par l' [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) pour le chargement des données de façon asynchrone.

## <a name="members"></a>Membres

L’interface **ID3DX10DataLoader** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10DataLoader** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX10DataLoader** possède ces méthodes.



| Méthode                                             | Description                                                                                                                                                                                                                        |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Décompresser**](id3dx10dataloader-decompress.md) | Utilisé pour décompresser des données encodées. En général, cette valeur est utilisée pour charger des ressources à partir de systèmes de fichiers, tels que des fichiers ZIP. Lors du chargement à partir d’une ressource non compressée, l’étape de décompression n’a pas besoin d’effectuer de travail.<br/> |
| [**Suppression**](id3dx10dataloader-destroy.md)       | Utilisé par une [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) pour détruire le chargeur après l’achèvement d’un élément de travail.<br/>                                                                                                   |
| [**Load**](id3dx10dataloader-load.md)             | Utilisé par une [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) pour charger des données à partir d’un disque.<br/>                                                                                                                            |



 

## <a name="remarks"></a>Remarques

Cet objet peut être hérité et ses membres redéfinis. Cela vous permettrait de personnaliser l’API pour le chargement et la décompression de vos propres formats de fichiers personnalisés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
