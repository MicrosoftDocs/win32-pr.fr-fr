---
description: Les États de rendu définissent des États de configuration pour tous les types de traitement des vertex et des pixels.
ms.assetid: 2fd56388-f3bd-409f-876c-ae893840b623
title: Énumération D3DRENDERSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRENDERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0a7ad803535032705e6e1bb5456109486c59d190
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343064"
---
# <a name="d3drenderstatetype-enumeration"></a>Énumération D3DRENDERSTATETYPE

Les États de rendu définissent des États de configuration pour tous les types de traitement des vertex et des pixels. Certains États de rendu configurent le traitement des vertex et un traitement des pixels configuré (voir [États de rendu (Direct3D 9)](render-states.md)). Les États de rendu peuvent être enregistrés et restaurés à l’aide de stateblocks (consultez États de l' [enregistrement et de la restauration des blocs d’État (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DRENDERSTATETYPE { 
  D3DRS_ZENABLE                     = 7,
  D3DRS_FILLMODE                    = 8,
  D3DRS_SHADEMODE                   = 9,
  D3DRS_ZWRITEENABLE                = 14,
  D3DRS_ALPHATESTENABLE             = 15,
  D3DRS_LASTPIXEL                   = 16,
  D3DRS_SRCBLEND                    = 19,
  D3DRS_DESTBLEND                   = 20,
  D3DRS_CULLMODE                    = 22,
  D3DRS_ZFUNC                       = 23,
  D3DRS_ALPHAREF                    = 24,
  D3DRS_ALPHAFUNC                   = 25,
  D3DRS_DITHERENABLE                = 26,
  D3DRS_ALPHABLENDENABLE            = 27,
  D3DRS_FOGENABLE                   = 28,
  D3DRS_SPECULARENABLE              = 29,
  D3DRS_FOGCOLOR                    = 34,
  D3DRS_FOGTABLEMODE                = 35,
  D3DRS_FOGSTART                    = 36,
  D3DRS_FOGEND                      = 37,
  D3DRS_FOGDENSITY                  = 38,
  D3DRS_RANGEFOGENABLE              = 48,
  D3DRS_STENCILENABLE               = 52,
  D3DRS_STENCILFAIL                 = 53,
  D3DRS_STENCILZFAIL                = 54,
  D3DRS_STENCILPASS                 = 55,
  D3DRS_STENCILFUNC                 = 56,
  D3DRS_STENCILREF                  = 57,
  D3DRS_STENCILMASK                 = 58,
  D3DRS_STENCILWRITEMASK            = 59,
  D3DRS_TEXTUREFACTOR               = 60,
  D3DRS_WRAP0                       = 128,
  D3DRS_WRAP1                       = 129,
  D3DRS_WRAP2                       = 130,
  D3DRS_WRAP3                       = 131,
  D3DRS_WRAP4                       = 132,
  D3DRS_WRAP5                       = 133,
  D3DRS_WRAP6                       = 134,
  D3DRS_WRAP7                       = 135,
  D3DRS_CLIPPING                    = 136,
  D3DRS_LIGHTING                    = 137,
  D3DRS_AMBIENT                     = 139,
  D3DRS_FOGVERTEXMODE               = 140,
  D3DRS_COLORVERTEX                 = 141,
  D3DRS_LOCALVIEWER                 = 142,
  D3DRS_NORMALIZENORMALS            = 143,
  D3DRS_DIFFUSEMATERIALSOURCE       = 145,
  D3DRS_SPECULARMATERIALSOURCE      = 146,
  D3DRS_AMBIENTMATERIALSOURCE       = 147,
  D3DRS_EMISSIVEMATERIALSOURCE      = 148,
  D3DRS_VERTEXBLEND                 = 151,
  D3DRS_CLIPPLANEENABLE             = 152,
  D3DRS_POINTSIZE                   = 154,
  D3DRS_POINTSIZE_MIN               = 155,
  D3DRS_POINTSPRITEENABLE           = 156,
  D3DRS_POINTSCALEENABLE            = 157,
  D3DRS_POINTSCALE_A                = 158,
  D3DRS_POINTSCALE_B                = 159,
  D3DRS_POINTSCALE_C                = 160,
  D3DRS_MULTISAMPLEANTIALIAS        = 161,
  D3DRS_MULTISAMPLEMASK             = 162,
  D3DRS_PATCHEDGESTYLE              = 163,
  D3DRS_DEBUGMONITORTOKEN           = 165,
  D3DRS_POINTSIZE_MAX               = 166,
  D3DRS_INDEXEDVERTEXBLENDENABLE    = 167,
  D3DRS_COLORWRITEENABLE            = 168,
  D3DRS_TWEENFACTOR                 = 170,
  D3DRS_BLENDOP                     = 171,
  D3DRS_POSITIONDEGREE              = 172,
  D3DRS_NORMALDEGREE                = 173,
  D3DRS_SCISSORTESTENABLE           = 174,
  D3DRS_SLOPESCALEDEPTHBIAS         = 175,
  D3DRS_ANTIALIASEDLINEENABLE       = 176,
  D3DRS_MINTESSELLATIONLEVEL        = 178,
  D3DRS_MAXTESSELLATIONLEVEL        = 179,
  D3DRS_ADAPTIVETESS_X              = 180,
  D3DRS_ADAPTIVETESS_Y              = 181,
  D3DRS_ADAPTIVETESS_Z              = 182,
  D3DRS_ADAPTIVETESS_W              = 183,
  D3DRS_ENABLEADAPTIVETESSELLATION  = 184,
  D3DRS_TWOSIDEDSTENCILMODE         = 185,
  D3DRS_CCW_STENCILFAIL             = 186,
  D3DRS_CCW_STENCILZFAIL            = 187,
  D3DRS_CCW_STENCILPASS             = 188,
  D3DRS_CCW_STENCILFUNC             = 189,
  D3DRS_COLORWRITEENABLE1           = 190,
  D3DRS_COLORWRITEENABLE2           = 191,
  D3DRS_COLORWRITEENABLE3           = 192,
  D3DRS_BLENDFACTOR                 = 193,
  D3DRS_SRGBWRITEENABLE             = 194,
  D3DRS_DEPTHBIAS                   = 195,
  D3DRS_WRAP8                       = 198,
  D3DRS_WRAP9                       = 199,
  D3DRS_WRAP10                      = 200,
  D3DRS_WRAP11                      = 201,
  D3DRS_WRAP12                      = 202,
  D3DRS_WRAP13                      = 203,
  D3DRS_WRAP14                      = 204,
  D3DRS_WRAP15                      = 205,
  D3DRS_SEPARATEALPHABLENDENABLE    = 206,
  D3DRS_SRCBLENDALPHA               = 207,
  D3DRS_DESTBLENDALPHA              = 208,
  D3DRS_BLENDOPALPHA                = 209,
  D3DRS_FORCE_DWORD                 = 0x7fffffff
} D3DRENDERSTATETYPE, *LPD3DRENDERSTATETYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS \_ ZENABLE**
</dt> <dd>

