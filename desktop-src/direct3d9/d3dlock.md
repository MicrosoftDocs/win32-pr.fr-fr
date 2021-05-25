---
description: Combinaison de zéro ou plusieurs options de verrouillage qui décrivent le type de verrou à effectuer.
ms.assetid: 46a611bd-a1ec-4967-b68d-72661d1b5cad
title: D3DLOCK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e4fcf8db9e60a30aee060dcc483b8d01e59b1c
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343194"
---
# <a name="d3dlock"></a>D3DLOCK

Combinaison de zéro ou plusieurs options de verrouillage qui décrivent le type de verrou à effectuer.



| \#définition                   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DLOCK \_ Ignorer           | L’application ignore toute la mémoire dans la région verrouillée. Pour les mémoires tampons de vertex et d’index, la mémoire tampon entière est ignorée. Cette option est valide uniquement lorsque la ressource est créée avec une utilisation dynamique (voir [D3DUSAGE](d3dusage.md)).                                                                                                                                                                                                                                                                                                                                                           |
| D3DLOCK \_ DONOTWAIT         | Permet à une application de récupérer les cycles de processeur si le pilote ne peut pas verrouiller immédiatement la surface. Si cet indicateur est défini et que le pilote ne peut pas verrouiller la surface immédiatement, l’appel de verrou retourne D3DERR \_ WASSTILLDRAWING. Cet indicateur ne peut être utilisé que lors du verrouillage d’une surface créée à l’aide de [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateRenderTarget**](/windows/desktop/api)ou [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface). Cet indicateur peut également être utilisé avec une mémoire tampon d’arrière-plan.            |
| D3DLOCK \_ aucune \_ \_ mise à jour incorrecte | Par défaut, un verrou sur une ressource ajoute une région modifiée à cette ressource. Cette option empêche toute modification de l’état de modification de la ressource. Les applications doivent utiliser cette option quand elles ont des informations supplémentaires sur l’ensemble des régions modifiées pendant l’opération de verrouillage.                                                                                                                                                                                                                                                                                                                    |
| D3DLOCK \_ NOOVERWRITE       | Indique que la mémoire qui a été référencée dans un appel de dessin depuis le dernier verrou sans cet indicateur ne sera pas modifiée pendant le verrouillage. Cela peut permettre des optimisations lorsque l’application ajoute des données à une ressource. Si vous spécifiez cet indicateur, le pilote est immédiatement retourné si la ressource est en cours d’utilisation. dans le cas contraire, le pilote doit terminer l’utilisation de la ressource avant de revenir au verrouillage.                                                                                                                                                                                            |
| D3DLOCK \_ NOSYSLOCK         | Le comportement par défaut d’un verrou de mémoire vidéo est de réserver une section critique au niveau du système, ce qui garantit qu’aucune modification du mode d’affichage ne se produit pendant la durée du verrouillage. Cette option entraîne la non-conservation de la section critique au niveau du système pendant la durée du verrouillage.<br/> L’opération de verrouillage prend beaucoup de temps, mais peut permettre au système d’exécuter d’autres tâches, telles que le déplacement du curseur de la souris. Cette option est utile pour les verrous de longue durée, tels que le verrouillage de la mémoire tampon d’arrière-plan pour le rendu logiciel qui, autrement, aurait un impact négatif sur la réactivité du système.<br/> |
| D3DLOCK en \_ lecture seule          | L’application n’écrira pas dans la mémoire tampon. Cela permet aux ressources stockées dans des formats non natifs d’enregistrer l’étape de recompression lors du déverrouillage.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="constant-information"></a>Informations constantes



|  Condition requise                        | Valeur            |
|--------------------------|-------------|
| En-tête                   | d3d9types. h |
| Système d’exploitation minimal | Windows 98  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**Verrouillage**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**Verrouillage**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[**Scellé**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**Scellé**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**LockIndexBuffer**](id3dxbasemesh--lockindexbuffer.md)
</dt> <dt>

[**LockVertexBuffer**](id3dxbasemesh--lockvertexbuffer.md)
</dt> <dt>

**LockVertexBuffer**
</dt> <dt>

[**LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

[**LockAttributeBuffer**](id3dxpatchmesh--lockattributebuffer.md)
</dt> <dt>

[**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md)
</dt> <dt>

[**LockVertexBuffer**](id3dxpatchmesh--lockvertexbuffer.md)
</dt> </dl>

 

 
