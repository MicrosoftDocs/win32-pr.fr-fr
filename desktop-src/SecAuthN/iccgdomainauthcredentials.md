---
description: Interface implémentée par le client qui permet aux développeurs de fournir leurs propres informations d’identification de manière dynamique au moment de l’exécution pour authentifier les conteneurs non joints à un domaine avec Active Directory.
title: Interface ICcgDomainAuthCredentials (ccgplugins. h)
ms.topic: reference
ms.date: 10/20/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- ICcgDomainAuthCredentials
api_type:
- COM
api_location:
- ccgplugins.dll
ms.openlocfilehash: 8217f806ff0a1a6b38d045c7f665758ccaf8b1f5
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "106545869"
---
# <a name="iccgdomainauthcredentials-interface"></a><span data-ttu-id="26cc9-103">Interface ICcgDomainAuthCredentials</span><span class="sxs-lookup"><span data-stu-id="26cc9-103">ICcgDomainAuthCredentials interface</span></span>

<span data-ttu-id="26cc9-104">Interface implémentée par le client qui permet aux développeurs de fournir leurs propres informations d’identification de manière dynamique au moment de l’exécution pour authentifier les conteneurs non joints à un domaine avec Active Directory.</span><span class="sxs-lookup"><span data-stu-id="26cc9-104">A client-implemented interface that allows developers to supply their own credentials dynamically at run time to authenticate non-domain joined containers with Active Directory.</span></span> 

## <a name="members"></a><span data-ttu-id="26cc9-105">Membres</span><span class="sxs-lookup"><span data-stu-id="26cc9-105">Members</span></span>

<span data-ttu-id="26cc9-106">L’interface **ICcgDomainAuthCredentials** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="26cc9-106">The **ICcgDomainAuthCredentials** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="26cc9-107">**ICcgDomainAuthCredentials** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="26cc9-107">**ICcgDomainAuthCredentials** also has these types of members:</span></span>

-   [<span data-ttu-id="26cc9-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="26cc9-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="26cc9-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="26cc9-109">Methods</span></span>

<span data-ttu-id="26cc9-110">L’interface **ICcgDomainAuthCredentials** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="26cc9-110">The **ICcgDomainAuthCredentials** interface has these methods.</span></span>



| <span data-ttu-id="26cc9-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="26cc9-111">Method</span></span>                                           | <span data-ttu-id="26cc9-112">Description</span><span class="sxs-lookup"><span data-stu-id="26cc9-112">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26cc9-113">**GetPasswordCredentials**</span><span class="sxs-lookup"><span data-stu-id="26cc9-113">**GetPasswordCredentials**</span></span>](iccgdomainauthcredentials-getpasswordcredentials.md)               | <span data-ttu-id="26cc9-114">Retourne les informations d’identification pour authentifier un conteneur non joint à un domaine avec Active Directory.</span><span class="sxs-lookup"><span data-stu-id="26cc9-114">Returns credentials to authenticate a non-domain joined container with Active Directory.</span></span><br/>                                                              |



 

## <a name="requirements"></a><span data-ttu-id="26cc9-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26cc9-115">Requirements</span></span>



| <span data-ttu-id="26cc9-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26cc9-116">Requirement</span></span> | <span data-ttu-id="26cc9-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="26cc9-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26cc9-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26cc9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="26cc9-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26cc9-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="26cc9-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26cc9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="26cc9-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26cc9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="26cc9-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="26cc9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="26cc9-123"><dt>ccgplugins. h</dt></span><span class="sxs-lookup"><span data-stu-id="26cc9-123"><dt>ccgplugins.h</dt></span></span> </dl>   |
| <span data-ttu-id="26cc9-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="26cc9-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="26cc9-125"><dt>ccgplugins. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="26cc9-125"><dt>ccgplugins.tlb</dt></span></span> </dl> |
| <span data-ttu-id="26cc9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="26cc9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26cc9-127"><dt>ccgplugins.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26cc9-127"><dt>ccgplugins.dll</dt></span></span> </dl> |
| <span data-ttu-id="26cc9-128">IID</span><span class="sxs-lookup"><span data-stu-id="26cc9-128">IID</span></span><br/>                      | <span data-ttu-id="26cc9-129">6ecda518-2010-4437-8bc3-46e752b7b172</span><span class="sxs-lookup"><span data-stu-id="26cc9-129">6ecda518-2010-4437-8bc3-46e752b7b172</span></span><br/>          |



 

