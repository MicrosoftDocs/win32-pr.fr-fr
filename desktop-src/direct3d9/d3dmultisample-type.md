---
description: Définit les niveaux d’échantillonnage multiple de la scène complète que l’appareil peut appliquer.
ms.assetid: 1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8
title: Énumération D3DMULTISAMPLE_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMULTISAMPLE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: da8f9c1c8bb3aa74c0ab22a5cc701e7d835898de
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922643"
---
# <a name="d3dmultisample_type-enumeration"></a>\_Énumération de type D3DMULTISAMPLE

Définit les niveaux d’échantillonnage multiple de la scène complète que l’appareil peut appliquer.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DMULTISAMPLE_TYPE { 
  D3DMULTISAMPLE_NONE          = 0,
  D3DMULTISAMPLE_NONMASKABLE   = 1,
  D3DMULTISAMPLE_2_SAMPLES     = 2,
  D3DMULTISAMPLE_3_SAMPLES     = 3,
  D3DMULTISAMPLE_4_SAMPLES     = 4,
  D3DMULTISAMPLE_5_SAMPLES     = 5,
  D3DMULTISAMPLE_6_SAMPLES     = 6,
  D3DMULTISAMPLE_7_SAMPLES     = 7,
  D3DMULTISAMPLE_8_SAMPLES     = 8,
  D3DMULTISAMPLE_9_SAMPLES     = 9,
  D3DMULTISAMPLE_10_SAMPLES    = 10,
  D3DMULTISAMPLE_11_SAMPLES    = 11,
  D3DMULTISAMPLE_12_SAMPLES    = 12,
  D3DMULTISAMPLE_13_SAMPLES    = 13,
  D3DMULTISAMPLE_14_SAMPLES    = 14,
  D3DMULTISAMPLE_15_SAMPLES    = 15,
  D3DMULTISAMPLE_16_SAMPLES    = 16,
  D3DMULTISAMPLE_FORCE_DWORD   = 0xffffffff
} D3DMULTISAMPLE_TYPE, *LPD3DMULTISAMPLE_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DMULTISAMPLE_NONE"></span><span id="d3dmultisample_none"></span>**D3DMULTISAMPLE \_ aucun**
</dt> <dd>

Aucun niveau d’échantillonnage multiple de la scène complète n’est disponible.

</dd> <dt>

<span id="D3DMULTISAMPLE_NONMASKABLE_"></span><span id="d3dmultisample_nonmaskable_"></span>**D3DMULTISAMPLE non \_ masquable** 
</dt> <dd>

Active la valeur de la qualité d’échantillonnage multiples. Consultez la section Notes.

</dd> <dt>

<span id="D3DMULTISAMPLE_2_SAMPLES"></span><span id="d3dmultisample_2_samples"></span>**\_Exemples D3DMULTISAMPLE 2 \_**
</dt> <dd>

Niveau d’échantillonnage multiple de scène intégrale disponible.

</dd> <dt>

<span id="D3DMULTISAMPLE_3_SAMPLES"></span><span id="d3dmultisample_3_samples"></span>**\_Exemples D3DMULTISAMPLE 3 \_**
</dt> <dd>

Niveau d’échantillonnage multiple de scène intégrale disponible.

</dd> <dt>

<span id="D3DMULTISAMPLE_4_SAMPLES"></span><span id="d3dmultisample_4_samples"></span>**\_Exemples D3DMULTISAMPLE 4 \_**
</dt> <dd>

Niveau d’échantillonnage multiple de scène intégrale disponible.

</dd> <dt>

<span id="D3DMULTISAMPLE_5_SAMPLES"></span><span id="d3dmultisample_5_samples"></span>**\_Exemples D3DMULTISAMPLE 5 \_**
</dt> <dd>

Niveau d’échantillonnage multiple de scène intégrale disponible.

</dd> <dt>

<span id="D3DMULTISAMPLE_6_SAMPLES"></span><span id="d3dmultisample_6_samples"></span>**\_Exemples D3DMULTISAMPLE 6 \_**
</dt> <dd>

Niveau d’échantillonnage multiple de scène intégrale disponible.

</dd> <dt>

<span id="D3DMULTISAMPLE_7_SAMPLES"></span><span id="d3dmultisample_7_samples"></span>**\_Exemples D3DMULTISAMPLE 7 \_**
</dt> <dd>

Niveau d’échantillonnage multiple de scène intégrale disponible.

</dd> <dt>

<span id="D3DMULTISAMPLE_8_SAMPLES"></span><span id="d3dmultisample_8_samples"></span>**\_Exemples D3DMULTISAMPLE 8 \_**
</dt> <dd>

Niveau d’échantillonnage multiple de scène intégrale disponible.

</dd> <dt>

<span id="D3DMULTISAMPLE_9_SAMPLES"></span><span id="d3dmultisample_9_samples"></span>**\_Exemples D3DMULTISAMPLE 9 \_**
</dt> <dd>

Niveau d’échantillonnage multiple de scène intégrale disponible.

