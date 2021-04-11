---
description: Événement qui se produit lorsqu’un nouveau périphérique matériel WIA (Windows Image Acquisition) est connecté.
ms.assetid: 327a29b8-581c-41b5-bea7-068bec95e653
title: Événement WIA. OnDeviceConnected
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceConnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 952b738e8afa0850bd67bab1206382e96419513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202899"
---
# <a name="wiaondeviceconnected-event"></a><span data-ttu-id="d43c7-103">Événement WIA. OnDeviceConnected</span><span class="sxs-lookup"><span data-stu-id="d43c7-103">Wia.OnDeviceConnected event</span></span>

<span data-ttu-id="d43c7-104">Événement qui se produit lorsqu’un nouveau périphérique matériel WIA (Windows Image Acquisition) est connecté.</span><span class="sxs-lookup"><span data-stu-id="d43c7-104">Event that occurs when a new Windows Image Acquisition (WIA) hardware device is connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="d43c7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d43c7-105">Syntax</span></span>


```JScript
Wia.OnDeviceConnected(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="d43c7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d43c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d43c7-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="d43c7-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="d43c7-108">Chaîne qui contient l’ID de l’appareil connecté.</span><span class="sxs-lookup"><span data-stu-id="d43c7-108">A string that contains the ID of the connected device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d43c7-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d43c7-109">Return value</span></span>

<span data-ttu-id="d43c7-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d43c7-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d43c7-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d43c7-111">Remarks</span></span>

<span data-ttu-id="d43c7-112">WIA notifie le script ou l’application chaque fois qu’un nouveau périphérique matériel est connecté à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d43c7-112">WIA notifies the script or application whenever a new hardware device is connected to the computer.</span></span> <span data-ttu-id="d43c7-113">Implémentez la sous-routine **objWia** \_ **OnDeviceConnected ()** pour permettre au script ou à l’application de répondre à la connexion de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d43c7-113">Implement the **objWia**\_**OnDeviceConnected()** subroutine to allow the script or application to respond to the device connection.</span></span>

<span data-ttu-id="d43c7-114">Par exemple, vous souhaiterez peut-être qu’un script actualise le regroupement d' [**appareils**](-wia-iwia-devices.md) lorsqu’un nouveau périphérique est installé.</span><span class="sxs-lookup"><span data-stu-id="d43c7-114">For example, you might want a script to refresh the [**Devices**](-wia-iwia-devices.md) collection when a new device is installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d43c7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d43c7-115">Requirements</span></span>



| <span data-ttu-id="d43c7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d43c7-116">Requirement</span></span> | <span data-ttu-id="d43c7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d43c7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d43c7-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d43c7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d43c7-119">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d43c7-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d43c7-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d43c7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d43c7-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d43c7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d43c7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d43c7-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d43c7-123"><dt>Wiascr.dll (version 4,90 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="d43c7-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




