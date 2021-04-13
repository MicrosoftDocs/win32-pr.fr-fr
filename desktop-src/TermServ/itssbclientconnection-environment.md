---
title: Propriété d’environnement ITsSbClientConnection
description: Récupère un objet qui contient des informations sur l’environnement qui héberge l’ordinateur cible.
ms.assetid: 97fe4851-96a9-4b23-8ad7-f42b87c655d0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriété d’environnement
- Services Bureau à distance de propriété d’environnement, interface ITsSbClientConnection
- Services Bureau à distance de l’interface ITsSbClientConnection, propriété d’environnement
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Environment
- ITsSbClientConnection.get_Environment
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18018c8f8fc5e7d017809cf5fe109db7c52712c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465979"
---
# <a name="itssbclientconnectionenvironment-property"></a><span data-ttu-id="d57f4-106">ITsSbClientConnection :: Environment, propriété</span><span class="sxs-lookup"><span data-stu-id="d57f4-106">ITsSbClientConnection::Environment property</span></span>

<span data-ttu-id="d57f4-107">Récupère un objet qui contient des informations sur l’environnement qui héberge l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="d57f4-107">Retrieves an object that contains information about the environment that hosts the target computer.</span></span> <span data-ttu-id="d57f4-108">Par exemple, dans un scénario de bureau virtuel, cet objet contient des informations sur l’ordinateur qui héberge l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="d57f4-108">For example, in a virtual desktop scenario, this object would contain information about the computer that hosts the virtual machine.</span></span>

<span data-ttu-id="d57f4-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d57f4-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d57f4-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d57f4-110">Syntax</span></span>


```C++
HRESULT get_Environment(
  [out, retval] ITsSbEnvironment **ppEnvironment
);
```



## <a name="property-value"></a><span data-ttu-id="d57f4-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d57f4-111">Property value</span></span>

<span data-ttu-id="d57f4-112">Pointeur vers un pointeur vers un objet d’environnement [**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) .</span><span class="sxs-lookup"><span data-stu-id="d57f4-112">A pointer to a pointer to an [**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) environment object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d57f4-113">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="d57f4-113">Error codes</span></span>

<span data-ttu-id="d57f4-114">Si la méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d57f4-114">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d57f4-115">Sinon, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="d57f4-115">Otherwise, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="d57f4-116">Les valeurs possibles incluent, mais ne sont pas limitées à, celles figurant dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="d57f4-116">Possible values include, but are not limited to, those in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d57f4-117">\_pointeur E</span><span class="sxs-lookup"><span data-stu-id="d57f4-117">E\_POINTER</span></span>
</dt> <dd>

<span data-ttu-id="d57f4-118">L’environnement est introuvable.</span><span class="sxs-lookup"><span data-stu-id="d57f4-118">The environment was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d57f4-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d57f4-119">Remarks</span></span>

<span data-ttu-id="d57f4-120">Un plug-in d’orchestration peut appeler cette méthode pour récupérer des informations d’environnement sur une machine virtuelle cible.</span><span class="sxs-lookup"><span data-stu-id="d57f4-120">An orchestration plug-in can call this method to retrieve environment information about a target virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="d57f4-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d57f4-121">Requirements</span></span>



| <span data-ttu-id="d57f4-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d57f4-122">Requirement</span></span> | <span data-ttu-id="d57f4-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d57f4-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d57f4-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d57f4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d57f4-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d57f4-125">None supported</span></span><br/>                                                            |
| <span data-ttu-id="d57f4-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d57f4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d57f4-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d57f4-127">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="d57f4-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="d57f4-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d57f4-129"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d57f4-129"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d57f4-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d57f4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d57f4-131">**ITsSbClientConnection**</span><span class="sxs-lookup"><span data-stu-id="d57f4-131">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

 





