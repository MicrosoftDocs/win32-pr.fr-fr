---
title: Tex-PS
description: Charge le registre de destination avec les données de couleur (RVBA) échantillonnées à partir d’une texture. La texture doit être liée à une étape de texture particulière (n) à l’aide de SetTexture. L’échantillonnage de texture est contrôlé par SetSamplerState.
ms.assetid: vs|directx_sdk|~\tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0646a057fdc2fb96e5f72e7451b9b273191ced22f5092a14fab11a9042c5de25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788108"
---
# <a name="tex---ps"></a>Tex-PS

Charge le registre de destination avec les données de couleur (RVBA) échantillonnées à partir d’une texture. La texture doit être liée à une étape de texture particulière (n) à l’aide de [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). L’échantillonnage de texture est contrôlé par [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).

## <a name="syntax"></a>Syntaxe



| Tex DST |
|---------|



 

where

-   l’heure d’été est le registre de destination.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Tex                   | x    | x    | x    |      |      |      |       |      |       |



 

Le numéro de registre de destination spécifie le numéro de l’étape de texture.

L’échantillonnage de texture utilise des coordonnées de texture pour rechercher, ou échantillonner, une valeur de couleur aux coordonnées spécifiées (u, v, w, q) tout en tenant compte des attributs d’état de la phase de texture.

Les données de coordonnée de texture sont interpolées à partir des données de coordonnée de texture de vertex et sont associées à une étape de texture spécifique. L’Association par défaut est un mappage un-à-un entre le numéro de l’étape de texture et l’ordre de déclaration des coordonnées de texture. Cela signifie que le premier jeu de coordonnées de texture défini dans le format de vertex est associé par défaut à l’étape de texture 0.

Les coordonnées de texture peuvent être associées à n’importe quelle étape à l’aide de deux techniques. Lors de l’utilisation d’un nuanceur de sommets de fonction fixe ou du pipeline de fonction fixe, l’indicateur d’état de l’étape de texture TSS \_ TEXCOORDINDEX peut être utilisé dans [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) pour associer des coordonnées à une étape. Sinon, les coordonnées de texture sont générées par le nuanceur de sommets oTn s’inscrit lors de l’utilisation d’un nuanceur de sommet programmable.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 