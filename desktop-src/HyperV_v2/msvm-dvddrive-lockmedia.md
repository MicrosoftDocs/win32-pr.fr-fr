---
description: 'Méthode LockMedia de la classe Msvm_DVDDrive : verrouille ou libère le média.'
ms.assetid: 924bc20a-901b-4618-be49-eaacf80c9465
title: Méthode LockMedia de la classe Msvm_DVDDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e00780fbeeeec60563b31008c8e5979a09f9d173
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119147"
---
# <a name="lockmedia-method-of-the-msvm_dvddrive-class"></a><span data-ttu-id="bd3cc-103">Méthode LockMedia de la \_ classe DVDDrive MSVM</span><span class="sxs-lookup"><span data-stu-id="bd3cc-103">LockMedia method of the Msvm\_DVDDrive class</span></span>

<span data-ttu-id="bd3cc-104">Verrouille ou libère le média.</span><span class="sxs-lookup"><span data-stu-id="bd3cc-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd3cc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd3cc-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="bd3cc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd3cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd3cc-107">*Verrou* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bd3cc-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd3cc-108">**true** pour verrouiller le média ; **false** pour libérer le média.</span><span class="sxs-lookup"><span data-stu-id="bd3cc-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd3cc-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bd3cc-109">Return value</span></span>

<span data-ttu-id="bd3cc-110">La méthode retourne l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="bd3cc-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="bd3cc-111">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="bd3cc-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bd3cc-112">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="bd3cc-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bd3cc-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd3cc-113">Requirements</span></span>



| <span data-ttu-id="bd3cc-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd3cc-114">Requirement</span></span> | <span data-ttu-id="bd3cc-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd3cc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd3cc-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd3cc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bd3cc-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="bd3cc-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="bd3cc-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd3cc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bd3cc-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="bd3cc-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="bd3cc-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bd3cc-120">Namespace</span></span><br/>                | <span data-ttu-id="bd3cc-121">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="bd3cc-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bd3cc-122">MOF</span><span class="sxs-lookup"><span data-stu-id="bd3cc-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd3cc-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd3cc-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd3cc-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bd3cc-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd3cc-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bd3cc-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bd3cc-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd3cc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd3cc-127">**MSVM \_ DVDDrive**</span><span class="sxs-lookup"><span data-stu-id="bd3cc-127">**Msvm\_DVDDrive**</span></span>](msvm-dvddrive.md)
</dt> </dl>

 

 




