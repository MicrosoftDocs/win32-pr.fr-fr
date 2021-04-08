---
title: IMsRdpClientShell2 propriété MsRdpWorkspace
description: Récupère un pointeur vers l’interface IMsRdpWorkspace, qui est utilisée pour gérer les informations d’identification et les connexions de Connexions aux programmes RemoteApp et aux services Bureau à distance.
ms.assetid: 5d505ce0-18cf-4e38-b1b8-026303f7069b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété MsRdpWorkspace
- Services Bureau à distance de la propriété MsRdpWorkspace, interface IMsRdpClientShell2
- Services Bureau à distance de l’interface IMsRdpClientShell2, propriété MsRdpWorkspace
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.MsRdpWorkspace
- IMsRdpClientShell2.get_MsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91eadd3f1b422e3da96d5bcd3a5178a2a0b0eb52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742397"
---
# <a name="imsrdpclientshell2msrdpworkspace-property"></a><span data-ttu-id="b4cb7-106">IMsRdpClientShell2 :: MsRdpWorkspace, propriété</span><span class="sxs-lookup"><span data-stu-id="b4cb7-106">IMsRdpClientShell2::MsRdpWorkspace property</span></span>

<span data-ttu-id="b4cb7-107">Récupère un pointeur vers l’interface [**IMsRdpWorkspace**](imsrdpworkspace.md) , qui est utilisée pour gérer les informations d’identification et les connexions de connexions aux programmes RemoteApp et aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b4cb7-107">Retrieves a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface, which is used to manage RemoteApp and Desktop Connection credentials and connections.</span></span>

<span data-ttu-id="b4cb7-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b4cb7-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4cb7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4cb7-109">Syntax</span></span>


```C++
HRESULT get_MsRdpWorkspace(
  [out, retval] IMsRdpWorkspace **pVal
);
```



## <a name="property-value"></a><span data-ttu-id="b4cb7-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b4cb7-110">Property value</span></span>

<span data-ttu-id="b4cb7-111">Adresse d’un pointeur vers l’interface [**IMsRdpWorkspace**](imsrdpworkspace.md) .</span><span class="sxs-lookup"><span data-stu-id="b4cb7-111">The address of a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4cb7-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b4cb7-112">Remarks</span></span>

<span data-ttu-id="b4cb7-113">L’interface [**IMsRdpWorkspace**](imsrdpworkspace.md) n’est pas exposée en tant qu’interface personnalisée.</span><span class="sxs-lookup"><span data-stu-id="b4cb7-113">The [**IMsRdpWorkspace**](imsrdpworkspace.md) interface is not exposed as a custom interface.</span></span> <span data-ttu-id="b4cb7-114">Il est accessible uniquement par le biais des méthodes [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="b4cb7-114">It is accessible through [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) methods only.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4cb7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4cb7-115">Requirements</span></span>



| <span data-ttu-id="b4cb7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4cb7-116">Requirement</span></span> | <span data-ttu-id="b4cb7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4cb7-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4cb7-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4cb7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b4cb7-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b4cb7-119">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b4cb7-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4cb7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b4cb7-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b4cb7-121">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="b4cb7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b4cb7-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4cb7-123"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4cb7-123"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4cb7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4cb7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4cb7-125">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="b4cb7-125">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

