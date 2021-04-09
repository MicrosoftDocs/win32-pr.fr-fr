---
description: Inversez le service dans l’état arrêté.
ms.assetid: d7469643-bccc-4f55-b2fc-d2bc2e392d84
title: Méthode StopService de la classe CIM_Service (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4eb354a48b074bad8adac4d5635e204844c31b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862862"
---
# <a name="stopservice-method-of-the-cim_service-class-hyper-v-management"></a><span data-ttu-id="b5375-103">Méthode StopService de la classe CIM_Service (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="b5375-103">StopService method of the CIM_Service class (Hyper-V management)</span></span>

<span data-ttu-id="b5375-104">Inversez le service dans l’état arrêté.</span><span class="sxs-lookup"><span data-stu-id="b5375-104">Paces the service in the stopped state.</span></span>

> [!Note]
>
> <span data-ttu-id="b5375-105">La sémantique de cette méthode se chevauche avec la méthode **RequestStateChange** héritée de [**la \_ EnabledLogicalElement CIM**](cim-enabledlogicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b5375-105">The semantics of this method overlap with the **RequestStateChange** method that is inherited from [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).</span></span> <span data-ttu-id="b5375-106">Cette méthode est conservée, car elle a été largement implémentée et sa sémantique « Stop » simple est pratique à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b5375-106">This method is maintained because it has been widely implemented, and its simple "stop" semantics are convenient to use.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b5375-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5375-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="b5375-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5375-108">Parameters</span></span>

<span data-ttu-id="b5375-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b5375-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b5375-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5375-110">Return value</span></span>

<span data-ttu-id="b5375-111">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="b5375-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5375-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5375-112">Requirements</span></span>



| <span data-ttu-id="b5375-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5375-113">Requirement</span></span> | <span data-ttu-id="b5375-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5375-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5375-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5375-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b5375-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b5375-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b5375-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5375-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b5375-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b5375-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b5375-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b5375-119">Namespace</span></span><br/>                | <span data-ttu-id="b5375-120">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="b5375-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b5375-121">MOF</span><span class="sxs-lookup"><span data-stu-id="b5375-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5375-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5375-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5375-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b5375-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5375-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b5375-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b5375-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5375-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5375-126">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="b5375-126">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




