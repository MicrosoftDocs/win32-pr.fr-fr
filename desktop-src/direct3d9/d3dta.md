---
description: 'Les constantes d’argument de texture sont utilisées comme valeurs pour les membres suivants du type énuméré D3DTEXTURESTAGESTATETYPE :'
ms.assetid: 36b2b715-5ced-4246-840e-8ea343521ef4
title: D3DTA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db520bee7e4352b3242824819cc579acd82b1d013d290b2155d54170bc478c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527313"
---
# <a name="d3dta"></a>D3DTA

Les constantes d’argument de texture sont utilisées comme valeurs pour les membres suivants du type énuméré [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) :

-   D3DTSS \_ ALPHAARG0
-   D3DTSS \_ ALPHAARG1
-   D3DTSS \_ ALPHAARG2
-   D3DTSS \_ COLORARG0
-   D3DTSS \_ COLORARG1
-   D3DTSS \_ COLORARG2
-   D3DTSS \_ RESULTARG

Définissez et récupérez des arguments de texture en appelant les méthodes [**SetTextureStageState**](/windows/desktop/api) et [**GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) .

Indicateurs d’argument

Vous pouvez combiner un indicateur d’argument avec un modificateur, mais deux indicateurs d’arguments ne peuvent pas être combinés.



| \#définition          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DTA \_ constante)   | Sélectionnez une constante dans une étape de texture. La valeur par défaut est 0xFFFFFFFF.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| D3DTA \_ actuel    | L’argument texture est le résultat de l’étape de fusion précédente. Dans la première étape de texture (étape 0), cet argument est équivalent à D3DTA \_ diffus. Si la phase de fusion précédente utilise une texture de la carte de bosselage ( \_ opération D3DTOP BUMPENVMAP), le système choisit la texture à partir de l’étape avant la texture de la carte de bosselage. Si s représente l’étape de texture actuelle et que s-1 contient une texture de carte de bosselage, cet argument devient la sortie de résultat par l’étape de texture s-2. Les autorisations sont en lecture/écriture. |
| \_Diffusion D3DTA    | L’argument texture est la couleur diffuse interpolée à partir des composants de vertex pendant l’ombrage Gouraud. Si le vertex ne contient pas de couleur diffuse, la couleur par défaut est 0xFFFFFFFF. Les autorisations sont en lecture seule.                                                                                                                                                                                                                                                                                          |
| D3DTA \_ SELECTMASK | Valeur de masque pour tous les arguments ; non utilisé lors de la définition des arguments de texture.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| D3DTA \_ spéculaire   | L’argument texture est la couleur spéculaire interpolée à partir des composants de vertex pendant l’ombrage Gouraud. Si le vertex ne contient pas de couleur spéculaire, la couleur par défaut est 0xFFFFFFFF. Les autorisations sont en lecture seule.                                                                                                                                                                                                                                                                                        |
| D3DTA \_ temp       | L’argument texture est une couleur de registre temporaire pour la lecture ou l’écriture. D3DTA \_ temp est pris en charge si la fonctionnalité de l’appareil [D3DPMISCCAPS \_ TSSARGTEMP](d3dpmisccaps.md) est présente. La valeur par défaut du Registre est (0,0, 0,0, 0,0, 0,0). Les autorisations sont en lecture/écriture.                                                                                                                                                                                                                                   |
| \_Texture D3DTA    | L’argument texture est la couleur de texture pour cette étape de texture. Les autorisations sont en lecture seule.                                                                                                                                                                                                                                                                                                                                                                                                               |
| D3DTA \_ TFACTOR    | L’argument texture est le facteur de texture défini dans un appel précédent à [**SetRenderState**](/windows/desktop/api) avec la valeur [**D3DRS \_ TEXTUREFACTOR**](./d3drenderstatetype.md) Render-State. Les autorisations sont en lecture seule.                                                                                                                                                                                                                                                       |



 

Indicateurs de modificateur

Un indicateur d’argument peut être combiné avec l’un des indicateurs de modificateur suivants.



| \#définition              | Description                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------|
| D3DTA \_ ALPHAREPLICATE | Répliquez les informations alpha sur tous les canaux de couleur avant la fin de l’opération. Il s’agit d’un modificateur de lecture. |
| \_Complément D3DTA     | Prenez le complément de l’argument x, (1,0-x). Il s’agit d’un modificateur de lecture.                                     |



 

## <a name="constant-information"></a>Informations constantes



|   Condition requise                       |  Valeur           |
|--------------------------|-------------|
| En-tête                   | d3d9types. h |
| Système d’exploitation minimal | Windows 98  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
