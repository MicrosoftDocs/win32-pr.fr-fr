---
description: Décrit une mémoire tampon d’index.
ms.assetid: 5d45213e-b3c0-4eb7-a4f9-8d8730eb3899
title: Structure D3DINDEXBUFFER_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DINDEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a7a25e56ccb9877fad6b370f9ed81c6c7dcf0744a96734b1e17d6dc3abbc0535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804931"
---
# <a name="d3dindexbuffer_desc-structure"></a>D3DINDEXBUFFER \_ desc, structure

Décrit une mémoire tampon d’index.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DINDEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
} D3DINDEXBUFFER_DESC, *LPD3DINDEXBUFFER_DESC;
```



## <a name="members"></a>Membres

<dl> <dt>

**Format**
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de surface des données de la mémoire tampon d’index.

</dd> <dt>

**Type**
</dt> <dd>

Type : **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Membre du type énuméré [**D3DRESOURCETYPE**](./d3dresourcetype.md) , identifiant cette ressource comme une mémoire tampon d’index.

</dd> <dt>

**Utilisation**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Combinaison d’un ou plusieurs des indicateurs suivants, en spécifiant l’utilisation de cette ressource.



| Valeur                                                                                                                                                                                                   | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DUSAGE_DONOTCLIP"></span><span id="d3dusage_donotclip"></span><dl> <dt>**D3DUSAGE \_ DONOTCLIP**</dt> </dl>                            | Défini pour indiquer que le contenu de la mémoire tampon d’index ne nécessitera jamais de découpage.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_DYNAMIC"></span><span id="d3dusage_dynamic"></span><dl> <dt>**D3DUSAGE \_ dynamique**</dt> </dl>                                  | Défini pour indiquer que la mémoire tampon d’index requiert l’utilisation de la mémoire dynamique. Cela est utile pour les pilotes, car cela leur permet de décider où placer la mémoire tampon. En général, les mémoires tampons d’index statiques sont placées dans la mémoire vidéo et les mémoires tampons d’index dynamiques sont placées dans la mémoire AGP. Notez qu’il n’y a pas d’utilisation statique distincte ; Si vous ne spécifiez pas D3DUSAGE \_ dynamique, le tampon d’index est rendu statique. D3DUSAGE \_ Dynamic est strictement appliqué via les \_ indicateurs de verrouillage D3DLOCK ignore et D3DLOCK \_ NOOVERWRITE. Par conséquent, les D3DLOCK \_ ignorés et D3DLOCK \_ NOOVERWRITE sont valides uniquement sur les tampons d’index créés avec D3DUSAGE \_ dynamique ; il ne s’agit pas d’indicateurs valides sur les mémoires tampons de vertex statiques.<br/> Pour plus d’informations sur l’utilisation des mémoires tampons d’index dynamiques, consultez [utilisation de mémoires tampons de vertex et d’index dynamiques](performance-optimizations.md).<br/> Notez que D3DUSAGE \_ Dynamic ne peut pas être spécifié dans les tampons d’index managés. Pour plus d’informations, consultez [gestion des ressources (Direct3D 9)](managing-resources.md).<br/> |
| <span id="D3DUSAGE_RTPATCHES"></span><span id="d3dusage_rtpatches"></span><dl> <dt>**D3DUSAGE \_ RTPATCHES**</dt> </dl>                            | Défini pour indiquer à quel moment la mémoire tampon d’index doit être utilisée pour le dessin des primitives d’ordre élevé.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DUSAGE_NPATCHES"></span><span id="d3dusage_npatches"></span><dl> <dt>**D3DUSAGE \_ NPATCHES**</dt> </dl>                               | Défini pour indiquer à quel moment la mémoire tampon d’index doit être utilisée pour le dessin des N correctifs.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_POINTS"></span><span id="d3dusage_points"></span><dl> <dt>**POINTS de D3DUSAGE \_**</dt> </dl>                                     | Défini pour indiquer le moment où le tampon d’index doit être utilisé pour les points de dessin des sprites ou les listes de points indexés.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="D3DUSAGE_SOFTWAREPROCESSING"></span><span id="d3dusage_softwareprocessing"></span><dl> <dt>**D3DUSAGE \_ SOFTWAREPROCESSING**</dt> </dl> | Défini pour indiquer que la mémoire tampon doit être utilisée avec le traitement logiciel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DUSAGE_WRITEONLY"></span><span id="d3dusage_writeonly"></span><dl> <dt>**D3DUSAGE \_ WRITEONLY**</dt> </dl>                            | Informe le système que l’application écrit uniquement dans la mémoire tampon d’index. L’utilisation de cet indicateur permet au pilote de choisir le meilleur emplacement de mémoire pour des opérations d’écriture et un rendu efficaces. Les tentatives de lecture à partir d’un tampon d’index créé avec cette fonctionnalité peuvent entraîner une dégradation des performances.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

**Pool**
</dt> <dd>

Type : **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , spécifiant la classe de mémoire allouée pour cette mémoire tampon d’index.

</dd> <dt>

**Taille**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Taille de la mémoire tampon d’index, en octets.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-getdesc)
</dt> <dt>

[Mémoires tampons d’index (Direct3D 9)](index-buffers.md)
</dt> </dl>

 

 
