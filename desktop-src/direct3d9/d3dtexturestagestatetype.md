---
description: Les États de l’étape de texture définissent des opérations de texture à plusieurs fusions.
ms.assetid: 87a5a1bb-e748-4c72-8320-ea82250dcc0e
title: Énumération D3DTEXTURESTAGESTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURESTAGESTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0530f428c9ebf89607fa89509c65ddd336fee293
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211727"
---
# <a name="d3dtexturestagestatetype-enumeration"></a>Énumération D3DTEXTURESTAGESTATETYPE

Les États de l’étape de texture définissent des opérations de texture à plusieurs fusions. Certains États de l’échantillonneur configurent le traitement des vertex et un traitement des pixels configuré. Les États de l’étape de texture peuvent être enregistrés et restaurés à l’aide de stateblocks (consultez États d' [enregistrement et de restauration des blocs d’État (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DTEXTURESTAGESTATETYPE { 
  D3DTSS_COLOROP                = 1,
  D3DTSS_COLORARG1              = 2,
  D3DTSS_COLORARG2              = 3,
  D3DTSS_ALPHAOP                = 4,
  D3DTSS_ALPHAARG1              = 5,
  D3DTSS_ALPHAARG2              = 6,
  D3DTSS_BUMPENVMAT00           = 7,
  D3DTSS_BUMPENVMAT01           = 8,
  D3DTSS_BUMPENVMAT10           = 9,
  D3DTSS_BUMPENVMAT11           = 10,
  D3DTSS_TEXCOORDINDEX          = 11,
  D3DTSS_BUMPENVLSCALE          = 22,
  D3DTSS_BUMPENVLOFFSET         = 23,
  D3DTSS_TEXTURETRANSFORMFLAGS  = 24,
  D3DTSS_COLORARG0              = 26,
  D3DTSS_ALPHAARG0              = 27,
  D3DTSS_RESULTARG              = 28,
  D3DTSS_CONSTANT               = 32,
  D3DTSS_FORCE_DWORD            = 0x7fffffff
} D3DTEXTURESTAGESTATETYPE, *LPD3DTEXTURESTAGESTATETYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS \_ COLOROP**
</dt> <dd>

L’état de la texture-étape est une opération de fusion des couleurs de texture identifiée par un membre du type énuméré [**D3DTEXTUREOP**](./d3dtextureop.md) . La valeur par défaut de la première étape de texture (étape 0) est D3DTOP \_ module. pour toutes les autres étapes, la valeur par défaut est D3DTOP \_ Désactiver.

</dd> <dt>

<span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS \_ COLORARG1**
</dt> <dd>

L’état de la texture-étape est le premier argument de couleur pour l’étape, identifié par l’un des [D3DTA](d3dta.md). L’argument par défaut est D3DTA \_ texture.

Spécifiez D3DTA \_ temp pour sélectionner une couleur de registre temporaire pour la lecture ou l’écriture. D3DTA \_ temp est pris en charge si la fonctionnalité de l' \_ appareil D3DPMISCCAPS TSSARGTEMP est présente. La valeur par défaut du Registre est (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS \_ COLORARG2**
</dt> <dd>

L’état de la texture-étape est le deuxième argument de couleur pour l’étape, identifié par [D3DTA](d3dta.md). L’argument par défaut est D3DTA \_ Current. Spécifiez D3DTA \_ temp pour sélectionner une couleur de registre temporaire pour la lecture ou l’écriture. D3DTA \_ temp est pris en charge si la fonctionnalité de l' \_ appareil D3DPMISCCAPS TSSARGTEMP est présente. La valeur par défaut du Registre est (0,0, 0,0, 0,0, 0,0)

</dd> <dt>

<span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS \_ ALPHAOP**
</dt> <dd>

L’état de la texture-étape est une opération de fusion alpha de texture identifiée par un membre du type énuméré [**D3DTEXTUREOP**](./d3dtextureop.md) . La valeur par défaut de la première étape de texture (étape 0) est D3DTOP \_ SELECTARG1, et pour toutes les autres étapes, la valeur par défaut est D3DTOP \_ Disable.

