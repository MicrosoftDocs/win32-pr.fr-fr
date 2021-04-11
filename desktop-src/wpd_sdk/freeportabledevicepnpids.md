---
description: 'Libère les identificateurs PnP (Plug-and-Play) récupérés par les méthodes IPortableDeviceManager :: GetDevices ou IPortableDeviceServiceManager :: GetDeviceServices.'
ms.assetid: b86f7733-81a3-4b60-bb7c-840c75f8d03f
title: FreePortableDevicePnPIDs, fonction (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePortableDevicePnPIDs
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 58bb5fa33007ed0e167226edf7078d08c2e5c3de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204037"
---
# <a name="freeportabledevicepnpids-function"></a><span data-ttu-id="1478f-103">FreePortableDevicePnPIDs fonction)</span><span class="sxs-lookup"><span data-stu-id="1478f-103">FreePortableDevicePnPIDs function</span></span>

<span data-ttu-id="1478f-104">La fonction d’assistance **FreePortableDevicePnPIDs** libère les identificateurs PnP (plug-and-Play) récupérés par les méthodes [**IPortableDeviceManager :: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) ou [**IPortableDeviceServiceManager :: GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) .</span><span class="sxs-lookup"><span data-stu-id="1478f-104">The **FreePortableDevicePnPIDs** helper function frees the Plug and Play (PnP) identifiers that are retrieved by the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) or [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="1478f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1478f-105">Syntax</span></span>


```C++
void FreePortableDevicePnPIDs(
   LPWSTR *pPnPIDs,
   DWORD  cPnPIDs
);
```



## <a name="parameters"></a><span data-ttu-id="1478f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1478f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1478f-107">*pPnPIDs*</span><span class="sxs-lookup"><span data-stu-id="1478f-107">*pPnPIDs*</span></span> 
</dt> <dd>

<span data-ttu-id="1478f-108">Tableau d’identificateurs PnP (Plug-and-Play) à libérer.</span><span class="sxs-lookup"><span data-stu-id="1478f-108">The array of Plug and Play (PnP) identifiers to be freed.</span></span>

</dd> <dt>

<span data-ttu-id="1478f-109">*cPnPIDs*</span><span class="sxs-lookup"><span data-stu-id="1478f-109">*cPnPIDs*</span></span> 
</dt> <dd>

<span data-ttu-id="1478f-110">Nombre d’identificateurs dans le tableau spécifié par le paramètre *pPnPIDs* .</span><span class="sxs-lookup"><span data-stu-id="1478f-110">The number of identifiers in the array specified by the *pPnPIDs* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1478f-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1478f-111">Return value</span></span>

<span data-ttu-id="1478f-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1478f-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1478f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="1478f-113">Remarks</span></span>

<span data-ttu-id="1478f-114">L’application est chargée de libérer le tableau de pointeurs qu’elle alloue.</span><span class="sxs-lookup"><span data-stu-id="1478f-114">The application is responsible for freeing the array of pointers that it allocates.</span></span>

## <a name="examples"></a><span data-ttu-id="1478f-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="1478f-115">Examples</span></span>


```C++
// Allocate an array of LPWSTR pointers.
    LPWSTR* pPnpDeviceIDs = new LPWSTR[cPnpDeviceIDs];
if (pPnpDeviceIDs != NULL)
{
    hr = pPortableDeviceManager->;GetDevices(pPnpDeviceIDs, &cPnpDeviceIDs);
    if (SUCCEEDED(hr))
    {
        // Free all returned PnPDeviceID strings allocated by IPortableDeviceManager::GetDevices.
     FreePortableDevicePnPIDs(pPnpDeviceIDs, cPnpDeviceIDs);
     // Application is responsible for deleting the array of LPWSTR pointers.
     delete [] pPnpDeviceIDs;
     pPnpDeviceIDs = NULL;      
 }
} 
```



## <a name="requirements"></a><span data-ttu-id="1478f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1478f-116">Requirements</span></span>



| <span data-ttu-id="1478f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1478f-117">Requirement</span></span> | <span data-ttu-id="1478f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1478f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1478f-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1478f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1478f-120">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1478f-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="1478f-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1478f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1478f-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1478f-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="1478f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1478f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1478f-124"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="1478f-124"><dt>PortableDevice.h</dt></span></span> </dl> |



 

 




