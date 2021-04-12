---
description: La méthode Configure doit être implémentée par le moniteur. Le MCSVC appelle cette méthode pour obtenir les informations de configuration de la capture.
ms.assetid: bc2a3246-28dc-4452-a98e-a8a2447bb127
title: IMonitor ::D méthode oConfigure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoConfigure
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: e9a0ba2ade1095f291d5cb325a0902e6caeac3f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112799"
---
# <a name="imonitordoconfigure-method"></a><span data-ttu-id="92f4c-104">IMonitor ::D méthode oConfigure</span><span class="sxs-lookup"><span data-stu-id="92f4c-104">IMonitor::DoConfigure method</span></span>

<span data-ttu-id="92f4c-105">La méthode **configure** doit être implémentée par le moniteur.</span><span class="sxs-lookup"><span data-stu-id="92f4c-105">The **DoConfigure** method must be implemented by the monitor.</span></span> <span data-ttu-id="92f4c-106">Le MCSVC appelle cette méthode pour obtenir les informations de configuration de la capture.</span><span class="sxs-lookup"><span data-stu-id="92f4c-106">The MCSVC calls this method to obtain configuration information for the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="92f4c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92f4c-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE DoConfigure(
  [in]  char *pName,
  [in]  char *pConfiguration,
  [out] char **ppScriptInstance
);
```



## <a name="parameters"></a><span data-ttu-id="92f4c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92f4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92f4c-109">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="92f4c-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92f4c-110">Nom d’une instance du moniteur.</span><span class="sxs-lookup"><span data-stu-id="92f4c-110">Name of an instance of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="92f4c-111">*pConfiguration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="92f4c-111">*pConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92f4c-112">Chaîne de configuration fournie par MCSVC.</span><span class="sxs-lookup"><span data-stu-id="92f4c-112">Configuration string provided by the MCSVC.</span></span> <span data-ttu-id="92f4c-113">L’analyse doit analyser cette chaîne pour les données de configuration.</span><span class="sxs-lookup"><span data-stu-id="92f4c-113">The monitor must parse this string for configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="92f4c-114">*ppScriptInstance* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="92f4c-114">*ppScriptInstance* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92f4c-115">Adresse de la chaîne HTML utilisée pour configurer l’analyse.</span><span class="sxs-lookup"><span data-stu-id="92f4c-115">Address of the HTML string used to configure the monitor.</span></span> <span data-ttu-id="92f4c-116">Si un script par défaut est utilisé pour la configuration, cette valeur doit être définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="92f4c-116">If a default script is used for configuration, this value should be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92f4c-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="92f4c-117">Return value</span></span>

<span data-ttu-id="92f4c-118">Si la méthode réussit, la valeur de retour est \_ OK (ce qui correspond à la même erreur) et MCSVC exécute l’analyse.</span><span class="sxs-lookup"><span data-stu-id="92f4c-118">If the method is successful, the return value is S\_OK (which is the same as NOERROR), and the MCSVC will run the monitor.</span></span>

<span data-ttu-id="92f4c-119">Si la méthode échoue, la valeur de retour est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="92f4c-119">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="92f4c-120">Une valeur de retour de \_ la configuration de l’analyseur de NMERR \_ \_ a échoué, mais lorsque cette erreur est retournée, le moniteur ne peut pas démarrer tant qu’un appel de **configuration** ultérieure n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="92f4c-120">A return value of NMERR\_MONITOR\_CONFIG\_FAILED is acceptable, but when this error is returned, the monitor cannot start until a future **DoConfigure** call succeeds.</span></span> <span data-ttu-id="92f4c-121">Toute autre erreur empêche l’activation de l’instance du moniteur.</span><span class="sxs-lookup"><span data-stu-id="92f4c-121">Any other error prevents the instance of the monitor from being enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="92f4c-122">Notes</span><span class="sxs-lookup"><span data-stu-id="92f4c-122">Remarks</span></span>

<span data-ttu-id="92f4c-123">Le MCSVC appelle cette méthode une fois qu’il s’est connecté au réseau et avant l’appel de la méthode [IRTC :: configure](irtc-configure.md) .</span><span class="sxs-lookup"><span data-stu-id="92f4c-123">The MCSVC calls this method after it has connected to the network and before the [IRTC::Configure](irtc-configure.md) method is called.</span></span>

<span data-ttu-id="92f4c-124">Le moniteur peut stocker les informations fournies par cet appel, mettre à jour le script HTML ou la chaîne de configuration, et définir le [filtre de capture](capture-filters.md) dans l’objet BLOB NPP.</span><span class="sxs-lookup"><span data-stu-id="92f4c-124">The monitor can store information provided by this call, update the HTML script or configuration string, and set the [capture filter](capture-filters.md) in the NPP BLOB.</span></span>

<span data-ttu-id="92f4c-125">Le MCSVC peut appeler cette méthode plusieurs fois, mais il ne peut pas être appelé pendant que l’analyse capture des données.</span><span class="sxs-lookup"><span data-stu-id="92f4c-125">The MCSVC may call this method several times, but it cannot be not called while the monitor is capturing data.</span></span> <span data-ttu-id="92f4c-126">Notez que chaque fois qu’un [NPP](network-packet-providers.md) démarre une capture, la connexion au réseau doit être configurée.</span><span class="sxs-lookup"><span data-stu-id="92f4c-126">Note that every time an [NPP](network-packet-providers.md) starts a capture, the connection to the network must be configured.</span></span> <span data-ttu-id="92f4c-127">Cette restriction comprend les situations dans lesquelles le NPP démarre et arrête la même capture.</span><span class="sxs-lookup"><span data-stu-id="92f4c-127">This restriction includes situations in which the NPP starts and stops the same capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="92f4c-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92f4c-128">Requirements</span></span>



| <span data-ttu-id="92f4c-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92f4c-129">Requirement</span></span> | <span data-ttu-id="92f4c-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="92f4c-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="92f4c-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92f4c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="92f4c-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92f4c-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="92f4c-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92f4c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="92f4c-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92f4c-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="92f4c-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="92f4c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="92f4c-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="92f4c-136"><dt>Netmon.h</dt></span></span> </dl> |



 

 




