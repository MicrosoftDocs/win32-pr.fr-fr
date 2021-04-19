---
description: La méthode Create de l’objet DeviceInfo établit une connexion à l’appareil WIA (Windows Image Acquisition) spécifiée par l’objet DeviceInfo et retourne un objet Item qui représente l’appareil.
ms.assetid: 57f3698c-3f9f-4775-8b53-a65a5591aa3d
title: DeviceInfo. Create, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1efc36ea8794de4b64c9af616320b09d547f6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533761"
---
# <a name="deviceinfocreate-method"></a><span data-ttu-id="f3907-103">DeviceInfo. Create, méthode</span><span class="sxs-lookup"><span data-stu-id="f3907-103">DeviceInfo.Create method</span></span>

<span data-ttu-id="f3907-104">La méthode **Create** de l’objet [**DeviceInfo**](-wia-deviceinfo.md) établit une connexion à l’appareil WIA (Windows Image Acquisition) spécifiée par l’objet **DeviceInfo** et retourne un objet [**Item**](-wia-item.md) qui représente l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f3907-104">The **Create** method of the [**DeviceInfo**](-wia-deviceinfo.md) object makes a connection to the Windows Image Acquisition (WIA) device specified by the **DeviceInfo** object, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3907-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3907-105">Syntax</span></span>


```JScript
retVal = DeviceInfo.Create()
```



## <a name="parameters"></a><span data-ttu-id="f3907-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3907-106">Parameters</span></span>

<span data-ttu-id="f3907-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f3907-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3907-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f3907-108">Return value</span></span>

<span data-ttu-id="f3907-109">Type : **IWiaDispatchItem**</span><span class="sxs-lookup"><span data-stu-id="f3907-109">Type: **IWiaDispatchItem**</span></span>

<span data-ttu-id="f3907-110">Cette méthode retourne l’objet d' [**élément**](-wia-item.md) qui représente l’appareil créé.</span><span class="sxs-lookup"><span data-stu-id="f3907-110">This method returns the [**Item**](-wia-item.md) object that represents the device that is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3907-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f3907-111">Remarks</span></span>

<span data-ttu-id="f3907-112">Utilisez la méthode **Create** pour créer une connexion à un périphérique matériel WIA après l’énumération du regroupement [**Devices**](-wia-iwia-devices.md) .</span><span class="sxs-lookup"><span data-stu-id="f3907-112">Use the **Create** method to create a connection to a WIA hardware device after enumerating the [**Devices**](-wia-iwia-devices.md) collection.</span></span> <span data-ttu-id="f3907-113">La méthode retourne un objet d' [**élément**](-wia-item.md) qui représente l’appareil (élément racine).</span><span class="sxs-lookup"><span data-stu-id="f3907-113">The method returns an [**Item**](-wia-item.md) object that represents the device (a root item).</span></span>

## <a name="examples"></a><span data-ttu-id="f3907-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="f3907-114">Examples</span></span>

<span data-ttu-id="f3907-115">L’exemple suivant illustre l’utilisation de la méthode **Create** .</span><span class="sxs-lookup"><span data-stu-id="f3907-115">The following example demonstrates the use of the **Create** method.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objDeviceInfo.Create()
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="f3907-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3907-116">Requirements</span></span>



| <span data-ttu-id="f3907-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3907-117">Requirement</span></span> | <span data-ttu-id="f3907-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3907-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3907-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3907-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f3907-120">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3907-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f3907-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3907-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f3907-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3907-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f3907-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f3907-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3907-124"><dt>Wiascr.dll (version 4,90 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="f3907-124"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




