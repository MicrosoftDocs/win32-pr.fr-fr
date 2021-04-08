---
description: La fonction InstallWiaDevice installe un appareil WIA (Windows Image Acquisition) comme périphérique énuméré à la racine. Il est possible qu’un message d’avertissement de sécurité s’indique si un programme d’installation ou un Coinstallateur n’est pas signé numériquement et approuvé.
ms.assetid: c7de27f5-5994-4fce-a6ec-6e7cfae2e591
title: Fonction InstallWiaDevice (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallWiaDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 62060d538b4b51fe22e10df09093f1f7f8c26a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752861"
---
# <a name="installwiadevice-function"></a><span data-ttu-id="ffa65-104">InstallWiaDevice fonction)</span><span class="sxs-lookup"><span data-stu-id="ffa65-104">InstallWiaDevice function</span></span>

<span data-ttu-id="ffa65-105">La fonction **InstallWiaDevice** installe un appareil WIA (Windows Image Acquisition) comme périphérique énuméré à la racine.</span><span class="sxs-lookup"><span data-stu-id="ffa65-105">The **InstallWiaDevice** function installs a Windows Image Acquisition (WIA) device as root-enumerated device.</span></span> <span data-ttu-id="ffa65-106">Il est possible qu’un message d’avertissement de sécurité s’indique si un programme d’installation ou un Coinstallateur n’est pas signé numériquement et approuvé.</span><span class="sxs-lookup"><span data-stu-id="ffa65-106">It may popup a security warning if any installing file or coinstaller is not digitally signed and trusted.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffa65-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffa65-107">Syntax</span></span>


```C++
DWORD WINAPI InstallWiaDevice(
  _In_ PWIADEVICEINSTALL *pWiaDeviceInstall
);
```



## <a name="parameters"></a><span data-ttu-id="ffa65-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ffa65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffa65-109">*pWiaDeviceInstall* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ffa65-109">*pWiaDeviceInstall* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffa65-110">Tapez : \**PWIADEVICEINSTALL \** _</span><span class="sxs-lookup"><span data-stu-id="ffa65-110">Type: \**PWIADEVICEINSTALL\** _</span></span>

<span data-ttu-id="ffa65-111">Pointeur vers une structure WIADEVICEINSTALL.</span><span class="sxs-lookup"><span data-stu-id="ffa65-111">Pointer to a WIADEVICEINSTALL structure.</span></span> <span data-ttu-id="ffa65-112">Le membre _szFriendlyName \* de la structure doit avoir la valeur de l’appareil FriendlyName réel.</span><span class="sxs-lookup"><span data-stu-id="ffa65-112">The _szFriendlyName\* member of the structure must be set to the actual device FriendlyName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffa65-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ffa65-113">Return value</span></span>

<span data-ttu-id="ffa65-114">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ffa65-114">Type: **DWORD**</span></span>

<span data-ttu-id="ffa65-115">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="ffa65-115">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="ffa65-116">Si la fonction échoue, elle retourne un code d’erreur Win32.</span><span class="sxs-lookup"><span data-stu-id="ffa65-116">If the function fails, it returns a Win32 error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffa65-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffa65-117">Requirements</span></span>



| <span data-ttu-id="ffa65-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffa65-118">Requirement</span></span> | <span data-ttu-id="ffa65-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffa65-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffa65-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffa65-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ffa65-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ffa65-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ffa65-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffa65-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ffa65-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ffa65-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ffa65-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="ffa65-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffa65-125"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffa65-125"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="ffa65-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ffa65-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="ffa65-127"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ffa65-127"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




