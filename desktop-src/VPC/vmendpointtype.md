---
title: Énumération VMEndpointType (VPCCOMInterfaces. h)
description: Spécifie le type de point de terminaison.
ms.assetid: b48bd860-50dc-4c8c-b65b-69c407d4612a
keywords:
- Virtual PC de l’énumération VMEndpointType
topic_type:
- apiref
api_name:
- VMEndpointType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912eb43147af03dd2b9923c4bdb778044f40d023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843509"
---
# <a name="vmendpointtype-enumeration"></a><span data-ttu-id="a5b03-104">Énumération VMEndpointType</span><span class="sxs-lookup"><span data-stu-id="a5b03-104">VMEndpointType enumeration</span></span>

<span data-ttu-id="a5b03-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a5b03-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a5b03-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a5b03-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a5b03-107">Spécifie le type de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="a5b03-107">Specifies the endpoint type.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5b03-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5b03-108">Syntax</span></span>


```C++
typedef enum  { 
  vmEndpoint_NamedPipe  = 0,
  vmEndpoint_TCPIP      = 1
} VMEndpointType;
```



## <a name="constants"></a><span data-ttu-id="a5b03-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="a5b03-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a5b03-110"><span id="vmEndpoint_NamedPipe"></span><span id="vmendpoint_namedpipe"></span><span id="VMENDPOINT_NAMEDPIPE"></span>**vmEndpoint \_ NamedPipe**</span><span class="sxs-lookup"><span data-stu-id="a5b03-110"><span id="vmEndpoint_NamedPipe"></span><span id="vmendpoint_namedpipe"></span><span id="VMENDPOINT_NAMEDPIPE"></span>**vmEndpoint\_NamedPipe**</span></span>
</dt> <dd>

<span data-ttu-id="a5b03-111">Côté hôte.</span><span class="sxs-lookup"><span data-stu-id="a5b03-111">The host side.</span></span>

</dd> <dt>

<span data-ttu-id="a5b03-112"><span id="vmEndpoint_TCPIP"></span><span id="vmendpoint_tcpip"></span><span id="VMENDPOINT_TCPIP"></span>**\_tcpip vmEndpoint**</span><span class="sxs-lookup"><span data-stu-id="a5b03-112"><span id="vmEndpoint_TCPIP"></span><span id="vmendpoint_tcpip"></span><span id="VMENDPOINT_TCPIP"></span>**vmEndpoint\_TCPIP**</span></span>
</dt> <dd>

<span data-ttu-id="a5b03-113">Côté invité.</span><span class="sxs-lookup"><span data-stu-id="a5b03-113">The guest side.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5b03-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5b03-114">Requirements</span></span>



| <span data-ttu-id="a5b03-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5b03-115">Requirement</span></span> | <span data-ttu-id="a5b03-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5b03-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b03-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5b03-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a5b03-118">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5b03-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a5b03-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5b03-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a5b03-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5b03-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a5b03-121">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a5b03-121">End of client support</span></span><br/>    | <span data-ttu-id="a5b03-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a5b03-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a5b03-123">Produit</span><span class="sxs-lookup"><span data-stu-id="a5b03-123">Product</span></span><br/>                  | <span data-ttu-id="a5b03-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a5b03-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a5b03-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5b03-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5b03-126"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5b03-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5b03-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5b03-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5b03-128">**IVMVirtualMachine::StartCommunicationChannel**</span><span class="sxs-lookup"><span data-stu-id="a5b03-128">**IVMVirtualMachine::StartCommunicationChannel**</span></span>](ivmvirtualmachine-startcommunicationchannel.md)
</dt> </dl>

 

