---
description: Windows 8 et Windows Server 2012 introduisent la capacité des logiciels qui s’exécutent sur une machine virtuelle à détecter qu’un événement de décalage horaire s’est produit.
ms.assetid: 0793E46B-8464-425E-8C5B-77C14DA90004
title: Identificateur de génération de l’ordinateur virtuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df6ecbb600dbc7ae2efe14d36cb17cc75816444
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521357"
---
# <a name="virtual-machine-generation-identifier"></a><span data-ttu-id="1e414-103">Identificateur de génération de l’ordinateur virtuel</span><span class="sxs-lookup"><span data-stu-id="1e414-103">Virtual machine generation identifier</span></span>

<span data-ttu-id="1e414-104">Windows 8 et Windows Server 2012 introduisent la capacité des logiciels qui s’exécutent sur une machine virtuelle à détecter qu’un événement de décalage horaire s’est produit.</span><span class="sxs-lookup"><span data-stu-id="1e414-104">Windows 8 and Windows Server 2012 introduce the ability for software that is running on a virtual machine to detect that a time shift event may have occurred.</span></span> <span data-ttu-id="1e414-105">Les événements de décalage temporel peuvent se produire suite à l’application d’un instantané d’ordinateur virtuel ou à la restauration d’une sauvegarde de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="1e414-105">Time shift events can occur as a result of an application of a virtual machine snapshot or the restoration of a virtual machine backup.</span></span> <span data-ttu-id="1e414-106">Pour plus d’informations sur cette fonctionnalité, consultez le livre blanc sur l' [ID de génération d’ordinateur virtuel](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx).</span><span class="sxs-lookup"><span data-stu-id="1e414-106">For more information about this functionality, see the [Virtual Machine Generation ID white paper](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1e414-107">Prérequis</span><span class="sxs-lookup"><span data-stu-id="1e414-107">Prerequisites</span></span>

<span data-ttu-id="1e414-108">Pour utiliser l’identificateur de génération d’ordinateur virtuel à partir d’un ordinateur virtuel, votre machine virtuelle doit être conforme aux conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="1e414-108">To use the virtual machine generation identifier from inside a virtual machine your virtual machine must conform to the following.</span></span>

-   <span data-ttu-id="1e414-109">L’ordinateur virtuel doit être en cours d’exécution sur un hyperviseur qui implémente la prise en charge des identificateurs de génération d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="1e414-109">The virtual machine must be running on a hypervisor that implements support for virtual machine generation identifiers.</span></span> <span data-ttu-id="1e414-110">Actuellement, il s’agit des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="1e414-110">Currently, these are the following:</span></span>
    -   <span data-ttu-id="1e414-111">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1e414-111">Windows 8</span></span>
    -   <span data-ttu-id="1e414-112">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1e414-112">Windows Server 2012</span></span>
    -   <span data-ttu-id="1e414-113">Microsoft Hyper-V Server 2012</span><span class="sxs-lookup"><span data-stu-id="1e414-113">Microsoft Hyper-V Server 2012</span></span>
-   <span data-ttu-id="1e414-114">L’ordinateur virtuel doit exécuter un système d’exploitation invité qui prend en charge l’identificateur de génération d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="1e414-114">The virtual machine must be running a guest operating system that has support for the virtual machine generation identifier.</span></span> <span data-ttu-id="1e414-115">Actuellement, il s’agit des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="1e414-115">Currently, these are the following.</span></span>

    <span data-ttu-id="1e414-116">Les systèmes d’exploitation suivants ont une prise en charge native de l’identificateur de génération d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="1e414-116">The following operating systems have native support for the virtual machine generation identifier.</span></span>

    -   <span data-ttu-id="1e414-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1e414-117">Windows 8</span></span>
    -   <span data-ttu-id="1e414-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1e414-118">Windows Server 2012</span></span>
    -   

    <span data-ttu-id="1e414-119">Le fonctionnement suivant peut être utilisé comme système d’exploitation invité si les services d’intégration Hyper-V de Windows 8 ou Windows Server 2012 sont installés.</span><span class="sxs-lookup"><span data-stu-id="1e414-119">The following operating can be used as the guest operating system if the Hyper-V integration services from Windows 8 or Windows Server 2012 are installed.</span></span>

    -   <span data-ttu-id="1e414-120">Windows Server 2008 R2 avec Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="1e414-120">Windows Server 2008 R2 with Service Pack 1 (SP1)</span></span>
    -   <span data-ttu-id="1e414-121">Windows 7 Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="1e414-121">Windows 7 with Service Pack 1 (SP1)</span></span>
    -   <span data-ttu-id="1e414-122">Windows Server 2008 avec Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="1e414-122">Windows Server 2008 with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="1e414-123">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1e414-123">Windows Server 2003 R2</span></span>
    -   <span data-ttu-id="1e414-124">Windows Server 2003 avec Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="1e414-124">Windows Server 2003 with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="1e414-125">Windows Vista avec Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="1e414-125">Windows Vista with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="1e414-126">Windows XP avec Service Pack 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="1e414-126">Windows XP with Service Pack 3 (SP3)</span></span>

