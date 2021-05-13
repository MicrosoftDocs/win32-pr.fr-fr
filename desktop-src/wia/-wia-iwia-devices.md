---
description: Collection d’objets DeviceInfo qui représentent tous les périphériques installés sur l’ordinateur.
ms.assetid: 2f124188-2b66-46cc-9b26-bfef3709a1af
title: WIA. Devices, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Devices
- SafeWia.Devices
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: b4d98bfe1552156071efde0b46899ad058e75aec
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841311"
---
# <a name="wiadevices-property"></a><span data-ttu-id="9a714-103">WIA. Devices, propriété</span><span class="sxs-lookup"><span data-stu-id="9a714-103">Wia.Devices property</span></span>

<span data-ttu-id="9a714-104">Collection d’objets [**DeviceInfo**](-wia-deviceinfo.md) qui représentent tous les périphériques installés sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9a714-104">Collection of [**DeviceInfo**](-wia-deviceinfo.md) objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="9a714-105">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9a714-105">Read-only.</span></span>

> [!Note]  
> <span data-ttu-id="9a714-106">Cette collection est de base 0.</span><span class="sxs-lookup"><span data-stu-id="9a714-106">This collection is 0-based.</span></span>

 

<span data-ttu-id="9a714-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9a714-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a714-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a714-108">Syntax</span></span>


```JScript
propVal = Wia.Devices
```



## <a name="property-value"></a><span data-ttu-id="9a714-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9a714-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="9a714-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="9a714-110">Examples</span></span>

<span data-ttu-id="9a714-111">L’exemple suivant illustre l’utilisation de la collection **Devices** pour énumérer les périphériques sur un système.</span><span class="sxs-lookup"><span data-stu-id="9a714-111">The following example illustrates the use of the **Devices** collection to enumerate the devices on a system.</span></span>


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    ! Do something with the DeviceInfo object
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="9a714-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9a714-112">Requirements</span></span>



| <span data-ttu-id="9a714-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a714-113">Requirement</span></span> | <span data-ttu-id="9a714-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a714-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a714-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a714-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9a714-116">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a714-116">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9a714-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a714-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9a714-118">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a714-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9a714-119">DLL</span><span class="sxs-lookup"><span data-stu-id="9a714-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a714-120"><dt>Wiascr.dll (version 4,90 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="9a714-120"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




