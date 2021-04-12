---
description: Demande une réinitialisation du LogicalDevice.
ms.assetid: f7655825-3de5-421f-a3e9-97d2f605affd
title: Méthode Reset de la classe CIM_LogicalDevice (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 851332103143e84863762d8cc1183ec3ad841ca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320094"
---
# <a name="reset-method-of-the-cim_logicaldevice-class-hyper-v-management"></a><span data-ttu-id="13041-103">Méthode Reset de la classe CIM_LogicalDevice (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="13041-103">Reset method of the CIM_LogicalDevice class (Hyper-V management)</span></span>

<span data-ttu-id="13041-104">Demande une réinitialisation du LogicalDevice.</span><span class="sxs-lookup"><span data-stu-id="13041-104">Requests a reset of the LogicalDevice.</span></span> <span data-ttu-id="13041-105">Dans une sous-classe, l’ensemble de codes de retour possibles peut être spécifié, à l’aide d’un qualificateur ValueMap sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="13041-105">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="13041-106">Les chaînes pour lesquelles le contenu ValueMap est « traduit » peuvent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de valeurs.</span><span class="sxs-lookup"><span data-stu-id="13041-106">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="13041-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13041-107">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="13041-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13041-108">Parameters</span></span>

<span data-ttu-id="13041-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="13041-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="13041-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="13041-110">Return value</span></span>

<span data-ttu-id="13041-111">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="13041-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="13041-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13041-112">Requirements</span></span>



| <span data-ttu-id="13041-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13041-113">Requirement</span></span> | <span data-ttu-id="13041-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="13041-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13041-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13041-115">Minimum supported client</span></span><br/> | <span data-ttu-id="13041-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="13041-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="13041-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13041-117">Minimum supported server</span></span><br/> | <span data-ttu-id="13041-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="13041-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="13041-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="13041-119">Namespace</span></span><br/>                | <span data-ttu-id="13041-120">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="13041-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="13041-121">MOF</span><span class="sxs-lookup"><span data-stu-id="13041-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13041-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13041-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="13041-123">DLL</span><span class="sxs-lookup"><span data-stu-id="13041-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13041-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="13041-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="13041-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13041-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13041-126">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="13041-126">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




