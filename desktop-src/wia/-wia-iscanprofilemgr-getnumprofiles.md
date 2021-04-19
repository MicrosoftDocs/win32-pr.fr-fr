---
description: Obtient le nombre de profils d’analyse créés pour l’utilisateur dans le système sous lequel votre application s’exécute.
ms.assetid: 0667a885-d61f-4c44-b988-a42242c2678e
title: 'IScanProfileMgr :: GetNumProfiles, méthode (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: a8c3167bd428054054a32d7823ce57e562501533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524235"
---
# <a name="iscanprofilemgrgetnumprofiles-method"></a><span data-ttu-id="24b86-103">IScanProfileMgr :: GetNumProfiles, méthode</span><span class="sxs-lookup"><span data-stu-id="24b86-103">IScanProfileMgr::GetNumProfiles method</span></span>

<span data-ttu-id="24b86-104">Obtient le nombre de profils d’analyse créés pour l’utilisateur dans le système sous lequel votre application s’exécute.</span><span class="sxs-lookup"><span data-stu-id="24b86-104">Gets the number of scan profiles created for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="24b86-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24b86-105">Syntax</span></span>


```C++
HRESULT GetNumProfiles(
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a><span data-ttu-id="24b86-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24b86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24b86-107">*pulNumProfiles* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="24b86-107">*pulNumProfiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24b86-108">Type : \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="24b86-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="24b86-109">Pointeur vers le nombre de profils créés pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="24b86-109">A pointer to the number of profiles created for the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24b86-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="24b86-110">Return value</span></span>

<span data-ttu-id="24b86-111">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="24b86-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="24b86-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="24b86-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="24b86-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="24b86-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="24b86-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24b86-114">Requirements</span></span>



| <span data-ttu-id="24b86-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24b86-115">Requirement</span></span> | <span data-ttu-id="24b86-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="24b86-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="24b86-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24b86-117">Minimum supported client</span></span><br/> | <span data-ttu-id="24b86-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24b86-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="24b86-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24b86-119">Minimum supported server</span></span><br/> | <span data-ttu-id="24b86-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24b86-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="24b86-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="24b86-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="24b86-122"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="24b86-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="24b86-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="24b86-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="24b86-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="24b86-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24b86-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24b86-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24b86-126">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="24b86-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="24b86-127">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="24b86-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