</dd> <dt>

<span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS \_ ALPHAARG1**
</dt> <dd>

L’état de la texture-étape est le premier argument alpha pour l’étape, identifié par par [D3DTA](d3dta.md). L’argument par défaut est D3DTA \_ texture. Si aucune texture n’est définie pour cette étape, l’argument par défaut est D3DTA \_ diffus. Spécifiez D3DTA \_ temp pour sélectionner une couleur de registre temporaire pour la lecture ou l’écriture. D3DTA \_ temp est pris en charge si la fonctionnalité de l' \_ appareil D3DPMISCCAPS TSSARGTEMP est présente. La valeur par défaut du Registre est (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS \_ ALPHAARG2**
</dt> <dd>

L’état de la texture-étape est le deuxième argument alpha pour l’étape, identifié par par [D3DTA](d3dta.md). L’argument par défaut est D3DTA \_ Current. Spécifiez D3DTA \_ temp pour sélectionner une couleur de registre temporaire pour la lecture ou l’écriture. D3DTA \_ temp est pris en charge si la fonctionnalité de l' \_ appareil D3DPMISCCAPS TSSARGTEMP est présente. La valeur par défaut du Registre est (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS \_ BUMPENVMAT00**
</dt> <dd>

L’état de la texture-étape est une valeur à virgule flottante pour le \[ \] \[ \] coefficient 0 0 dans une matrice de mappage de relief. La valeur par défaut est 0.0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS \_ BUMPENVMAT01**
</dt> <dd>

L’état de la texture-étape est une valeur à virgule flottante pour le \[ \] \[ \] coefficient 0 1 dans une matrice de mappage de relief. La valeur par défaut est 0.0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS \_ BUMPENVMAT10**
</dt> <dd>

L’état de la texture-étape est une valeur à virgule flottante pour le \[ \] \[ \] coefficient 1 0 dans une matrice de mappage de relief. La valeur par défaut est 0.0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS \_ BUMPENVMAT11**
</dt> <dd>

L’état de la texture-étape est une valeur à virgule flottante pour le \[ \] \[ \] coefficient 1 1 dans une matrice de mappage de relief. La valeur par défaut est 0.0.

</dd> <dt>

<span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS \_ TEXCOORDINDEX**
</dt> <dd>

Index du jeu de coordonnées de texture à utiliser avec cette étape de texture. Vous pouvez spécifier jusqu’à huit jeux de coordonnées de texture par vertex. Si un vertex n’inclut pas un jeu de coordonnées de texture à l’index spécifié, le système utilise par défaut les coordonnées v et v (0,0).

Lors du rendu à l’aide de nuanceurs vertex, l’index des coordonnées de texture de chaque étape doit être défini sur sa valeur par défaut. L’index par défaut de chaque étape est égal à l’index de la phase. Définissez cet État sur l’index de base zéro de l’ensemble de coordonnées pour chaque vertex utilisé par cette étape de texture.

En outre, les applications peuvent inclure, comme logique ou avec l’index en cours de définition, l’une des constantes pour demander que Direct3D génère automatiquement les coordonnées de texture d’entrée pour une transformation de texture. Pour obtenir la liste de toutes les constantes, consultez [D3DTSS \_ TCI](d3dtss-tci.md).

À l’exception de D3DTSS \_ TCI \_ PASSTHRU, qui correspond à zéro, si l’une des valeurs suivantes est incluse avec l’index en cours de définition, le système utilise l’index strictement pour déterminer le mode d’habillage de texture. Ces indicateurs sont particulièrement utiles lors de l’exécution d’un mappage d’environnement.

</dd> <dt>

<span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS \_ BUMPENVLSCALE**
</dt> <dd>

Valeur de mise à l’échelle à virgule flottante pour la luminance de la carte de relief. La valeur par défaut est 0.0.

</dd> <dt>