État de mise en mémoire tampon de profondeur comme un membre du type énuméré [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) . Définissez cet État sur D3DZB \_ true pour activer la mise en mémoire tampon z, D3DZB \_ USEW pour activer la mise en mémoire tampon w ou D3DZB \_ false pour désactiver la mise en mémoire tampon de profondeur.

La valeur par défaut de cet état de rendu est D3DZB \_ true si un stencil de profondeur a été créé avec la chaîne de permutation en affectant la valeur **true** au membre EnableAutoDepthStencil de la structure de [**\_ paramètres D3DPRESENT**](d3dpresent-parameters.md) et D3DZB \_ false dans le cas contraire.

</dd> <dt>

<span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS \_ FillMode**
</dt> <dd>

Un ou plusieurs membres du type énuméré [**D3DFILLMODE**](./d3dfillmode.md) . La valeur par défaut est D3DFILL \_ Solid.

</dd> <dt>

<span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS \_ SHADEMODE**
</dt> <dd>

Un ou plusieurs membres du type énuméré [**D3DSHADEMODE**](./d3dshademode.md) . La valeur par défaut est D3DSHADE \_ Gouraud.

</dd> <dt>

<span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS \_ ZWRITEENABLE**
</dt> <dd>

**True** pour permettre à l’application d’écrire dans le tampon de profondeur. La valeur par défaut est **true**. Ce membre permet à une application d’empêcher le système de mettre à jour la mémoire tampon de profondeur avec de nouvelles valeurs de profondeur. Si la **valeur est false**, les comparaisons de profondeur sont toujours effectuées en fonction de l’état de rendu D3DRS \_ ZFUNC, en supposant que la mise en mémoire tampon de profondeur a lieu, mais que les valeurs de profondeur ne sont pas écrites dans la mémoire tampon.

</dd> <dt>

<span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS \_ ALPHATESTENABLE**
</dt> <dd>

**True** pour activer le test alpha par pixel. Si le test réussit, le pixel est traité par la mémoire tampon de trame. Dans le cas contraire, tout le traitement de la mémoire tampon de trame est ignoré pour le pixel.

Le test est effectué en comparant la valeur alpha entrante avec la valeur alpha de référence, à l’aide de la fonction de comparaison fournie par l' \_ État de rendu D3DRS ALPHAFUNC. La valeur alpha de référence est déterminée par la valeur définie pour D3DRS \_ ALPHAREF. Pour plus d’informations, consultez [État des tests alpha (Direct3D 9)](alpha-testing-state.md).

La valeur par défaut de ce paramètre est **false**.

</dd> <dt>

<span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS \_ LASTPIXEL**
</dt> <dd>

La valeur par défaut est **true**, ce qui permet de dessiner le dernier pixel d’une ligne. Pour empêcher le dessin du dernier pixel, définissez cette valeur sur **false**. Pour plus d’informations, consultez état de la [structure et du remplissage (Direct3D 9)](outline-and-fill-state.md).

</dd> <dt>

<span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS \_ SRCBLEND**
</dt> <dd>

Un membre du type énuméré [**D3DBLEND**](./d3dblend.md) . La valeur par défaut est D3DBLEND \_ .

</dd> <dt>

<span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS \_ DESTBLEND**
</dt> <dd>

Un membre du type énuméré [**D3DBLEND**](./d3dblend.md) . La valeur par défaut est D3DBLEND \_ zéro.

</dd> <dt>

<span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS \_ CULLMODE**
</dt> <dd>

Spécifie la manière dont les triangles d’arrière-plan sont éliminés, si ce n’est pas le cas. Peut être défini sur un membre du type énuméré [**D3DCULL**](./d3dcull.md) . La valeur par défaut est D3DCULL \_ CCW.

</dd> <dt>

<span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS \_ ZFUNC**
</dt> <dd>

Un membre du type énuméré [**D3DCMPFUNC**](./d3dcmpfunc.md) . La valeur par défaut est D3DCMP \_ LESSEQUAL. Ce membre permet à une application d’accepter ou de rejeter un pixel, en fonction de sa distance par rapport à l’appareil photo.

La valeur de profondeur du pixel est comparée à la valeur de la mémoire tampon de profondeur. Si la valeur de profondeur du pixel passe la fonction de comparaison, le pixel est écrit.

La valeur de profondeur est écrite dans le tampon de profondeur uniquement si l’état de rendu est **true**.

Les rastériseurs de logiciels et de nombreux accélérateurs de matériel fonctionnent plus rapidement si le test de profondeur échoue, car il n’est pas nécessaire de filtrer et de moduler la texture si le pixel n’est pas rendu.

</dd> <dt>

<span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS \_ ALPHAREF**
</dt> <dd>

Valeur qui spécifie une valeur alpha de référence par rapport à laquelle les pixels sont testés lorsque le test alpha est activé. Il s’agit d’une valeur de 8 bits placée dans les 8 bits de poids faible de la valeur de l’état de rendu DWORD. Les valeurs peuvent être comprises entre 0x00000000 et 0x000000FF. La valeur par défaut est 0.

</dd> <dt>

<span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS \_ ALPHAFUNC**
</dt> <dd>

Un membre du type énuméré [**D3DCMPFUNC**](./d3dcmpfunc.md) . La valeur par défaut est D3DCMP \_ Always. Ce membre permet à une application d’accepter ou de rejeter un pixel, en fonction de sa valeur alpha.

</dd> <dt>

<span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS \_ DITHERENABLE**
</dt> <dd>

**True** pour activer le tramage. La valeur par défaut est **FALSE**.

</dd> <dt>

<span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS \_ ALPHABLENDENABLE**
</dt> <dd>

**True** pour activer la transparence à contrôle alpha. La valeur par défaut est **FALSE**.

