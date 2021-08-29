---
description: Définit les opérations de fusion de texture par étape.
ms.assetid: 7bfdcb15-c3c3-4e7e-b924-6ecfa350e2f3
title: Énumération D3DTEXTUREOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: c8d3108c59ddf810a815cbfa5f05a6fe66704325ffcee3f5dc2436b83c2c605d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987298"
---
# <a name="d3dtextureop-enumeration"></a>Énumération D3DTEXTUREOP

Définit les opérations de fusion de texture par étape.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DTEXTUREOP { 
  D3DTOP_DISABLE                    = 1,
  D3DTOP_SELECTARG1                 = 2,
  D3DTOP_SELECTARG2                 = 3,
  D3DTOP_MODULATE                   = 4,
  D3DTOP_MODULATE2X                 = 5,
  D3DTOP_MODULATE4X                 = 6,
  D3DTOP_ADD                        = 7,
  D3DTOP_ADDSIGNED                  = 8,
  D3DTOP_ADDSIGNED2X                = 9,
  D3DTOP_SUBTRACT                   = 10,
  D3DTOP_ADDSMOOTH                  = 11,
  D3DTOP_BLENDDIFFUSEALPHA          = 12,
  D3DTOP_BLENDTEXTUREALPHA          = 13,
  D3DTOP_BLENDFACTORALPHA           = 14,
  D3DTOP_BLENDTEXTUREALPHAPM        = 15,
  D3DTOP_BLENDCURRENTALPHA          = 16,
  D3DTOP_PREMODULATE                = 17,
  D3DTOP_MODULATEALPHA_ADDCOLOR     = 18,
  D3DTOP_MODULATECOLOR_ADDALPHA     = 19,
  D3DTOP_MODULATEINVALPHA_ADDCOLOR  = 20,
  D3DTOP_MODULATEINVCOLOR_ADDALPHA  = 21,
  D3DTOP_BUMPENVMAP                 = 22,
  D3DTOP_BUMPENVMAPLUMINANCE        = 23,
  D3DTOP_DOTPRODUCT3                = 24,
  D3DTOP_MULTIPLYADD                = 25,
  D3DTOP_LERP                       = 26,
  D3DTOP_FORCE_DWORD                = 0x7fffffff
} D3DTEXTUREOP, *LPD3DTEXTUREOP;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**Désactivation de D3DTOP \_**
</dt> <dd>

Désactive la sortie de cette étape de texture et toutes les étapes avec un index plus élevé. Pour désactiver le mappage de texture, définissez-le en tant qu’opération de couleur pour la première étape de texture (étape 0). Les opérations alpha ne peuvent pas être désactivées lorsque les opérations de couleur sont activées. La définition de l’opération alpha sur D3DTOP \_ désactive lorsque la fusion de couleurs est activée entraîne un comportement indéfini.

</dd> <dt>

<span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**D3DTOP \_ SELECTARG1**
</dt> <dd>

Utilisez la première couleur ou l’argument alpha de cette étape de texture, non modifié, comme sortie. Cette opération affecte l’argument Color lorsqu’il est utilisé avec l' \_ État D3DTSS COLOROP texture-stage et l’argument alpha en cas d’utilisation avec D3DTSS \_ ALPHAOP.

![équation de cet argument (s (RVBA) = Arg1)](images/topfrm1.png)

</dd> <dt>

<span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**D3DTOP \_ SELECTARG2**
</dt> <dd>

Utilisez la deuxième couleur de cette étape de texture ou l’argument alpha, non modifié, comme sortie. Cette opération affecte l’argument de couleur lorsqu’il est utilisé avec l’état de l' \_ étape de texture D3DTSS COLOROP, et l’argument alpha lorsqu’il est utilisé avec D3DTSS \_ ALPHAOP.

![équation de cet argument (s (RVBA) = Arg2)](images/topfrm2.png)

</dd> <dt>

<span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**\_Modulation D3DTOP**
</dt> <dd>

Multipliez les composants des arguments.

![équation de l’opération de modulation (s (RVBA) = Arg1 x ARG 2)](images/topfrm3.png)

</dd> <dt>

<span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**D3DTOP \_ MODULATE2X**
</dt> <dd>

Multipliez les composants des arguments et décalez les produits vers le bit de gauche 1 (en les multipliant par 2) pour l’éclaircissement.

![équation de l’opération Modulate2X (s (RVBA) = (Arg1 x ARG 2) puis décalée vers la gauche 1)](images/topfrm4.png)

</dd> <dt>

<span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**D3DTOP \_ MODULATE4X**
</dt> <dd>

Multipliez les composants des arguments et décalez les produits vers les 2 bits de gauche (en les multipliant par 4) pour l’éclaircissement.

