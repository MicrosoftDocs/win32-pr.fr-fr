---
description: Windows 8 et Windows Server 2012 introduisent la capacité des logiciels qui s’exécutent sur une machine virtuelle à détecter qu’un événement de décalage horaire s’est produit.
ms.assetid: 0793E46B-8464-425E-8C5B-77C14DA90004
title: Identificateur de génération de l’ordinateur virtuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d810a1a65e95f4dde0ccf9779b1e955f2630623e362ffbf94ab8ca36d51d116e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899009"
---
# <a name="virtual-machine-generation-identifier"></a>Identificateur de génération de l’ordinateur virtuel

Windows 8 et Windows Server 2012 introduisent la capacité des logiciels qui s’exécutent sur une machine virtuelle à détecter qu’un événement de décalage horaire s’est produit. Les événements de décalage temporel peuvent se produire suite à l’application d’un instantané d’ordinateur virtuel ou à la restauration d’une sauvegarde de machine virtuelle. Pour plus d’informations sur cette fonctionnalité, consultez le livre blanc sur l' [ID de génération d’ordinateur virtuel](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx).

## <a name="prerequisites"></a>Prérequis

Pour utiliser l’identificateur de génération d’ordinateur virtuel à partir d’un ordinateur virtuel, votre machine virtuelle doit être conforme aux conditions suivantes.

-   L’ordinateur virtuel doit être en cours d’exécution sur un hyperviseur qui implémente la prise en charge des identificateurs de génération d’ordinateur virtuel. Actuellement, il s’agit des éléments suivants :
    -   Windows 8
    -   Windows Server 2012
    -   Microsoft Hyper-V Server 2012
-   L’ordinateur virtuel doit exécuter un système d’exploitation invité qui prend en charge l’identificateur de génération d’ordinateur virtuel. Actuellement, il s’agit des éléments suivants.

    Les systèmes d’exploitation suivants ont une prise en charge native de l’identificateur de génération d’ordinateur virtuel.

    -   Windows 8
    -   Windows Server 2012
    -   

    le fonctionnement suivant peut être utilisé comme système d’exploitation invité si les services d’intégration Hyper-V de Windows 8 ou Windows Server 2012 sont installés.

    -   Windows Server 2008 R2 avec Service Pack 1 (SP1)
    -   Windows 7 Service Pack 1 (SP1)
    -   Windows Server 2008 avec Service Pack 2 (SP2)
    -   Windows Server 2003 R2
    -   Windows Server 2003 avec Service Pack 2 (SP2)
    -   Windows Vista avec Service Pack 2 (SP2)
    -   Windows XP avec Service Pack 3 (SP3)

## <a name="obtaining-the-virtual-machine-generation-identifier"></a>Obtention de l’identificateur de génération de l’ordinateur virtuel

Pour obtenir par programme l’identificateur de génération d’ordinateur virtuel, procédez comme suit.

> [!Note]  
> Les éléments suivants doivent être exécutés avec des privilèges administrateur ou système pour fonctionner correctement.

 

1.  Incluez le fichier d’en-tête « vmgenerationcounter. h » dans votre application. Le fichier d’en-tête contient les définitions suivantes :
    ```C++
    DEFINE_GUID(
        GUID_DEVINTERFACE_VM_GENCOUNTER,
        0x3ff2c92b, 
        0x6598, 
        0x4e60, 
        0x8e, 
        0x1c, 
        0x0c, 
        0xcf, 
        0x49, 
        0x27, 
        0xe3, 
        0x19);

    #define VM_GENCOUNTER_SYMBOLIC_LINK_NAME L"VmGenerationCounter"

    #define IOCTL_VMGENCOUNTER_READ CTL_CODE( \
        FILE_DEVICE_ACPI, \
        0x1, METHOD_BUFFERED, \
        FILE_READ_ACCESS | FILE_WRITE_ACCESS)

    typedef struct _VM_GENCOUNTER
    {
        ULONGLONG GenerationCount;
        ULONGLONG GenerationCountHigh;
    } VM_GENCOUNTER, *PVM_GENCOUNTER;
    ```

    

