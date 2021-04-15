---
title: Comment appeler une méthode WMI
description: L’objectif principal de WMI est de fournir l’accès aux classes et aux instances qui représentent des objets sur votre réseau.
ms.assetid: 8d559eee-3dbf-4132-b1c0-a6925b8feb56
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 892561785280e78ecf29da1030883994990fc822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529554"
---
# <a name="how-to-call-a-wmi-method"></a><span data-ttu-id="f1d0c-103">Comment appeler une méthode WMI</span><span class="sxs-lookup"><span data-stu-id="f1d0c-103">How to call a WMI method</span></span>

<span data-ttu-id="f1d0c-104">L’objectif principal de WMI est de fournir l’accès aux classes et aux instances qui représentent des objets sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="f1d0c-104">The main purpose of WMI is to provide access to classes and instances that represent objects on your network.</span></span> <span data-ttu-id="f1d0c-105">Ces classes et instances sont prises en charge par les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="f1d0c-105">These classes and instances are supported by providers.</span></span> <span data-ttu-id="f1d0c-106">Par exemple, toutes les instances qui représentent des périphériques matériels standard de votre entreprise, tels que [**Win32 \_ PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) ou [**Win32 \_ Printer**](/windows/desktop/CIMWin32Prov/win32-printer), sont prises en charge par le fournisseur Win32.</span><span class="sxs-lookup"><span data-stu-id="f1d0c-106">For example, all of the instances that represent standard hardware devices on your enterprise, such as [**Win32\_PhysicalMemory**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) or [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer), are supported by the Win32 provider.</span></span> <span data-ttu-id="f1d0c-107">De même, vous pouvez accéder au journal des événements par le biais du fournisseur du journal des événements et du Registre par le biais du fournisseur de registre.</span><span class="sxs-lookup"><span data-stu-id="f1d0c-107">Similarly, you can access the event log through the Event Log provider, and the registry through the Registry provider.</span></span>

<span data-ttu-id="f1d0c-108">Les méthodes implémentées par WMI dans des interfaces telles que [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) ou des objets de script tels que [**SWbemServices**](swbemservices.md), sont principalement destinées à l’obtention et à la manipulation génériques des données fournies par n’importe quel fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f1d0c-108">The methods that WMI implements in interfaces such as [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) or scripting objects such as [**SWbemServices**](swbemservices.md), are primarily for generically obtaining and manipulating data supplied by any provider.</span></span> <span data-ttu-id="f1d0c-109">Par exemple, utilisez [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) pour obtenir toutes les instances du [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process) dans un sous-ensemble d’ordinateurs d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="f1d0c-109">For example, use [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) to obtain all the instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) in a subset of enterprise computers.</span></span> <span data-ttu-id="f1d0c-110">Vous pouvez ensuite appeler la méthode du fournisseur Win32 [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) sur chaque objet de **\_ processus Win32** .</span><span class="sxs-lookup"><span data-stu-id="f1d0c-110">You can then call the Win32 provider method [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) on each **Win32\_Process** object.</span></span>

<span data-ttu-id="f1d0c-111">Dans l’exemple suivant, la méthode [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) est appelée en tant que méthode Automation sur l’objet Process.</span><span class="sxs-lookup"><span data-stu-id="f1d0c-111">In the following example, the [**GetOwnerSid**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) method is called as an automation method on the Process object.</span></span> <span data-ttu-id="f1d0c-112">Une méthode WMI, telle que la [**méthode \_ path**](swbemobject-path-.md) définie pour [**SWbemObject**](swbemobject.md) , peut également être appelée sur l’objet **Process** .</span><span class="sxs-lookup"><span data-stu-id="f1d0c-112">A WMI method, such as the [**Path\_**](swbemobject-path-.md) method defined for [**SWbemObject**](swbemobject.md) could also be called on the **Process** object.</span></span>


```VB
Set ProcessCollection = _
    GetObject("WinMgmts:").InstancesOf("Win32_Process")

For Each Process In ProcessCollection
    SID = Process.GetOwnerSid
Next
```



<span data-ttu-id="f1d0c-113">Le processus d’utilisation des méthodes WMI est identique à celui d’une autre interface COM ou Automation Windows.</span><span class="sxs-lookup"><span data-stu-id="f1d0c-113">The actual process of using the WMI methods is identical to using any other Windows COM or automation interface.</span></span> <span data-ttu-id="f1d0c-114">Pour plus d’informations, consultez [com](../cossdk/component-services-portal.md) et [création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="f1d0c-114">For more information, see [COM](../cossdk/component-services-portal.md) and [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span> <span data-ttu-id="f1d0c-115">Pour plus d’informations sur les interfaces prises en charge par WMI, consultez [API com pour WMI](com-api-for-wmi.md) et [API de script pour WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="f1d0c-115">For more information about the interfaces that WMI supports, see [COM API for WMI](com-api-for-wmi.md) and [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

<span data-ttu-id="f1d0c-116">Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="f1d0c-116">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1d0c-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f1d0c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1d0c-118">Appel d’une méthode</span><span class="sxs-lookup"><span data-stu-id="f1d0c-118">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
