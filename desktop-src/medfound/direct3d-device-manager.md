---
description: Gestionnaire de périphériques Direct3D
ms.assetid: d82fd82d-510e-4004-b18b-8f2372e29701
title: Gestionnaire de périphériques Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aeff41b790df9537854ab715724d95cee646168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317978"
---
# <a name="direct3d-device-manager"></a><span data-ttu-id="7ed7b-103">Gestionnaire de périphériques Direct3D</span><span class="sxs-lookup"><span data-stu-id="7ed7b-103">Direct3D Device Manager</span></span>

<span data-ttu-id="7ed7b-104">Le gestionnaire de périphériques Microsoft Direct3D permet à deux objets ou plus de partager le même appareil Microsoft Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-104">The Microsoft Direct3D device manager enables two or more objects to share the same Microsoft Direct3D 9 device.</span></span> <span data-ttu-id="7ed7b-105">Un objet agit en tant que propriétaire de l’appareil Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-105">One object acts as the owner of the Direct3D 9 device.</span></span> <span data-ttu-id="7ed7b-106">Pour partager l’appareil, le propriétaire de l’appareil crée le gestionnaire de périphériques Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-106">To share the device, the owner of the device creates the Direct3D device manager.</span></span> <span data-ttu-id="7ed7b-107">D’autres objets peuvent obtenir un pointeur vers le gestionnaire de périphériques à partir du propriétaire de l’appareil, puis utiliser le gestionnaire de périphériques pour obtenir un pointeur vers l’appareil Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-107">Other objects can obtain a pointer to the device manager from the device owner, then use the device manager to get a pointer to the Direct3D device.</span></span> <span data-ttu-id="7ed7b-108">Tout objet qui utilise l’appareil détient un verrou exclusif qui empêche d’autres objets d’utiliser l’appareil en même temps.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-108">Any object that uses the device holds an exclusive lock, which prevents other objects from using the device at the same time.</span></span>

> [!Note]  
> <span data-ttu-id="7ed7b-109">Le Gestionnaire de périphériques Direct3D prend en charge uniquement les périphériques Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-109">The Direct3D Device Manager supports Direct3D 9 devices only.</span></span> <span data-ttu-id="7ed7b-110">Elle ne prend pas en charge les appareils DXGI.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-110">It does not support DXGI devices.</span></span>

 