Le type de fusion alpha est déterminé par les États de \_ rendu D3DRS SRCBLEND et D3DRS \_ DESTBLEND.

</dd> <dt>

<span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS \_ FOGENABLE**
</dt> <dd>

**True** pour activer la fusion de brouillard. La valeur par défaut est **FALSE**. Pour plus d’informations sur l’utilisation de la fusion de brouillard, consultez [brouillard](fog.md).

</dd> <dt>

<span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS \_ SpecularEnable**
</dt> <dd>

**True** pour activer les surbrillances spéculaires. La valeur par défaut est **FALSE**.

Les surbrillances spéculaires sont calculées comme si chaque vertex de l’objet allumé se trouve à l’origine de l’objet. Cela donne les résultats attendus tant que l’objet est modélisé autour de l’origine et que la distance entre la lumière et l’objet est relativement importante. Dans d’autres cas, les résultats ne sont pas définis.

Lorsque ce membre a la valeur **true**, la couleur spéculaire est ajoutée à la couleur de base après la cascade de texture, mais avant la fusion alpha.

</dd> <dt>

<span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS \_ FOGCOLOR**
</dt> <dd>

Valeur dont le type est [**D3DCOLOR**](d3dcolor.md). La valeur par défaut est 0. Pour plus d’informations sur la couleur de brouillard, consultez [couleur de brouillard (Direct3D 9)](fog-color.md).

</dd> <dt>

<span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS \_ FOGTABLEMODE**
</dt> <dd>

Formule de brouillard à utiliser pour le brouillard de pixel. Défini sur l’un des membres du type énuméré [**D3DFOGMODE**](./d3dfogmode.md) . La valeur par défaut est D3DFOG \_ None. Pour plus d’informations sur le brouillard de pixel, consultez la rubrique [brouillard de pixel (Direct3D 9)](pixel-fog.md).

</dd> <dt>

<span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS \_ FOGSTART**
</dt> <dd>

Profondeur à laquelle les effets de brouillard de pixel ou de vertex commencent pour le mode de brouillard linéaire. La valeur par défaut est 0.0 f. La profondeur est spécifiée dans l’espace universel pour le brouillard de vertex et l’espace \[ de périphérique 0,0, 1,0 \] ou l’espace universel pour le brouillard de pixel. Pour le brouillard de pixel, ces valeurs se trouvent dans l’espace de l’appareil lorsque le système utilise z pour les calculs de brouillard et l’espace universel lorsque le système utilise le brouillard relatif à l’oeil (w-brouillard). Pour plus d’informations, consultez [paramètres de brouillard (Direct3D 9)](fog-parameters.md) et [profondeur oculaire ou Z](pixel-fog.md).

Les valeurs de cet état de rendu sont des valeurs à virgule flottante. Étant donné que la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte les valeurs DWORD, votre application doit effectuer un cast d’une variable qui contient la valeur, comme indiqué dans l’exemple de code suivant.


```
pDevice9->SetRenderState(D3DRS_FOGSTART, 
                         *((DWORD*) (&fFogStart)));
```



</dd> <dt>

<span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS \_ FOGEND**
</dt> <dd>

Profondeur à laquelle les effets de brouillard de pixel ou de vertex se terminent pour le mode de brouillard linéaire. La valeur par défaut est 1,0 f. La profondeur est spécifiée dans l’espace universel pour le brouillard de vertex et l’espace \[ de périphérique 0,0, 1,0 \] ou l’espace universel pour le brouillard de pixel. Pour le brouillard de pixel, ces valeurs se trouvent dans l’espace de l’appareil lorsque le système utilise z pour les calculs de brouillard et dans l’espace universel quand le système utilise le brouillard relatif à l’oeil (w-brouillard). Pour plus d’informations, consultez [paramètres de brouillard (Direct3D 9)](fog-parameters.md) et [profondeur oculaire ou Z](pixel-fog.md).

Les valeurs de cet état de rendu sont des valeurs à virgule flottante. Étant donné que la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte les valeurs DWORD, votre application doit effectuer un cast d’une variable qui contient la valeur, comme indiqué dans l’exemple de code suivant.


```
m_pDevice9->SetRenderState(D3DRS_FOGEND, *((DWORD*) (&fFogEnd)));
```



</dd> <dt>

<span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**D3DRS \_ FOGDENSITY**
</dt> <dd>

Densité de brouillard pour le brouillard de pixel ou vertex utilisé dans les modes de brouillard exponentiels (D3DFOG \_ exp et D3DFOG \_ EXP2). Les valeurs de densité valides sont comprises entre 0,0 et 1,0. La valeur par défaut est 1,0. Pour plus d’informations, consultez [paramètres de brouillard (Direct3D 9)](fog-parameters.md).

Les valeurs de cet état de rendu sont des valeurs à virgule flottante. Étant donné que la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte les valeurs DWORD, votre application doit effectuer un cast d’une variable qui contient la valeur, comme indiqué dans l’exemple de code suivant.


```
    m_pDevice9->SetRenderState(D3DRS_FOGDENSITY, *((DWORD*) (&fFogDensity)));
```



</dd> <dt>

<span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS \_ RANGEFOGENABLE**
</dt> <dd>

**True** pour activer le brouillard de vertex basé sur une plage. La valeur par défaut est **false**, auquel cas le système utilise le brouillard basé sur la profondeur. Dans le brouillard basé sur une plage, la distance d’un objet à partir de la visionneuse est utilisée pour calculer les effets de brouillard, et non la profondeur de l’objet (autrement dit, la coordonnée z) dans la scène. Dans le brouillard basé sur une plage, toutes les méthodes de brouillard fonctionnent comme d’habitude, sauf qu’elles utilisent la plage au lieu de la profondeur dans les calculs.

La plage est le facteur approprié à utiliser pour les calculs de brouillard, mais la profondeur est couramment utilisée à la place, car la plage prend du temps pour calculer et la profondeur est généralement déjà disponible. L’utilisation de Depth pour calculer le brouillard a l’effet indésirable que le fogginess des objets périphériques change à mesure que l’œil de la visionneuse se déplace. dans ce cas, les modifications de profondeur et la plage restent constantes.

Étant donné qu’aucun matériel ne prend actuellement en charge le brouillard basé sur une plage par pixel, la correction de plage est proposée uniquement pour le brouillard de vertex.

Pour plus d’informations, consultez la rubrique [brouillard de vertex (Direct3D 9)](vertex-fog.md).

