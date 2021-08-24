---
description: L’interface ID3DXBuffer est utilisée comme mémoire tampon de données, en stockant les informations de vertex, d’adjacence et de matériau pendant les opérations d’optimisation et de chargement du maillage.
ms.assetid: 63ee3b2d-c0e6-4ad4-9274-2b1dfd77f89d
title: Interface ID3DXBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2cc69262949b9cc700f0a7c477bcfacb7dacd1fc51eb836ad76dfaa2fecb7358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121677"
---
# <a name="id3dxbuffer-interface"></a>Interface ID3DXBuffer

L’interface ID3DXBuffer est utilisée comme mémoire tampon de données, en stockant les informations de vertex, d’adjacence et de matériau pendant les opérations d’optimisation et de chargement du maillage. L’objet buffer est utilisé pour retourner des données de longueur arbitraire. En outre, les objets de mémoire tampon sont utilisés pour retourner le code objet et les messages d’erreur dans les méthodes qui assemblent des nuanceurs vertex et de pixels.

## <a name="members"></a>Membres

L’interface **ID3DXBuffer** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXBuffer** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXBuffer** possède ces méthodes.



| Méthode                                                    | Description                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------|
| [**GetBufferPointer**](id3dxbuffer--getbufferpointer.md) | Récupère un pointeur vers les données dans la mémoire tampon.<br/>      |
| [**GetBufferSize**](id3dxbuffer--getbuffersize.md)       | Récupère la taille totale des données dans la mémoire tampon.<br/> |



 

## <a name="remarks"></a>Remarques

L’interface **ID3DXBuffer** est obtenue en appelant la fonction [**D3DXCreateBuffer**](d3dxcreatebuffer.md) .

Le type LPD3DXBUFFER est défini comme un pointeur vers l’interface **ID3DXBuffer** .


```
typedef interface ID3DXBuffer ID3DXBuffer;
typedef interface ID3DXBuffer *LPD3DXBUFFER;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
