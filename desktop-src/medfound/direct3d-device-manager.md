---
description: Gestionnaire de périphériques Direct3D
ms.assetid: d82fd82d-510e-4004-b18b-8f2372e29701
title: Gestionnaire de périphériques Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aeff41b790df9537854ab715724d95cee646168
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525781"
---
# <a name="direct3d-device-manager"></a>Gestionnaire de périphériques Direct3D

Le gestionnaire de périphériques Microsoft Direct3D permet à deux objets ou plus de partager le même appareil Microsoft Direct3D 9. Un objet agit en tant que propriétaire de l’appareil Direct3D 9. Pour partager l’appareil, le propriétaire de l’appareil crée le gestionnaire de périphériques Direct3D. D’autres objets peuvent obtenir un pointeur vers le gestionnaire de périphériques à partir du propriétaire de l’appareil, puis utiliser le gestionnaire de périphériques pour obtenir un pointeur vers l’appareil Direct3D. Tout objet qui utilise l’appareil détient un verrou exclusif qui empêche d’autres objets d’utiliser l’appareil en même temps.

> [!Note]  
> Le Gestionnaire de périphériques Direct3D prend en charge uniquement les périphériques Direct3D 9. Elle ne prend pas en charge les appareils DXGI.

 

Pour créer le gestionnaire de périphériques Direct3D, appelez [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9). Cette fonction retourne un pointeur vers l’interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) du gestionnaire de périphériques, ainsi qu’un jeton de réinitialisation. Le jeton de réinitialisation permet au propriétaire de l’appareil Direct3D de définir (et de réinitialiser) l’appareil sur le gestionnaire de périphériques. Pour initialiser le gestionnaire de périphériques, appelez [**IDirect3DDeviceManager9 :: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice). Transmettez un pointeur vers l’appareil Direct3D, ainsi que le jeton de réinitialisation.

Le code suivant montre comment créer et initialiser le gestionnaire de périphériques.


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



Le propriétaire de l’appareil doit fournir à d’autres objets un moyen d’obtenir un pointeur vers l’interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) . Le mécanisme standard consiste à implémenter l’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) . Le GUID du service est \_ un \_ service d’accélération vidéo \_ .

Pour partager l’appareil entre plusieurs objets, chaque objet (y compris le propriétaire de l’appareil) doit accéder à l’appareil via le gestionnaire de périphériques, comme suit :

1.  Appelez [**IDirect3DDeviceManager9 :: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) pour obtenir un descripteur de l’appareil.
2.  Pour utiliser l’appareil, appelez [**IDirect3DDeviceManager9 :: LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) et transmettez le descripteur de l’appareil. La méthode retourne un pointeur vers l’interface **IDirect3DDevice9** . La méthode peut être appelée en mode blocage ou non bloquant, en fonction de la valeur du paramètre *fBlock* .
3.  Lorsque vous avez terminé d’utiliser l’appareil, appelez [**IDirect3DDeviceManager9 :: UnlockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice). Cette méthode met l’appareil à la disposition d’autres objets.
4.  Avant de quitter, appelez [**IDirect3DDeviceManager9 :: CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) pour fermer le handle de l’appareil.

Vous devez conserver le verrou de l’appareil uniquement lors de l’utilisation de l’appareil, car le maintien du verrouillage de l’appareil empêche les autres objets d’utiliser l’appareil.

Le propriétaire de l’appareil peut basculer vers un autre appareil à tout moment en appelant [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice), généralement parce que l’appareil d’origine a été perdu. Une perte d’appareil peut se produire pour diverses raisons, notamment des modifications dans la résolution du moniteur, des actions de gestion de l’alimentation, le verrouillage et le déverrouillage de l’ordinateur, etc. Pour plus d’informations, consultez la documentation de Direct3D.

La méthode [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) invalide tous les descripteurs de périphérique qui ont été ouverts précédemment. Lorsqu’un descripteur d’appareil n’est pas valide, la méthode [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) retourne **DXVA2 \_ E \_ New \_ Video \_ Device**. Si cela se produit, fermez le handle et appelez à nouveau [**OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) pour obtenir un nouveau handle de périphérique, comme indiqué dans le code suivant.

L’exemple suivant montre comment ouvrir un handle de périphérique et verrouiller l’appareil.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accélération vidéo DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 