</dd> <dt>

<span id="D3DMULTISAMPLE_10_SAMPLES"></span><span id="d3dmultisample_10_samples"></span>**\_Exemples D3DMULTISAMPLE 10 \_**
</dt> <dd>

Niveau d’échantillonnage multiple de scène intégrale disponible.

</dd> <dt>

<span id="D3DMULTISAMPLE_11_SAMPLES"></span><span id="d3dmultisample_11_samples"></span>**\_Exemples D3DMULTISAMPLE 11 \_**
</dt> <dd>

Niveau d’échantillonnage multiple de scène intégrale disponible.

</dd> <dt>

<span id="D3DMULTISAMPLE_12_SAMPLES"></span><span id="d3dmultisample_12_samples"></span>**\_Exemples D3DMULTISAMPLE 12 \_**
</dt> <dd>

Niveau d’échantillonnage multiple de scène intégrale disponible.

</dd> <dt>

<span id="D3DMULTISAMPLE_13_SAMPLES"></span><span id="d3dmultisample_13_samples"></span>**\_Exemples D3DMULTISAMPLE 13 \_**
</dt> <dd>

Niveau d’échantillonnage multiple de scène intégrale disponible.

</dd> <dt>

<span id="D3DMULTISAMPLE_14_SAMPLES"></span><span id="d3dmultisample_14_samples"></span>**\_Exemples D3DMULTISAMPLE 14 \_**
</dt> <dd>

Niveau d’échantillonnage multiple de scène intégrale disponible.

</dd> <dt>

<span id="D3DMULTISAMPLE_15_SAMPLES"></span><span id="d3dmultisample_15_samples"></span>**\_Exemples D3DMULTISAMPLE 15 \_**
</dt> <dd>

Niveau d’échantillonnage multiple de scène intégrale disponible.

</dd> <dt>

<span id="D3DMULTISAMPLE_16_SAMPLES"></span><span id="d3dmultisample_16_samples"></span>**\_Exemples D3DMULTISAMPLE 16 \_**
</dt> <dd>

Niveau d’échantillonnage multiple de scène intégrale disponible.

</dd> <dt>

<span id="D3DMULTISAMPLE_FORCE_DWORD"></span><span id="d3dmultisample_force_dword"></span>**D3DMULTISAMPLE \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

En plus de l’activation de l’échantillonnage multiple de scène complète à [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) Time, des États de rendu transforment différents aspects en fonction des niveaux affinés.

L’échantillonnage multiple est valide uniquement sur une chaîne de permutation en cours de création ou de réinitialisation à l’aide de l' \_ effet D3DSWAPEFFECT ignorer l’échange.

La valeur d’anticrénelage sur plusieurs échantillons peut être définie avec les paramètres (ou sous-paramètres) dans les méthodes suivantes.



| Méthode                                                                                             | Paramètres                         | Sous-paramètres                     |
|----------------------------------------------------------------------------------------------------|------------------------------------|------------------------------------|
| [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)           | MultiSampleType et pQualityLevels |                                    |
| [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)                                       | pPresentationParameters            | MultiSampleType et pQualityLevels |
| [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) | pPresentationParameters            | MultiSampleType et pQualityLevels |
| [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) | MultiSampleType et pQualityLevels |                                    |
| [**IDirect3DDevice9::CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)               | MultiSampleType et pQualityLevels |                                    |
| [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)                                         | pPresentationParameters            | MultiSampleType et pQualityLevels |



 

Il n’est pas recommandé de passer d’un type à plusieurs échantillons à un autre pour augmenter la qualité de l’anticrénelage.

D3DMULTISAMPLE \_ None active les effets d’échange autres que l’abandon, le verrouillage, etc.

Si le périphérique d’affichage prend en charge l’échantillonnage multiple masquable (plusieurs exemples pour un format de cible de rendu à plusieurs échantillons et la prise en charge de l’anticrénelage) ou simplement un échantillonnage non masquable (uniquement la prise en charge de l’anticrénelage), le pilote de l’appareil fournit le nombre de niveaux de qualité pour le \_ type d’échantillon multiple non masquable D3DMULTISAMPLE. Les applications qui utilisent simplement plusieurs échantillonnages à des fins d’anticrénelage ont uniquement besoin d’interroger le nombre de niveaux de qualité à plusieurs exemples non masquables que le pilote prend en charge.

Les niveaux de qualité pris en charge par l’appareil peuvent être obtenus à l’aide du paramètre pQualityLevels de [**IDirect3D9 :: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype). Les niveaux de qualité utilisés par l’application sont définis avec le paramètre MultiSampleQuality de [**IDirect3DDevice9 :: CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) et [**IDirect3DDevice9 :: CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget).

Pour plus \_ d’informations sur l’échantillonnage masquable, consultez D3DRS MULTISAMPLEMASK.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**\_Paramètres D3DPRESENT**](d3dpresent-parameters.md)
</dt> <dt>

[**D3DSURFACE \_ desc**](d3dsurface-desc.md)
</dt> </dl>

 

 
