---
description: arrête le service.
ms.assetid: ac6b8df2-e2f2-47df-8c1e-07460a15e8e2
title: Méthode StopService de la classe Msvm_TransparentBridgingService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 118954217cadf12b69cf3a2b1ec52b2c02cae226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114207"
---
# <a name="stopservice-method-of-the-msvm_transparentbridgingservice-class"></a><span data-ttu-id="551a5-103">Méthode StopService de la \_ classe MSVM TransparentBridgingService</span><span class="sxs-lookup"><span data-stu-id="551a5-103">StopService method of the Msvm\_TransparentBridgingService class</span></span>

<span data-ttu-id="551a5-104">arrête le service.</span><span class="sxs-lookup"><span data-stu-id="551a5-104">Stops the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="551a5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="551a5-105">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="551a5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="551a5-106">Parameters</span></span>

<span data-ttu-id="551a5-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="551a5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="551a5-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="551a5-108">Return value</span></span>

<span data-ttu-id="551a5-109">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="551a5-109">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="551a5-110">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="551a5-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="551a5-111">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="551a5-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="551a5-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="551a5-112">Requirements</span></span>



| <span data-ttu-id="551a5-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="551a5-113">Requirement</span></span> | <span data-ttu-id="551a5-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="551a5-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="551a5-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="551a5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="551a5-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="551a5-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="551a5-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="551a5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="551a5-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="551a5-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="551a5-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="551a5-119">Namespace</span></span><br/>                | <span data-ttu-id="551a5-120">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="551a5-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="551a5-121">MOF</span><span class="sxs-lookup"><span data-stu-id="551a5-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="551a5-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="551a5-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="551a5-123">DLL</span><span class="sxs-lookup"><span data-stu-id="551a5-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="551a5-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="551a5-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="551a5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="551a5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="551a5-126">**MSVM \_ TransparentBridgingService**</span><span class="sxs-lookup"><span data-stu-id="551a5-126">**Msvm\_TransparentBridgingService**</span></span>](msvm-transparentbridgingservice.md)
</dt> </dl>

 

 




