---
title: IMsRdpClient9 propriété TransportSettings4
description: Récupère un objet qui prend en charge l’interface IMsRdpClientTransportSettings4.
ms.assetid: 808259b9-a1a4-4611-8602-b6877013c4f6
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété TransportSettings4
- Services Bureau à distance de la propriété TransportSettings4, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété TransportSettings4
- Services Bureau à distance de la propriété TransportSettings4, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété TransportSettings4
topic_type:
- apiref
api_name:
- IMsRdpClient9.TransportSettings4
- IMsRdpClient9.get_TransportSettings4
- IMsRdpClient10.TransportSettings4
- IMsRdpClient10.get_TransportSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765d2ad5a50e0608e4c11731742debbaede51737
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317129"
---
# <a name="imsrdpclient9transportsettings4-property"></a><span data-ttu-id="8c677-108">IMsRdpClient9 :: TransportSettings4, propriété</span><span class="sxs-lookup"><span data-stu-id="8c677-108">IMsRdpClient9::TransportSettings4 property</span></span>

<span data-ttu-id="8c677-109">Récupère un objet qui prend en charge l’interface [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="8c677-109">Retrieves an object that supports the [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) interface.</span></span>

<span data-ttu-id="8c677-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8c677-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c677-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c677-111">Syntax</span></span>


```C++
HRESULT get_TransportSettings4(
  [out, retval] IMsRdpClientTransportSettings4 **ppXportSet4
);
```



## <a name="property-value"></a><span data-ttu-id="8c677-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8c677-112">Property value</span></span>

<span data-ttu-id="8c677-113">Retourne un pointeur d’interface [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="8c677-113">Returns an [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c677-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c677-114">Requirements</span></span>



| <span data-ttu-id="8c677-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c677-115">Requirement</span></span> | <span data-ttu-id="8c677-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c677-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c677-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c677-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8c677-118">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8c677-118">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="8c677-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c677-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8c677-120">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8c677-120">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="8c677-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="8c677-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="8c677-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c677-122"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="8c677-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8c677-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c677-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c677-124"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="8c677-125">IID</span><span class="sxs-lookup"><span data-stu-id="8c677-125">IID</span></span><br/>                      | <span data-ttu-id="8c677-126">Le CLSID \_ MsRdpClient9 est défini en tant que 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="8c677-126">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="8c677-127">Le CLSID \_ MsRdpClient9NotSafeForScripting est défini en tant que 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="8c677-127">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="8c677-128">IID \_ IMsRdpClient9 est défini en tant que 28904001-04B6-436C-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="8c677-128">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8c677-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c677-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c677-130">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="8c677-130">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="8c677-131">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="8c677-131">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





