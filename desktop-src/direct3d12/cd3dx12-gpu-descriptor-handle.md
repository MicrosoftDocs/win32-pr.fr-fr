---
title: Structure CD3DX12_GPU_DESCRIPTOR_HANDLE (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure de handle de \_ descripteur GPU D3D12 \_ .
ms.assetid: 6E405AD6-D370-4B87-849A-C52D64C79BF7
keywords:
- Structure CD3DX12_GPU_DESCRIPTOR_HANDLE
topic_type:
- apiref
api_name:
- CD3DX12_GPU_DESCRIPTOR_HANDLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429d41d401b7d3e928bc4ab76850b36ae41b1e8a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537241"
---
# <a name="cd3dx12_gpu_descriptor_handle-structure"></a>\_Structure du \_ handle du descripteur GPU CD3DX12 \_

Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ \_ \_ handle de descripteur GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_GPU_DESCRIPTOR_HANDLE  : public D3D12_GPU_DESCRIPTOR_HANDLE{
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE();
                                  explicit CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &o);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(CD3DX12_DEFAULT);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &other, INT offsetScaledByIncrementSize);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_GPU_DESCRIPTOR_HANDLE&  Offset(INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_GPU_DESCRIPTOR_HANDLE&  Offset(INT offsetScaledByIncrementSize);
  bool                            inline operator==( _In_ const D3D12_GPU_DESCRIPTOR_HANDLE& other) const;
  bool                            inline operator!=( _In_ const D3D12_GPU_DESCRIPTOR_HANDLE& other) const;
  CD3DX12_GPU_DESCRIPTOR_HANDLE & operator=(const D3D12_GPU_DESCRIPTOR_HANDLE &other);
  void                            inline InitOffsetted(_In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            inline InitOffsetted(_In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_GPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_GPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_ \_ Handle de descripteur GPU CD3DX12 \_ ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ \_ handle de descripteur GPU CD3DX12 \_ .

</dd> <dt>

**\_ \_ handle de descripteur GPU CD3DX12 explicite \_ ( \_ handle de descripteur gpu const D3D12 \_ \_ &o)**
</dt> <dd>

Crée une nouvelle instance d’un \_ handle de \_ descripteur GPU CD3DX12 \_ , initialisée avec le contenu d’une autre structure de [**\_ \_ \_ handle de descripteur GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) .

</dd> <dt>

**\_Handle du \_ descripteur GPU CD3DX12 \_ (CD3DX12 \_ par défaut)**
</dt> <dd>

Crée une nouvelle instance d’un \_ handle de \_ descripteur GPU CD3DX12 \_ , initialisée avec les paramètres par défaut (définit le pointeur sur zéro).

</dd> <dt>

**\_ \_ Handle de descripteur GPU CD3DX12 \_ ( \_ handle de descripteur gpu const D3D12 \_ \_ &autre, int offsetScaledByIncrementSize)**
</dt> <dd>

Crée une nouvelle instance d’un \_ handle de \_ descripteur GPU CD3DX12 \_ , en initialisant les paramètres suivants :

\_Handle du \_ descripteur GPU D3D12 \_ &autre

INT offsetScaledByIncrementSize : nombre d’incréments de décalage.

</dd> <dt>

**\_ \_ Handle de descripteur GPU CD3DX12 \_ ( \_ handle de descripteur gpu const D3D12 \_ \_ &autre, int offsetInDescriptors, uint descriptorIncrementSize)**
</dt> <dd>

Crée une nouvelle instance d’un \_ handle de \_ descripteur GPU CD3DX12 \_ , en initialisant les paramètres suivants :

\_Handle du \_ descripteur GPU D3D12 \_ &autre

INT offsetInDescriptors : nombre de descripteurs par incrément.

UINT descriptorIncrementSize : quantité par laquelle incrémenter pour chaque descripteur, y compris le remplissage.

</dd> <dt>

**Offset (INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Définit le décalage en fonction du nombre spécifié de descripteurs et de la quantité d’incrémentation pour chaque descripteur. Utilise les paramètres suivants :

INT offsetInDescriptors : nombre de descripteurs par incrément.

UINT descriptorIncrementSize : quantité par laquelle incrémenter pour chaque descripteur, y compris le remplissage.

</dd> <dt>

**Offset (INT offsetScaledByIncrementSize)**
</dt> <dd>

Définit le décalage en fonction du nombre d’incréments spécifié. Utilise les paramètres suivants :

INT offsetScaledByIncrementSize : nombre d’incréments de décalage.

</dd> <dt>

**opérateur inline = = ( \_ dans le \_ handle de \_ descripteur de GPU const D3D12 \_ \_& autre) const**
</dt> <dd>

Teste l’égalité entre le \_ handle du descripteur GPU CD3DX12 actuel et le handle du descripteur GPU D3D12 ou le handle du descripteur GPU \_ \_ \_ CD3DX12 spécifié \_ \_ \_ \_ \_ .

</dd> <dt>

**opérateur inline ! = ( \_ dans le \_ handle de \_ descripteur GPU const D3D12 \_ \_& autre) const**
</dt> <dd>

Vérifie l’inégalité entre le handle du \_ descripteur GPU CD3DX12 actuel et le handle du descripteur GPU D3D12 ou le handle du descripteur GPU \_ \_ \_ CD3DX12 spécifié \_ \_ \_ \_ \_ .

</dd> <dt>

**Operator = (D3D12 \_ \_ &handle du descripteur GPU const \_ )**
</dt> <dd>

Définit le handle du \_ \_ descripteur GPU CD3DX12 actuel \_ sur les mêmes valeurs que le handle du descripteur GPU D3D12 \_ ou le \_ \_ \_ \_ \_ handle du descripteur GPU CD3DX12 spécifié.

</dd> <dt>

**Inline InitOffsetted ( \_ dans le \_ handle du \_ descripteur GPU const D3D12 \_ \_ &base, int offsetScaledByIncrementSize)**
</dt> <dd>

Initialise une structure [**de \_ \_ \_ handle de descripteur GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) avec le nombre spécifié d’éléments. Utilise les paramètres suivants :

\_Dans \_ \_ \_ le handle de descripteur GPU const D3D12 \_ &base : adresse de base à partir de laquelle l’offset doit être décalé.

INT offsetScaledByIncrementSize : nombre d’incréments de décalage.

</dd> <dt>

**Inline InitOffsetted ( \_ dans le \_ handle du \_ descripteur GPU const D3D12 \_ \_ &base, int offsetInDescriptors, uint descriptorIncrementSize)**
</dt> <dd>

Initialise une structure [**de \_ \_ \_ handle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) de descripteur GPU D3D12 avec un offset, à l’aide du nombre spécifié de descripteurs de la taille donnée. Utilise les paramètres suivants :

\_Dans \_ \_ \_ le handle de descripteur GPU const D3D12 \_ &base : adresse de base à partir de laquelle l’offset doit être décalé.

INT offsetInDescriptors : nombre de descripteurs par lequel décaler.

UINT descriptorIncrementSize : quantité par laquelle incrémenter pour chaque descripteur, y compris le remplissage.

</dd> <dt>

**handle \_ \_ \_ de descripteur InitOffsetted (out D3D12 \_ descripteur &de descripteur, handle \_ de de&scripteur \_ de \_ \_ \_ \_ graphique**
</dt> <dd>

Initialise une structure [**de \_ \_ \_ handle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) de descripteur GPU D3D12 avec un offset, à l’aide du nombre spécifié de descripteurs de la taille donnée. Utilise les paramètres suivants :

\_\_D3D12 handle \_ \_ du descripteur GPU \_ de sortie de la gestion des & : génère le \_ handle du \_ descripteur GPU D3D12 résultant \_ .

\_Dans \_ \_ \_ le handle de descripteur GPU const D3D12 \_ &base : adresse de base à partir de laquelle l’offset doit être décalé.

INT offsetScaledByIncrementSize : nombre d’incréments de décalage.

</dd> <dt>

**static Inline InitOffsetted ( \_ \_ \_ \_ descripteur de descripteur GPU out D3D12 \_ &handle, \_ dans le \_ handle de \_ descripteur GPU const D3D12 \_ \_ &base, int offsetInDescriptors, uint descriptorIncrementSize)**
</dt> <dd>

Initialise une structure [**de \_ \_ \_ handle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) de descripteur GPU D3D12 avec un offset, à l’aide du nombre spécifié de descripteurs de la taille donnée. Utilise les paramètres suivants :

\_\_D3D12 handle \_ \_ du descripteur GPU \_ de sortie de la gestion des & : génère le \_ handle du \_ descripteur GPU D3D12 résultant \_ .

\_Dans \_ \_ \_ le handle de descripteur GPU const D3D12 \_ &base : adresse de base à partir de laquelle l’offset doit être décalé.

INT offsetInDescriptors : nombre de descripteurs par lequel décaler.

UINT descriptorIncrementSize : quantité par laquelle incrémenter pour chaque descripteur, y compris le remplissage.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Handle du \_ descripteur GPU D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