![équation de l’opération Modulate4X (s (RVBA) = (Arg1 x ARG 2) puis décalée vers la gauche 2)](images/topfrm5.png)

</dd> <dt>

<span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP \_ Ajouter**
</dt> <dd>

Ajoutez les composants des arguments.

![équation de l’opération d’ajout (s (RVBA) = Arg1 + ARG 2)](images/topfrm6.png)

</dd> <dt>

<span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**D3DTOP \_ ADDSIGNED**
</dt> <dd>

Ajoutez les composants des arguments avec un décalage-0,5, ce qui rend la plage effective des valeurs comprises entre-0,5 et 0,5.

![équation de l’ajout d’une ou de plusieurs opérations signées (RVBA) = Arg1 + ARG 2 – 0,5)](images/topfrm7.png)

</dd> <dt>

<span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**D3DTOP \_ ADDSIGNED2X**
</dt> <dd>

Ajoutez les composants des arguments avec un décalage-0,5, puis décalez les produits vers la gauche 1 bit.

![équation de l’opération Add signed 2x ((s (RVBA) = Arg1 + ARG 2-0,5), puis décalée vers la gauche 1)](images/topfrm8.png)

</dd> <dt>

<span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**D3DTOP \_ soustraire**
</dt> <dd>

Soustraire les composants du deuxième argument de ceux du premier argument.

![équation de l’opération de soustraction (s (RVBA) = Arg1-ARG 2)](images/topfrm9.png)

</dd> <dt>

<span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**D3DTOP \_ ADDSMOOTH**
</dt> <dd>

Ajoutez le premier et le deuxième arguments ; soustrayez ensuite le produit de la somme.

![équation de l’ajout d’opérations lisses (s (RVBA) = Arg1 + ARG 2 x (1-Arg1))](images/topfrm10.png)

</dd> <dt>

<span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**D3DTOP \_ BLENDDIFFUSEALPHA**
</dt> <dd>

Mélanger de manière linéaire cette étape de texture à l’aide de l’alpha interpolé à partir de chaque vertex.

