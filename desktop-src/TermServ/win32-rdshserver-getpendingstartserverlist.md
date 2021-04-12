---
title: Méthode GetPendingStartServerList de la classe Win32_RDSHServer
description: Récupère une liste de serveurs en attente de démarrage.
ms.assetid: 7af7a0e7-dc00-4e3a-8e0c-5987bd2bc3a2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetPendingStartServerList
- Services Bureau à distance de la méthode GetPendingStartServerList, classe Win32_RDSHServer
- Win32_RDSHServer de la classe Services Bureau à distance, méthode GetPendingStartServerList
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetPendingStartServerList
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99b96453b33f931b18d89f13413513d3baf82bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384756"
---
# <a name="getpendingstartserverlist-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="8d26a-106">Méthode GetPendingStartServerList de la \_ classe Win32 RDSHServer</span><span class="sxs-lookup"><span data-stu-id="8d26a-106">GetPendingStartServerList method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="8d26a-107">Récupère une liste de serveurs en attente de démarrage.</span><span class="sxs-lookup"><span data-stu-id="8d26a-107">Retrieves a list of server waiting to start.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d26a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d26a-108">Syntax</span></span>


```mof
uint32 GetPendingStartServerList(
  [in]  uint32 maxServers,
  [out] string ServerFQDNs[]
);
```



## <a name="parameters"></a><span data-ttu-id="8d26a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d26a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d26a-110">*maxServers* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d26a-110">*maxServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d26a-111">Nombre maximal de serveurs à retourner dans la liste.</span><span class="sxs-lookup"><span data-stu-id="8d26a-111">The maximum number of servers to return in the list.</span></span>

</dd> <dt>

<span data-ttu-id="8d26a-112">*ServerFQDNs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8d26a-112">*ServerFQDNs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d26a-113">En cas de réussite, contient une collection de noms de domaine complets des serveurs en attente de démarrage.</span><span class="sxs-lookup"><span data-stu-id="8d26a-113">On success, contains a collection of fully-qualified domain names of the servers waiting to start.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d26a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8d26a-114">Remarks</span></span>

<span data-ttu-id="8d26a-115">La liste des serveurs est réinitialisée après chaque appel, de sorte que l’appel suivant n’obtiendra pas de serveur dupliqué.</span><span class="sxs-lookup"><span data-stu-id="8d26a-115">The list of servers is reset after every call, so that the next call will not get a duplicate server.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d26a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d26a-116">Requirements</span></span>



| <span data-ttu-id="8d26a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d26a-117">Requirement</span></span> | <span data-ttu-id="8d26a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d26a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d26a-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d26a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8d26a-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d26a-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="8d26a-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d26a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8d26a-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8d26a-122">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="8d26a-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8d26a-123">Namespace</span></span><br/>                | <span data-ttu-id="8d26a-124">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="8d26a-124">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="8d26a-125">MOF</span><span class="sxs-lookup"><span data-stu-id="8d26a-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d26a-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d26a-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d26a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8d26a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d26a-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d26a-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="8d26a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d26a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d26a-130">**\_RDSHServer Win32**</span><span class="sxs-lookup"><span data-stu-id="8d26a-130">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





