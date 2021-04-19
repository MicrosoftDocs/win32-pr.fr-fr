---
description: Définit les paramètres de la ressource partagée.
ms.assetid: 592d0fa6-c865-4f70-89c3-b58204a8c5a6
ms.tgt_platform: multiple
title: Méthode SetShareInfo de la classe Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bda6fe36d1168045ea9f8d331ff334920ed1dd19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515379"
---
# <a name="setshareinfo-method-of-the-win32_clustershare-class"></a><span data-ttu-id="f4c6a-103">Méthode SetShareInfo de la \_ classe Win32 ClusterShare</span><span class="sxs-lookup"><span data-stu-id="f4c6a-103">SetShareInfo method of the Win32\_ClusterShare class</span></span>

<span data-ttu-id="f4c6a-104">Définit les paramètres de la ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="f4c6a-104">Sets the parameters of the shared resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4c6a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4c6a-105">Syntax</span></span>


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="f4c6a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4c6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4c6a-107">*MaximumAllowed* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f4c6a-107">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f4c6a-108">Limite du nombre maximal d’utilisateurs autorisés à utiliser cette ressource simultanément.</span><span class="sxs-lookup"><span data-stu-id="f4c6a-108">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="f4c6a-109">*Description* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f4c6a-109">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f4c6a-110">Décrit la ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="f4c6a-110">Describes the resource being shared.</span></span>

</dd> <dt>

<span data-ttu-id="f4c6a-111">*Accès* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f4c6a-111">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f4c6a-112">Descripteur de sécurité pour les autorisations au niveau de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f4c6a-112">Security descriptor for user-level permissions.</span></span> <span data-ttu-id="f4c6a-113">Un descripteur de sécurité contient des informations sur l’autorisation, le propriétaire et les capacités d’accès de la ressource.</span><span class="sxs-lookup"><span data-stu-id="f4c6a-113">A security descriptor contains information about the permission, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="f4c6a-114">Pour plus d’informations, [**consultez \_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="f4c6a-114">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4c6a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4c6a-115">Requirements</span></span>



| <span data-ttu-id="f4c6a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4c6a-116">Requirement</span></span> | <span data-ttu-id="f4c6a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4c6a-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4c6a-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4c6a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f4c6a-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f4c6a-119">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="f4c6a-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4c6a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f4c6a-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f4c6a-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="f4c6a-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f4c6a-122">Namespace</span></span><br/>                | <span data-ttu-id="f4c6a-123">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f4c6a-123">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f4c6a-124">MOF</span><span class="sxs-lookup"><span data-stu-id="f4c6a-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4c6a-125"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4c6a-125"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4c6a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f4c6a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4c6a-127"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4c6a-127"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4c6a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4c6a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4c6a-129">**\_ClusterShare Win32**</span><span class="sxs-lookup"><span data-stu-id="f4c6a-129">**Win32\_ClusterShare**</span></span>](win32-clustershare.md)
</dt> </dl>

 

