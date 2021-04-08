---
description: Comme avec n’importe quelle fonctionnalité, le pilote utilisé par votre application peut ne pas prendre en charge tous les types de mise en mémoire tampon de profondeur.
ms.assetid: 8bf022f6-fd97-43f5-ac19-6a75ddb45f5e
title: Interrogation de la prise en charge des tampons de profondeur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfe7555c1fa0fccddcfcb12ff8bc53f1a0f5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745524"
---
# <a name="querying-for-depth-buffer-support-direct3d-9"></a><span data-ttu-id="3d7a7-103">Interrogation de la prise en charge des tampons de profondeur (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3d7a7-103">Querying for Depth Buffer Support (Direct3D 9)</span></span>

<span data-ttu-id="3d7a7-104">Comme avec n’importe quelle fonctionnalité, le pilote utilisé par votre application peut ne pas prendre en charge tous les types de mise en mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="3d7a7-104">As with any feature, the driver that your application uses might not support all types of depth buffering.</span></span> <span data-ttu-id="3d7a7-105">Vérifiez toujours les capacités du pilote.</span><span class="sxs-lookup"><span data-stu-id="3d7a7-105">Always check the driver's capabilities.</span></span> <span data-ttu-id="3d7a7-106">Bien que la plupart des pilotes prennent en charge la mise en mémoire tampon de profondeur z, tous ne prennent pas en charge la mise en mémoire tampon de profondeur basée sur w.</span><span class="sxs-lookup"><span data-stu-id="3d7a7-106">Although most drivers support z-based depth buffering, not all will support w-based depth buffering.</span></span> <span data-ttu-id="3d7a7-107">Les pilotes n’échouent pas si vous tentez d’activer un schéma non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3d7a7-107">Drivers do not fail if you attempt to enable an unsupported scheme.</span></span> <span data-ttu-id="3d7a7-108">Ils reviennent à une autre méthode de mise en mémoire tampon de profondeur à la place, ou parfois désactivent complètement la mise en mémoire tampon de profondeur, ce qui peut entraîner un rendu des scènes avec des artefacts de tri de profondeur extrême.</span><span class="sxs-lookup"><span data-stu-id="3d7a7-108">They fall back on another depth buffering method instead, or sometimes disable depth buffering altogether, which can result in scenes rendered with extreme depth-sorting artifacts.</span></span>

<span data-ttu-id="3d7a7-109">Vous pouvez vérifier la prise en charge générale des tampons de profondeur en interrogeant Direct3D sur le périphérique d’affichage que votre application utilisera avant de créer un appareil Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3d7a7-109">You can check for general support for depth buffers by querying Direct3D for the display device that your application will use before you create a Direct3D device.</span></span> <span data-ttu-id="3d7a7-110">Si l’objet Direct3D signale qu’il prend en charge la mise en mémoire tampon de profondeur, les périphériques matériels que vous créez à partir de cet objet Direct3D prennent en charge la mise en mémoire tampon z.</span><span class="sxs-lookup"><span data-stu-id="3d7a7-110">If the Direct3D object reports that it supports depth buffering, any hardware devices you create from this Direct3D object will support z-buffering.</span></span>

<span data-ttu-id="3d7a7-111">Pour interroger la prise en charge de la mise en mémoire tampon de profondeur, vous pouvez utiliser la méthode [**IDirect3D9 :: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) , comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="3d7a7-111">To query for depth buffering support, you can use the [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) method, as shown in the following code example.</span></span>


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



<span data-ttu-id="3d7a7-112">[**IDirect3D9 :: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) vous permet de choisir un appareil à créer en fonction des fonctionnalités de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="3d7a7-112">[**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) allows you to choose a device to create based on the capabilities of that device.</span></span> <span data-ttu-id="3d7a7-113">Dans ce cas, les appareils qui ne prennent pas en charge les mémoires tampons de profondeur 16 bits sont rejetés.</span><span class="sxs-lookup"><span data-stu-id="3d7a7-113">In this case, devices that do not support 16-bit depth buffers are rejected.</span></span>

<span data-ttu-id="3d7a7-114">L’utilisation de [**IDirect3D9 :: CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch) pour déterminer la compatibilité du stencil de profondeur avec une cible de rendu est illustrée dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="3d7a7-114">Using [**IDirect3D9::CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch) to determine depth-stencil compatibility with a render target is illustrated in the following code example.</span></span>


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



<span data-ttu-id="3d7a7-115">Lorsque vous savez que le pilote prend en charge les mémoires tampons de profondeur, vous pouvez vérifier la prise en charge de w-buffer.</span><span class="sxs-lookup"><span data-stu-id="3d7a7-115">When you know that the driver supports depth buffers, you can verify w-buffer support.</span></span> <span data-ttu-id="3d7a7-116">Bien que les tampons de profondeur soient pris en charge pour tous les rastériseurs logiciels, les tampons w sont pris en charge uniquement par le rastériseur de référence, ce qui n’est pas adapté à une utilisation par des applications réelles.</span><span class="sxs-lookup"><span data-stu-id="3d7a7-116">Although depth buffers are supported for all software rasterizers, w-buffers are supported only by the reference rasterizer, which is not suited for use by real-world applications.</span></span> <span data-ttu-id="3d7a7-117">Quel que soit le type d’appareil utilisé par votre application, vérifiez la prise en charge de w-buffers avant d’essayer d’activer la mise en mémoire tampon de profondeur w.</span><span class="sxs-lookup"><span data-stu-id="3d7a7-117">Regardless of the type of device your application uses, verify support for w-buffers before you attempt to enable w-based depth buffering.</span></span>

1.  <span data-ttu-id="3d7a7-118">Après avoir créé votre appareil, appelez la méthode [**IDirect3DDevice9 :: GetDeviceCaps**](/windows/desktop/api) , en passant une structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) initialisée.</span><span class="sxs-lookup"><span data-stu-id="3d7a7-118">After creating your device, call the [**IDirect3DDevice9::GetDeviceCaps**](/windows/desktop/api) method, passing an initialized [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span>
2.  <span data-ttu-id="3d7a7-119">Après l’appel, le membre LineCaps contient des informations sur la prise en charge du pilote pour le rendu des primitives.</span><span class="sxs-lookup"><span data-stu-id="3d7a7-119">After the call, the LineCaps member contains information about the driver's support for rendering primitives.</span></span>
3.  <span data-ttu-id="3d7a7-120">Si le membre RasterCaps de cette structure contient l' \_ indicateur D3DPRASTERCAPS WBUFFER, le pilote prend en charge la mise en mémoire tampon de profondeur w pour ce type primitif.</span><span class="sxs-lookup"><span data-stu-id="3d7a7-120">If the RasterCaps member of this structure contains the D3DPRASTERCAPS\_WBUFFER flag, then the driver supports w-based depth buffering for that primitive type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d7a7-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d7a7-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d7a7-122">Mémoires tampons de profondeur</span><span class="sxs-lookup"><span data-stu-id="3d7a7-122">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
