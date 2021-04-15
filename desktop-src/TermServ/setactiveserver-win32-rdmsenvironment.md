---
title: Méthode SetActiveServer de la classe Win32_RDMSEnvironment
description: Définit le nom de domaine complet de l’environnement des services de gestion de Bureau à distance (RDMS) sur le nœud actuel.
ms.assetid: ed7b71cf-c3a4-4d2f-856a-31332f94fac9
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetActiveServer
- Services Bureau à distance de la méthode SetActiveServer, classe Win32_RDMSEnvironment
- Win32_RDMSEnvironment de la classe Services Bureau à distance, méthode SetActiveServer
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f11b378b15e271200c730691c3654fd10e80f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465110"
---
# <a name="setactiveserver-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="fe0a6-106">Méthode SetActiveServer de la \_ classe Win32 RDMSEnvironment</span><span class="sxs-lookup"><span data-stu-id="fe0a6-106">SetActiveServer method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="fe0a6-107">Définit le nom de domaine complet de l’environnement des services de gestion de Bureau à distance (RDMS) sur le nœud actuel.</span><span class="sxs-lookup"><span data-stu-id="fe0a6-107">Sets the FQDN of the Remote Desktop Management Services (RDMS) environment to the current node.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe0a6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe0a6-108">Syntax</span></span>


```mof
uint32 SetActiveServer();
```



## <a name="parameters"></a><span data-ttu-id="fe0a6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe0a6-109">Parameters</span></span>

<span data-ttu-id="fe0a6-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="fe0a6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe0a6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fe0a6-111">Return value</span></span>

<span data-ttu-id="fe0a6-112">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="fe0a6-112">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe0a6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe0a6-113">Requirements</span></span>



| <span data-ttu-id="fe0a6-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe0a6-114">Requirement</span></span> | <span data-ttu-id="fe0a6-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe0a6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe0a6-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe0a6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fe0a6-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe0a6-117">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="fe0a6-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe0a6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fe0a6-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fe0a6-119">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="fe0a6-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fe0a6-120">Namespace</span></span><br/>                | <span data-ttu-id="fe0a6-121">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="fe0a6-121">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="fe0a6-122">MOF</span><span class="sxs-lookup"><span data-stu-id="fe0a6-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe0a6-123"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe0a6-123"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe0a6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="fe0a6-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe0a6-125"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe0a6-125"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="fe0a6-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe0a6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe0a6-127">**\_RDMSEnvironment Win32**</span><span class="sxs-lookup"><span data-stu-id="fe0a6-127">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





