---
description: Comme avec n’importe quelle fonctionnalité, le pilote utilisé par votre application peut ne pas prendre en charge tous les types de mise en mémoire tampon de profondeur.
ms.assetid: 8bf022f6-fd97-43f5-ac19-6a75ddb45f5e
title: Interrogation de la prise en charge des tampons de profondeur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1050edc61e5359cca0ac9c2990d35f27c8c8db6b193d219f928ac336e99d760
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118579"
---
# <a name="querying-for-depth-buffer-support-direct3d-9"></a>Interrogation de la prise en charge des tampons de profondeur (Direct3D 9)

Comme avec n’importe quelle fonctionnalité, le pilote utilisé par votre application peut ne pas prendre en charge tous les types de mise en mémoire tampon de profondeur. Vérifiez toujours les capacités du pilote. Bien que la plupart des pilotes prennent en charge la mise en mémoire tampon de profondeur z, tous ne prennent pas en charge la mise en mémoire tampon de profondeur basée sur w. Les pilotes n’échouent pas si vous tentez d’activer un schéma non pris en charge. Ils reviennent à une autre méthode de mise en mémoire tampon de profondeur à la place, ou parfois désactivent complètement la mise en mémoire tampon de profondeur, ce qui peut entraîner un rendu des scènes avec des artefacts de tri de profondeur extrême.

Vous pouvez vérifier la prise en charge générale des tampons de profondeur en interrogeant Direct3D sur le périphérique d’affichage que votre application utilisera avant de créer un appareil Direct3D. Si l’objet Direct3D signale qu’il prend en charge la mise en mémoire tampon de profondeur, les périphériques matériels que vous créez à partir de cet objet Direct3D prennent en charge la mise en mémoire tampon z.

Pour interroger la prise en charge de la mise en mémoire tampon de profondeur, vous pouvez utiliser la méthode [**IDirect3D9 :: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) , comme indiqué dans l’exemple de code suivant.


```
// The following example assumes that pCaps is a valid pointer to an 
// initialized D3DCAPS9 structure
if(FAILED(m_pD3D->CheckDeviceFormat(pCaps->AdapterOrdinal, 
                                    pCaps->DeviceType, 
                                    AdapterFormat, 
                                    D3DUSAGE_DEPTHSTENCIL, 
                                    D3DRTYPE_SURFACE,
                                    D3DFMT_D16)))
    return E_FAIL;
```



[**IDirect3D9 :: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) vous permet de choisir un appareil à créer en fonction des fonctionnalités de cet appareil. Dans ce cas, les appareils qui ne prennent pas en charge les mémoires tampons de profondeur 16 bits sont rejetés.

L’utilisation de [**IDirect3D9 :: CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch) pour déterminer la compatibilité du stencil de profondeur avec une cible de rendu est illustrée dans l’exemple de code suivant.


```
// Reject devices that cannot create a render target of RTFormat while
// the back buffer is of RTFormat and the depth-stencil buffer is
// at least 8 bits of stencil
if(FAILED(m_pD3D->CheckDepthStencilMatch(pCaps->AdapterOrdinal,
                                        pCaps->DeviceType, 
                                        AdapterFormat, 
                                        RTFormat, 
                                        D3DFMT_D24S8)))
    return E_FAIL;
```



Lorsque vous savez que le pilote prend en charge les mémoires tampons de profondeur, vous pouvez vérifier la prise en charge de w-buffer. Bien que les tampons de profondeur soient pris en charge pour tous les rastériseurs logiciels, les tampons w sont pris en charge uniquement par le rastériseur de référence, ce qui n’est pas adapté à une utilisation par des applications réelles. Quel que soit le type d’appareil utilisé par votre application, vérifiez la prise en charge de w-buffers avant d’essayer d’activer la mise en mémoire tampon de profondeur w.

1.  Après avoir créé votre appareil, appelez la méthode [**IDirect3DDevice9 :: GetDeviceCaps**](/windows/desktop/api) , en passant une structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) initialisée.
2.  Après l’appel, le membre LineCaps contient des informations sur la prise en charge du pilote pour le rendu des primitives.
3.  Si le membre RasterCaps de cette structure contient l' \_ indicateur D3DPRASTERCAPS WBUFFER, le pilote prend en charge la mise en mémoire tampon de profondeur w pour ce type primitif.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons de profondeur](depth-buffers.md)
</dt> </dl>

 

 
