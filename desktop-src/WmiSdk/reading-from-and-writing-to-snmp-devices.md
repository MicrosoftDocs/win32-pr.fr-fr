---
description: Les périphériques SNMP sont accessibles en lisant ou en écrivant dans l’instance de classe correspondante dans le stockage SMIR WMI (référentiel des informations du module SNMP).
ms.assetid: af5e1321-b552-447e-a217-eecbebe1f203
ms.tgt_platform: multiple
title: Lecture et écriture dans des périphériques SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8fc25f384d499e16e19c5e909f7d091ea34f9a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528605"
---
# <a name="reading-from-and-writing-to-snmp-devices"></a><span data-ttu-id="4ebeb-103">Lecture et écriture dans des périphériques SNMP</span><span class="sxs-lookup"><span data-stu-id="4ebeb-103">Reading from and Writing to SNMP Devices</span></span>

<span data-ttu-id="4ebeb-104">Les périphériques SNMP sont accessibles en lisant ou en écrivant dans l’instance de classe correspondante dans le stockage SMIR WMI (référentiel des informations du module SNMP).</span><span class="sxs-lookup"><span data-stu-id="4ebeb-104">SNMP devices can be accessed by reading from or writing to their corresponding class instance in the WMI SMIR (SNMP Module Information Repository).</span></span> <span data-ttu-id="4ebeb-105">Lorsque vous travaillez avec plusieurs appareils du même type, pour des performances optimales, chargez l’MiB pour un type d’appareil SNMP dans le stockage SMIR.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-105">When you are working with multiple devices of the same type, for efficiency, load the MIBs for one SNMP device type into the SMIR.</span></span>

> [!Note]  
> <span data-ttu-id="4ebeb-106">Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="4ebeb-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="4ebeb-107">Sélectionnez l’une des options suivantes pour lire ou écrire à partir de chaque type d’appareil SNMP en mettant à jour les informations de contexte de l’instance avant de communiquer avec chacune d’elles.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-107">Select one of the following options to read to or write from each SNMP device type by updating the context information of the instance before communicating with each one.</span></span>

-   <span data-ttu-id="4ebeb-108">Utilisez un nom DNS au lieu de l’adresse IP lors du référencement d’un appareil spécifique.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-108">Use a DNS name instead of the IP address when referencing a specific device.</span></span>

    <span data-ttu-id="4ebeb-109">L’exemple suivant montre comment utiliser le nom DNS pour un appareil spécifique.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-109">The following example shows how to use the DNS name for a specific device.</span></span>

    ```VB
    strNamedValue = Context.Add("AgentAddress", "Router1" )
    ```

    

-   <span data-ttu-id="4ebeb-110">Créez un espace de noms distinct et associez une adresse d’appareil à l’objet d’espace de noms à l’aide du qualificateur d’instance AgentAddress afin que l’espace de noms soit définitivement lié à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-110">Create a separate namespace and associate a device address to the namespace object using the AgentAddress instance qualifier so that the namespace is permanently bound to the device.</span></span> <span data-ttu-id="4ebeb-111">Dans ce cas, vous n’avez pas besoin de spécifier les informations de l’objet de contexte.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-111">In this case, you need not specify the context object information.</span></span>
-   <span data-ttu-id="4ebeb-112">Lire à partir d’un périphérique SNMP.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-112">Read from an SNMP device.</span></span>

    <span data-ttu-id="4ebeb-113">L’exemple suivant effectue une opération d’extraction sur une classe d’appareil.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-113">The following example performs a Get operation on a device class.</span></span>

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set objSet = objServices.ExecQuery _
        ("SELECT * FROM SNMP_NET_DEVICE_123 WHERE hdwr_idx>1",, _
          wbemFlagReturnWhenComplete)
    for each obj in objset 
      'do whatever 
    next
    ```

    

-   <span data-ttu-id="4ebeb-114">Écrire sur un périphérique SNMP.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-114">Write to an SNMP device.</span></span>

    <span data-ttu-id="4ebeb-115">L’exemple suivant effectue une opération set sur une classe d’appareil.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-115">The following example performs a Set operation on a device class.</span></span>

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set obj= objServices.Get("SNMP_NET_DEVICE_123=@")
    obj.deviceLocation = "40/5073"
    obj.put_
    ```

    

<span data-ttu-id="4ebeb-116">Les classes corrélées sont celles qu’un appareil SNMP donné peut prendre en charge lorsque l’énumération se produit.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-116">Correlated classes are those that a given SNMP device is known to support when enumeration occurs.</span></span> <span data-ttu-id="4ebeb-117">La corrélation affecte l’ensemble des classes retournées à partir du stockage SMIR.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-117">Correlation affects the set of classes returned from the SMIR.</span></span> <span data-ttu-id="4ebeb-118">L’énumération non corrélée retourne toutes les classes présentes dans le stockage SMIR, que l’appareil les prenne en charge ou non.</span><span class="sxs-lookup"><span data-stu-id="4ebeb-118">Noncorrelated enumeration returns all classes present within the SMIR, regardless of whether the device supports them.</span></span> <span data-ttu-id="4ebeb-119">Pour plus d’informations sur l’utilisation des techniques de corrélation WMI, consultez [corrélation de classe SNMP WMI](wmi-snmp-class-correlation.md).</span><span class="sxs-lookup"><span data-stu-id="4ebeb-119">For more information about using WMI correlation techniques, see [WMI SNMP Class Correlation](wmi-snmp-class-correlation.md).</span></span>

 

 



