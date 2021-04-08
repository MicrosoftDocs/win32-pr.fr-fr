---
title: Propriété ITsSbEnvironment Name
description: Récupère une valeur qui indique le nom de l’environnement qui héberge l’ordinateur cible.
ms.assetid: 8104bdae-f445-425b-b326-cc3333839d29
ms.tgt_platform: multiple
keywords:
- Propriété Name Services Bureau à distance
- Name, propriété Services Bureau à distance, ITsSbEnvironment, interface
- Services Bureau à distance de l’interface ITsSbEnvironment, propriété Name
topic_type:
- apiref
api_name:
- ITsSbEnvironment.Name
- ITsSbEnvironment.get_Name
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b5ac2fd725ec07102c08e93b2bfb39dabe701ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941870"
---
# <a name="itssbenvironmentname-property"></a><span data-ttu-id="79be7-106">ITsSbEnvironment :: Name, propriété</span><span class="sxs-lookup"><span data-stu-id="79be7-106">ITsSbEnvironment::Name property</span></span>

<span data-ttu-id="79be7-107">Récupère une valeur qui indique le nom de l’environnement qui héberge l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="79be7-107">Retrieves a value that indicates the name of the environment that hosts the target computer.</span></span>

<span data-ttu-id="79be7-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="79be7-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="79be7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79be7-109">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="79be7-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="79be7-110">Property value</span></span>

<span data-ttu-id="79be7-111">Pointeur vers une variable **BSTR** qui contient le nom de l’environnement.</span><span class="sxs-lookup"><span data-stu-id="79be7-111">A pointer to a **BSTR** variable that contains the name of the environment.</span></span>

## <a name="remarks"></a><span data-ttu-id="79be7-112">Notes</span><span class="sxs-lookup"><span data-stu-id="79be7-112">Remarks</span></span>

<span data-ttu-id="79be7-113">Cette méthode retourne une chaîne qui n’est pas utilisée directement par Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="79be7-113">This method returns a string that is not directly used by Remote Desktop Connection Broker (RD Connection Broker).</span></span> <span data-ttu-id="79be7-114">Le Service Broker pour les connexions Bureau à distance transmet cette chaîne aux plug-ins de ressources.</span><span class="sxs-lookup"><span data-stu-id="79be7-114">RD Connection Broker passes this string to resource plug-ins.</span></span>

## <a name="requirements"></a><span data-ttu-id="79be7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79be7-115">Requirements</span></span>



| <span data-ttu-id="79be7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79be7-116">Requirement</span></span> | <span data-ttu-id="79be7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="79be7-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="79be7-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79be7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="79be7-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="79be7-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="79be7-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79be7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="79be7-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="79be7-121">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="79be7-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="79be7-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="79be7-123"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="79be7-123"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79be7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79be7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79be7-125">**ITsSbEnvironment**</span><span class="sxs-lookup"><span data-stu-id="79be7-125">**ITsSbEnvironment**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> </dl>

 

 





