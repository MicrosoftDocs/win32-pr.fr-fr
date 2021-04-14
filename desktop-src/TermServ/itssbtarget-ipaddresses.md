---
title: Propriété ITsSbTarget adressesIP
description: Récupère ou spécifie les adresses IP externes de la cible.
ms.assetid: 938a753c-d541-4772-b41b-817324488685
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété TargetExternalIpAddresses
- Services Bureau à distance de la propriété TargetExternalIpAddresses, interface ITsSbTarget
- Services Bureau à distance de la propriété TargetExternalIpAddresses, interface ITsSbTarget
- Propriété adressesIP Services Bureau à distance
- Propriété adressesIP Services Bureau à distance, interface ITsSbTarget
- Services Bureau à distance de l’interface ITsSbTarget, propriété adressesIP
- Propriété adressesIP Services Bureau à distance, interface ITsSbTargetEx
- Services Bureau à distance de l’interface ITsSbTargetEx, propriété adressesIP
topic_type:
- apiref
api_name:
- ITsSbTarget.IpAddresses
- ITsSbTarget.get_IpAddresses
- ITsSbTarget.put_IpAddresses
- ITsSbTargetEx.IpAddresses
- ITsSbTargetEx.get_IpAddresses
- ITsSbTargetEx.put_IpAddresses
- TargetExternalIpAddresses
- ITsSbTarget.TargetExternalIpAddresses
- ITsSbTarget get_TargetExternalIpAddresses
- ITsSbTarget put_TargetExternalIpAddresses
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b3902840b24bc49ae3bda0510c8355afb67810
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380758"
---
# <a name="itssbtargetipaddresses-property"></a><span data-ttu-id="893c1-111">ITsSbTarget :: adressesIP, propriété</span><span class="sxs-lookup"><span data-stu-id="893c1-111">ITsSbTarget::IpAddresses property</span></span>

<span data-ttu-id="893c1-112">Récupère ou spécifie les adresses IP externes de la cible.</span><span class="sxs-lookup"><span data-stu-id="893c1-112">Retrieves or specifies the external IP addresses of the target.</span></span>

<span data-ttu-id="893c1-113">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="893c1-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="893c1-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="893c1-114">Syntax</span></span>


```C++
HRESULT put_IpAddresses(
  [in, size_is(numAddresses)]   TSSD_ConnectionPoint *sockaddr,
  [in]                          DWORD                numAddresses
);

HRESULT get_IpAddresses(
  [out, size_is(*numAddresses)] TSSD_ConnectionPoint *sockaddr,
  [in, out]                     DWORD                *numAddresses
);
```



## <a name="property-value"></a><span data-ttu-id="893c1-115">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="893c1-115">Property value</span></span>

<span data-ttu-id="893c1-116">Pointeur vers un tableau de structures [**TSSD \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) qui reçoivent les adresses IP externes de la cible.</span><span class="sxs-lookup"><span data-stu-id="893c1-116">A pointer to an array of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures that receive the external IP addresses of the target.</span></span>

<span data-ttu-id="893c1-117">Pointeur vers une variable **DWORD** qui contient le nombre d’adresses IP externes dans le paramètre *sockaddr* .</span><span class="sxs-lookup"><span data-stu-id="893c1-117">A pointer to a **DWORD** variable that contains the number of external IP addresses in the *sockaddr* parameter.</span></span> <span data-ttu-id="893c1-118">Si le nombre d’adresses est inconnu, transmettez *sockaddr* comme **null**.</span><span class="sxs-lookup"><span data-stu-id="893c1-118">If the number of addresses is unknown, pass *sockaddr* as **NULL**.</span></span> <span data-ttu-id="893c1-119">La méthode retourne le nombre de structures [**TSSD \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) nécessaires à l’allocation dans le tableau pointé par le paramètre *sockaddr* .</span><span class="sxs-lookup"><span data-stu-id="893c1-119">The method will return the number of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures necessary to allocate in the array pointed to by the *sockaddr* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="893c1-120">Notes</span><span class="sxs-lookup"><span data-stu-id="893c1-120">Remarks</span></span>

<span data-ttu-id="893c1-121">Cette propriété était anciennement appelée **TargetExternalIpAddresses** dans Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="893c1-121">This property was formerly known as **TargetExternalIpAddresses** in Windows Server 2008 R2.</span></span>

<span data-ttu-id="893c1-122">Si le nombre d’adresses IP externes est inconnu, vous pouvez appeler cette méthode avec *sockaddr* défini sur la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="893c1-122">If the number of external IP addresses is unknown, you can call this method with *sockaddr* set to **NULL**.</span></span> <span data-ttu-id="893c1-123">La méthode retourne ensuite, dans le paramètre *numAddresses* , le nombre de structures [**TSSD \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) nécessaires pour recevoir toutes les adresses IP externes.</span><span class="sxs-lookup"><span data-stu-id="893c1-123">The method will then return, in the *numAddresses* parameter, the number of [**TSSD\_ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) structures necessary to receive all the external IP addresses.</span></span> <span data-ttu-id="893c1-124">Allouez le tableau pour *sockaddr* en fonction de ce nombre, puis appelez à nouveau la méthode, en affectant à *sockaddr* le tableau nouvellement alloué et *numAddresses* au nombre retourné par le premier appel.</span><span class="sxs-lookup"><span data-stu-id="893c1-124">Allocate the array for *sockaddr* based on this number, and then call the method again, setting *sockaddr* to the newly allocated array and *numAddresses* to the number returned by the first call.</span></span>

## <a name="requirements"></a><span data-ttu-id="893c1-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="893c1-125">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="893c1-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="893c1-126">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="893c1-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="893c1-127">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="893c1-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="893c1-128">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="893c1-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="893c1-129">Windows Server 2012</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="893c1-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="893c1-130">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="893c1-131"><dt>Sbtsv. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="893c1-131"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="893c1-132">IID</span><span class="sxs-lookup"><span data-stu-id="893c1-132">IID</span></span><br/></td>
<td><span data-ttu-id="893c1-133">IID_ITsSbTarget est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="893c1-133">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="893c1-134">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="893c1-134">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="893c1-135">e85e10ea-DB0B-4752-B456-5fd5840901c0 sur Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="893c1-135">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="893c1-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="893c1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="893c1-137">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="893c1-137">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="893c1-138">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="893c1-138">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[<span data-ttu-id="893c1-139">**TSSD \_ ConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="893c1-139">**TSSD\_ConnectionPoint**</span></span>](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)
</dt> </dl>

 

 