![équation de l’opération Blend diffuse alpha (s (RVBA) = Arg1 x alpha + ARG 2 x (1-alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**D3DTOP \_ BLENDTEXTUREALPHA**
</dt> <dd>

Fusionne de manière linéaire cette étape de texture à l’aide de l’alpha de la texture de cette étape.

![équation de l’opération alpha de texture de fusion (s (RVBA) = Arg1 x alpha + ARG 2 x (1-alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**D3DTOP \_ BLENDFACTORALPHA**
</dt> <dd>

Mélangez de manière linéaire cette étape de texture à l’aide d’un alpha scalaire défini avec l' \_ État de rendu D3DRS TEXTUREFACTOR.

![équation du facteur de fusion alpha Operation (s (RVBA) = Arg1 x alpha + ARG 2 x (1-alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**D3DTOP \_ BLENDTEXTUREALPHAPM**
</dt> <dd>

Fusionne de manière linéaire une étape de texture qui utilise une alpha prémultipliée.

![équation de la texture de fusion alpha PM (s (RVBA) = Arg1 + ARG 2 x (1-alpha))](images/topfrm12.png)

</dd> <dt>

<span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**D3DTOP \_ BLENDCURRENTALPHA**
</dt> <dd>

Mélangez de manière linéaire cette étape de texture à l’aide de l’alpha prélevé à partir de l’étape de texture précédente.

![équation de l’opération alpha actuelle de fusion (s (RVBA) = Arg1 x alpha + Arg2 x (1-alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**Prémodulation D3DTOP \_**
</dt> <dd>

Le \_ PRÉMODULATION D3DTOP est défini à l’étape n. La sortie de la phase n est Arg1. En outre, s’il y a une texture à la phase n + 1, tout D3DTA \_ actuel à la phase n + 1 est prémultiplié par la texture à l’étape n + 1.

</dd> <dt>

<span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**D3DTOP \_ MODULATEALPHA \_ ADDCOLOR**
</dt> <dd>

Moduler la couleur du deuxième argument, à l’aide de l’alpha du premier argument ; Ajoutez ensuite le résultat à l’argument 1. Cette opération est prise en charge uniquement pour les opérations de couleur (D3DTSS \_ COLOROP).

![équation de l’opération d’ajout de couleurs module alpha (s (RVBA) = Arg1 (RVB) + Arg1 (a) x Arg2 (RVB))](images/topfrm13.png)

</dd> <dt>

<span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP \_ MODULATECOLOR \_ ADDALPHA**
</dt> <dd>

Moduler les arguments ; Ajoutez ensuite le alpha du premier argument. Cette opération est prise en charge uniquement pour les opérations de couleur (D3DTSS \_ COLOROP).

![équation de l’opération de couleur ajouter un module alpha (s (RVBA) = Arg1 (RVB) x Arg2 (RVB) + Arg1 (a))](images/topfrm14.png)

</dd> <dt>

<span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**D3DTOP \_ MODULATEINVALPHA \_ ADDCOLOR**
</dt> <dd>

Semblable à D3DTOP \_ MODULATEALPHA \_ ADDCOLOR, mais utilise l’inverse de l’alpha du premier argument. Cette opération est prise en charge uniquement pour les opérations de couleur (D3DTSS \_ COLOROP).

![équation de l’ajout de couleur module de l’opération alpha inverse (s (RVBA) = (1-Arg1 (a)) x Arg2 (RVB) + Arg1 (RVB))](images/topfrm15.png)

</dd> <dt>

<span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP \_ MODULATEINVCOLOR \_ ADDALPHA**
</dt> <dd>

Semblable à D3DTOP \_ MODULATECOLOR \_ ADDALPHA, mais utilise l’inverse de la couleur du premier argument. Cette opération est prise en charge uniquement pour les opérations de couleur (D3DTSS \_ COLOROP).

![équation de l’opération ajouter une couleur d’inversion de module alpha (RVBA) = (1-Arg1 (RVB)) x Arg2 (RVB) + Arg1 (a))](images/topfrm16.png)

</dd> <dt>

<span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**D3DTOP \_ BUMPENVMAP**
</dt> <dd>

Effectuez un mappage de bosselage par pixel à l’aide de la carte d’environnement dans l’étape de texture suivante, sans luminance. Cette opération est prise en charge uniquement pour les opérations de couleur (D3DTSS \_ COLOROP).

</dd> <dt>

<span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**D3DTOP \_ BUMPENVMAPLUMINANCE**
</dt> <dd>

Effectuez un mappage de bosselage par pixel, à l’aide de la carte d’environnement dans l’étape de texture suivante, avec la luminance. Cette opération est prise en charge uniquement pour les opérations de couleur (D3DTSS \_ COLOROP).

</dd> <dt>

<span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**D3DTOP \_ DOTPRODUCT3**
</dt> <dd>

Moduler les composants de chaque argument en tant que composants signés, ajouter leurs produits ; Ensuite, répliquez la somme sur tous les canaux de couleurs, y compris alpha. Cette opération est prise en charge pour les opérations de couleur et alpha.

![équation du point produit 3 Operations (s (RVBA) = Arg1 (r) x Arg2 (r) + Arg1 (g) x Arg2 (g) + Arg1 (b) x Arg2 (b))](images/topfrm17.png)

Dans DirectX 6 et DirectX 7, les opérations de multitextures, les entrées ci-dessus sont toutes décalées de moitié (y = x-0,5) avant d’être utilisées pour simuler des données signées, et le résultat scalaire est automatiquement ancré aux valeurs positives et répliqué sur les trois canaux de sortie. Notez également qu’en tant qu’opération de couleur, cela ne met pas à jour le alpha, il met simplement à jour les composants RGB.

Toutefois, dans les nuanceurs DirectX 8,1, vous pouvez spécifier que la sortie doit être acheminée vers les composants. RGB ou. a ou les deux (valeur par défaut). Vous pouvez également spécifier une opération scalaire distincte sur le canal alpha.

</dd> <dt>

<span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**D3DTOP \_ MULTIPLYADD**
</dt> <dd>

Effectue une opération de multiplication cumulée. Elle prend les deux derniers arguments, les multiplie et les ajoute à l’argument d’entrée/source restant, et les place dans le résultat.

S<sub>RVBA</sub> = Arg1 + Arg2 \* Arg3

</dd> <dt>

<span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**D3DTOP \_ LERP**
</dt> <dd>

Interpole de manière linéaire entre le deuxième et le troisième argument source en fonction d’une proportion spécifiée dans le premier argument source.

S<sub>RVBA</sub> = (Arg1) \* Arg2 + (1-Arg1) \* Arg3.

</dd> <dt>

<span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les membres de ce type sont utilisés lors de la définition d’opérations de couleur ou alpha à l’aide des \_ valeurs D3DTSS COLOROP ou D3DTSS \_ ALPHAOP avec la méthode [**IDirect3DDevice9 :: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) .

Dans les formules ci-dessus, S<sub>RVBA</sub> est la couleur RVBA produite par une opération de texture, et Arg1, Arg2 et Arg3 représentent la couleur RVBA complète des arguments de texture. Les composants individuels d’un argument sont affichés avec des indices. Par exemple, le composant alpha pour l’argument 1 s’affiche comme Arg1<sub>A</sub>.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
