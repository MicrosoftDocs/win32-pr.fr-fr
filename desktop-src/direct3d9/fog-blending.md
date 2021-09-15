---
description: La fusion de brouillard fait référence à l’application du facteur de brouillard au brouillard et aux couleurs d’objet pour produire la couleur finale qui apparaît dans une scène, comme indiqué dans formules de brouillard (Direct3D 9).
ms.assetid: b5b43f12-bbed-4464-aebc-02ad6dab1951
title: Fusion de brouillard (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa918715a7bbe37b200568a0a9098135c5558b0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403365"
---
# <a name="fog-blending-direct3d-9"></a>Fusion de brouillard (Direct3D 9)

La fusion de brouillard fait référence à l’application du facteur de brouillard au brouillard et aux couleurs d’objet pour produire la couleur finale qui apparaît dans une scène, comme indiqué dans [formules de brouillard (Direct3D 9)](fog-formulas.md). L' \_ État de rendu D3DRS FOGENABLE contrôle la fusion de brouillard. Affectez la valeur **true** à cet état de rendu pour activer la fusion de brouillard, comme indiqué dans l’exemple de code suivant. La valeur par défaut est **false**.


```
// For this example, g_pDevice is a valid pointer
// to an IDirect3DDevice9 interface.
HRESULT hr;
hr = g_pDevice->SetRenderState(
                    D3DRS_FOGENABLE,
                    TRUE);
if FAILED(hr)
    return hr;
```



Vous devez activer la fusion de brouillard pour le brouillard de pixel et le brouillard de vertex. Pour plus d’informations sur l’utilisation de ces types de brouillard, consultez [nuance de pixels (Direct3D 9)](pixel-fog.md) et [brouillard de vertex (Direct3D 9)](vertex-fog.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de brouillard](fog-types.md)
</dt> </dl>

 

 



