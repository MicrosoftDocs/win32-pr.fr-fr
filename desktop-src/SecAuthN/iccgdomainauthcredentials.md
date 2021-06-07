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
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387807"
---
# <a name="iccgdomainauthcredentials-interface"></a><span data-ttu-id="78d42-103">Interface ICcgDomainAuthCredentials</span><span class="sxs-lookup"><span data-stu-id="78d42-103">ICcgDomainAuthCredentials interface</span></span>

<span data-ttu-id="78d42-104">Interface implémentée par le client qui permet aux développeurs de fournir leurs propres informations d’identification de manière dynamique au moment de l’exécution pour authentifier les conteneurs non joints à un domaine avec Active Directory.</span><span class="sxs-lookup"><span data-stu-id="78d42-104">A client-implemented interface that allows developers to supply their own credentials dynamically at run time to authenticate non-domain joined containers with Active Directory.</span></span> 

## <a name="members"></a><span data-ttu-id="78d42-105">Membres</span><span class="sxs-lookup"><span data-stu-id="78d42-105">Members</span></span>

<span data-ttu-id="78d42-106">L’interface **ICcgDomainAuthCredentials** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="78d42-106">The **ICcgDomainAuthCredentials** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="78d42-107">**ICcgDomainAuthCredentials** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="78d42-107">**ICcgDomainAuthCredentials** also has these types of members:</span></span>

-   [<span data-ttu-id="78d42-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="78d42-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="78d42-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="78d42-109">Methods</span></span>

<span data-ttu-id="78d42-110">L’interface **ICcgDomainAuthCredentials** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="78d42-110">The **ICcgDomainAuthCredentials** interface has these methods.</span></span>



| <span data-ttu-id="78d42-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="78d42-111">Method</span></span>                                           | <span data-ttu-id="78d42-112">Description</span><span class="sxs-lookup"><span data-stu-id="78d42-112">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78d42-113">**GetPasswordCredentials**</span><span class="sxs-lookup"><span data-stu-id="78d42-113">**GetPasswordCredentials**</span></span>](iccgdomainauthcredentials-getpasswordcredentials.md)               | <span data-ttu-id="78d42-114">Retourne les informations d’identification pour authentifier un conteneur non joint à un domaine avec Active Directory.</span><span class="sxs-lookup"><span data-stu-id="78d42-114">Returns credentials to authenticate a non-domain joined container with Active Directory.</span></span><br/>                                                              |



 

## <a name="requirements"></a><span data-ttu-id="78d42-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="78d42-115">Requirements</span></span>



| <span data-ttu-id="78d42-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78d42-116">Requirement</span></span> | <span data-ttu-id="78d42-117">Value</span><span class="sxs-lookup"><span data-stu-id="78d42-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78d42-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78d42-118">Minimum supported client</span></span><br/> | <span data-ttu-id="78d42-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78d42-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="78d42-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78d42-120">Minimum supported server</span></span><br/> | <span data-ttu-id="78d42-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78d42-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="78d42-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="78d42-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="78d42-123"><dt>ccgplugins. h</dt></span><span class="sxs-lookup"><span data-stu-id="78d42-123"><dt>ccgplugins.h</dt></span></span> </dl>   |
| <span data-ttu-id="78d42-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="78d42-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="78d42-125"><dt>ccgplugins. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="78d42-125"><dt>ccgplugins.tlb</dt></span></span> </dl> |
| <span data-ttu-id="78d42-126">DLL</span><span class="sxs-lookup"><span data-stu-id="78d42-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78d42-127"><dt>ccgplugins.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78d42-127"><dt>ccgplugins.dll</dt></span></span> </dl> |
| <span data-ttu-id="78d42-128">IID</span><span class="sxs-lookup"><span data-stu-id="78d42-128">IID</span></span><br/>                      | <span data-ttu-id="78d42-129">6ecda518-2010-4437-8bc3-46e752b7b172</span><span class="sxs-lookup"><span data-stu-id="78d42-129">6ecda518-2010-4437-8bc3-46e752b7b172</span></span><br/>          |



 

