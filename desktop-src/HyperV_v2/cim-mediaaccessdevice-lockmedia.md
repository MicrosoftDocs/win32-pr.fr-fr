---
description: Verrouille et déverrouille le média dans un appareil d’accès amovible.
ms.assetid: 357ee552-82d0-4201-bcc2-0acf208e16a0
title: Méthode LockMedia de la classe CIM_MediaAccessDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 12c4aa6c6ba9e57a2ab88e58624b246fb98065f3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104042919"
---
# <a name="lockmedia-method-of-the-cim_mediaaccessdevice-class"></a><span data-ttu-id="310d2-103">Méthode LockMedia de la \_ classe CIM MediaAccessDevice</span><span class="sxs-lookup"><span data-stu-id="310d2-103">LockMedia method of the CIM\_MediaAccessDevice class</span></span>

<span data-ttu-id="310d2-104">Verrouille et déverrouille le média dans un appareil d’accès amovible.</span><span class="sxs-lookup"><span data-stu-id="310d2-104">Locks and unlocks the media in a removeable access device.</span></span>

## <a name="syntax"></a><span data-ttu-id="310d2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="310d2-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="310d2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="310d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="310d2-107">*Verrou* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="310d2-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="310d2-108">Si la **valeur est true**, verrouille le média.</span><span class="sxs-lookup"><span data-stu-id="310d2-108">If **TRUE**, locks the media.</span></span> <span data-ttu-id="310d2-109">Si la **valeur est false**, libère le média.</span><span class="sxs-lookup"><span data-stu-id="310d2-109">If **FALSE**, releases the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="310d2-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="310d2-110">Return value</span></span>

<span data-ttu-id="310d2-111">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="310d2-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="310d2-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="310d2-112">Requirements</span></span>



| <span data-ttu-id="310d2-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="310d2-113">Requirement</span></span> | <span data-ttu-id="310d2-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="310d2-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="310d2-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="310d2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="310d2-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="310d2-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="310d2-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="310d2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="310d2-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="310d2-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="310d2-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="310d2-119">Namespace</span></span><br/>                | <span data-ttu-id="310d2-120">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="310d2-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="310d2-121">MOF</span><span class="sxs-lookup"><span data-stu-id="310d2-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="310d2-122"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="310d2-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="310d2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="310d2-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="310d2-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="310d2-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="310d2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="310d2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="310d2-126">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="310d2-126">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

 




