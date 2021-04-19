---
title: CBCreateClientInstance, fonction (Cbclient. h)
description: Crée une instance du client RPC Connexion Bureau à distance Broker.
ms.assetid: 700E47BC-C547-44AB-8607-B9797D542AA7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la fonction CBCreateClientInstance
topic_type:
- apiref
api_name:
- CBCreateClientInstance
api_location:
- Cbclient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2b30f2d236bcc90dfa4977f54d56a5d1717d18a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542794"
---
# <a name="cbcreateclientinstance-function"></a><span data-ttu-id="59d8a-104">CBCreateClientInstance fonction)</span><span class="sxs-lookup"><span data-stu-id="59d8a-104">CBCreateClientInstance function</span></span>

<span data-ttu-id="59d8a-105">Crée une instance du client RPC Connexion Bureau à distance Broker.</span><span class="sxs-lookup"><span data-stu-id="59d8a-105">Creates an instance of the Remote Desktop Connection Broker RPC client.</span></span>

## <a name="syntax"></a><span data-ttu-id="59d8a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59d8a-106">Syntax</span></span>


```C++
HRESULT CBCreateClientInstance(
  _In_  DWORD                   Version,
  _Out_ IConnectionBrokerClient **ppCbClient
);
```



## <a name="parameters"></a><span data-ttu-id="59d8a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59d8a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59d8a-108">*Version* \[ de dans\]</span><span class="sxs-lookup"><span data-stu-id="59d8a-108">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59d8a-109">Spécifie la version de l’interface du client Connexion Bureau à distance Broker demandée.</span><span class="sxs-lookup"><span data-stu-id="59d8a-109">Specifies the version of the Remote Desktop Connection Broker client interface being requested.</span></span> <span data-ttu-id="59d8a-110">Il doit s’agir de la valeur suivante.</span><span class="sxs-lookup"><span data-stu-id="59d8a-110">This must be the following value.</span></span>

<dt>

<span data-ttu-id="59d8a-111">1</span><span class="sxs-lookup"><span data-stu-id="59d8a-111">1</span></span>
</dt> <dd>

<span data-ttu-id="59d8a-112">Version 1 du client Connexion Bureau à distance Broker.</span><span class="sxs-lookup"><span data-stu-id="59d8a-112">Version 1 of the Remote Desktop Connection Broker client.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="59d8a-113">*ppCbClient* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="59d8a-113">*ppCbClient* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59d8a-114">Adresse d’un pointeur d’interface [**IConnectionBrokerClient**](iconnectionbrokerclient.md) qui reçoit l’objet client Connexion Bureau à distance Broker.</span><span class="sxs-lookup"><span data-stu-id="59d8a-114">The address of an [**IConnectionBrokerClient**](iconnectionbrokerclient.md) interface pointer that receives the Remote Desktop Connection Broker client object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59d8a-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59d8a-115">Return value</span></span>

<span data-ttu-id="59d8a-116">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="59d8a-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="59d8a-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="59d8a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="59d8a-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59d8a-118">Requirements</span></span>



| <span data-ttu-id="59d8a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59d8a-119">Requirement</span></span> | <span data-ttu-id="59d8a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="59d8a-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59d8a-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="59d8a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="59d8a-122"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="59d8a-122"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="59d8a-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="59d8a-123">Library</span></span><br/> | <dl> <span data-ttu-id="59d8a-124"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59d8a-124"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="59d8a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="59d8a-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="59d8a-126"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59d8a-126"><dt>Cbclient.dll</dt></span></span> </dl> |



 

 





