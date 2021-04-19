---
description: Place le service dans l’état Démarré.
ms.assetid: 8977b806-150c-4ddc-a471-3fdafdcb4a55
title: Méthode StartService de la classe CIM_Service (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 73b89f7fc789639fb45acbde61da4c7962650177
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529671"
---
# <a name="startservice-method-of-the-cim_service-class-hyper-v-management"></a><span data-ttu-id="cad72-103">Méthode StartService de la classe CIM_Service (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="cad72-103">StartService method of the CIM_Service class (Hyper-V management)</span></span>

<span data-ttu-id="cad72-104">Place le service dans l’état Démarré.</span><span class="sxs-lookup"><span data-stu-id="cad72-104">Places the service in the started state.</span></span>

> [!Note]
>
> <span data-ttu-id="cad72-105">La sémantique de cette méthode se chevauche avec la méthode **RequestStateChange** héritée de [**la \_ EnabledLogicalElement CIM**](cim-enabledlogicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cad72-105">The semantics of this method overlap with the **RequestStateChange** method that is inherited from [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).</span></span> <span data-ttu-id="cad72-106">Cette méthode est conservée, car elle a été largement implémentée et sa sémantique « Start » simple est pratique à utiliser.</span><span class="sxs-lookup"><span data-stu-id="cad72-106">This method is maintained because it has been widely implemented, and its simple "start" semantics are convenient to use.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="cad72-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cad72-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="cad72-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cad72-108">Parameters</span></span>

<span data-ttu-id="cad72-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="cad72-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cad72-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cad72-110">Return value</span></span>

<span data-ttu-id="cad72-111">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="cad72-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="cad72-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cad72-112">Requirements</span></span>



| <span data-ttu-id="cad72-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cad72-113">Requirement</span></span> | <span data-ttu-id="cad72-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="cad72-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cad72-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cad72-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cad72-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cad72-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="cad72-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cad72-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cad72-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="cad72-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="cad72-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cad72-119">Namespace</span></span><br/>                | <span data-ttu-id="cad72-120">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="cad72-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cad72-121">MOF</span><span class="sxs-lookup"><span data-stu-id="cad72-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cad72-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cad72-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cad72-123">DLL</span><span class="sxs-lookup"><span data-stu-id="cad72-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cad72-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cad72-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cad72-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cad72-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cad72-126">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="cad72-126">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




