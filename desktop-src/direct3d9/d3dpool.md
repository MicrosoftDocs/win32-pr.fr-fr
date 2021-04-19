---
description: Définit la classe de mémoire qui contient les mémoires tampons d’une ressource.
ms.assetid: 29720b5f-16d7-4bd9-a7bd-e4dbfb00070b
title: Énumération D3DPOOL (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPOOL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dc1d69d094b2f810855f9ce2116c472ba8ab605e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535821"
---
# <a name="d3dpool-enumeration"></a>Énumération D3DPOOL

Définit la classe de mémoire qui contient les mémoires tampons d’une ressource.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DPOOL { 
  D3DPOOL_DEFAULT      = 0,
  D3DPOOL_MANAGED      = 1,
  D3DPOOL_SYSTEMMEM    = 2,
  D3DPOOL_SCRATCH      = 3,
  D3DPOOL_FORCE_DWORD  = 0x7fffffff
} D3DPOOL, *LPD3DPOOL;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**D3DPOOL \_ par défaut**
</dt> <dd>

Les ressources sont placées dans le pool de mémoire le plus approprié pour l’ensemble des utilisations demandées pour la ressource donnée. Il s’agit généralement de la mémoire vidéo, y compris la mémoire vidéo locale et la mémoire AGP. Le \_ pool par défaut D3DPOOL est distinct de D3DPOOL \_ géré et D3DPOOL \_ SYSTEMMEM, et il spécifie que la ressource est placée dans la mémoire par défaut pour l’accès à l’appareil. Notez que D3DPOOL \_ default n’indique jamais que D3DPOOL \_ géré ou D3DPOOL \_ SYSTEMMEM doit être choisi comme type de pool de mémoire pour cette ressource. Les textures placées dans le \_ pool par défaut D3DPOOL ne peuvent pas être verrouillées, sauf s’il s’agit de textures dynamiques ou de formats privés, FourCC et de pilote. Pour accéder aux textures qui ne sont pas verrouillées, vous devez utiliser des fonctions telles que [**IDirect3DDevice9 :: UpdateSurface**](/windows/desktop/api), [**IDirect3DDevice9 :: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture), [**IDirect3DDevice9 :: GetFrontBufferData**](/windows/desktop/api)et [**IDirect3DDevice9 :: GetRenderTargetData**](/windows/desktop/api). D3DPOOL \_ Managed est probablement un meilleur choix que D3DPOOL \_ Default pour la plupart des applications. Notez que certaines textures créées dans un format de pixel propriétaire du pilote, inconnues du runtime Direct3D, peuvent être verrouillées. Notez également que, à la différence des textures, les mémoires tampons d’arrière-plan, les cibles de rendu, les mémoires tampons de vertex et les mémoires tampons d’index peuvent être verrouillées. Quand un appareil est perdu, les ressources créées à l’aide de D3DPOOL \_ par défaut doivent être libérées avant d’appeler [**IDirect3DDevice9 :: Reset**](/windows/desktop/api). Pour plus d’informations, consultez [appareils perdus (Direct3D 9)](lost-devices.md).

Lors de la création de ressources avec D3DPOOL \_ par défaut, si la mémoire de carte vidéo est déjà validée, les ressources managées sont supprimées pour libérer suffisamment de mémoire pour satisfaire la demande.

</dd> <dt>

<span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**Géré par D3DPOOL \_**
</dt> <dd>

Les ressources sont automatiquement copiées dans la mémoire accessible par l’appareil en fonction des besoins. Les ressources managées sont sauvegardées par la mémoire système et n’ont pas besoin d’être recréées lorsqu’un appareil est perdu. Pour plus d’informations, consultez [gestion des ressources (Direct3D 9)](managing-resources.md) . Les ressources managées peuvent être verrouillées. Seule la copie de la mémoire système est directement modifiée. En fonction des besoins, Direct3D copie vos modifications dans la mémoire accessible par le pilote.



|                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Différences entre Direct3D 9 et Direct3D 9Ex :<br/> D3DPOOL \_ Managed est valide avec [**IDirect3DDevice9**](/windows/desktop/api); Toutefois, il n’est pas valide avec [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex).<br/> |



 

</dd> <dt>

<span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**D3DPOOL \_ SYSTEMMEM**
</dt> <dd>

Les ressources sont placées dans la mémoire qui n’est généralement pas accessible par le périphérique Direct3D. Cette allocation de mémoire consomme la mémoire RAM du système, mais ne réduit pas la mémoire RAM paginable. Ces ressources n’ont pas besoin d’être recréées lorsqu’un appareil est perdu. Les ressources de ce pool peuvent être verrouillées et peuvent être utilisées comme source pour une opération [**IDirect3DDevice9 :: UpdateSurface**](/windows/desktop/api) ou [**IDirect3DDevice9 :: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) sur une ressource mémoire créée avec D3DPOOL \_ par défaut.

</dd> <dt>

<span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**\_ÉRAFLURE D3DPOOL**
</dt> <dd>

Les ressources sont placées dans la mémoire vive du système et n’ont pas besoin d’être recréées lorsqu’un appareil est perdu. Ces ressources ne sont pas liées par la taille de l’appareil ou les restrictions de format. Pour cette raison, ces ressources ne sont pas accessibles par l’appareil Direct3D ni définies en tant que textures ou cibles de rendu. Toutefois, ces ressources peuvent toujours être créées, verrouillées et copiées.

</dd> <dt>

<span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

Tous les types de pools sont valides avec toutes les ressources, notamment : les mémoires tampons de vertex, les mémoires tampons d’index, les textures et les surfaces.

Les tableaux suivants indiquent des restrictions sur les types de pools pour les cibles de rendu, les stencils de profondeur et les utilisations dynamiques et de mipmap. Un x indique une combinaison compatible ; l’absence d’un x indique une incompatibilité.



| pool               | D3DUSAGE \_ RENDERTARGET | D3DUSAGE \_ DEPTHSTENCIL |
|--------------------|------------------------|------------------------|
| D3DPOOL \_ par défaut   | x                      | x                      |
| Géré par D3DPOOL \_   |                        |                        |
| \_ÉRAFLURE D3DPOOL   |                        |                        |
| D3DPOOL \_ SYSTEMMEM |                        |                        |



 



| pool               | D3DUSAGE \_ dynamique | D3DUSAGE \_ AUTOGENMIPMAP |
|--------------------|-------------------|-------------------------|
| D3DPOOL \_ par défaut   | x                 | x                       |
| Géré par D3DPOOL \_   |                   | x                       |
| \_ÉRAFLURE D3DPOOL   |                   |                         |
| D3DPOOL \_ SYSTEMMEM | x                 |                         |



 

Pour plus d’informations sur les types d’utilisation, consultez [**D3DUSAGE**](d3dusage.md).

Les pools ne peuvent pas être mélangés pour différents objets contenus dans une ressource (niveaux MIP dans un mipmap) et, lorsqu’un pool est choisi, il ne peut pas être modifié.

Les applications doivent utiliser D3DPOOL \_ géré pour la plupart des ressources statiques, car cela évite à l’application d’avoir à gérer les périphériques perdus. (Les ressources managées sont restaurées par le Runtime.) Cela est particulièrement bénéfique pour les systèmes d’architecture de mémoire unifiée (UMA). Les autres ressources dynamiques ne constituent pas une bonne correspondance pour la gestion de D3DPOOL \_ . En fait, les mémoires tampons d’index et les mémoires tampons de vertex ne peuvent pas être créées à l’aide \_ de D3DPOOL géré avec D3DUSAGE \_ Dynamic.

Pour les textures dynamiques, il est parfois préférable d’utiliser une paire de textures de mémoire vidéo et de mémoire système, d’allouer la mémoire vidéo à l’aide de D3DPOOL \_ par défaut et de la mémoire système à l’aide de D3DPOOL \_ SYSTEMMEM. Vous pouvez verrouiller et modifier les bits de la texture de la mémoire système à l’aide d’une méthode de verrouillage. Vous pouvez ensuite mettre à jour la texture de la mémoire vidéo à l’aide de [**IDirect3DDevice9 :: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DUSAGE**](d3dusage.md)
</dt> <dt>

[**IDirect3DDevice9::CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
</dt> <dt>

[**IDirect3DDevice9::CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
</dt> <dt>

[**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
</dt> <dt>

[**IDirect3DDevice9::CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
</dt> <dt>

[**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
</dt> <dt>

[**D3DINDEXBUFFER \_ desc**](d3dindexbuffer-desc.md)
</dt> <dt>

[**D3DSURFACE \_ desc**](d3dsurface-desc.md)
</dt> <dt>

[**D3DVERTEXBUFFER \_ desc**](d3dvertexbuffer-desc.md)
</dt> <dt>

[**D3DVOLUME \_ desc**](d3dvolume-desc.md)
</dt> </dl>

 

 