2.  Ouvrez un handle vers le \\ \\ . \\ VmGenerationCounter» à l’aide de la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) . Vous pouvez également utiliser le Gestionnaire PnP pour utiliser le GUID d’interface de **périphérique \_ DEVINTERFACE \_ VM \_ GENCOUNTER** ({3ff2c92b-6598-4e60-8e1c-0ccf4927e319}). Ces objets ne seront pas présents si l’application n’est pas exécutée sur une machine virtuelle.
3.  Envoyez l’IOCTL de [**\_ \_ lecture IOCTL VMGENCOUNTER**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) au pilote pour récupérer l’identificateur de génération.

    L’IOCTL de [**\_ \_ lecture VMGENCOUNTER IOCTL**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) fonctionne dans l’un des deux modes, *interrogation* et *piloté par événement*.

    Pour émettre l’IOCTL en mode d’interrogation, vous devez soumettre l’IOCTL avec une mémoire tampon d’entrée de longueur nulle. En réponse à cela, le pilote récupère l’identificateur de génération actuel, l’écrit dans la mémoire tampon de sortie et termine l’IOCTL.

    Pour émettre l’IOCTL en mode piloté par les événements, soumettez l’IOCTL avec une mémoire tampon d’entrée qui contient un identificateur de génération existant. En réponse à cela, le pilote attend que l’identificateur de génération actuel soit différent de l’identificateur de génération passé. Lorsque l’identificateur de génération change, le pilote écrit l’identificateur de génération actuel dans la mémoire tampon de sortie et termine l’IOCTL.

    Dans les deux modes, le format et la longueur de la mémoire tampon de sortie sont dictés par la structure [**\_ GENCOUNTER de la machine virtuelle**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) .

    Le mode d’interrogation est pris en charge sur tous les systèmes d’exploitation invités listés ci-dessus. le mode piloté par les événements est pris en charge uniquement sur Windows Vista avec sp2, Windows Server 2008 avec sp2 et les systèmes d’exploitation ultérieurs. Sur les systèmes d’exploitation antérieurs, l’IOCTL échoue avec l’erreur de code d’erreur **\_ non \_ prise en charge** lorsqu’elle est émise en mode piloté par les événements.

    Il est possible que l’identificateur de génération change entre le moment où il est récupéré par le pilote et le moment où l’IOCTL est terminée. Cela peut entraîner la réception par l’application cliente de données obsolètes. Pour éviter cela, l’application cliente peut utiliser le mode piloté par les événements pour s’assurer qu’elle finira par se familiariser avec les mises à jour de l’identificateur de génération. En prenant l’identificateur actuel de l’application cliente comme entrée, le mode piloté par les événements évite les conditions de concurrence potentielles qui pourraient provoquer l’absence de notifications de l’appelant.

L’exemple de code suivant montre comment effectuer les actions ci-dessus pour obtenir l’identificateur de génération d’ordinateur virtuel.

> [!Note]  
> Le code suivant doit être exécuté avec des privilèges administrateur ou système pour fonctionner correctement.

 


```C++
HRESULT GetVmCounter(bool fWaitForChange)
{
    BOOL success = FALSE;
    DWORD error = ERROR_SUCCESS;
    VM_GENCOUNTER vmCounterOutput = {0};
    DWORD size = 0;
    HANDLE handle = INVALID_HANDLE_VALUE;
    HRESULT hr = S_OK;

    handle = CreateFile(
        L"\\\\.\\" VM_GENCOUNTER_SYMBOLIC_LINK_NAME,
        GENERIC_READ | GENERIC_WRITE,
        FILE_SHARE_READ | FILE_SHARE_WRITE,
        NULL,
        OPEN_EXISTING,
        0,
        NULL);

    if (handle == INVALID_HANDLE_VALUE)
    {
        error = GetLastError();

        wprintf(
            L"Unable to open device %s. Error code = %d.", 
            VM_GENCOUNTER_SYMBOLIC_LINK_NAME, 
            error);

        hr = HRESULT_FROM_WIN32(error);

        goto Cleanup;
    }

    /*
    Call into the driver. 

    Because the 4th parameter to DeviceIoControl (nInBufferSize) is zero, this 
    is a polling request rather than an event-driven request.
    */
    success = DeviceIoControl(
        handle,
        IOCTL_VMGENCOUNTER_READ,
        NULL,
        0,
        &vmCounterOutput,
        sizeof(vmCounterOutput),
        &size,
        NULL);

    if (!success)
    {
        error = GetLastError();

        wprintf(L"Call IOCTL_VMGENCOUNTER_READ failed with %d.", error);

        hr = HRESULT_FROM_WIN32(error);

        goto Cleanup;
    }

    wprintf(
        L"VmCounterValue: %I64x:%I64x",
        vmCounterOutput.GenerationCount,
        vmCounterOutput.GenerationCountHigh);

    if (fWaitForChange)
    {
        /*
        Call into the driver again in event-driven mode. DeviceIoControl won't 
        return until the generation identifier has changed.
        */
        success = DeviceIoControl(
            handle,
            IOCTL_VMGENCOUNTER_READ,
            &vmCounterOutput,
            sizeof(vmCounterOutput),
            &vmCounterOutput,
            sizeof(vmCounterOutput),
            &size,
            NULL);

        if (!success)
        {
            error = GetLastError();

            wprintf(L"Call IOCTL_VMGENCOUNTER_READ failed with %d.", error);

            hr = HRESULT_FROM_WIN32(error);

            goto Cleanup;
        }

        wprintf(
            L"VmCounterValue changed to: %I64x:%I64x",
            vmCounterOutput.GenerationCount,
            vmCounterOutput.GenerationCountHigh);
    }

Cleanup:

    if (handle != INVALID_HANDLE_VALUE)
    {
        CloseHandle(handle);
    }

    return hr;
};
```



## <a name="determining-if-a-time-shift-event-has-occurred"></a>Déterminer si un événement de décalage horaire s’est produit

Une fois que vous avez obtenu l’identificateur de génération de l’ordinateur virtuel, vous devez le stocker pour une utilisation ultérieure. Avant que votre application effectue une opération qui respecte le temps, telle que la validation dans une base de données, vous devez récupérer l’identificateur de génération et le comparer à la valeur stockée. Si l’identificateur a changé, cela signifie qu’un événement de décalage horaire s’est produit et que votre application doit agir de manière appropriée.

 

 
