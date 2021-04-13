---
description: La méthode Create de l’objet WIA établit une connexion à l’appareil WIA (Windows Image Acquisition) spécifié et retourne un objet Item qui représente l’appareil.
ms.assetid: c33c635a-159c-4ac3-8ad5-6f21a1986702
title: WIA. Create, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Create
- SafeWia.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 6a388ba2b3ee0506b093221275e34104e3f91bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529151"
---
# <a name="wiacreate-method"></a><span data-ttu-id="820e8-103">WIA. Create, méthode</span><span class="sxs-lookup"><span data-stu-id="820e8-103">Wia.Create method</span></span>

<span data-ttu-id="820e8-104">La méthode **Create** de l’objet [**WIA**](-wia-wia.md) établit une connexion à l’appareil WIA (Windows Image Acquisition) spécifié et retourne un objet [**Item**](-wia-item.md) qui représente l’appareil.</span><span class="sxs-lookup"><span data-stu-id="820e8-104">The **Create** method of the [**Wia**](-wia-wia.md) object makes a connection to the specified Windows Image Acquisition (WIA) device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="820e8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="820e8-105">Syntax</span></span>


```JScript
retVal = Wia.Create(
  Device
)
```



## <a name="parameters"></a><span data-ttu-id="820e8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="820e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="820e8-107">*Appareil mobile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="820e8-107">*Device* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="820e8-108">Type : \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="820e8-108">Type: \**VARIANT\** _</span></span>

<span data-ttu-id="820e8-109">Spécifie l’appareil WIA auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="820e8-109">Specifies the WIA device to which to connect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="820e8-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="820e8-110">Return value</span></span>

<span data-ttu-id="820e8-111">Type : _ *IWiaDispatchItem*\*</span><span class="sxs-lookup"><span data-stu-id="820e8-111">Type: _ *IWiaDispatchItem*\*</span></span>

<span data-ttu-id="820e8-112">En cas de réussite, cette méthode retourne un objet d' [**élément**](-wia-item.md) qui représente un périphérique matériel WIA (élément racine).</span><span class="sxs-lookup"><span data-stu-id="820e8-112">If successful, this method returns an [**Item**](-wia-item.md) object that represents a WIA hardware device (a root item).</span></span>

## <a name="remarks"></a><span data-ttu-id="820e8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="820e8-113">Remarks</span></span>

<span data-ttu-id="820e8-114">Le paramètre *Device* spécifie un objet [**DeviceInfo**](-wia-deviceinfo.md) en passant l’objet lui-même, son index d’un objet collection ou la valeur de sa propriété [**ID**](-wia-iwiadeviceinfo-id.md) .</span><span class="sxs-lookup"><span data-stu-id="820e8-114">The *Device* parameter specifies a [**DeviceInfo**](-wia-deviceinfo.md) object by passing the object itself, its index from a collection object, or the value of its [**Id**](-wia-iwiadeviceinfo-id.md) property.</span></span> <span data-ttu-id="820e8-115">**Ne rien** faire pour afficher une boîte de dialogue qui permet à un utilisateur de sélectionner un appareil.</span><span class="sxs-lookup"><span data-stu-id="820e8-115">Pass **Nothing** to display a dialog box that allows a user to select a device.</span></span>

## <a name="examples"></a><span data-ttu-id="820e8-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="820e8-116">Examples</span></span>

<span data-ttu-id="820e8-117">Les exemples VBScript suivants illustrent l’utilisation de la méthode **Create** .</span><span class="sxs-lookup"><span data-stu-id="820e8-117">The following VBScript examples demonstrate the use of the **Create** method.</span></span>

<span data-ttu-id="820e8-118">Le premier exemple passe un objet [**DeviceInfo**](-wia-deviceinfo.md) à la méthode **Create** .</span><span class="sxs-lookup"><span data-stu-id="820e8-118">The first example passes a [**DeviceInfo**](-wia-deviceinfo.md) object to the **Create** method.</span></span> <span data-ttu-id="820e8-119">Notez que le passage de la propriété [**ID**](-wia-iwiadeviceinfo-id.md) de l’objet provoque exactement le même comportement.</span><span class="sxs-lookup"><span data-stu-id="820e8-119">Note that passing the object's [**Id**](-wia-iwiadeviceinfo-id.md) property causes exactly the same behavior.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objWia.Create(objDeviceInfo)
Next
</SCRIPT>
```



<span data-ttu-id="820e8-120">Dans l’exemple suivant, l’application appelante passe l’index de l’objet [**DeviceInfo**](-wia-deviceinfo.md) de la collection à la méthode **Create** .</span><span class="sxs-lookup"><span data-stu-id="820e8-120">In the next example, the calling application passes the index of the [**DeviceInfo**](-wia-deviceinfo.md) object in the collection to the **Create** method.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objItem
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For i = 0 To objDeviceInfoCollection.Count-1
    Set objItem = objWia.Create(i)
Next
</SCRIPT>
```



<span data-ttu-id="820e8-121">L’exemple suivant passe **Nothing** à la méthode **Create** pour afficher une boîte de dialogue qui permet à un utilisateur de sélectionner un appareil.</span><span class="sxs-lookup"><span data-stu-id="820e8-121">The next example passes **Nothing** to the **Create** method to display a dialog box that allows a user to select a device.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objItem
 
Set objWia = objWia.Create(Nothing)
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="820e8-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="820e8-122">Requirements</span></span>



| <span data-ttu-id="820e8-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="820e8-123">Requirement</span></span> | <span data-ttu-id="820e8-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="820e8-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="820e8-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="820e8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="820e8-126">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="820e8-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="820e8-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="820e8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="820e8-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="820e8-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="820e8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="820e8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="820e8-130"><dt>Wiascr.dll (version 4,90 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="820e8-130"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




