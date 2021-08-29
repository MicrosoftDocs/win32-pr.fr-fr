---
description: Cette section contient des informations sur les fonctions fournies par DXGI.
ms.assetid: 209d2e65-b118-47a7-aece-fb140fdede3f
title: DXGI, fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881151c2225d58f583c466b799f15002bc9a23a83f56d878c76088a85f500f57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745679"
---
# <a name="dxgi-functions"></a>DXGI, fonctions

Cette section contient des informations sur les fonctions fournies par DXGI.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDXGIFactory**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory)<br/>                               | Crée une fabrique DXGI 1,0 que vous pouvez utiliser pour générer d’autres objets DXGI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1)<br/>                             | Crée une fabrique DXGI 1,1 que vous pouvez utiliser pour générer d’autres objets DXGI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2)<br/>                             | Crée une fabrique DXGI 1,3 que vous pouvez utiliser pour générer d’autres objets DXGI.<br/> dans Windows 8, toute fabrique DXGI créée pendant que DXGIDebug.dll était présente sur le système le chargerait et l’utiliserait. à partir de Windows 8.1, les applications demandent explicitement que DXGIDebug.dll être chargé à la place. Utilisez [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) et spécifiez l' \_ \_ \_ indicateur de débogage dxgi create Factory pour demander DXGIDebug.dll ; la dll sera chargée si elle est présente sur le système.<br/> |
| [**DXGIDeclareAdapterRemovalSupport**](/windows/desktop/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport)<br/> | Permet à un processus d’indiquer qu’il est résilient à l’un de ses appareils graphiques en cours de suppression.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**DXGIGetDebugInterface**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)<br/>                       | Récupère une interface de débogage.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**DXGIGetDebugInterface1**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1)<br/>                     | récupère une interface que Windows applications du windows Store utilisent pour déboguer l’Infrastructure Microsoft DirectX graphics (DXGI).<br/>                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence DXGI](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

 




