---
title: ITsSbTarget propriété TargetLoad
description: Récupère le chargement relatif sur une cible.
ms.assetid: 56618dcf-1319-4310-80ba-7ed71b8b02e8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété TargetLoad
- Services Bureau à distance de la propriété TargetLoad, interface ITsSbTarget
- Services Bureau à distance de l’interface ITsSbTarget, propriété TargetLoad
- Services Bureau à distance de la propriété TargetLoad, interface ITsSbTargetEx
- Services Bureau à distance de l’interface ITsSbTargetEx, propriété TargetLoad
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetLoad
- ITsSbTarget.get_TargetLoad
- ITsSbTargetEx.TargetLoad
- ITsSbTargetEx.get_TargetLoad
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddfc9be9805406ab76b166e2a34bc47a7f5e9ab5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678589"
---
# <a name="itssbtargettargetload-property"></a><span data-ttu-id="294c2-108">ITsSbTarget :: TargetLoad, propriété</span><span class="sxs-lookup"><span data-stu-id="294c2-108">ITsSbTarget::TargetLoad property</span></span>

<span data-ttu-id="294c2-109">Récupère le chargement relatif sur une cible.</span><span class="sxs-lookup"><span data-stu-id="294c2-109">Retrieves the relative load on a target.</span></span> <span data-ttu-id="294c2-110">Cette valeur est basée sur le nombre de sessions existantes et en attente.</span><span class="sxs-lookup"><span data-stu-id="294c2-110">This value is based on the number of existing and pending sessions.</span></span> <span data-ttu-id="294c2-111">Par défaut, une session en attente a la même valeur qu’une session existante.</span><span class="sxs-lookup"><span data-stu-id="294c2-111">By default a pending session has the same value as an existing session.</span></span>

<span data-ttu-id="294c2-112">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="294c2-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="294c2-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="294c2-113">Syntax</span></span>


```C++
HRESULT get_TargetLoad(
  [out, retval] DWORD *pTargetLoad
);
```



## <a name="property-value"></a><span data-ttu-id="294c2-114">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="294c2-114">Property value</span></span>

<span data-ttu-id="294c2-115">Nombre représentant la charge relative sur une cible.</span><span class="sxs-lookup"><span data-stu-id="294c2-115">A number representing the relative load on a target.</span></span>

## <a name="remarks"></a><span data-ttu-id="294c2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="294c2-116">Remarks</span></span>

<span data-ttu-id="294c2-117">Le poids d’une session en attente par rapport à une session active peut être modifié en définissant la valeur du paramètre *lb \_ ConnectionEstablishmentPenalty* pour le Service Broker pour les connexions.</span><span class="sxs-lookup"><span data-stu-id="294c2-117">The weight of a pending session relative to an active session can be changed by setting the value of the *LB\_ConnectionEstablishmentPenalty* parameter for the Connection Broker.</span></span> <span data-ttu-id="294c2-118">Ce paramètre se trouve sous la clé de Registre **HKLM \\ System \\ CurrentControlSet \\ services \\ Tssdis \\ Parameters** .</span><span class="sxs-lookup"><span data-stu-id="294c2-118">This parameter is located under the **HKLM\\System\\CurrentControlSet\\Services\\Tssdis\\Parameters** registry key.</span></span> <span data-ttu-id="294c2-119">La valeur par défaut 1 indique que les sessions en attente ont le même poids que les sessions actives.</span><span class="sxs-lookup"><span data-stu-id="294c2-119">The default value of 1 specifies that pending sessions have the same weight as active sessions.</span></span>

<span data-ttu-id="294c2-120">Cette propriété est disponible sur Windows Server 2012 R2 avec [KB3091411](https://support.microsoft.com/kb/3091411) installé dans l’interface [**ITsSbTargetEx**](itssbtargetex.md) .</span><span class="sxs-lookup"><span data-stu-id="294c2-120">This property is available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbTargetEx**](itssbtargetex.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="294c2-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="294c2-121">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="294c2-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="294c2-122">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="294c2-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="294c2-123">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="294c2-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="294c2-124">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="294c2-125">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="294c2-125">Windows Server 2016</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="294c2-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="294c2-126">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="294c2-127"><dt>Sbtsv. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="294c2-127"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="294c2-128">IID</span><span class="sxs-lookup"><span data-stu-id="294c2-128">IID</span></span><br/></td>
<td><span data-ttu-id="294c2-129">IID_ITsSbTarget est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="294c2-129">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="294c2-130">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="294c2-130">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="294c2-131">e85e10ea-DB0B-4752-B456-5fd5840901c0 sur Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="294c2-131">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="294c2-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="294c2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="294c2-133">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="294c2-133">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="294c2-134">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="294c2-134">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





