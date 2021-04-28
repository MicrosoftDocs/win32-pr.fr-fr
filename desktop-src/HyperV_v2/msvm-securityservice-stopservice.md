---
description: 'Méthode StopService de la classe Msvm_SecurityService : arrête le service.'
ms.assetid: cf100cea-b0e1-42e9-831e-6422aded47c5
title: Méthode StopService de la classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a9a16fef951fdee5ed7fc580da61f43d848a8dec
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118707"
---
# <a name="stopservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="500e0-103">Méthode StopService de la \_ classe MSVM securityservice</span><span class="sxs-lookup"><span data-stu-id="500e0-103">StopService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="500e0-104">arrête le service.</span><span class="sxs-lookup"><span data-stu-id="500e0-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="500e0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="500e0-105">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="500e0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="500e0-106">Parameters</span></span>

<span data-ttu-id="500e0-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="500e0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="500e0-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="500e0-108">Return value</span></span>

<span data-ttu-id="500e0-109">En cas de réussite, retourne 0 ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="500e0-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="500e0-110">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="500e0-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="500e0-111">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="500e0-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="500e0-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="500e0-112">Requirements</span></span>



| <span data-ttu-id="500e0-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="500e0-113">Requirement</span></span> | <span data-ttu-id="500e0-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="500e0-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="500e0-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="500e0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="500e0-116">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="500e0-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="500e0-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="500e0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="500e0-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="500e0-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="500e0-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="500e0-119">Namespace</span></span><br/>                | <span data-ttu-id="500e0-120">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="500e0-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="500e0-121">MOF</span><span class="sxs-lookup"><span data-stu-id="500e0-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="500e0-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="500e0-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="500e0-123">DLL</span><span class="sxs-lookup"><span data-stu-id="500e0-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="500e0-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="500e0-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="500e0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="500e0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="500e0-126">**MSVM \_ securityservice**</span><span class="sxs-lookup"><span data-stu-id="500e0-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