## <a name="obtaining-the-virtual-machine-generation-identifier"></a><span data-ttu-id="1e414-127">Obtention de l’identificateur de génération de l’ordinateur virtuel</span><span class="sxs-lookup"><span data-stu-id="1e414-127">Obtaining the virtual machine generation identifier</span></span>

<span data-ttu-id="1e414-128">Pour obtenir par programme l’identificateur de génération d’ordinateur virtuel, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="1e414-128">To programmatically obtain the virtual machine generation identifier, perform the following steps.</span></span>

> [!Note]  
> <span data-ttu-id="1e414-129">Les éléments suivants doivent être exécutés avec des privilèges administrateur ou système pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="1e414-129">The following must be run with administrator or system privileges to function correctly.</span></span>

 

1.  <span data-ttu-id="1e414-130">Incluez le fichier d’en-tête « vmgenerationcounter. h » dans votre application.</span><span class="sxs-lookup"><span data-stu-id="1e414-130">Include header file "vmgenerationcounter.h" in your app.</span></span> <span data-ttu-id="1e414-131">Le fichier d’en-tête contient les définitions suivantes :</span><span class="sxs-lookup"><span data-stu-id="1e414-131">The header file contains these definitions:</span></span>
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

    

2.  <span data-ttu-id="1e414-132">Ouvrez un handle vers le \\ \\ . \\ VmGenerationCounter» à l’aide de la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="1e414-132">Open a handle to the "\\\\.\\VmGenerationCounter" device using the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="1e414-133">Vous pouvez également utiliser le Gestionnaire PnP pour utiliser le GUID d’interface de **périphérique \_ DEVINTERFACE \_ VM \_ GENCOUNTER** ({3ff2c92b-6598-4e60-8e1c-0ccf4927e319}).</span><span class="sxs-lookup"><span data-stu-id="1e414-133">Alternatively, you can use the PnP manager to consume the device interface **GUID\_DEVINTERFACE\_VM\_GENCOUNTER** ({3ff2c92b-6598-4e60-8e1c-0ccf4927e319}).</span></span> <span data-ttu-id="1e414-134">Ces objets ne seront pas présents si l’application n’est pas exécutée sur une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="1e414-134">These objects will not be present if the app is not running in a virtual machine.</span></span>
3.  <span data-ttu-id="1e414-135">Envoyez l’IOCTL de [**\_ \_ lecture IOCTL VMGENCOUNTER**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) au pilote pour récupérer l’identificateur de génération.</span><span class="sxs-lookup"><span data-stu-id="1e414-135">Send the [**IOCTL\_VMGENCOUNTER\_READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL to the driver to retrieve the generation identifier.</span></span>

    <span data-ttu-id="1e414-136">L’IOCTL de [**\_ \_ lecture VMGENCOUNTER IOCTL**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) fonctionne dans l’un des deux modes, *interrogation* et *piloté par événement*.</span><span class="sxs-lookup"><span data-stu-id="1e414-136">The [**IOCTL\_VMGENCOUNTER\_READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL operates in one of two modes, *polling*, and *event driven*.</span></span>

    <span data-ttu-id="1e414-137">Pour émettre l’IOCTL en mode d’interrogation, vous devez soumettre l’IOCTL avec une mémoire tampon d’entrée de longueur nulle.</span><span class="sxs-lookup"><span data-stu-id="1e414-137">To issue the IOCTL in polling mode, you submit the IOCTL with an input buffer of zero length.</span></span> <span data-ttu-id="1e414-138">En réponse à cela, le pilote récupère l’identificateur de génération actuel, l’écrit dans la mémoire tampon de sortie et termine l’IOCTL.</span><span class="sxs-lookup"><span data-stu-id="1e414-138">In response to this, the driver retrieves the current generation identifier, writes it to the output buffer, and completes the IOCTL.</span></span>

    <span data-ttu-id="1e414-139">Pour émettre l’IOCTL en mode piloté par les événements, soumettez l’IOCTL avec une mémoire tampon d’entrée qui contient un identificateur de génération existant.</span><span class="sxs-lookup"><span data-stu-id="1e414-139">To issue the IOCTL in event driven mode, submit the IOCTL with an input buffer that contains an existing generation identifier.</span></span> <span data-ttu-id="1e414-140">En réponse à cela, le pilote attend que l’identificateur de génération actuel soit différent de l’identificateur de génération passé.</span><span class="sxs-lookup"><span data-stu-id="1e414-140">In response to this, the driver waits until the current generation identifier becomes different from the generation identifier that was passed in.</span></span> <span data-ttu-id="1e414-141">Lorsque l’identificateur de génération change, le pilote écrit l’identificateur de génération actuel dans la mémoire tampon de sortie et termine l’IOCTL.</span><span class="sxs-lookup"><span data-stu-id="1e414-141">When the generation identifier changes, the driver writes the current generation identifier to the output buffer and completes the IOCTL.</span></span>

    <span data-ttu-id="1e414-142">Dans les deux modes, le format et la longueur de la mémoire tampon de sortie sont dictés par la structure [**\_ GENCOUNTER de la machine virtuelle**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) .</span><span class="sxs-lookup"><span data-stu-id="1e414-142">In both modes, the format and length of the output buffer is dictated by the [**VM\_GENCOUNTER**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) structure.</span></span>

    <span data-ttu-id="1e414-143">Le mode d’interrogation est pris en charge sur tous les systèmes d’exploitation invités listés ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="1e414-143">Polling mode is supported on all of the guest operating systems listed above.</span></span> <span data-ttu-id="1e414-144">Le mode piloté par les événements est pris en charge uniquement sur Windows Vista avec SP2, Windows Server 2008 avec SP2 et les systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="1e414-144">Event driven mode is supported only on Windows Vista with SP2, Windows Server 2008 with SP2, and later operating systems.</span></span> <span data-ttu-id="1e414-145">Sur les systèmes d’exploitation antérieurs, l’IOCTL échoue avec l’erreur de code d’erreur **\_ non \_ prise en charge** lorsqu’elle est émise en mode piloté par les événements.</span><span class="sxs-lookup"><span data-stu-id="1e414-145">On earlier operating systems, the IOCTL will fail with the error code **ERROR\_NOT\_SUPPORTED** when issued in event driven mode.</span></span>

    <span data-ttu-id="1e414-146">Il est possible que l’identificateur de génération change entre le moment où il est récupéré par le pilote et le moment où l’IOCTL est terminée.</span><span class="sxs-lookup"><span data-stu-id="1e414-146">It is possible for the generation identifier to change between the time that it is retrieved by the driver and the time the IOCTL is completed.</span></span> <span data-ttu-id="1e414-147">Cela peut entraîner la réception par l’application cliente de données obsolètes.</span><span class="sxs-lookup"><span data-stu-id="1e414-147">This can result in the client app receiving stale data.</span></span> <span data-ttu-id="1e414-148">Pour éviter cela, l’application cliente peut utiliser le mode piloté par les événements pour s’assurer qu’elle finira par se familiariser avec les mises à jour de l’identificateur de génération.</span><span class="sxs-lookup"><span data-stu-id="1e414-148">To avoid this, the client app can use event driven mode to ensure that it will eventually learn about any updates to the generation identifier.</span></span> <span data-ttu-id="1e414-149">En prenant l’identificateur actuel de l’application cliente comme entrée, le mode piloté par les événements évite les conditions de concurrence potentielles qui pourraient provoquer l’absence de notifications de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="1e414-149">By taking the client app's current identifier as input, event driven mode avoids potential race conditions that would cause the caller to miss notifications.</span></span>

<span data-ttu-id="1e414-150">L’exemple de code suivant montre comment effectuer les actions ci-dessus pour obtenir l’identificateur de génération d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="1e414-150">The following code example shows how to perform the above actions to obtain the virtual machine generation identifier.</span></span>

> [!Note]  
> <span data-ttu-id="1e414-151">Le code suivant doit être exécuté avec des privilèges administrateur ou système pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="1e414-151">The following code must be run with administrator or system privileges to function correctly.</span></span>

 


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



## <a name="determining-if-a-time-shift-event-has-occurred"></a><span data-ttu-id="1e414-152">Déterminer si un événement de décalage horaire s’est produit</span><span class="sxs-lookup"><span data-stu-id="1e414-152">Determining if a time shift event has occurred</span></span>

<span data-ttu-id="1e414-153">Une fois que vous avez obtenu l’identificateur de génération de l’ordinateur virtuel, vous devez le stocker pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1e414-153">After you have obtained the virtual machine generation identifier, you should store it for future use.</span></span> <span data-ttu-id="1e414-154">Avant que votre application effectue une opération qui respecte le temps, telle que la validation dans une base de données, vous devez récupérer l’identificateur de génération et le comparer à la valeur stockée.</span><span class="sxs-lookup"><span data-stu-id="1e414-154">Before your app performs a time-sensitive operation, such as committing to a database, you should re-obtain the generation identifier and compare it to the stored value.</span></span> <span data-ttu-id="1e414-155">Si l’identificateur a changé, cela signifie qu’un événement de décalage horaire s’est produit et que votre application doit agir de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="1e414-155">If the identifier has changed, that means that a time shift event has occurred, and your app must act appropriately.</span></span>

 

 
