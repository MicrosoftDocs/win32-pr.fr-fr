---
description: Récupère le suivant d’un ou plusieurs objets IPortableDeviceConnector dans la séquence d’énumération.
ms.assetid: 5aed563a-5ecc-49c0-8a0c-622405453896
title: 'IEnumPortableDeviceConnectors :: Next, méthode (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Next
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 709e938c28f9bf09e34d918eea7be3029c7a11e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534107"
---
# <a name="ienumportabledeviceconnectorsnext-method"></a><span data-ttu-id="f14bd-103">IEnumPortableDeviceConnectors :: Next, méthode</span><span class="sxs-lookup"><span data-stu-id="f14bd-103">IEnumPortableDeviceConnectors::Next method</span></span>

<span data-ttu-id="f14bd-104">La méthode **suivante** récupère le suivant d’un ou plusieurs objets [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="f14bd-104">The **Next** method retrieves the next one or more [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) objects in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="f14bd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f14bd-105">Syntax</span></span>


```C++
HRESULT Next(
  [in]      UINT32                   cRequested,
  [out]     IPortableDeviceConnector **pConnectors,
  [in, out] UINT32                   *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="f14bd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f14bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f14bd-107">*cRequested* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f14bd-107">*cRequested* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f14bd-108">Nombre d’appareils demandés.</span><span class="sxs-lookup"><span data-stu-id="f14bd-108">The number of requested devices.</span></span> <span data-ttu-id="f14bd-109">Cette valeur indique également le nombre d’éléments dans le tableau alloué par l’appelant spécifié par le paramètre *pConnectors* .</span><span class="sxs-lookup"><span data-stu-id="f14bd-109">This value also indicates the number of elements in the caller-allocated array specified by the *pConnectors* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f14bd-110">*pConnectors* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f14bd-110">*pConnectors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f14bd-111">Tableau de pointeurs [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , chacun spécifiant un périphérique Bluetooth MTP couplé.</span><span class="sxs-lookup"><span data-stu-id="f14bd-111">An array of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) pointers, each specifying a paired MTP Bluetooth device.</span></span> <span data-ttu-id="f14bd-112">L’appelant doit allouer un tableau de pointeurs **IPortableDeviceConnector** avec la longueur de tableau spécifiée par le paramètre *cRequested* .</span><span class="sxs-lookup"><span data-stu-id="f14bd-112">The caller must allocate an array of **IPortableDeviceConnector** pointers, with the array length specified by the *cRequested* parameter.</span></span> <span data-ttu-id="f14bd-113">En cas de retour réussi, l’appelant doit libérer à la fois le tableau et les pointeurs retournés.</span><span class="sxs-lookup"><span data-stu-id="f14bd-113">On successful return, the caller must free both the array and the returned pointers.</span></span> <span data-ttu-id="f14bd-114">Les interfaces **IPortableDeviceConnector** sont libérées en appelant la méthode **IUnknown :: Release** .</span><span class="sxs-lookup"><span data-stu-id="f14bd-114">The **IPortableDeviceConnector** interfaces are freed by calling the **IUnknown::Release** method.</span></span>

</dd> <dt>

<span data-ttu-id="f14bd-115">*pcFetched* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f14bd-115">*pcFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f14bd-116">Nombre d’interfaces [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) réellement récupérées.</span><span class="sxs-lookup"><span data-stu-id="f14bd-116">The number of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) interfaces that are actually retrieved.</span></span> <span data-ttu-id="f14bd-117">Si aucune interface **IPortableDeviceConnector** n’est récupérée et que la valeur de retour est **\_ false**, il n’y a plus d’interfaces **IPortableDeviceConnector** à énumérer.</span><span class="sxs-lookup"><span data-stu-id="f14bd-117">If no **IPortableDeviceConnector** interfaces are retrieved and the return value is **S\_FALSE**, there are no more **IPortableDeviceConnector** interfaces to enumerate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f14bd-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f14bd-118">Return value</span></span>

<span data-ttu-id="f14bd-119">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f14bd-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f14bd-120">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f14bd-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f14bd-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f14bd-121">Return code</span></span>                                                                             | <span data-ttu-id="f14bd-122">Description</span><span class="sxs-lookup"><span data-stu-id="f14bd-122">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="f14bd-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f14bd-123"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="f14bd-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="f14bd-124">The method succeeded.</span></span><br/>                                 |
| <dl> <span data-ttu-id="f14bd-125"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="f14bd-125"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="f14bd-126">Il n’y a plus d’appareils Bluetooth MTP à énumérer.</span><span class="sxs-lookup"><span data-stu-id="f14bd-126">There are no more MTP Bluetooth devices to enumerate.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="f14bd-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="f14bd-127">Examples</span></span>

<span data-ttu-id="f14bd-128">L’exemple suivant illustre l’utilisation de cette méthode pour énumérer des appareils MTP/Bluetooth couplés et pour envoyer une demande de connexion asynchrone à chacun.</span><span class="sxs-lookup"><span data-stu-id="f14bd-128">The following example demonstrates the use of this method to enumerate paired MTP/Bluetooth devices, and to send an asynchronous connection request to each.</span></span>


```C++
IEnumPortableDeviceConnectors* pEnum = NULL;
    HRESULT hrEnum = S_OK;
 HRESULT hr = CoCreateInstance(CLSID_EnumBthMtpConnectors, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pEnum));
    if (SUCCEEDED(hr))
{
  while (S_OK == hrEnum)
    {
       UINT32  uFetched        = 0;
       LPWSTR  wszDevicePnPID  = NULL;
       IPortableDeviceConnector* pDevice = NULL;
       hrEnum = pEnum->Next(1, &spDevice, &uFetched);
       if (hrEnum == S_OK && uFetched == 1)
        {
          // Send an asynchronous connect request.  
          hr = pDevice ->Connect(NULL);
          // Release the device when done
          pDevice->Release();
          pDevice = NULL;
        }
     }  // while S_OK == hrEnum
  // Release the enumerator when done
    if (pEnum)
    {
     pEnum->Release();
     pEnum = NULL;
   }
    }
       
```



## <a name="requirements"></a><span data-ttu-id="f14bd-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f14bd-129">Requirements</span></span>



| <span data-ttu-id="f14bd-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f14bd-130">Requirement</span></span> | <span data-ttu-id="f14bd-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f14bd-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f14bd-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f14bd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f14bd-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f14bd-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="f14bd-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f14bd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f14bd-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f14bd-135">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="f14bd-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="f14bd-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f14bd-137"><dt>Devpkey. h ; </dt> <dt>PortableDeviceConnectApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f14bd-137"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="f14bd-138">MIDL</span><span class="sxs-lookup"><span data-stu-id="f14bd-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f14bd-139"><dt>PortableDeviceConnectApi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f14bd-139"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="f14bd-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f14bd-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="f14bd-141"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f14bd-141"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="f14bd-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f14bd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f14bd-143">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="f14bd-143">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




