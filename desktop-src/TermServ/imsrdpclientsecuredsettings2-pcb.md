---
title: Propriété IMsRdpClientSecuredSettings2 PCB
description: Spécifie le paramètre d’objet BLOB de préconnexion à utiliser avant la connexion pour la transmission au serveur. | Propriété IMsRdpClientSecuredSettings2 PCB
ms.assetid: e2ddd9fd-d868-4fc5-835d-0f4db5da71e3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriété PCB
- Services Bureau à distance de propriété PCB, interface IMsRdpClientSecuredSettings2
- Services Bureau à distance de l’interface IMsRdpClientSecuredSettings2, propriété PCB
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings2.PCB
- IMsRdpClientSecuredSettings2.get_PCB
- IMsRdpClientSecuredSettings2.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99b9a04a854f218fcbe1735ec6271aa4a58edba
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523793"
---
# <a name="imsrdpclientsecuredsettings2pcb-property"></a><span data-ttu-id="11fc1-107">IMsRdpClientSecuredSettings2 ::P propriété CB</span><span class="sxs-lookup"><span data-stu-id="11fc1-107">IMsRdpClientSecuredSettings2::PCB property</span></span>

<span data-ttu-id="11fc1-108">Spécifie le paramètre d’objet BLOB de préconnexion à utiliser avant la connexion pour la transmission au serveur.</span><span class="sxs-lookup"><span data-stu-id="11fc1-108">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span>

<span data-ttu-id="11fc1-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="11fc1-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="11fc1-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11fc1-110">Syntax</span></span>


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *bstrPCB
);
```



## <a name="property-value"></a><span data-ttu-id="11fc1-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="11fc1-111">Property value</span></span>

<span data-ttu-id="11fc1-112">Paramètre PCB.</span><span class="sxs-lookup"><span data-stu-id="11fc1-112">The PCB setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="11fc1-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11fc1-113">Requirements</span></span>



| <span data-ttu-id="11fc1-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11fc1-114">Requirement</span></span> | <span data-ttu-id="11fc1-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="11fc1-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11fc1-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11fc1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="11fc1-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="11fc1-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="11fc1-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11fc1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="11fc1-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11fc1-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="11fc1-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="11fc1-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="11fc1-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11fc1-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="11fc1-122">DLL</span><span class="sxs-lookup"><span data-stu-id="11fc1-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11fc1-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11fc1-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11fc1-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11fc1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11fc1-125">**IMsRdpClientSecuredSettings2**</span><span class="sxs-lookup"><span data-stu-id="11fc1-125">**IMsRdpClientSecuredSettings2**</span></span>](imsrdpclientsecuredsettings2.md)
</dt> </dl>

 

 





