---
description: Statistiques des ressources collectées par le \_ RESOURCEMANAGER D3DDEVINFO lors de l’utilisation du mécanisme de requête asynchrone.
ms.assetid: f4d9c6db-4002-439c-9a88-485763badc82
title: D3DRESOURCESTATS, structure (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRESOURCESTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f6f549011b9750f69187c0e0cbf34ec94764c9ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542145"
---
# <a name="d3dresourcestats-structure"></a>D3DRESOURCESTATS, structure

Statistiques des ressources collectées par le [**\_ ResourceManager D3DDEVINFO**](d3ddevinfo-resourcemanager.md) lors de l’utilisation du mécanisme de requête asynchrone.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DRESOURCESTATS {
  BOOL  bThrashing;
  DWORD ApproxBytesDownloaded;
  DWORD NumEvicts;
  DWORD NumVidCreates;
  DWORD LastPri;
  DWORD NumUsed;
  DWORD NumUsedInVidMem;
  DWORD WorkingSet;
  DWORD WorkingSetBytes;
  DWORD TotalManaged;
  DWORD TotalBytes;
} D3DRESOURCESTATS, *LPD3DRESOURCESTATS;
```



## <a name="members"></a>Membres

<dl> <dt>

**bThrashing**
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Indique si une surcharge se produit.

</dd> <dt>

**ApproxBytesDownloaded**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre approximatif d’octets téléchargés par le gestionnaire de ressources.

</dd> <dt>

**NumEvicts**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre d’objets évincés.

</dd> <dt>

**NumVidCreates**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre d’objets créés dans la mémoire vidéo.

</dd> <dt>

**LastPri**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Priorité du dernier objet expulsé.

</dd> <dt>

**NumUsed**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre d’objets définis sur l’appareil.

</dd> <dt>

**NumUsedInVidMem**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre d’objets définis sur l’appareil, qui se trouvent déjà dans la mémoire vidéo.

</dd> <dt>

**WorkingSet**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre d’objets dans la mémoire vidéo.

</dd> <dt>

**WorkingSetBytes**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre d’octets dans la mémoire vidéo.

</dd> <dt>

**TotalManaged**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre total d’objets gérés.

</dd> <dt>

**TotalBytes**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nombre total d’octets d’objets managés.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[Notification asynchrone (Direct3D 9)](asynchronous-notification.md)
</dt> </dl>

 

 