</dd> <dt>

<span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS \_ STENCILENABLE**
</dt> <dd>

**True** pour activer le stencil, ou **false** pour désactiver le stencil. La valeur par défaut est **FALSE**. Pour plus d’informations, consultez [techniques de tampon de stencil (Direct3D 9)](stencil-buffer-techniques.md).

</dd> <dt>

<span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS \_ STENCILFAIL**
</dt> <dd>

Opération de stencil à effectuer en cas d’échec du test du stencil. Les valeurs proviennent du type énuméré [**D3DSTENCILOP**](./d3dstencilop.md) . La valeur par défaut est D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS \_ STENCILZFAIL**
</dt> <dd>

Opération de stencil à effectuer si le test de stencil réussit et que le test de profondeur (z-test) échoue. Les valeurs proviennent du type énuméré [**D3DSTENCILOP**](./d3dstencilop.md) . La valeur par défaut est D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS \_ STENCILPASS**
</dt> <dd>

Opération de stencil à effectuer si le stencil et les tests de profondeur (z) réussissent. Les valeurs proviennent du type énuméré [**D3DSTENCILOP**](./d3dstencilop.md) . La valeur par défaut est D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS \_ STENCILFUNC**
</dt> <dd>

Fonction de comparaison pour le test de stencil. Les valeurs proviennent du type énuméré [**D3DCMPFUNC**](./d3dcmpfunc.md) . La valeur par défaut est D3DCMP \_ Always.

La fonction de comparaison est utilisée pour comparer la valeur de référence à une entrée de tampon de stencil. Cette comparaison s’applique uniquement aux bits dans la valeur de référence et à l’entrée de mémoire tampon de stencil qui sont définis dans le masque de stencil (défini par l' \_ État de rendu D3DRS STENCILMASK). Si la **valeur est true**, le test du stencil réussit.

</dd> <dt>

<span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS \_ STENCILREF**
</dt> <dd>

Valeur de référence int pour le test de stencil. La valeur par défaut est 0.

</dd> <dt>

<span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS \_ STENCILMASK**
</dt> <dd>

Masque appliqué à la valeur de référence et à chaque entrée de tampon de stencil pour déterminer les bits significatifs pour le test de stencil. Le masque par défaut est 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS \_ STENCILWRITEMASK**
</dt> <dd>

Masque d’écriture appliqué aux valeurs écrites dans la mémoire tampon du stencil. Le masque par défaut est 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS \_ TEXTUREFACTOR**
</dt> <dd>

Couleur utilisée pour la fusion de textures multiples avec l' \_ argument D3DTA TFACTOR texture-Blending ou l' \_ opération de fusion de texture D3DTOP BLENDFACTORALPHA. La valeur associée est une variable [**D3DCOLOR**](d3dcolor.md) . La valeur par défaut est opaque white (0xFFFFFFFF).

</dd> <dt>

<span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS \_ WRAP0**
</dt> <dd>

Comportement d’habillage de texture pour plusieurs jeux de coordonnées de texture. Les valeurs valides pour cet état de rendu peuvent être n’importe quelle combinaison des D3DWRAPCOORD \_ 0 (ou D3DWRAP \_ U), D3DWRAPCOORD \_ 1 (ou D3DWRAP \_ V), D3DWRAPCOORD \_ 2 (ou D3DWRAP \_ W) et D3DWRAPCOORD \_ 3 indicateurs. Cela amène le système à encapsuler dans le sens des premières, deuxième, troisième et quatrième dimensions, parfois appelées directions s, t, r et q, pour une texture donnée. La valeur par défaut de cet état de rendu est 0 (encapsulation désactivée dans toutes les directions).

</dd> <dt>

<span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS \_ WRAP1**
</dt> <dd>

Consultez D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS \_ WRAP2**
</dt> <dd>

Consultez D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS \_ WRAP3**
</dt> <dd>

Consultez D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS \_ WRAP4**
</dt> <dd>

Consultez D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS \_ WRAP5**
</dt> <dd>

Consultez D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS \_ WRAP6**
</dt> <dd>

Consultez D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS \_ WRAP7**
</dt> <dd>

Consultez D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**\_Découpage D3DRS**
</dt> <dd>

**True** pour activer le découpage primitif par Direct3D, ou **false** pour le désactiver. La valeur par défaut est **true**.

</dd> <dt>

<span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**\_Éclairage D3DRS**
</dt> <dd>

**True** pour activer l’éclairage Direct3D, ou **false** pour le désactiver. La valeur par défaut est **true**. Seuls les vertex qui incluent un sommet normal sont correctement allumés ; les vertex qui ne contiennent pas de normales utilisent un produit scalaire de 0 dans tous les calculs d’éclairage.

</dd> <dt>

<span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS \_ ambiant**
</dt> <dd>

Couleur de l’éclairage ambiant. Cette valeur est de type [**D3DCOLOR**](d3dcolor.md). La valeur par défaut est 0.

</dd> <dt>

<span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS \_ FOGVERTEXMODE**
</dt> <dd>

Formule de brouillard à utiliser pour le brouillard de vertex. Défini sur un membre du type énuméré [**D3DFOGMODE**](./d3dfogmode.md) . La valeur par défaut est D3DFOG \_ None.

</dd> <dt>

<span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS \_ COLORVERTEX**
</dt> <dd>

**True** pour activer la couleur par vertex ou **false** pour la désactiver. La valeur par défaut est **true**. L’activation de la couleur par vertex permet au système d’inclure la couleur définie pour les vertex individuels dans ses calculs d’éclairage.

Pour plus d’informations, consultez les États de rendu suivants :

-   D3DRS \_ DIFFUSEMATERIALSOURCE
-   D3DRS \_ SPECULARMATERIALSOURCE
-   D3DRS \_ AMBIENTMATERIALSOURCE
-   D3DRS \_ EMISSIVEMATERIALSOURCE

</dd> <dt>

<span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS \_ LOCALVIEWER**
</dt> <dd>

**True** pour activer les surbrillances spéculaires relatives à l’appareil photo, ou **false** pour utiliser les surbrillances spéculaires orthogonales. La valeur par défaut est **true**. Les applications qui utilisent la projection orthogonale doivent spécifier **false**.

</dd> <dt>

<span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS \_ NORMALIZENORMALS**
</dt> <dd>

**True** pour activer la normalisation automatique des normales des sommets, ou **false** pour la désactiver. La valeur par défaut est **FALSE**. L’activation de cette fonctionnalité amène le système à normaliser les normales des vertex pour les vertex après les avoir transformées en espace de caméra, ce qui peut prendre du temps.

</dd> <dt>

<span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS \_ DIFFUSEMATERIALSOURCE**
</dt> <dd>

Source de couleur diffuse pour les calculs d’éclairage. Les valeurs valides sont les membres du type énuméré [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) . La valeur par défaut est D3DMCS \_ COLOR1. La valeur de cet état de rendu est utilisée uniquement si l' \_ État de rendu D3DRS COLORVERTEX est défini sur **true**.

</dd> <dt>

<span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS \_ SPECULARMATERIALSOURCE**
</dt> <dd>

Source de couleur spéculaire pour les calculs d’éclairage. Les valeurs valides sont les membres du type énuméré [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) . La valeur par défaut est D3DMCS \_ COLOR2.

</dd> <dt>

<span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS \_ AMBIENTMATERIALSOURCE**
</dt> <dd>

Source de couleur ambiante pour les calculs d’éclairage. Les valeurs valides sont les membres du type énuméré [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) . La valeur par défaut est D3DMCS \_ Material.

</dd> <dt>

<span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS \_ EMISSIVEMATERIALSOURCE**
</dt> <dd>

Source de couleur émissif pour les calculs d’éclairage. Les valeurs valides sont les membres du type énuméré [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) . La valeur par défaut est D3DMCS \_ Material.

</dd> <dt>

<span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS \_ VERTEXBLEND**
</dt> <dd>

Nombre de matrices à utiliser pour effectuer la fusion géométrique, le cas échéant. Les valeurs valides sont les membres du type énuméré [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) . La valeur par défaut est D3DVBF \_ Disable.

</dd> <dt>

<span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS \_ CLIPPLANEENABLE**
</dt> <dd>

Active ou désactive les plans de découpage définis par l’utilisateur. Les valeurs valides sont n’importe quelle valeur DWORD dans laquelle l’état de chaque bit (défini ou non défini) active ou désactive l’état d’activation d’un plan de découpage défini par l’utilisateur correspondant. Le bit le moins significatif (bit 0) contrôle le premier plan de découpage à l’index 0, et les bits suivants contrôlent l’activation des plans de découpage à des index plus élevés. Si un bit est défini, le système applique le plan de découpage approprié pendant le rendu de la scène. La valeur par défaut est 0.

Les macros [**D3DCLIPPLANEn**](d3dclipplanen.md) sont définies pour fournir un moyen pratique d’activer les plans de découpage.

</dd> <dt>

<span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS \_ pointe**
</dt> <dd>

Valeur flottante qui spécifie la taille à utiliser pour le calcul de la taille du point dans les cas où la taille du point n’est pas spécifiée pour chaque vertex. Cette valeur n’est pas utilisée lorsque le vertex contient une taille de point. Cette valeur est en unités d’espace d’écran si D3DRS \_ POINTSCALEENABLE a la valeur **false**; sinon, cette valeur est dans les unités d’espace universel. La valeur par défaut est la valeur retournée par un pilote. Si un pilote retourne 0 ou 1, la valeur par défaut est 64, ce qui permet l’émulation de la taille du point logiciel. Étant donné que la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte les valeurs DWORD, votre application doit effectuer un cast d’une variable qui contient la valeur, comme indiqué dans l’exemple de code suivant.


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE, *((DWORD*)&pointSize));
```



</dd> <dt>

<span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS \_ pointe \_ min.**
</dt> <dd>

Valeur flottante qui spécifie la taille minimale des primitives de point. Les primitives de point sont ancrées à cette taille pendant le rendu. Si vous définissez cette valeur sur des valeurs inférieures à 1,0, les points qui chutent lorsque le point ne couvre pas un centre de pixels et l’anticrénelage sont désactivés ou rendus avec une intensité réduite lorsque l’anticrénelage est activé. La valeur par défaut est 1,0 f. La plage de cette valeur est supérieure ou égale à 0.0 f. Étant donné que la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte les valeurs DWORD, votre application doit effectuer un cast d’une variable qui contient la valeur, comme indiqué dans l’exemple de code suivant.


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE_MIN, *((DWORD*)&pointSizeMin));
```



