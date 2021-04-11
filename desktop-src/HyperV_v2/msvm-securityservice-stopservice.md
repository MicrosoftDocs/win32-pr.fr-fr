---
description: arrête le service.
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
ms.openlocfilehash: 68e88e2c88d4f75f4d7671c389bab0cd81d0deb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203607"
---
# <a name="stopservice-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="9b470-103">Méthode StopService de la \_ classe MSVM securityservice</span><span class="sxs-lookup"><span data-stu-id="9b470-103">StopService method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="9b470-104">arrête le service.</span><span class="sxs-lookup"><span data-stu-id="9b470-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b470-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b470-105">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="9b470-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b470-106">Parameters</span></span>

<span data-ttu-id="9b470-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9b470-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9b470-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9b470-108">Return value</span></span>

<span data-ttu-id="9b470-109">En cas de réussite, retourne 0 ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="9b470-109">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="9b470-110">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="9b470-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9b470-111">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="9b470-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9b470-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b470-112">Requirements</span></span>



| <span data-ttu-id="9b470-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b470-113">Requirement</span></span> | <span data-ttu-id="9b470-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b470-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b470-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b470-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9b470-116">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b470-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9b470-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b470-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9b470-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9b470-118">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9b470-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9b470-119">Namespace</span></span><br/>                | <span data-ttu-id="9b470-120">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9b470-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9b470-121">MOF</span><span class="sxs-lookup"><span data-stu-id="9b470-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b470-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b470-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b470-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9b470-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b470-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9b470-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9b470-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b470-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b470-126">**MSVM \_ securityservice**</span><span class="sxs-lookup"><span data-stu-id="9b470-126">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




