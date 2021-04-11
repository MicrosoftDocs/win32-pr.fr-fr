---
description: Événement qui se produit lorsqu’un nouveau périphérique matériel WIA (Windows Image Acquisition) est déconnecté.
ms.assetid: 9c3ccdba-288c-4bdd-b257-b03999bc6fd9
title: Événement WIA. OnDeviceDisconnected
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceDisconnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 45652f3c447c1dd0f59b0470823782c6ba635cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202898"
---
# <a name="wiaondevicedisconnected-event"></a><span data-ttu-id="639ea-103">Événement WIA. OnDeviceDisconnected</span><span class="sxs-lookup"><span data-stu-id="639ea-103">Wia.OnDeviceDisconnected event</span></span>

<span data-ttu-id="639ea-104">Événement qui se produit lorsqu’un nouveau périphérique matériel WIA (Windows Image Acquisition) est déconnecté.</span><span class="sxs-lookup"><span data-stu-id="639ea-104">Event that occurs when a new Windows Image Acquisition (WIA) hardware device is disconnected.</span></span>

## <a name="syntax"></a><span data-ttu-id="639ea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="639ea-105">Syntax</span></span>


```JScript
Wia.OnDeviceDisconnected(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="639ea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="639ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="639ea-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="639ea-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="639ea-108">Chaîne qui contient l’ID de l’appareil connecté.</span><span class="sxs-lookup"><span data-stu-id="639ea-108">A string that contains the ID of the connected device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="639ea-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="639ea-109">Return value</span></span>

<span data-ttu-id="639ea-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="639ea-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="639ea-111">Notes</span><span class="sxs-lookup"><span data-stu-id="639ea-111">Remarks</span></span>

<span data-ttu-id="639ea-112">WIA notifie le script ou l’application chaque fois qu’un périphérique matériel est déconnecté de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="639ea-112">WIA notifies the script or application whenever a hardware device is disconnected from the computer.</span></span> <span data-ttu-id="639ea-113">Implémentez la sous-routine **objWia** \_ **OnDeviceDisconnected ()** pour permettre au script ou à l’application de répondre à la déconnexion de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="639ea-113">Implement the **objWia**\_**OnDeviceDisconnected()** subroutine to allow the script or application to respond to the device disconnection.</span></span>

<span data-ttu-id="639ea-114">Par exemple, vous souhaiterez peut-être qu’un script actualise le regroupement d' [**appareils**](-wia-iwia-devices.md) lorsqu’un appareil est supprimé de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="639ea-114">For example, you might want a script to refresh the [**Devices**](-wia-iwia-devices.md) collection when a device is removed from the computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="639ea-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="639ea-115">Requirements</span></span>



| <span data-ttu-id="639ea-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="639ea-116">Requirement</span></span> | <span data-ttu-id="639ea-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="639ea-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="639ea-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="639ea-118">Minimum supported client</span></span><br/> | <span data-ttu-id="639ea-119">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="639ea-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="639ea-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="639ea-120">Minimum supported server</span></span><br/> | <span data-ttu-id="639ea-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="639ea-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="639ea-122">DLL</span><span class="sxs-lookup"><span data-stu-id="639ea-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="639ea-123"><dt>Wiascr.dll (version 4,90 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="639ea-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