</dd> <dt>

<span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS \_ POINTSPRITEENABLE**
</dt> <dd>

valeur bool. Lorsque la **valeur est true**, les coordonnées de texture des primitives de point sont définies de sorte que les textures complètes soient mappées sur chaque point. Quand la **valeur est false**, les coordonnées de texture de vertex sont utilisées pour le point entier. La valeur par défaut est **FALSE**. Vous pouvez obtenir des points à un seul pixel de style DirectX 7 en affectant \_ à D3DRS POINTSCALEENABLE la **valeur false** et à D3DRS \_ la valeur 1,0, qui sont les valeurs par défaut.

</dd> <dt>

<span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS \_ POINTSCALEENABLE**
</dt> <dd>

valeur bool qui contrôle le calcul de la taille pour les primitives de point. Lorsque la valeur est **true**, la taille du point est interprétée comme une valeur d’espace de caméra et est mise à l’échelle par la fonction distance et la frustum à la mise à l’échelle de l’axe y pour calculer la taille finale du point d’espace d’écran. Quand la **valeur est false**, la taille du point est interprétée comme un espace à l’écran et utilisée directement. La valeur par défaut est **FALSE**.

</dd> <dt>

<span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS \_ POINTSCALE \_ A**
</dt> <dd>

Valeur float qui contrôle l’atténuation de la taille basée sur la distance pour les primitives de point. Actif uniquement lorsque D3DRS \_ POINTSCALEENABLE a la **valeur true**. La valeur par défaut est 1,0 f. La plage de cette valeur est supérieure ou égale à 0.0 f. Étant donné que la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte les valeurs DWORD, votre application doit effectuer un cast d’une variable qui contient la valeur, comme indiqué dans l’exemple de code suivant.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_A, *((DWORD*)&pointScaleA));
```



</dd> <dt>

<span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS \_ POINTSCALE \_ B**
</dt> <dd>

Valeur float qui contrôle l’atténuation de la taille basée sur la distance pour les primitives de point. Actif uniquement lorsque D3DRS \_ POINTSCALEENABLE a la **valeur true**. La valeur par défaut est 0.0 f. La plage de cette valeur est supérieure ou égale à 0.0 f. Étant donné que la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte les valeurs DWORD, votre application doit effectuer un cast d’une variable qui contient la valeur, comme indiqué dans l’exemple de code suivant.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_B, *((DWORD*)&pointScaleB));
```



