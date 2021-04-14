---
title: Débogage des applications DirectX à distance
description: Vous pouvez utiliser Visual Studio et le kit de développement logiciel (SDK) Windows 8 pour déboguer des applications DirectX à distance.
ms.assetid: CA471465-47C2-4706-B391-C9E6C2CD69D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55548cd282bf643e16f22177e46643c6e283a909
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382812"
---
# <a name="debugging-directx-apps-remotely"></a><span data-ttu-id="83588-103">Débogage des applications DirectX à distance</span><span class="sxs-lookup"><span data-stu-id="83588-103">Debugging DirectX apps remotely</span></span>

<span data-ttu-id="83588-104">Vous pouvez utiliser Visual Studio et le kit de développement logiciel (SDK) Windows 8 pour déboguer des applications DirectX à distance.</span><span class="sxs-lookup"><span data-stu-id="83588-104">You can use Visual Studio and the Windows 8 SDK to debug DirectX apps remotely.</span></span> <span data-ttu-id="83588-105">Le kit de développement logiciel (SDK) Windows 8 fournit un ensemble de composants qui prennent en charge le développement DirectX et fournissent une vérification des erreurs et une validation des paramètres en plus du débogage fourni par Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="83588-105">The Windows 8 SDK provides a set of components that support DirectX development and provide error checking and parameter validation in addition to the debugging that Visual Studio provides.</span></span> <span data-ttu-id="83588-106">Ces composants sont D3D11 \_1SDKLayers.dll, D2D1Debug1.dll et Dxgidebug.dll.</span><span class="sxs-lookup"><span data-stu-id="83588-106">These components are D3D11\_1SDKLayers.dll, D2D1Debug1.dll, and Dxgidebug.dll.</span></span>

<span data-ttu-id="83588-107">Si vous souhaitez effectuer un débogage à distance sur un ordinateur où le kit de développement logiciel (SDK) Windows 8 est installé et que vous souhaitez cette fonctionnalité de débogage supplémentaire, vous devez installer le package de débogage distant approprié à l’architecture sur laquelle vous souhaitez effectuer le débogage.</span><span class="sxs-lookup"><span data-stu-id="83588-107">If you want to debug remotely on a computer without the Windows 8 SDK installed and you want this additional debugging capability, you must install the remote debugging package that is appropriate for the architecture on which you want to debug.</span></span> <span data-ttu-id="83588-108">Les packages Windows Installer dans `C:\Program Files (x86)\Windows Kits\8.0\Remote\<arch>` installent la prise en charge appropriée.</span><span class="sxs-lookup"><span data-stu-id="83588-108">The Windows Installer Packages in `C:\Program Files (x86)\Windows Kits\8.0\Remote\<arch>` install the appropriate support.</span></span>

<span data-ttu-id="83588-109">Pour activer les fonctionnalités de débogage supplémentaires pour les applications Direct2D, utilisez ce code :</span><span class="sxs-lookup"><span data-stu-id="83588-109">To enable the additional debugging capabilities for Direct2D apps, use this code:</span></span>

```cpp
    D2D1_FACTORY_OPTIONS options;
    ZeroMemory(&options, sizeof(D2D1_FACTORY_OPTIONS));

#if defined(_DEBUG)
     // If the project is in a debug build, enable Direct2D debugging via SDK Layers.
    options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;
#endif

    DX::ThrowIfFailed(
        D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            __uuidof(ID2D1Factory1),
            &options,
            &m_d2dFactory
            )
        );         
```

<span data-ttu-id="83588-110">Pour activer les fonctionnalités de débogage supplémentaires pour les applications Direct3D, utilisez ce code :</span><span class="sxs-lookup"><span data-stu-id="83588-110">To enable the additional debugging capabilities for Direct3D apps, use this code:</span></span>

```cpp
    // This flag supports surfaces with a different color channel ordering than the API default.
    // It is recommended usage, and is required for compatibility with Direct2D.
    UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
    ComPtr<IDXGIDevice> dxgiDevice;

#if defined(_DEBUG)
    // If the project is in a debug build, enable debugging via SDK Layers with this flag.
    creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
    DX::ThrowIfFailed(
        D3D11CreateDevice(
            nullptr,                    // specify null to use the default adapter
            D3D_DRIVER_TYPE_HARDWARE,
            0,                          // leave as 0 unless software device
            creationFlags,              // optionally set debug and Direct2D compatibility flags
            featureLevels,              // list of feature levels this app can support
            ARRAYSIZE(featureLevels),   // number of entries in above list
            D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION for modern
            &device,                    // returns the Direct3D device created
            &m_featureLevel,            // returns feature level of device created
            &context                    // returns the device immediate context
            )
        );
```

<span data-ttu-id="83588-111">Pour plus d’informations sur le débogage des applications Direct2D, voir [couche de débogage Direct2D](/windows/desktop/Direct2D/direct2ddebuglayer-portal).</span><span class="sxs-lookup"><span data-stu-id="83588-111">For more info about debugging Direct2D apps, see [Direct2D Debug Layer](/windows/desktop/Direct2D/direct2ddebuglayer-portal).</span></span>

<span data-ttu-id="83588-112">Pour plus d’informations sur le débogage des applications Direct3D, consultez couche de débogage [Direct3D](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers).</span><span class="sxs-lookup"><span data-stu-id="83588-112">For more info about debugging Direct3D apps, see [Direct3D Debug Layer](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers).</span></span>