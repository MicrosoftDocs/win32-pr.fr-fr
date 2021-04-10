---
title: INapSoHConstructor Initialize, méthode (NapProtocol. h)
description: Initialise un paquet de protocole SoH dans le système NAP.
ms.assetid: 1678b677-c8c8-465c-a412-9b929e39bbac
keywords:
- Initialiser la méthode NAP
- Méthode Initialize NAP, interface INapSoHConstructor
- INapSoHConstructor interface NAP, Initialize, méthode
topic_type:
- apiref
api_name:
- INapSoHConstructor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab8d6b27547be6e7c7e9abb59f7edb7b49e716e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942055"
---
# <a name="inapsohconstructorinitialize-method"></a><span data-ttu-id="414f0-106">INapSoHConstructor :: Initialize, méthode</span><span class="sxs-lookup"><span data-stu-id="414f0-106">INapSoHConstructor::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="414f0-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="414f0-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="414f0-108">La méthode **INapSoHConstructor :: Initialize** Initialise un paquet de protocole SOH dans le système NAP.</span><span class="sxs-lookup"><span data-stu-id="414f0-108">The **INapSoHConstructor::Initialize** method initializes a SoH protocol packet in the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="414f0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="414f0-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId id,
  [in] BOOL                 isRequest
);
```



## <a name="parameters"></a><span data-ttu-id="414f0-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="414f0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="414f0-111">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="414f0-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="414f0-112">[SystemHealthEntityId](nap-datatypes.md) unique qui contient l’ID de l’agent SHA ou SHV qui construit le paquet.</span><span class="sxs-lookup"><span data-stu-id="414f0-112">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA or SHV that is constructing the packet.</span></span>

</dd> <dt>

<span data-ttu-id="414f0-113">*isRequest* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="414f0-113">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="414f0-114">Valeur **booléenne** qui est **true** si le paquet doit être un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) et **false** s’il doit s’agir d’un **SoHResponse**.</span><span class="sxs-lookup"><span data-stu-id="414f0-114">A **BOOL** that is **TRUE** if the packet is to be an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is to be an **SoHResponse**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="414f0-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="414f0-115">Return value</span></span>

<span data-ttu-id="414f0-116">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="414f0-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="414f0-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="414f0-117">Return code</span></span>                                                                                     | <span data-ttu-id="414f0-118">Description</span><span class="sxs-lookup"><span data-stu-id="414f0-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="414f0-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="414f0-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="414f0-120">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="414f0-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="414f0-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="414f0-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="414f0-122">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="414f0-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="414f0-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="414f0-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="414f0-124">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="414f0-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="414f0-125">Notes</span><span class="sxs-lookup"><span data-stu-id="414f0-125">Remarks</span></span>

<span data-ttu-id="414f0-126">Cette méthode doit être appelée exactement une fois par paquet.</span><span class="sxs-lookup"><span data-stu-id="414f0-126">This method must be called exactly once per packet.</span></span>

<span data-ttu-id="414f0-127">Le [SystemHealthEntityId](nap-datatypes.md) spécifié dans *ID*, est le premier TLV dans le paquet SOH nouvellement construit et a le type d’attribut [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md).</span><span class="sxs-lookup"><span data-stu-id="414f0-127">The [SystemHealthEntityId](nap-datatypes.md) specified in *id*, is the first TLV in the newly constructed SOH packet and has the attribute type [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="414f0-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="414f0-128">Requirements</span></span>



| <span data-ttu-id="414f0-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="414f0-129">Requirement</span></span> | <span data-ttu-id="414f0-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="414f0-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="414f0-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="414f0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="414f0-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="414f0-132">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="414f0-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="414f0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="414f0-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="414f0-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="414f0-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="414f0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="414f0-136"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="414f0-136"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="414f0-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="414f0-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="414f0-138"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="414f0-138"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="414f0-139">DLL</span><span class="sxs-lookup"><span data-stu-id="414f0-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="414f0-140"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="414f0-140"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="414f0-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="414f0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="414f0-142">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="414f0-142">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