<span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS \_ BUMPENVLOFFSET**
</dt> <dd>

Valeur de décalage à virgule flottante pour la luminance de la carte de relief. La valeur par défaut est 0.0.

</dd> <dt>

<span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**D3DTSS \_ TEXTURETRANSFORMFLAGS**
</dt> <dd>

Membre du type énuméré [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) qui contrôle la transformation des coordonnées de texture pour cette étape de texture. La valeur par défaut est D3DTTFF \_ Disable.

</dd> <dt>

<span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS \_ COLORARG0**
</dt> <dd>

Paramètres du troisième opérande de couleur pour les opérations tripliées (multiplication, ajout et interpolation linéaire), identifiées par [D3DTA](d3dta.md). Ce paramètre est pris en charge si les fonctionnalités de l' \_ appareil D3DTEXOPCAPS MULTIPLYADD ou D3DTEXOPCAPS \_ LERP sont présentes. L’argument par défaut est D3DTA \_ Current. Spécifiez D3DTA \_ temp pour sélectionner une couleur de registre temporaire pour la lecture ou l’écriture. D3DTA \_ temp est pris en charge si la fonctionnalité de l' \_ appareil D3DPMISCCAPS TSSARGTEMP est présente. La valeur par défaut du Registre est (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS \_ ALPHAARG0**
</dt> <dd>

Paramètres de l’opérande du sélecteur de canal alpha pour les opérations tripliées (multiplication, ajout et interpolation linéaire), identifiées par [D3DTA](d3dta.md). Ce paramètre est pris en charge si les fonctionnalités de l' \_ appareil D3DTEXOPCAPS MULTIPLYADD ou D3DTEXOPCAPS \_ LERP sont présentes. L’argument par défaut est D3DTA \_ Current. Spécifiez D3DTA \_ temp pour sélectionner une couleur de registre temporaire pour la lecture ou l’écriture. D3DTA \_ temp est pris en charge si la fonctionnalité de l' \_ appareil D3DPMISCCAPS TSSARGTEMP est présente. L’argument par défaut est (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS \_ RESULTARG**
</dt> <dd>

Paramètre permettant de sélectionner le registre de destination pour le résultat de cette étape, identifié par [D3DTA](d3dta.md). Cette valeur peut être définie sur D3DTA \_ Current (valeur par défaut) ou sur D3DTA \_ temp, qui est un registre temporaire unique qui peut être lu dans les étapes suivantes sous forme d’argument d’entrée. La couleur finale transmise au mélangeur de brouillard et à la mémoire tampon de trame est extraite de D3DTA \_ actuel, de sorte que l’état de la dernière étape de texture active doit être défini pour écrire dans le en cours. Ce paramètre est pris en charge si la fonctionnalité de l' \_ appareil D3DPMISCCAPS TSSARGTEMP est présente.

</dd> <dt>

<span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**D3DTSS \_ constante)**
</dt> <dd>

Couleur constante par étape. Pour savoir si un appareil prend en charge une couleur constante par étape, consultez la \_ constante D3DPMISCCAPS PERSTAGECONSTANT dans [D3DPMISCCAPS](d3dpmisccaps.md). La \_ constante D3DTSS est utilisée par la \_ constante D3DTA. Consultez [D3DTA](d3dta.md).

</dd> <dt>

<span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

Les membres de ce type énuméré sont utilisés avec les méthodes [**IDirect3DDevice9 :: GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) et [**IDirect3DDevice9 :: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) pour récupérer et définir des valeurs d’état de texture.

La plage de valeurs valide pour les \_ coefficients de matrice de mappage D3DTSS BUMPENVMAT00, D3DTSS \_ BUMPENVMAT01, D3DTSS \_ BUMPENVMAT10 et D3DTSS BUMPENVMAT11 \_ est supérieure ou égale à-8,0 et inférieure à 8,0. Cette plage, exprimée en notation mathématique, est (-8.0, 8.0).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)
</dt> <dt>

[**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
</dt> </dl>

 

 
