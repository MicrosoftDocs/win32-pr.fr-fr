---
title: PxeProviderInitialize fonction de rappel
description: Exportation à partir d’une bibliothèque de liens dynamiques (DLL) de fournisseur qui initialise le fournisseur et la prépare à recevoir des demandes du client.
ms.assetid: 433b051c-9fde-4589-92e2-58d3774826ac
keywords:
- Fonction de rappel PxeProviderInitialize des services de déploiement Windows
topic_type:
- apiref
api_name:
- PxeProviderInitialize
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b8d8fed4c1cc91c2090b957894b4f6641adad32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509356"
---
# <a name="pxeproviderinitialize-callback-function"></a><span data-ttu-id="1fdb6-104">PxeProviderInitialize fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="1fdb6-104">PxeProviderInitialize callback function</span></span>

<span data-ttu-id="1fdb6-105">Exportation à partir d’une bibliothèque de liens dynamiques (DLL) de fournisseur qui initialise le fournisseur et la prépare à recevoir des demandes du client.</span><span class="sxs-lookup"><span data-stu-id="1fdb6-105">An export from a provider dynamic-link library (DLL) that initializes the provider and prepares it to receive client requests.</span></span> <span data-ttu-id="1fdb6-106">Les fournisseurs sont requis pour exporter la fonction *PxeProviderInitialize* .</span><span class="sxs-lookup"><span data-stu-id="1fdb6-106">Providers are required to export the *PxeProviderInitialize* function.</span></span> <span data-ttu-id="1fdb6-107">Tous les rappels du fournisseur doivent être inscrits avec un appel à la fonction [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) pendant le traitement de *PxeProviderInitialize*.</span><span class="sxs-lookup"><span data-stu-id="1fdb6-107">Any callbacks to the provider must be registered with a call to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function during the processing of *PxeProviderInitialize*.</span></span> <span data-ttu-id="1fdb6-108">Au retour de cette fonction, le fournisseur doit être entièrement initialisé et prêt à traiter les demandes des clients.</span><span class="sxs-lookup"><span data-stu-id="1fdb6-108">On the return of this function, the provider must be fully initialized and ready to process client requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fdb6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1fdb6-109">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderInitialize(
  _In_ HANDLE hProvider,
  _In_ HKEY   hProviderKey
);
```



## <a name="parameters"></a><span data-ttu-id="1fdb6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1fdb6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fdb6-111">*hProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1fdb6-111">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fdb6-112">Handle de l’instance du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1fdb6-112">Handle to the provider instance.</span></span> <span data-ttu-id="1fdb6-113">Ce descripteur doit être stocké par le fournisseur et utilisé dans les appels suivants.</span><span class="sxs-lookup"><span data-stu-id="1fdb6-113">This handle must be stored by the provider and used in any subsequent calls.</span></span> <span data-ttu-id="1fdb6-114">Ce handle est valide jusqu’à ce que la fonction de rappel [*PxeProviderShutdown*](pxeprovidershutdown.md) soit appelée.</span><span class="sxs-lookup"><span data-stu-id="1fdb6-114">This handle is valid until the [*PxeProviderShutdown*](pxeprovidershutdown.md) callback function is called.</span></span>

</dd> <dt>

<span data-ttu-id="1fdb6-115">*hProviderKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1fdb6-115">*hProviderKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fdb6-116">Handle d’une clé de Registre dans laquelle les informations de configuration du fournisseur doivent être stockées.</span><span class="sxs-lookup"><span data-stu-id="1fdb6-116">Handle to a registry key where provider configuration information is to be stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fdb6-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1fdb6-117">Return value</span></span>

<span data-ttu-id="1fdb6-118">Si l’initialisation du fournisseur réussit, le rappel doit retourner **la \_ réussite** de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1fdb6-118">If the provider initialization succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="1fdb6-119">En cas d’échec, un code d’erreur approprié doit être retourné.</span><span class="sxs-lookup"><span data-stu-id="1fdb6-119">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fdb6-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1fdb6-120">Requirements</span></span>



| <span data-ttu-id="1fdb6-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1fdb6-121">Requirement</span></span> | <span data-ttu-id="1fdb6-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fdb6-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1fdb6-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fdb6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1fdb6-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fdb6-124">None supported</span></span><br/>                                                          |
| <span data-ttu-id="1fdb6-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fdb6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1fdb6-126">Windows Server 2008, Windows Server 2003 avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1fdb6-126">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1fdb6-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fdb6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fdb6-128">Fonctions du serveur des services de déploiement Windows</span><span class="sxs-lookup"><span data-stu-id="1fdb6-128">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="1fdb6-129">*PxeProviderShutdown*</span><span class="sxs-lookup"><span data-stu-id="1fdb6-129">*PxeProviderShutdown*</span></span>](pxeprovidershutdown.md)
</dt> </dl>

 

 





