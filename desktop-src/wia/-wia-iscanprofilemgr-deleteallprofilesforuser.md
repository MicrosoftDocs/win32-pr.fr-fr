---
description: Supprime tous les profils d’analyse disponibles pour l’utilisateur dans le système sous lequel votre application s’exécute.
ms.assetid: 1a79fd0e-1309-4fc4-863f-6dfb20594d91
title: IScanProfileMgr ::D méthode eleteAllProfilesForUser (Scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteAllProfilesForUser
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: c5d723379bb542346e3612f70c19a1629d325ebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113907"
---
# <a name="iscanprofilemgrdeleteallprofilesforuser-method"></a><span data-ttu-id="1cf2b-103">IScanProfileMgr ::D méthode eleteAllProfilesForUser</span><span class="sxs-lookup"><span data-stu-id="1cf2b-103">IScanProfileMgr::DeleteAllProfilesForUser method</span></span>

<span data-ttu-id="1cf2b-104">Supprime tous les profils d’analyse disponibles pour l’utilisateur dans le système sous lequel votre application s’exécute.</span><span class="sxs-lookup"><span data-stu-id="1cf2b-104">Deletes all the scan profiles available for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cf2b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cf2b-105">Syntax</span></span>


```C++
HRESULT DeleteAllProfilesForUser();
```



## <a name="parameters"></a><span data-ttu-id="1cf2b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cf2b-106">Parameters</span></span>

<span data-ttu-id="1cf2b-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1cf2b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1cf2b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1cf2b-108">Return value</span></span>

<span data-ttu-id="1cf2b-109">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1cf2b-109">Type: **HRESULT**</span></span>

<span data-ttu-id="1cf2b-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1cf2b-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1cf2b-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1cf2b-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cf2b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cf2b-112">Requirements</span></span>



| <span data-ttu-id="1cf2b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cf2b-113">Requirement</span></span> | <span data-ttu-id="1cf2b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cf2b-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cf2b-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cf2b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1cf2b-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cf2b-116">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="1cf2b-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cf2b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1cf2b-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cf2b-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1cf2b-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="1cf2b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cf2b-120"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cf2b-120"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="1cf2b-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="1cf2b-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1cf2b-122"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1cf2b-122"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cf2b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cf2b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cf2b-124">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="1cf2b-124">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="1cf2b-125">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="1cf2b-125">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




