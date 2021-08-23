---
description: Cette rubrique décrit les nouveautés de Microsoft DirectX Graphics infrastructure (DXGI) 1,6 pour les différentes versions de Windows 10.
ms.assetid: C68EC437-7600-43A8-8DEA-5A6AEE75D5AA
title: Améliorations de DXGI 1,6
ms.topic: article
ms.date: 12/04/2019
ms.openlocfilehash: 748878cc041b0987a013608556cd9ec30aaf638e0fcac1ef9386a4675f57ef0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727579"
---
# <a name="dxgi-16-improvements"></a>Améliorations de DXGI 1,6

Cette rubrique décrit les nouveautés de Microsoft DirectX Graphics infrastructure (DXGI) 1,6 pour les différentes versions de Windows 10.

## <a name="windows-10-october-2018-update"></a>Windows 10 avec la mise à jour d’octobre 2018

ces api ont été ajoutées pour Windows 10, version 1809 (10,0 ; Build 17763) &mdash; également connu sous le nom de Mise à jour d’octobre 2018 de Windows 10.

- Interface [**IDXGIFactory7**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory7) et ses méthodes.

## <a name="windows-10-april-2018-update"></a>Mise à jour d’avril 2018 de Windows 10

ces api ont été ajoutées pour Windows 10, version 1803 (10,0 ; Build 17134) &mdash; également connue sous le nom de Windows 10 mise à jour d’avril 2018.

- Énumération [**DXGI_GPU_PREFERENCE**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference) .
- Interface [**IDXGIFactory6**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory6) et ses méthodes.

## <a name="windows-10-fall-creators-update"></a>Windows 10 Fall Creators Update

pour Windows 10, version 1709 (10,0 ; la Build 16299) &mdash; est également connue sous le nom de Windows 10 Fall Creators Update &mdash; ces constantes ont été ajoutées à l’énumération [**DXGI_ADAPTER_FLAG3**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3) . 

- **DXGI_ADAPTER_FLAG3_SUPPORT_MONITORED_FENCES**
- **DXGI_ADAPTER_FLAG3_SUPPORT_NON_MONITORED_FENCES**
- **DXGI_ADAPTER_FLAG3_KEYED_MUTEX_CONFORMANCE**

## <a name="windows-10-creators-update"></a>Windows 10 Creators Update

pour Windows 10, version 1703 (10,0 ; Build 15063) &mdash; également connu sous le nom de Windows 10 Creators Update &mdash; les fonctionnalités suivantes ont été ajoutées à Microsoft DirectX graphics Infrastructure (DXGI) 1,6 afin de détecter les affichages HDR.

### <a name="high-dynamic-range-hdr-detection"></a>Détection HDR (High dynamique Range)

Ces API ont été ajoutées afin de détecter les affichages HDR.

- Structure [**DXGI_ADAPTER_DESC3**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_adapter_desc3)
- Énumération [**DXGI_ADAPTER_FLAG3**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3)
- Énumération [**DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags)
- Structure [**DXGI_OUTPUT_DESC1**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1)
- [**DXGIDeclareAdapterRemovalSupport**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport) fonction)
- Interface [**IDXGIAdapter4**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgiadapter4) et ses méthodes
- Interface [**IDXGIOutput6**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgioutput6) et ses méthodes

En outre, les constantes ont été ajoutées à l’énumération [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) pour prendre en charge ces API.

## <a name="related-topics"></a>Rubriques connexes
[Guide de programmation pour DXGI](dx-graphics-dxgi-overviews.md)
