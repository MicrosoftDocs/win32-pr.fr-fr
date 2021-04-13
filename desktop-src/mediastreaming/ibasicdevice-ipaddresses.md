---
title: IBasicDevice (méthode)
description: Retourne un vecteur d’adresses IP.
ms.assetid: F48B91DC-3AE2-462F-835B-292BF86904B3
keywords:
- Méthode adressesIP diffusion multimédia en continu API
- AdressesIP méthode diffusion multimédia en continu API, interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode adressesIP
topic_type:
- apiref
api_name:
- IBasicDevice.IpAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0623b6e2e5d96cb0a400ab1e820424b7eecf46c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380764"
---
# <a name="ibasicdeviceipaddresses-method"></a><span data-ttu-id="25614-106">IBasicDevice :: adressesIP, méthode</span><span class="sxs-lookup"><span data-stu-id="25614-106">IBasicDevice::IpAddresses method</span></span>

<span data-ttu-id="25614-107">Retourne un vecteur d’adresses IP.</span><span class="sxs-lookup"><span data-stu-id="25614-107">Returns a vector of IP addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="25614-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25614-108">Syntax</span></span>


```C++
HRESULT IpAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a><span data-ttu-id="25614-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25614-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25614-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="25614-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25614-111">Reçoit une collection énumérable de pointeurs vers des adresses IP.</span><span class="sxs-lookup"><span data-stu-id="25614-111">Receives an enumerable collection of pointers to IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25614-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25614-112">Return value</span></span>

<span data-ttu-id="25614-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="25614-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="25614-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="25614-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="25614-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="25614-115">Return code</span></span>                                                                          | <span data-ttu-id="25614-116">Description</span><span class="sxs-lookup"><span data-stu-id="25614-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="25614-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="25614-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="25614-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="25614-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="25614-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25614-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25614-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="25614-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





