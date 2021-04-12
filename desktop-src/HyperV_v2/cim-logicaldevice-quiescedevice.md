---
description: La méthode QuiesceDevice a été dépréciée à la place de la méthode RequestStateChange plus générale qui chevauche directement les fonctionnalités fournies par cette méthode.
ms.assetid: c5154c00-ff9c-40d8-bb76-41ae72ce86ae
title: Méthode QuiesceDevice de la classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.QuiesceDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 82041b36592f00bf71dc7e2d744fcf94b7a666c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320098"
---
# <a name="quiescedevice-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="33558-103">Méthode QuiesceDevice de la \_ classe du LOGICALDEVICE CIM</span><span class="sxs-lookup"><span data-stu-id="33558-103">QuiesceDevice method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="33558-104">La méthode **QuiesceDevice** a été dépréciée à la place de la méthode **RequestStateChange** plus générale qui chevauche directement les fonctionnalités fournies par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="33558-104">The **QuiesceDevice** method has been deprecated in lieu of the more general **RequestStateChange** method that directly overlaps with the functionality provided by this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="33558-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33558-105">Syntax</span></span>


```mof
uint32 QuiesceDevice(
  [in] boolean Quiesce
);
```



## <a name="parameters"></a><span data-ttu-id="33558-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33558-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33558-107">*Suspendre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33558-107">*Quiesce* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33558-108">Si la valeur est **true** , arrête correctement toute l’activité, si l’activité de reprise est **false** .</span><span class="sxs-lookup"><span data-stu-id="33558-108">If set to **TRUE** then cleanly cease all activity, if **FALSE** resume activity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33558-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33558-109">Return value</span></span>

<span data-ttu-id="33558-110">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="33558-110">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="33558-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33558-111">Requirements</span></span>



| <span data-ttu-id="33558-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33558-112">Requirement</span></span> | <span data-ttu-id="33558-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="33558-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33558-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33558-114">Minimum supported client</span></span><br/> | <span data-ttu-id="33558-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="33558-115">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="33558-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33558-116">Minimum supported server</span></span><br/> | <span data-ttu-id="33558-117">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="33558-117">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="33558-118">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="33558-118">Namespace</span></span><br/>                | <span data-ttu-id="33558-119">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="33558-119">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="33558-120">MOF</span><span class="sxs-lookup"><span data-stu-id="33558-120">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33558-121"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33558-121"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="33558-122">DLL</span><span class="sxs-lookup"><span data-stu-id="33558-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33558-123"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="33558-123"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="33558-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33558-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33558-125">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="33558-125">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