<span data-ttu-id="7ed7b-111">Pour créer le gestionnaire de périphériques Direct3D, appelez [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span><span class="sxs-lookup"><span data-stu-id="7ed7b-111">To create the Direct3D device manager, call [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span></span> <span data-ttu-id="7ed7b-112">Cette fonction retourne un pointeur vers l’interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) du gestionnaire de périphériques, ainsi qu’un jeton de réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-112">This function returns a pointer to the device manager's [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface, along with a reset token.</span></span> <span data-ttu-id="7ed7b-113">Le jeton de réinitialisation permet au propriétaire de l’appareil Direct3D de définir (et de réinitialiser) l’appareil sur le gestionnaire de périphériques.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-113">The reset token enables the owner of the Direct3D device to set (and reset) the device on the device manager.</span></span> <span data-ttu-id="7ed7b-114">Pour initialiser le gestionnaire de périphériques, appelez [**IDirect3DDeviceManager9 :: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span><span class="sxs-lookup"><span data-stu-id="7ed7b-114">To initialize the device manager, call [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span></span> <span data-ttu-id="7ed7b-115">Transmettez un pointeur vers l’appareil Direct3D, ainsi que le jeton de réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-115">Pass in a pointer to the Direct3D device, along with the reset token.</span></span>

<span data-ttu-id="7ed7b-116">Le code suivant montre comment créer et initialiser le gestionnaire de périphériques.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-116">The following code shows how to create and initialize the device manager.</span></span>


```C++
HRESULT CreateD3DDeviceManager(
    IDirect3DDevice9 *pDevice, 
    UINT *pReset, 
    IDirect3DDeviceManager9 **ppManager
    )
{
    UINT resetToken = 0;

    IDirect3DDeviceManager9 *pD3DManager = NULL;

    HRESULT hr = DXVA2CreateDirect3DDeviceManager9(&resetToken, &pD3DManager);

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pD3DManager->ResetDevice(pDevice, resetToken);

    if (FAILED(hr))
    {
        goto done;
    }

    *ppManager = pD3DManager;
    (*ppManager)->AddRef();

    *pReset = resetToken;


done:
    SafeRelease(&pD3DManager);
    return hr;
}
```



<span data-ttu-id="7ed7b-117">Le propriétaire de l’appareil doit fournir à d’autres objets un moyen d’obtenir un pointeur vers l’interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .</span><span class="sxs-lookup"><span data-stu-id="7ed7b-117">The device owner must provide a way for other objects to get a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span> <span data-ttu-id="7ed7b-118">Le mécanisme standard consiste à implémenter l’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="7ed7b-118">The standard mechanism is to implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span> <span data-ttu-id="7ed7b-119">Le GUID du service est \_ un \_ service d’accélération vidéo \_ .</span><span class="sxs-lookup"><span data-stu-id="7ed7b-119">The service GUID is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>

<span data-ttu-id="7ed7b-120">Pour partager l’appareil entre plusieurs objets, chaque objet (y compris le propriétaire de l’appareil) doit accéder à l’appareil via le gestionnaire de périphériques, comme suit :</span><span class="sxs-lookup"><span data-stu-id="7ed7b-120">To share the device among several objects, each object (including the owner of the device) must access the device through the device manager, as follows:</span></span>

1.  <span data-ttu-id="7ed7b-121">Appelez [**IDirect3DDeviceManager9 :: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) pour obtenir un descripteur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-121">Call [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) to get a handle to the device.</span></span>
2.  <span data-ttu-id="7ed7b-122">Pour utiliser l’appareil, appelez [**IDirect3DDeviceManager9 :: LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) et transmettez le descripteur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-122">To use the device, call [**IDirect3DDeviceManager9::LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) and pass in the device handle.</span></span> <span data-ttu-id="7ed7b-123">La méthode retourne un pointeur vers l’interface **IDirect3DDevice9** .</span><span class="sxs-lookup"><span data-stu-id="7ed7b-123">The method returns a pointer to the **IDirect3DDevice9** interface.</span></span> <span data-ttu-id="7ed7b-124">La méthode peut être appelée en mode blocage ou non bloquant, en fonction de la valeur du paramètre *fBlock* .</span><span class="sxs-lookup"><span data-stu-id="7ed7b-124">The method can be called in a blocking mode or a non-blocking mode, depending on the value of the *fBlock* parameter.</span></span>
3.  <span data-ttu-id="7ed7b-125">Lorsque vous avez terminé d’utiliser l’appareil, appelez [**IDirect3DDeviceManager9 :: UnlockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice).</span><span class="sxs-lookup"><span data-stu-id="7ed7b-125">When you are done using the device, call [**IDirect3DDeviceManager9::UnlockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice).</span></span> <span data-ttu-id="7ed7b-126">Cette méthode met l’appareil à la disposition d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-126">This method makes the device available to other objects.</span></span>
4.  <span data-ttu-id="7ed7b-127">Avant de quitter, appelez [**IDirect3DDeviceManager9 :: CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) pour fermer le handle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-127">Before exiting, call [**IDirect3DDeviceManager9::CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) to close the device handle.</span></span>

<span data-ttu-id="7ed7b-128">Vous devez conserver le verrou de l’appareil uniquement lors de l’utilisation de l’appareil, car le maintien du verrouillage de l’appareil empêche les autres objets d’utiliser l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-128">You should hold the device lock only while using the device, because holding the device lock prevents other objects from using the device.</span></span>

<span data-ttu-id="7ed7b-129">Le propriétaire de l’appareil peut basculer vers un autre appareil à tout moment en appelant [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice), généralement parce que l’appareil d’origine a été perdu.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-129">The owner of the device can switch to another device at any time by calling [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice), typically because the original device was lost.</span></span> <span data-ttu-id="7ed7b-130">Une perte d’appareil peut se produire pour diverses raisons, notamment des modifications dans la résolution du moniteur, des actions de gestion de l’alimentation, le verrouillage et le déverrouillage de l’ordinateur, etc.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-130">Device loss can occur for various reasons, including changes in the monitor resolution, power management actions, locking and unlocking the computer, and so forth.</span></span> <span data-ttu-id="7ed7b-131">Pour plus d’informations, consultez la documentation de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-131">For more information, see the Direct3D documentation.</span></span>

<span data-ttu-id="7ed7b-132">La méthode [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) invalide tous les descripteurs de périphérique qui ont été ouverts précédemment.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-132">The [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) method invalidates any device handles that were opened previously.</span></span> <span data-ttu-id="7ed7b-133">Lorsqu’un descripteur d’appareil n’est pas valide, la méthode [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) retourne **DXVA2 \_ E \_ New \_ Video \_ Device**.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-133">When a device handle is invalid, the [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) method returns **DXVA2\_E\_NEW\_VIDEO\_DEVICE**.</span></span> <span data-ttu-id="7ed7b-134">Si cela se produit, fermez le handle et appelez à nouveau [**OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) pour obtenir un nouveau handle de périphérique, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-134">If this occurs, close the handle and call [**OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) again to obtain a new device handle, as shown in the following code.</span></span>

<span data-ttu-id="7ed7b-135">L’exemple suivant montre comment ouvrir un handle de périphérique et verrouiller l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7ed7b-135">The following example shows how to open a device handle and lock the device.</span></span>


```C++
HRESULT LockDevice(
    IDirect3DDeviceManager9 *pDeviceManager,
    BOOL fBlock,
    IDirect3DDevice9 **ppDevice, // Receives a pointer to the device.
    HANDLE *pHandle              // Receives a device handle.   
    )
{
    *pHandle = NULL;
    *ppDevice = NULL;

    HANDLE hDevice = 0;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);

    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->LockDevice(hDevice, ppDevice, fBlock);
    }

    if (hr == DXVA2_E_NEW_VIDEO_DEVICE)
    {
        // Invalid device handle. Try to open a new device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (SUCCEEDED(hr))
        {
            hr = pDeviceManager->OpenDeviceHandle(&hDevice);
        }

        // Try to lock the device again.
        if (SUCCEEDED(hr))
        {
            hr = pDeviceManager->LockDevice(hDevice, ppDevice, TRUE); 
        }
    }

    if (SUCCEEDED(hr))
    {
        *pHandle = hDevice;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="7ed7b-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7ed7b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ed7b-137">Accélération vidéo DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="7ed7b-137">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 



