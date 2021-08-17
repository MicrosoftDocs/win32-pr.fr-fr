---
title: Structure CD3DX12_CPU_DESCRIPTOR_HANDLE (D3dx12. h)
description: Structure d’assistance pour permettre l’initialisation simple d’une structure de \_ \_ handle de descripteur de processeur D3D12 \_ .
ms.assetid: 91736069-7D13-47B0-B78C-0F6F104F97EB
keywords:
- Structure CD3DX12_CPU_DESCRIPTOR_HANDLE
topic_type:
- apiref
api_name:
- CD3DX12_CPU_DESCRIPTOR_HANDLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e6fd6ba75caccf19f3782e0c39581d1e652de0c4187c3c5a203bb5f3b7ceec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117913076"
---
# <a name="cd3dx12_cpu_descriptor_handle-structure"></a>\_Structure de \_ handle de descripteur de processeur CD3DX12 \_

Structure d’assistance pour permettre l’initialisation simple d’une structure [**de \_ \_ \_ handle de descripteur de processeur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_CPU_DESCRIPTOR_HANDLE  : public D3D12_CPU_DESCRIPTOR_HANDLE{
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE();
                                  explicit CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &o);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(CD3DX12_DEFAULT);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &other, INT offsetScaledByIncrementSize);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_CPU_DESCRIPTOR_HANDLE&  Offset(INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_CPU_DESCRIPTOR_HANDLE&  Offset(INT offsetScaledByIncrementSize);
  bool                            operator==( _In_ const D3D12_CPU_DESCRIPTOR_HANDLE& other) const;
  bool                            operator!=(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE& other) const;
  CD3DX12_CPU_DESCRIPTOR_HANDLE & operator=(const D3D12_CPU_DESCRIPTOR_HANDLE &other);
  void                            inline InitOffsetted(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            inline InitOffsetted(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_CPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_CPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_ \_ Handle de descripteur de processeur CD3DX12 \_ ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ \_ handle de descripteur de processeur CD3DX12 \_ .

</dd> <dt>

**\_ \_ handle de descripteur de processeur CD3DX12 explicite \_ ( \_ handle de descripteur d’uc const D3D12 \_ \_ &o)**
</dt> <dd>

Crée une nouvelle instance d’un \_ handle de \_ descripteur de processeur CD3DX12 \_ , initialisée avec le contenu d’une autre structure de [**\_ \_ \_ handle de descripteur de processeur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) .

</dd> <dt>

**\_ \_ Handle de descripteur de processeur CD3DX12 \_ (CD3DX12 \_ par défaut)**
</dt> <dd>

Crée une nouvelle instance d’un \_ handle de \_ descripteur de processeur CD3DX12 \_ , initialisée avec les paramètres par défaut (pointeur défini sur zéro).

</dd> <dt>

**\_ \_ Handle de descripteur de processeur CD3DX12 \_ ( \_ handle de descripteur de processeur const D3D12 \_ \_ &autre, int offsetScaledByIncrementSize)**
</dt> <dd>

Crée une nouvelle instance d’un \_ handle de \_ descripteur d’UC CD3DX12 \_ , en initialisant les paramètres suivants :

\_Handle de \_ descripteur de processeur D3D12 \_ &autre

INT offsetScaledByIncrementSize : nombre d’incréments de décalage.

</dd> <dt>

**\_ \_ Handle de descripteur de processeur CD3DX12 \_ ( \_ handle de descripteur de processeur const D3D12 \_ \_ &autre, int offsetInDescriptors, uint descriptorIncrementSize)**
</dt> <dd>

Crée une nouvelle instance d’un \_ handle de \_ descripteur d’UC CD3DX12 \_ , en initialisant les paramètres suivants :

\_Handle de \_ descripteur de processeur D3D12 \_ &autre

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

**opérateur = = ( \_ dans le \_ handle de \_ descripteur d’UC const D3D12 \_ \_& autre) const**
</dt> <dd>

Teste l’égalité entre le handle de descripteur de processeur CD3DX12 actuel et le handle de descripteur de processeur D3D12 ou le handle de descripteur \_ \_ \_ de processeur \_ CD3DX12 spécifié \_ \_ \_ \_ \_ .

</dd> <dt>

**opérateur ! = ( \_ dans le \_ handle de \_ descripteur d’UC const D3D12 \_ \_& autre) const**
</dt> <dd>

Vérifie l’inégalité entre le handle du descripteur d’UC CD3DX12 actuel et le handle de descripteur d’UC D3D12 ou le handle de descripteur \_ \_ \_ \_ \_ \_ de processeur CD3DX12 spécifié \_ \_ \_ .

</dd> <dt>

**opérateur = (const D3D12 \_ \_ handle de descripteur d’UC \_ &autre)**
</dt> <dd>

Définit le \_ \_ handle de descripteur de processeur CD3DX12 actuel \_ sur les mêmes valeurs que le handle de \_ \_ descripteur de processeur D3D12 \_ ou le \_ \_ \_ handle de descripteur de processeur CD3DX12 spécifié.

</dd> <dt>

**Inline InitOffsetted ( \_ dans le \_ handle de \_ descripteur d’UC const D3D12 \_ \_ &base, int offsetScaledByIncrementSize)**
</dt> <dd>

Initialise une structure [**de \_ \_ \_ handle de descripteur de processeur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) avec le nombre spécifié d’éléments. Utilise les paramètres suivants :

\_Dans \_ \_ le handle de descripteur d’UC const D3D12 \_ \_ &base : adresse de base à partir de laquelle le décalage est pris.

INT offsetScaledByIncrementSize : nombre d’incréments de décalage.

</dd> <dt>

**Inline InitOffsetted ( \_ dans le \_ handle de \_ descripteur d’UC const D3D12 \_ \_ &base, int offsetInDescriptors, uint descriptorIncrementSize)**
</dt> <dd>

Initialise une structure [**de \_ \_ \_ handle de descripteur de processeur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) avec un offset, à l’aide du nombre spécifié de descripteurs de la taille donnée. Utilise les paramètres suivants :

\_Dans \_ \_ le handle de descripteur d’UC const D3D12 \_ \_ &base : adresse de base à partir de laquelle le décalage est pris.

INT offsetInDescriptors : nombre de descripteurs par lequel décaler.

UINT descriptorIncrementSize : quantité par laquelle incrémenter pour chaque descripteur, y compris le remplissage.

</dd> <dt>

**handle \_ \_ \_ \_ de de&scripteur InitOffsetted (out D3D12 descripteur de descripteur inline \_ ) statique, dans le handle \_ de \_ \_ descripteur d’UC const D3D12 \_ \_ &base, int offsetScaledByIncrementSize)**
</dt> <dd>

Initialise une structure [**de \_ \_ \_ handle de descripteur de processeur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) avec un offset, à l’aide du nombre spécifié de descripteurs de la taille donnée. Utilise les paramètres suivants :

\_\_DeD3D12 \_ \_ de&scripteur de descripteur de processeur out handle \_ : génère le \_ handle de descripteur d’UC D3D12 résultant \_ \_ .

\_Dans \_ \_ le handle de descripteur d’UC const D3D12 \_ \_ &base : adresse de base à partir de laquelle le décalage est pris.

INT offsetScaledByIncrementSize : nombre d’incréments de décalage.

</dd> <dt>

**static Inline InitOffsetted ( \_ handle \_ \_ \_ de descripteur de processeur out D3D12 \_ &handle, \_ dans le \_ handle de \_ descripteur d’UC const D3D12 \_ \_ &base, int offsetInDescriptors, uint descriptorIncrementSize)**
</dt> <dd>

Initialise une structure [**de \_ \_ \_ handle de descripteur de processeur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) avec un offset, à l’aide du nombre spécifié de descripteurs de la taille donnée. Utilise les paramètres suivants :

\_\_DeD3D12 \_ \_ de&scripteur de descripteur de processeur out handle \_ : génère le \_ handle de descripteur d’UC D3D12 résultant \_ \_ .

\_Dans \_ \_ le handle de descripteur d’UC const D3D12 \_ \_ &base : adresse de base à partir de laquelle le décalage est pris.

INT offsetInDescriptors : nombre de descripteurs par lequel décaler.

UINT descriptorIncrementSize : quantité par laquelle incrémenter pour chaque descripteur, y compris le remplissage.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





