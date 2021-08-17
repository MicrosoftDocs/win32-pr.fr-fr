---
description: Indicateurs pour les options de création de surface et de ressource.
ms.assetid: b5026566-89b5-458e-b36d-a55e5f8c10c1
title: DXGI_USAGE (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d7bc0773794c6c2243d8a3171cbd6ffdafbe1cdd558e1198c2c8cc0b1a3440d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117909930"
---
# <a name="dxgi_usage"></a>utilisation de DXGI \_

Indicateurs pour les options de création de surface et de ressource.



| Constante/valeur                                                                                                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_USAGE_BACK_BUFFER"></span><span id="dxgi_usage_back_buffer"></span><dl> <dt>**Dxgi \_ \_ \_ Mémoire tampon d’arrière-plan d’utilisation**</dt> <dt>1L <<  (2 + 4)</dt> </dl>                             | La surface ou la ressource est utilisée comme mémoire tampon d’arrière-plan. Vous n’avez pas besoin de transmettre la **\_ \_ \_ mémoire tampon d’arrière-plan d’utilisation dxgi** quand vous créez une chaîne de permutation. Toutefois, vous pouvez déterminer si une ressource appartient à une chaîne de permutation quand vous appelez [**IDXGIResource :: GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) et obtenir une **\_ \_ \_ mémoire tampon d’arrière-plan d’utilisation dxgi**.<br/> |
| <span id="DXGI_USAGE_DISCARD_ON_PRESENT"></span><span id="dxgi_usage_discard_on_present"></span><dl> <dt>**Dxgi \_ UTILISATION \_ ignorée \_ le \_**</dt> <dt> <<  1L présent (5 + 4)</dt> </dl>       | Cet indicateur est destiné à un usage interne uniquement.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="DXGI_USAGE_READ_ONLY"></span><span id="dxgi_usage_read_only"></span><dl> <dt>**Dxgi \_ <<  \_ lecture \_ seule 1L de l’utilisation**</dt> <dt>(4 + 4)</dt> </dl>                                   | Utilisez l’aire ou la ressource pour la lecture uniquement.<br/>                                                                                                                                                                                                                                                                        |
| <span id="DXGI_USAGE_RENDER_TARGET_OUTPUT"></span><span id="dxgi_usage_render_target_output"></span><dl> <dt>**Dxgi \_ \_ \_ \_ Sortie de la cible de rendu de l’utilisation**</dt> <dt>1L <<  (1 + 4)</dt> </dl> | Utilisez la surface ou la ressource en tant que cible de rendu de sortie.<br/>                                                                                                                                                                                                                                                              |
| <span id="DXGI_USAGE_SHADER_INPUT"></span><span id="dxgi_usage_shader_input"></span><dl> <dt>**Dxgi \_ <<  \_ \_ d’entrée du nuanceur d’utilisation**</dt> <dt>1L (0 + 4)</dt> </dl>                          | Utilisez la surface ou la ressource comme entrée d’un nuanceur.<br/>                                                                                                                                                                                                                                                                 |
| <span id="DXGI_USAGE_SHARED"></span><span id="dxgi_usage_shared"></span><dl> <dt>**Dxgi \_ 1L \_ partagé d’utilisation**</dt> <dt> <<  (3 + 4)</dt> </dl>                                             | Partager l’aire ou la ressource.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="DXGI_USAGE_UNORDERED_ACCESS"></span><span id="dxgi_usage_unordered_access"></span><dl> <dt>**Dxgi \_ Utilisation non \_ triée \_ de l’accès**</dt> <dt>1L <<  (6 + 4)</dt> </dl>              | Utilisez l’aire ou la ressource pour un accès non ordonné.<br/>                                                                                                                                                                                                                                                                    |



## <a name="remarks"></a>Remarques

Chaque indicateur est défini comme un entier non signé.

``` syntax
#define DXGI_CPU_ACCESS_NONE    ( 0 )
#define DXGI_CPU_ACCESS_DYNAMIC    ( 1 )
#define DXGI_CPU_ACCESS_READ_WRITE    ( 2 )
#define DXGI_CPU_ACCESS_SCRATCH    ( 3 )
#define DXGI_CPU_ACCESS_FIELD        15
#define DXGI_USAGE_SHADER_INPUT             ( 1L << (0 + 4) )
#define DXGI_USAGE_RENDER_TARGET_OUTPUT     ( 1L << (1 + 4) )
#define DXGI_USAGE_BACK_BUFFER              ( 1L << (2 + 4) )
#define DXGI_USAGE_SHARED                   ( 1L << (3 + 4) )
#define DXGI_USAGE_READ_ONLY                ( 1L << (4 + 4) )
#define DXGI_USAGE_DISCARD_ON_PRESENT       ( 1L << (5 + 4) )
#define DXGI_USAGE_UNORDERED_ACCESS         ( 1L << (6 + 4) )
typedef UINT DXGI_USAGE;
```

Ces options d’indicateur sont utilisées dans un appel à la méthode [**IDXGIFactory :: CreateSwapChain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain), [**IDXGIFactory2 :: CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**IDXGIFactory2 :: CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)ou [**IDXGIFactory2 :: CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) pour décrire les options d’accès à l’utilisation de la surface et de l’UC pour la mémoire tampon d’arrière-plan d’une chaîne de permutation. Vous ne pouvez pas utiliser les valeurs **\_ \_ Shared dxgi Shared**, **dxgi \_ usage \_ ignore \_ on \_ present** et **dxgi \_ usage \_ Read \_ only** comme entrée pour créer une chaîne de permutation. Toutefois, DXGI peut définir **le \_ \_ rejet \_ de l' \_ utilisation de dxgi en présence** et **\_ l’utilisation de dxgi \_ \_ uniquement** pour certaines des mémoires tampons d’arrière-plan de la chaîne de permutation au nom de l’application. Vous pouvez appeler la méthode [**IDXGIResource :: GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) pour récupérer l’utilisation de ces mémoires tampons d’arrière-plan. La chaîne de permutation ne prend en charge que la valeur None de l’accès de l' **\_ UC \_ \_ dxgi** dans la partie du **\_ \_ \_ champ d’accès UC dxgi** de l' **\_ utilisation de dxgi**.

Ces options d’indicateur sont également utilisées par la méthode [**IDXGIDevice :: CreateSurface**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




