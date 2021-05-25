---
description: Décrit les paramètres de présentation.
ms.assetid: d677aeb7-a188-4ddc-b8c9-48e13676e9c8
title: Structure D3DPRESENT_PARAMETERS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENT_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f113b3df247765b958dfe47bb04fafb6c9a13bbe
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343104"
---
# <a name="d3dpresent_parameters-structure"></a>D3DPRESENT, \_ structure de paramètres

Décrit les paramètres de présentation.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct D3DPRESENT_PARAMETERS {
  UINT                BackBufferWidth;
  UINT                BackBufferHeight;
  D3DFORMAT           BackBufferFormat;
  UINT                BackBufferCount;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  D3DSWAPEFFECT       SwapEffect;
  HWND                hDeviceWindow;
  BOOL                Windowed;
  BOOL                EnableAutoDepthStencil;
  D3DFORMAT           AutoDepthStencilFormat;
  DWORD               Flags;
  UINT                FullScreen_RefreshRateInHz;
  UINT                PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```



## <a name="members"></a>Membres

<dl> <dt>

**BackBufferWidth**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Largeur des mémoires tampons d’arrière-plan de la nouvelle chaîne d’échange, en pixels. Si **Windowed** a la valeur **false** (la présentation est pleine d’écran), cette valeur doit être égale à la largeur de l’un des modes d’affichage énumérés trouvés par le biais de [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes). Si **Windowed** a la **valeur true** et que **BackBufferWidth** ou **BackBufferHeight** est égal à zéro, la dimension correspondante de la zone cliente de **HDeviceWindow** (ou la fenêtre de focus, si **hDeviceWindow** est **null**) est prise.

</dd> <dt>

**BackBufferHeight**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Hauteur des mémoires tampons d’arrière-plan de la nouvelle chaîne d’échange, en pixels. Si **Windowed** a la valeur **false** (la présentation est pleine d’écran), cette valeur doit être égale à la hauteur de l’un des modes d’affichage énumérés trouvés par le biais de [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes). Si **Windowed** a la **valeur true** et que **BackBufferWidth** ou **BackBufferHeight** est égal à zéro, la dimension correspondante de la zone cliente de **HDeviceWindow** (ou la fenêtre de focus, si **hDeviceWindow** est **null**) est prise.

</dd> <dt>

**BackBufferFormat**
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Format de la mémoire tampon d’arrière-plan. Pour plus d’informations sur les formats, consultez [D3DFORMAT](d3dformat.md). Cette valeur doit être l’un des formats de cible de rendu tels qu’ils sont validés par [**CheckDeviceType**](/windows/desktop/api). Vous pouvez utiliser [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) pour obtenir le format actuel.

En fait, D3DFMT \_ Unknown peut être spécifié pour **backBufferFormat** en mode fenêtre. Cela indique au runtime d’utiliser le format de mode d’affichage actuel et d’éliminer la nécessité d’appeler [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).

Pour les applications Windows, le format de mémoire tampon d’arrière-plan n’a plus besoin de correspondre au format de mode d’affichage, car la conversion de couleur peut désormais être effectuée par le matériel (si le matériel prend en charge la conversion de couleur). L’ensemble de formats de mémoire tampon d’arrière-plan possibles est restreint, mais le runtime permet de présenter tout format de mémoire tampon d’arrière-plan valide à n’importe quel format de bureau. (Il existe une condition supplémentaire que l’appareil soit utilisable dans le Bureau ; les appareils ne fonctionnent généralement pas dans les modes 8 bits par pixel.)

Les applications plein écran ne peuvent pas effectuer de conversion de couleurs.

</dd> <dt>

**BackBufferCount**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Cette valeur peut être comprise entre 0 et [D3DPRESENT \_ \_ tampons \_ ](d3dpresent-back-buffers.md) d’arrière-plan Max (ou [D3DPRESENT des \_ \_ mémoires tampons d’arrière-plan \_ Max \_ ](d3dpresent-back-buffers.md) , par exemple lors de l’utilisation de Direct3D 9Ex). Les valeurs de 0 sont traitées comme 1. Si le nombre de mémoires tampons d’arrière-plan ne peut pas être créé, le runtime échouera à l’appel de la méthode et remplira cette valeur avec le nombre de mémoires tampons d’arrière-plan qui pourraient être créées. Par conséquent, une application peut appeler la méthode deux fois avec la même \_ structure de paramètres D3DPRESENT et s’attendre à ce qu’elle fonctionne la deuxième fois.

La méthode échoue si une mémoire tampon d’arrière-plan ne peut pas être créée. La valeur de **BackBufferCount** influence le jeu d’effets de permutation autorisés. Plus précisément, tous les \_ effets d’échange de copie D3DSWAPEFFECT nécessitent une seule mémoire tampon d’arrière-plan.

</dd> <dt>

**MultiSampleType**
</dt> <dd>

Type : **[ **D3DMULTISAMPLE \_**](./d3dmultisample-type.md)**

</dd> <dd>

Membre du type énuméré de [**\_ type D3DMULTISAMPLE**](./d3dmultisample-type.md) . La valeur doit être D3DMULTISAMPLE \_ None, sauf si **SwapEffect** a été défini sur D3DSWAPEFFECT \_ Discard. L’échantillonnage multiple est pris en charge uniquement si l’effet d’échange est D3DSWAPEFFECT \_ ignore.

</dd> <dt>

**MultiSampleQuality**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Niveau de qualité. La plage valide est comprise entre zéro et un de moins que le niveau retourné par pQualityLevels utilisé par [**CheckDeviceMultiSampleType**](/windows/desktop/api). La transmission d’une valeur supérieure retourne l’erreur D3DERR \_ INVALIDCALL. Les valeurs jumelées des cibles de rendu ou des surfaces du stencil de profondeur et du [**\_ type de D3DMULTISAMPLE**](./d3dmultisample-type.md) doivent correspondre.

</dd> <dt>

**SwapEffect**
</dt> <dd>

Type : **[ **D3DSWAPEFFECT**](./d3dswapeffect.md)**

</dd> <dd>

Membre du type énuméré [**D3DSWAPEFFECT**](./d3dswapeffect.md) . Le runtime garantit la sémantique implicite concernant le comportement de l’échange de mémoire tampon ; par conséquent, si **Windowed** a la **valeur true** et que **SwapEffect** a la valeur D3DSWAPEFFECT \_ Flip, le runtime crée une mémoire tampon d’arrière-plan supplémentaire et copie celle qui devient la mémoire tampon d’arrière-plan au moment de la présentation.

D3DSWAPEFFECT \_ Copy requiert que **BackBufferCount** soit défini sur 1.

D3DSWAPEFFECT \_ Discard sera appliqué dans le runtime de débogage en remplissant toute mémoire tampon avec un bruit après sa présentation.

Différences entre Direct3D9 et Direct3D9Ex :

- Dans Direct3D9Ex, D3DSWAPEFFECT \_ FLIPEX est ajouté pour désigner le moment où une application adopte le mode Flip. Autrement dit, Whan le frame d’une application est passé en mode de fenêtre (au lieu d’être copié) au Gestionnaire de fenêtrage (DWM) pour la composition. Le mode Flip fournit une bande passante de mémoire plus efficace et permet à une application de tirer parti des statistiques de présentation plein écran. Elle ne modifie pas le comportement plein écran. Le comportement en mode Flip est disponible à partir de Windows 7.



 

</dd> <dt>

**hDeviceWindow**
</dt> <dd>

Type : **[ **HWND**](../winprog/windows-data-types.md)**

</dd> <dd>

La fenêtre de l’appareil détermine l’emplacement et la taille de la mémoire tampon d’arrière-plan sur l’écran. Utilisé par Direct3D lorsque le contenu de la mémoire tampon d’arrière-plan est copié dans le tampon d’avant pendant la [**présente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).

-   Pour une application en plein écran, il s’agit d’un handle vers la fenêtre supérieure (qui est la fenêtre de focus).

    Pour les applications qui utilisent plusieurs appareils plein écran (par exemple, un système multimoniteur), un seul périphérique peut utiliser la fenêtre de focus comme fenêtre d’appareil. Tous les autres appareils doivent avoir des fenêtres d’appareil uniques.

-   Pour une application en mode fenêtre, ce descripteur est la fenêtre cible par défaut pour le [**présent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present). Si ce handle est **null**, la fenêtre de focus est prise.

Notez qu’aucune tentative n’est effectuée par le runtime pour refléter les modifications apportées par l’utilisateur dans la taille de la fenêtre. La mémoire tampon d’arrière-plan n’est pas réinitialisée implicitement lorsque cette fenêtre est réinitialisée. Toutefois, la méthode [**présente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) effectue automatiquement le suivi des modifications de position de la fenêtre.

</dd> <dt>

**Fenêtrées**
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

**True** si l’application s’exécute sous la fenêtre ; **False** si l’application s’exécute en mode plein écran.

</dd> <dt>

**EnableAutoDepthStencil**
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Si cette valeur est **true**, Direct3D gère les tampons de profondeur pour l’application. L’appareil crée une mémoire tampon de stencil de profondeur lors de sa création. La mémoire tampon du stencil de profondeur est définie automatiquement en tant que cible de rendu de l’appareil. Lorsque l’appareil est réinitialisé, la mémoire tampon du stencil de profondeur est automatiquement détruite et recréée dans la nouvelle taille.

Si EnableAutoDepthStencil a la **valeur true**, AutoDepthStencilFormat doit être un format de stencil de profondeur valide.

</dd> <dt>

**AutoDepthStencilFormat**
</dt> <dd>

Type : **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Membre du type énuméré [D3DFORMAT](d3dformat.md) . Format de la surface de stencil de profondeur automatique que l’appareil va créer. Ce membre est ignoré, sauf si **EnableAutoDepthStencil** a la **valeur true**.

</dd> <dt>

**Indicateurs**
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Une des constantes [D3DPRESENTFLAG](d3dpresentflag.md) .

</dd> <dt>

**RefreshRateInHz plein écran \_**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Vitesse à laquelle la carte d’affichage actualise l’écran. La valeur dépend du mode dans lequel l’application s’exécute :

-   Pour le mode fenêtre, la fréquence d’actualisation doit être 0.
-   Pour le mode plein écran, la fréquence d’actualisation est l’un des taux d’actualisation retournés par [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).

</dd> <dt>

**PresentationInterval**
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Vitesse maximale à laquelle les mémoires tampons d’arrière-plan de la chaîne de permutation peuvent être présentées au tampon d’avant. Pour obtenir une explication détaillée des modes et des intervalles pris en charge, consultez [D3DPRESENT](d3dpresent.md).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[**CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain)
</dt> <dt>

[**Trouver**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
</dt> <dt>

[**Réinitialiser**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
</dt> </dl>

 

 
