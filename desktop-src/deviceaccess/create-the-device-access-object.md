---
title: Implémenter l’objet d’accès de l’appareil
description: Cette rubrique explique comment instancier l’objet d’accès de l’appareil et l’utiliser pour accéder à un appareil.
ms.assetid: 26619A25-67FE-44DC-82DD-36076326748D
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 9fee82f84a9325472928de69513e5f8e1c3ea1d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521820"
---
# <a name="implement-the-device-access-object"></a>Implémenter l’objet d’accès de l’appareil

Cette rubrique explique comment instancier l’objet d’accès de l’appareil et l’utiliser pour accéder à un appareil. La classe instanciée implémente les interfaces [**IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol) et [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) .

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1

Pour instancier l’objet d’accès de l’appareil, vous devez d’abord appeler la fonction [**CreateDeviceAccessInstance**](/windows/win32/api/deviceaccess/nf-deviceaccess-createdeviceaccessinstance) . Si **CreateDeviceAccessInstance** a abouti, vous pouvez ensuite appeler la méthode [**Wait**](/windows/win32/api/Deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-wait) pour attendre la fin de l’opération asynchrone. Si l' **attente** a échoué, vous pouvez récupérer un objet [**IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol) (ou l’erreur appropriée) à partir de la méthode [**GetResult**](/windows/win32/api/Deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-getresult) .

```C++
HRESULT
CMyServer::Initialize(
        PCWSTR   pszDeviceInterfacePath
    )

/*++
Routine Description:

    This routine is called to initialize the Device Access object.
    It's not part of the constructor as the initialization can fail.
    It opens the device and gets the IDeviceIoControl interface to the device instance
    via the broker.

Arguments:
    pszDeviceInterfacePath - the device interface string that needs to be opened

Return Value:

    HRESULT

--*/

{
    HRESULT hr;
    ICreateDeviceAccessAsync *pDeviceAccess;

     //
     // Here's the actual open call.  This will *fail* if your lowbox does
     // not have the capability mapped to the interface class specified.
     // If you are running this as normal user, it will just pass through to
     // create file.
     //

   hr = CreateDeviceAccessInstance(pszDeviceInterfacePath,
                                   GENERIC_READ|GENERIC_WRITE,
                                   &pDeviceAccess);

    if (FAILED(hr)) {
        return hr;
    }

    if (SUCCEEDED(hr)) {
        hr = pDeviceAccess->Wait(INFINITE);
    }

    if (SUCCEEDED(hr)) {
        hr = pDeviceAccess->GetResult(IID_IDeviceIoControl,
                                            (void **)&m_pDeviceIoControl);
    }

    pDeviceAccess->Release();

    return hr;
}
```



### <a name="step-2"></a>Étape 2

Voici un exemple d’appel à la méthode **DeviceIoControlSync** .


```C++
IFACEMETHODIMP 
CMyServer::put_SevenSegmentDisplay(
    BYTE   value
    )
/*++

Routine Description:
    This routine puts the display value into the device.

Arguments:
    
    value - The value to be written to the device.
    
Return Value:

    HRESULT

--*/
{
    BYTE sevenSegment = 0;
    HRESULT hr;

    if (value >= ARRAYSIZE(g_NumberToMask)) {
        return E_INVALIDARG;
    }


    sevenSegment = g_NumberToMask[value];
    hr = m_pDeviceIoControl->DeviceIoControlSync(
                         IOCTL_OSRUSBFX2_SET_7_SEGMENT_DISPLAY,
                         &sevenSegment,
                         sizeof(BYTE),
                         NULL,
                         0,
                         NULL
                         );

    return hr;
}
```



## <a name="remarks"></a>Notes

Vous pouvez également envoyer un IOCTL de manière asynchrone à l’aide de la méthode [**DeviceIoControlAsync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync) . Dans ce cas, vous devez implémenter l’interface [**IDeviceRequestCompletionCallback**](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback) .

## <a name="related-topics"></a>Rubriques connexes

[exemple d’accès personnalisé aux pilotes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [applications de l’appareil UWP pour les appareils internes](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Centre de développement matériel](/windows-hardware/drivers/)
