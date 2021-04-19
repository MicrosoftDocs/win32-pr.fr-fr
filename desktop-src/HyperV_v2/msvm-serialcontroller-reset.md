---
description: Réinitialise l’appareil.
ms.assetid: 4ac8ee27-0629-45aa-80ee-f308c044d7fc
title: Méthode Reset de la classe Msvm_SerialController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialController.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bf5fd2ff0218a4a4f39e64921e41fd497753d04e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529863"
---
# <a name="reset-method-of-the-msvm_serialcontroller-class"></a><span data-ttu-id="e1119-103">Méthode Reset de la \_ classe MSVM SerialController</span><span class="sxs-lookup"><span data-stu-id="e1119-103">Reset method of the Msvm\_SerialController class</span></span>

<span data-ttu-id="e1119-104">Réinitialise l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e1119-104">Resets the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1119-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1119-105">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="e1119-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1119-106">Parameters</span></span>

<span data-ttu-id="e1119-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e1119-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1119-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1119-108">Return value</span></span>

<span data-ttu-id="e1119-109">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="e1119-109">Returns 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="e1119-110">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="e1119-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e1119-111">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="e1119-111">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e1119-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1119-112">Requirements</span></span>



| <span data-ttu-id="e1119-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1119-113">Requirement</span></span> | <span data-ttu-id="e1119-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1119-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1119-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1119-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e1119-116">Windows 8.1, version 1703</span><span class="sxs-lookup"><span data-stu-id="e1119-116">Windows 8.1, version 1703</span></span><br/>                                                                    |
| <span data-ttu-id="e1119-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1119-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e1119-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e1119-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="e1119-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e1119-119">Namespace</span></span><br/>                | <span data-ttu-id="e1119-120">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e1119-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e1119-121">MOF</span><span class="sxs-lookup"><span data-stu-id="e1119-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1119-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1119-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1119-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e1119-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1119-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e1119-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e1119-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1119-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1119-126">**MSVM \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="e1119-126">**Msvm\_SerialController**</span></span>](msvm-serialcontroller.md)
</dt> </dl>

 

 