</dd> <dt>

<span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS \_ POINTSCALE \_ C**
</dt> <dd>

Valeur float qui contrôle l’atténuation de la taille basée sur la distance pour les primitives de point. Actif uniquement lorsque D3DRS \_ POINTSCALEENABLE a la **valeur true**. La valeur par défaut est 0.0 f. La plage de cette valeur est supérieure ou égale à 0.0 f. Étant donné que la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte les valeurs DWORD, votre application doit effectuer un cast d’une variable qui contient la valeur, comme indiqué dans l’exemple de code suivant.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_C, *((DWORD*)&pointScaleC));
```



</dd> <dt>

<span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS \_ MULTISAMPLEANTIALIAS**
</dt> <dd>

valeur booléenne qui détermine la façon dont les échantillons individuels sont calculés lors de l’utilisation d’un tampon de cible de rendu à plusieurs échantillons. Quand la valeur est **true**, les différents échantillons sont calculés de manière à ce que l’anticrénelage complet soit effectué par échantillonnage à différentes positions d’échantillonnage pour chaque échantillon multiple. Quand la valeur est **false**, les exemples multiples sont tous écrits avec la même valeur d’échantillon, échantillonnés au centre de pixels, ce qui permet un rendu non-sans alias dans une mémoire tampon d’échantillonnage multiple. Cet état de rendu n’a aucun effet lors du rendu d’une mémoire tampon d’exemple unique. La valeur par défaut est **true**.

</dd> <dt>

<span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS \_ MULTISAMPLEMASK**
</dt> <dd>

Chaque bit de ce masque, à partir du bit le moins significatif (LSB), contrôle la modification de l’un des exemples dans une cible de rendu à plusieurs échantillons. Par conséquent, pour une cible de rendu à 8 échantillons, l’octet de poids faible contient les huit exemples d’écriture pour chacun des huit échantillons. Cet état de rendu n’a aucun effet lors du rendu d’une mémoire tampon d’exemple unique. La valeur par défaut est 0xFFFFFFFF.

Cet état de rendu permet l’utilisation d’une mémoire tampon d’exemples en tant que mémoire tampon d’accumulation, en procédant à un rendu multipasse de Geometry où chaque passe met à jour un sous-ensemble d’échantillons.

S’il existe n exemples d’échantillonnages et k, l’intensité résultante de l’image rendue doit être k/n. Chaque composant RVB de chaque pixel est pondéré par k/n.

</dd> <dt>

<span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS \_ PATCHEDGESTYLE**
</dt> <dd>

Définit si les bords des correctifs utilisent le pavage de style flottant. Les valeurs possibles sont définies par le type énuméré [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) . La valeur par défaut est D3DPATCHEDGE \_ discrète.

</dd> <dt>

<span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS \_ DEBUGMONITORTOKEN**
</dt> <dd>

Défini uniquement pour le débogage de l’analyse. Les valeurs possibles sont définies par le type énuméré [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) . Notez que si D3DRS \_ DEBUGMONITORTOKEN est défini, l’appel est traité comme la transmission d’un jeton à l’analyse de débogage. Par exemple, si-après passage de D3DDMT \_ Enable ou D3DDMT \_ Disable à D3DRS \_ DEBUGMONITORTOKEN-les autres valeurs de jeton sont transmises, l’État (activé ou désactivé) de l’analyse de débogage est toujours conservé.

Cet État est utile uniquement pour les versions Debug. La valeur par défaut de l’analyse de débogage est D3DDMT \_ activer.

</dd> <dt>

<span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS \_ pointe \_ Max.**
</dt> <dd>

Valeur flottante qui spécifie la taille maximale à laquelle les points de sprite seront fixés. La valeur doit être inférieure ou égale au membre MaxPointSize de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) et supérieur ou égal à D3DRS \_ \_ . La valeur par défaut est 64,0. Étant donné que la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte les valeurs DWORD, votre application doit effectuer un cast d’une variable qui contient la valeur, comme indiqué dans l’exemple de code suivant.


```
m_pDevice9->SetRenderState(D3DRS_PONTSIZE_MAX, *((DWORD*)&pointSizeMax));
```



</dd> <dt>

<span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS \_ INDEXEDVERTEXBLENDENABLE**
</dt> <dd>

valeur booléenne qui active ou désactive la fusion de vertex indexée. La valeur par défaut est **FALSE**. Lorsque la valeur est **true**, la fusion des vertex indexée est activée. Quand la valeur est **false**, la fusion des vertex indexés est désactivée. Si cet état de rendu est activé, l’utilisateur doit passer des index de matrice comme un DWORDwith compressé tous les vertex. Lorsque l’état de rendu est désactivé et que la fusion de vertex est activée par le biais de l' \_ État D3DRS VERTEXBLEND, cela équivaut à avoir des index de matrice 0, 1, 2, 3 dans chaque vertex.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS \_ COLORWRITEENABLE**
</dt> <dd>

Valeur UINT qui active une écriture par canal pour la mémoire tampon de couleur de rendu cible. Un bit de jeu entraîne la mise à jour du canal de couleur pendant le rendu 3D. Un bit clair entraîne l’inaffectation du canal de couleur. Cette fonctionnalité est disponible si le \_ bit des fonctionnalités D3DPMISCCAPS COLORWRITEENABLE est défini dans le membre PrimitiveMiscCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) pour l’appareil. Cet état de rendu n’affecte pas l’opération d’effacement. La valeur par défaut est 0x0000000F.

Les valeurs valides pour cet état de rendu peuvent être n’importe quelle combinaison des \_ indicateurs D3DCOLORWRITEENABLE alpha, D3DCOLORWRITEENABLE \_ Blue, D3DCOLORWRITEENABLE \_ vert ou D3DCOLORWRITEENABLE \_ Red.

</dd> <dt>

<span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS \_ TWEENFACTOR**
</dt> <dd>

Valeur flottante qui contrôle le facteur d’interpolation. La valeur par défaut est 0.0 f. Étant donné que la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accepte les valeurs DWORD, votre application doit effectuer un cast d’une variable qui contient la valeur, comme indiqué dans l’exemple de code suivant.


```
m_pDevice9->SetRenderState(D3DRS_TWEENFACTOR, *((DWORD*)&TweenFactor));
```



</dd> <dt>

<span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS \_ BLENDOP**
</dt> <dd>

Valeur utilisée pour sélectionner l’opération arithmétique appliquée lorsque l’état de rendu de la fusion alpha, D3DRS \_ ALPHABLENDENABLE, a la valeur **true**. Les valeurs valides sont définies par le type énuméré [**D3DBLENDOP**](./d3dblendop.md) . La valeur par défaut est D3DBLENDOP \_ Add.

Si la fonctionnalité de l' \_ appareil D3DPMISCCAPS BLENDOP n’est pas prise en charge, l’ajout de D3DBLENDOP \_ est effectué.

</dd> <dt>

<span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS \_ POSITIONDEGREE**
</dt> <dd>

Degré d’interpolation de la position N-patch. Les valeurs peuvent être D3DDEGREE \_ cubique (par défaut) ou D3DDEGREE \_ Linear. Pour plus d’informations, consultez [**D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

<span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS \_ NORMALDEGREE**
</dt> <dd>

Degré d’interpolation normale N-patch. Les valeurs peuvent être D3DDEGREE \_ Linear (par défaut) ou D3DDEGREE \_ quadratique. Pour plus d’informations, consultez [**D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

<span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS \_ SCISSORTESTENABLE**
</dt> <dd>

**True** pour activer le test de ciseaux et **false** pour le désactiver. La valeur par défaut est **FALSE**.

</dd> <dt>

<span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS \_ SLOPESCALEDEPTHBIAS**
</dt> <dd>

Utilisé pour déterminer la quantité d’écart pouvant être appliquée aux primitives coplanaires pour réduire la lutte z. La valeur par défaut est 0.

Bias = (Max \* D3DRS \_ SLOPESCALEDEPTHBIAS) + D3DRS \_ DEPTHBIAS.

où Max est la pente de profondeur maximale du triangle rendu.

</dd> <dt>

<span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS \_ ANTIALIASEDLINEENABLE**
</dt> <dd>

**True** pour activer l’anticrénelage de ligne, **false** pour désactiver l’anticrénelage de ligne. La valeur par défaut est **FALSE**.

Lors du rendu sur une cible de rendu d’échantillonnage, D3DRS \_ ANTIALIASEDLINEENABLE est ignoré et toutes les lignes sont associées à un alias. Utilisez [**ID3DXLine**](id3dxline.md) pour le rendu de ligne avec anticrénelage dans une cible de rendu multiéchantillon.

</dd> <dt>

<span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS \_ MINTESSELLATIONLEVEL**
</dt> <dd>

Niveau de pavage minimal. La valeur par défaut est 1,0 f. Voir [pavage (Direct3D 9)](tessellation.md).

</dd> <dt>

<span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS \_ MAXTESSELLATIONLEVEL**
</dt> <dd>

Niveau de pavage maximal. La valeur par défaut est 1,0 f. Voir [pavage (Direct3D 9)](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS \_ ADAPTIVETESS \_ X**
</dt> <dd>

Valeur de paver de manière adaptative, sur l’axe x. La valeur par défaut est 0.0 f. Consultez [pavage adaptative](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS \_ ADAPTIVETESS \_ Y**
</dt> <dd>

Valeur de paver adaptative, sur l’axe y. La valeur par défaut est 0.0 f. Consultez [ \_ pavage adaptative](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS \_ ADAPTIVETESS \_ Z**
</dt> <dd>

Valeur de paver de manière adaptative, en z. La valeur par défaut est 1,0 f. Consultez [ \_ pavage adaptative](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS \_ ADAPTIVETESS \_ W**
</dt> <dd>

Valeur de paver adaptative, dans la direction w. La valeur par défaut est 0.0 f. Consultez [ \_ pavage adaptative](tessellation.md).

</dd> <dt>

<span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS \_ ENABLEADAPTIVETESSELLATION**
</dt> <dd>

**True** pour activer le pavage adaptative, **false** pour le désactiver. La valeur par défaut est **FALSE**. Consultez [ \_ pavage adaptative](tessellation.md).

</dd> <dt>

<span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS \_ TWOSIDEDSTENCILMODE**
</dt> <dd>

**True** active le stencil à deux côtés, **false** le désactive. La valeur par défaut est **FALSE**. L’application doit définir D3DRS \_ CULLMODE sur D3DCULL \_ None pour activer le mode stencil à deux côtés. Si l’ordre d’enroulement du triangle est dans le sens des aiguilles d’une montre, les \_ opérations du stencil D3DRS \* sont utilisées. Si l’ordre d’enroulement est dans le sens inverse des aiguilles d' \_ une passe, les opérations du stencil D3DRS CCW \_ \* sont utilisées.

Pour voir si le stencil à deux côtés est pris en charge, consultez le membre StencilCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) pour D3DSTENCILCAPS \_ TWOSIDED. Voir aussi [D3DSTENCILCAPS](d3dstencilcaps.md).

</dd> <dt>

<span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS \_ CCW \_ STENCILFAIL**
</dt> <dd>

Opération de stencil à effectuer si le test du stencil CCW échoue. Les valeurs proviennent du type énuméré [**D3DSTENCILOP**](./d3dstencilop.md) . La valeur par défaut est D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS \_ CCW \_ STENCILZFAIL**
</dt> <dd>

Opération de stencil à exécuter si le test de stencil CCW réussit et que le test z échoue. Les valeurs proviennent du type énuméré [**D3DSTENCILOP**](./d3dstencilop.md) . La valeur par défaut est D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS \_ CCW \_ STENCILPASS**
</dt> <dd>

Opération de stencil à effectuer si les deux stencils CCW et z-tests réussissent. Les valeurs proviennent du type énuméré [**D3DSTENCILOP**](./d3dstencilop.md) . La valeur par défaut est D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS \_ CCW \_ STENCILFUNC**
</dt> <dd>

Fonction de comparaison. Le test du stencil CCW réussit si la fonction de stencil ((Ref & Mask) (gabarit & Mask)) a la **valeur true**. Les valeurs proviennent du type énuméré [**D3DCMPFUNC**](./d3dcmpfunc.md) . La valeur par défaut est D3DCMP \_ Always.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS \_ COLORWRITEENABLE1**
</dt> <dd>

Valeurs ColorWriteEnable supplémentaires pour les appareils. Consultez D3DRS \_ COLORWRITEENABLE. Cette fonctionnalité est disponible si le \_ bit des fonctionnalités D3DPMISCCAPS INDEPENDENTWRITEMASKS est défini dans le membre PrimitiveMiscCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) pour l’appareil. La valeur par défaut est 0x0000000f.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS \_ COLORWRITEENABLE2**
</dt> <dd>

Valeurs ColorWriteEnable supplémentaires pour les appareils. Consultez D3DRS \_ COLORWRITEENABLE. Cette fonctionnalité est disponible si le \_ bit des fonctionnalités D3DPMISCCAPS INDEPENDENTWRITEMASKS est défini dans le membre PrimitiveMiscCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) pour l’appareil. La valeur par défaut est 0x0000000f.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS \_ COLORWRITEENABLE3**
</dt> <dd>

Valeurs ColorWriteEnable supplémentaires pour les appareils. Consultez D3DRS \_ COLORWRITEENABLE. Cette fonctionnalité est disponible si le \_ bit des fonctionnalités D3DPMISCCAPS INDEPENDENTWRITEMASKS est défini dans le membre PrimitiveMiscCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) pour l’appareil. La valeur par défaut est 0x0000000f.

</dd> <dt>

<span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS \_ BLENDFACTOR**
</dt> <dd>

[**D3DCOLOR**](d3dcolor.md) utilisé pour une constante Blend-Factor pendant la fusion alpha. Cette fonctionnalité est disponible si le \_ bit des fonctionnalités D3DPBLENDCAPS BLENDFACTOR est défini dans le membre SrcBlendCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) ou le membre DestBlendCaps de **D3DCAPS9**. Consultez [**D3DRENDERSTATETYPE**](). La valeur par défaut est 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS \_ SRGBWRITEENABLE**
</dt> <dd>

Activez la valeur gamma des écritures de la cible de rendu pour qu’elles soient corrigées en sRVB. Le format doit exposer D3DUSAGE \_ SRGBWRITE. La valeur par défaut est 0.

</dd> <dt>

<span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS \_ DEPTHBIAS**
</dt> <dd>

Valeur à virgule flottante utilisée pour la comparaison des valeurs de profondeur. Consultez [décalage de profondeur (Direct3D 9)](depth-bias.md). La valeur par défaut est 0.

</dd> <dt>

<span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS \_ WRAP8**
</dt> <dd>

Consultez D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS \_ WRAP9**
</dt> <dd>

Consultez D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS \_ WRAP10**
</dt> <dd>

Consultez D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS \_ WRAP11**
</dt> <dd>

Consultez D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS \_ WRAP12**
</dt> <dd>

Consultez D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS \_ WRAP13**
</dt> <dd>

Consultez D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS \_ WRAP14**
</dt> <dd>

Consultez D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS \_ WRAP15**
</dt> <dd>

Consultez D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS \_ SEPARATEALPHABLENDENABLE**
</dt> <dd>

**True** active le mode de fondu distinct pour le canal alpha. La valeur par défaut est **FALSE**.

Quand la valeur est **false**, les facteurs et les opérations de fusion de cible de rendu appliqués à alpha sont forcés à être les mêmes que ceux définis pour la couleur. Ce mode est effectivement câblé à **false** sur les implémentations qui ne définissent pas le SEPARATEALPHABLEND Cap D3DPMISCCAPS \_ . Consultez [D3DPMISCCAPS](d3dpmisccaps.md).

Le type de fusion alpha distincte est déterminé par les États de \_ rendu D3DRS SRCBLENDALPHA et D3DRS \_ DESTBLENDALPHA.

</dd> <dt>

<span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS \_ SRCBLENDALPHA**
</dt> <dd>

Un membre du type énuméré [**D3DBLEND**](./d3dblend.md) . Cette valeur est ignorée, sauf si D3DRS \_ SEPARATEALPHABLENDENABLE a la valeur **true**. La valeur par défaut est D3DBLEND \_ .

</dd> <dt>

<span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS \_ DESTBLENDALPHA**
</dt> <dd>

Un membre du type énuméré [**D3DBLEND**](./d3dblend.md) . Cette valeur est ignorée, sauf si D3DRS \_ SEPARATEALPHABLENDENABLE a la valeur **true**. La valeur par défaut est D3DBLEND \_ zéro.

</dd> <dt>

<span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS \_ BLENDOPALPHA**
</dt> <dd>

Valeur utilisée pour sélectionner l’opération arithmétique appliquée à la fusion alpha distincte lorsque l’état de rendu D3DRS \_ SEPARATEALPHABLENDENABLE est défini sur **true**.

Les valeurs valides sont définies par le type énuméré [**D3DBLENDOP**](./d3dblendop.md) . La valeur par défaut est D3DBLENDOP \_ Add.

Si la fonctionnalité de l' \_ appareil D3DPMISCCAPS BLENDOP n’est pas prise en charge, l’ajout de D3DBLENDOP \_ est effectué. Consultez [D3DPMISCCAPS](d3dpmisccaps.md).

</dd> <dt>

<span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Remarques



| États de rendu        |   Échantillonneur de texture                 |
|----------------------|--------------------|
| PS \_ 1 \_ 1 à PS \_ 1 \_ 3 | 4 échantillonneurs de texture |



 

Direct3D définit la \_ constante WRAPBIAS D3DRENDERSTATE comme un moyen pratique pour les applications d’activer ou de désactiver le renvoi à la ligne, en fonction de l’entier de base zéro d’un jeu de coordonnées de texture (plutôt que d’utiliser explicitement l’une des \_ valeurs d’État n de retour de D3DRS). Ajoutez la \_ valeur WRAPBIAS D3DRENDERSTATE à l’index de base zéro d’un jeu de coordonnées de texture pour calculer la \_ valeur n Wrap D3DRS correspondant à cet index, comme indiqué dans l’exemple suivant.


```
// Enable U/V wrapping for textures that use the texture 
// coordinate set at the index within the dwIndex variable
    
HRESULT hr = pd3dDevice->SetRenderState(
dwIndex + D3DRENDERSTATE_WRAPBIAS,  
D3DWRAPCOORD_0 | D3DWRAPCOORD_1);
     
// If dwIndex is 3, the value that results from 
// the addition equals D3DRS_WRAP3 (131)
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrenderstate)
</dt> <dt>

[**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)
</dt> </dl>

 

 
