---
description: Définit les effets d’échange.
ms.assetid: 522a5f71-3ad9-4cfc-a899-e25b9b721b1b
title: Énumération D3DSWAPEFFECT (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSWAPEFFECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 58354e35ca8456f6fde57d2f2567a6b6a202f6d7
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343034"
---
# <a name="d3dswapeffect-enumeration"></a>Énumération D3DSWAPEFFECT

Définit les effets d’échange.

## <a name="syntax"></a>Syntaxe

```cpp
typedef enum D3DSWAPEFFECT { 
  D3DSWAPEFFECT_DISCARD      = 1,
  D3DSWAPEFFECT_FLIP         = 2,
  D3DSWAPEFFECT_COPY         = 3,
  D3DSWAPEFFECT_OVERLAY      = 4,
  D3DSWAPEFFECT_FLIPEX       = 5,
  D3DSWAPEFFECT_FORCE_DWORD  = 0xFFFFFFFF
} D3DSWAPEFFECT, *LPD3DSWAPEFFECT;
```

## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSWAPEFFECT_DISCARD"></span><span id="d3dswapeffect_discard"></span>**D3DSWAPEFFECT \_ Ignorer**
</dt> <dd>

Lorsqu’une chaîne de permutation est créée avec un effet d’échange de D3DSWAPEFFECT \_ Flip ou D3DSWAPEFFECT \_ Copy, le runtime garantit qu’une opération [**IDirect3DDevice9 ::P renvoyée**](/windows/desktop/api) n’affectera pas le contenu de l’une des mémoires tampons d’arrière-plan. Malheureusement, la satisfaction de cette garantie peut impliquer une mémoire vidéo importante ou des frais de traitement importants, en particulier lors de l’implémentation de la sémantique de basculement pour une chaîne de permutation à fenêtres ou une sémantique de copie pour une chaîne de permutation plein écran. Une application peut utiliser l' \_ effet d’échange D3DSWAPEFFECT pour éviter ces frais généraux et permettre au pilote d’affichage de sélectionner la technique de présentation la plus efficace pour la chaîne de permutation. Il s’agit également du seul effet d’échange qui peut être utilisé lors de la spécification d’une valeur autre que D3DMULTISAMPLE \_ None pour le membre MultiSampleType des [**\_ paramètres D3DPRESENT**](d3dpresent-parameters.md).

À l’instar d’une chaîne de permutation qui utilise D3DSWAPEFFECT \_ Flip, une chaîne de permutation qui utilise D3DSWAPEFFECT \_ Discard peut inclure plusieurs mémoires tampons d’arrière-plan, qui sont accessibles à l’aide de [**IDirect3DDevice9 :: GetBackBuffer**](/windows/desktop/api) ou [**IDirect3DSwapChain9 :: GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer). La chaîne de permutation est surtout envisagée comme une file d’attente dans laquelle 0 indexe toujours la mémoire tampon d’arrière-plan qui sera affichée par l’opération suivante et à partir de laquelle les tampons sont ignorés lorsqu’ils ont été affichés.

Une application qui utilise cet effet d’échange ne peut pas faire d’hypothèses sur le contenu d’une mémoire tampon d’arrière-plan ignorée et doit donc mettre à jour l’intégralité d’une mémoire tampon d’arrière-plan avant d’appeler une opération de présentation qui l’afficherait. Bien que cela ne soit pas appliqué, la version Debug du runtime remplace le contenu des mémoires tampons d’arrière-plan ignorées par des données aléatoires pour permettre aux développeurs de vérifier que leurs applications mettent correctement à jour les surfaces de la mémoire tampon d’arrière-plan.

</dd> <dt>

<span id="D3DSWAPEFFECT_FLIP"></span><span id="d3dswapeffect_flip"></span>**D3DSWAPEFFECT \_ Flip**
</dt> <dd>

La chaîne de permutation peut inclure plusieurs mémoires tampons d’arrière-plan et est surtout considérée comme une file d’attente circulaire qui inclut la mémoire tampon d’avant. Dans cette file d’attente, les mémoires tampons d’arrière-plan sont toujours numérotées de manière séquentielle de 0 à (n-1), où n est le nombre de mémoires tampons d’arrière-plan, de sorte que 0 désigne la mémoire tampon présentée le moins récemment. Quand elle est appelée, la file d’attente est « pivotée » afin que la mémoire tampon d’arrière-plan devienne la mémoire tampon d’arrière-plan (n-1), tandis que la mémoire tampon d’arrière-plan 0 devient la nouvelle mémoire tampon d’arrière-plan.

</dd> <dt>

<span id="D3DSWAPEFFECT_COPY"></span><span id="d3dswapeffect_copy"></span>**\_Copie D3DSWAPEFFECT**
</dt> <dd>

Cet effet d’échange ne peut être spécifié que pour une chaîne de permutation comprenant une seule mémoire tampon d’arrière-plan. Que la chaîne d’échange soit de type fenêtre ou plein écran, le runtime garantit la sémantique impliquée par une opération présente de copie, à savoir que l’opération laisse le contenu de la mémoire tampon d’arrière-plan inchangé, au lieu de la remplacer par le contenu de la mémoire tampon d’arrière-plan en tant qu’opération présente à base de basculement.

Pour une chaîne d’échange plein écran, le runtime utilise une combinaison d’opérations de basculement et de copie, prise en charge si nécessaire par les mémoires tampons d’arrière-plan masquées, pour accomplir l’opération actuelle. En conséquence, la présentation est synchronisée avec le retraçage vertical de la carte d’affichage et son taux est imposé par l’intervalle de présentation choisi. Une chaîne de permutation spécifiée avec \_ l' \_ indicateur D3DPRESENT intervalle immédiat est la seule exception. (Reportez-vous à la description du membre **PresentationIntervals** de la structure de [**\_ paramètres D3DPRESENT**](d3dpresent-parameters.md) .) Dans ce cas, une opération de présentation copie le contenu de la mémoire tampon d’arrière-plan directement dans le tampon d’avant sans attendre le retraçage vertical.

</dd> <dt>

<span id="D3DSWAPEFFECT_OVERLAY"></span><span id="d3dswapeffect_overlay"></span>**Superposition D3DSWAPEFFECT \_**
</dt> <dd>

Utilisez une zone dédiée de la mémoire vidéo qui peut être superposée sur la surface principale. Aucune copie n’est effectuée lorsque la superposition est affichée. L’opération de superposition est effectuée dans le matériel, sans modification des données dans la surface principale.

Différences entre Direct3D 9 et Direct3D 9Ex :

- La \_ superposition D3DSWAPEFFECT est disponible uniquement dans les Direct3D9Ex qui s’exécutent sur Windows 7 (ou plus le système d’exploitation actuel).

</dd> <dt>

<span id="D3DSWAPEFFECT_FLIPEX"></span><span id="d3dswapeffect_flipex"></span>**D3DSWAPEFFECT \_ FLIPEX**
</dt> <dd>

Désigne le moment où une application adopte le mode Flip, pendant lequel le frame d’une application est passé au lieu d’être copié dans le Gestionnaire de fenêtrage (DWM) pour la composition lorsque l’application est présente en mode fenêtre. Le mode de basculement permet à une application d’utiliser plus efficacement la bande passante de mémoire et de permettre à une application de tirer parti des statistiques complètes en plein écran. Le mode Flip n’affecte pas le comportement plein écran.

> [!Note]  
> Si vous créez une chaîne de permutation avec D3DSWAPEFFECT \_ FLIPEX, vous ne pouvez pas remplacer le membre **hDeviceWindow** de la structure de [**\_ paramètres D3DPRESENT**](d3dpresent-parameters.md) lorsque vous présentez un nouveau Frame à afficher. Autrement dit, vous devez passer **null** au paramètre *hDestWindowOverride* de [**IDirect3DDevice9Ex ::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) pour indiquer au runtime d’utiliser le membre **hDeviceWindow** des **\_ paramètres D3DPRESENT** pour la présentation.

Différences entre Direct3D 9 et Direct3D 9Ex :

- D3DSWAPEFFECT \_ FLIPEX est disponible uniquement dans Direct3D9Ex qui s’exécute sur Windows 7 (ou plus le système d’exploitation actuel).

</dd> <dt>

<span id="D3DSWAPEFFECT_FORCE_DWORD"></span><span id="d3dswapeffect_force_dword"></span>**D3DSWAPEFFECT \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’état de la mémoire tampon d’arrière-plan après un appel à present est bien défini par chacun de ces effets de permutation, et indique si le périphérique Direct3D a été créé avec une chaîne d’échange plein écran ou si une chaîne de permutation à fenêtres n’a aucun effet sur cet État. En particulier, l' \_ effet de basculement D3DSWAPEFFECT bascule fonctionne de la même façon qu’il s’agisse d’une fenêtre ou d’un plein écran, et le runtime Direct3D garantit cela en créant des mémoires tampons supplémentaires. Par conséquent, il est recommandé que les applications utilisent D3DSWAPEFFECT \_ Discard dans la mesure du possible pour éviter de telles pénalités. Cela est dû au fait que cet effet d’échange sera toujours le plus efficace en termes de consommation de mémoire et de performances.

Les applications qui utilisent D3DSWAPEFFECT \_ Flip ou D3DSWAPEFFECT \_ Discard ne doivent pas s’attendre à ce que l’alpha de destination plein écran fonctionne. Cela signifie que l' \_ État de rendu D3DRS DESTBLEND ne fonctionnera pas comme prévu, car les chaînes de permutation à l’écran complet avec ces effets de permutation n’ont pas de format de pixel explicite du point de vue du pilote. Le pilote déduit qu’il doit prendre le format d’affichage, qui n’a pas de canal alpha. Pour contourner ce processus, procédez comme suit :

-   Utilisez la \_ copie D3DSWAPEFFECT.
-   Vérifiez l' \_ \_ \_ \_ indicateur Flip ou ignore D3DCAPS3 alpha fullscreen \_ dans le membre Caps3 de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) . Cet indicateur indique si le pilote peut effectuer une fusion alpha quand D3DSWAPEFFECT \_ Flip ou D3DSWAPEFFECT \_ Discard est utilisé.
-   Les applications utilisant l’effet de permutation en mode Flip (D3DSWAPEFFECT \_ FLIPEX) doivent appeler [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) après un changement de taille ou de région de fenêtre pour s’assurer que le contenu d’affichage est mis à jour.

Une fenêtre invisible ne peut pas recevoir d’événements en mode utilisateur ; en outre, une fenêtre en plein écran invisible interfère avec la présentation d’une fenêtre en mode fenêtre de l’autre application. Par conséquent, chaque application doit s’assurer qu’une fenêtre d’appareil est visible lorsqu’un utilise permutation est présenté en mode plein écran.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |

## <a name="see-also"></a>Voir aussi

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)

[**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
