---
description: La définition de l’interface ISCardAuth est fournie en tant que norme qui peut être suivie lors du développement d’un fournisseur de services de carte à puce. L’interface ISCardAuth peut être utilisée pour exposer des services d’authentification pris en charge par une carte à puce.
ms.assetid: 6b8a5b90-49ad-48fd-813c-c3c3337ec8f1
title: Interface ISCardAuth
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: bf8df3702aceb2ac8bbf5ad090802be2dc07e45a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484721"
---
# <a name="iscardauth-interface"></a><span data-ttu-id="f85ab-103">Interface ISCardAuth</span><span class="sxs-lookup"><span data-stu-id="f85ab-103">ISCardAuth interface</span></span>

<span data-ttu-id="f85ab-104">\[L’interface **ISCardAuth** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="f85ab-104">\[The **ISCardAuth** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f85ab-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f85ab-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f85ab-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="f85ab-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f85ab-107">La définition de l’interface **ISCardAuth** est fournie en tant que norme qui peut être suivie lors du développement d’un [*fournisseur de services*](../secgloss/c-gly.md)de [*carte à puce*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f85ab-107">The **ISCardAuth** interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="f85ab-108">L’interface **ISCardAuth** peut être utilisée pour exposer des services d’authentification pris en charge par une carte à puce.</span><span class="sxs-lookup"><span data-stu-id="f85ab-108">The **ISCardAuth** interface can be used to expose authentication services supported by a smart card.</span></span> <span data-ttu-id="f85ab-109">Ces services incluent l’authentification de l’application, l’authentification par carte à puce et l’authentification des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f85ab-109">These services include application authentication, smart card authentication, and user authentication.</span></span>

<span data-ttu-id="f85ab-110">L’exemple suivant illustre une utilisation type de l’interface **ISCardAuth** .</span><span class="sxs-lookup"><span data-stu-id="f85ab-110">The following example shows a typical use of the **ISCardAuth** interface.</span></span>

<span data-ttu-id="f85ab-111">**Pour utiliser ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="f85ab-111">**To use ISCardAuth**</span></span>

1.  <span data-ttu-id="f85ab-112">Créez une interface **ISCardAuth** (à l’aide de la méthode d’interface [**ISCardManage**](iscardmanage.md) correspondante).</span><span class="sxs-lookup"><span data-stu-id="f85ab-112">Create an **ISCardAuth** interface (through the corresponding [**ISCardManage**](iscardmanage.md) interface method).</span></span>
2.  <span data-ttu-id="f85ab-113">Appelez la méthode **ISCardAuth** appropriée ([**\_ authentification**](iscardauth-app-auth.md)de l’application, [**GetChallenge**](iscardauth-getchallenge.md), [**\_ authentification ICC**](iscardauth-icc-auth.md)ou [**\_ authentification utilisateur**](iscardauth-user-auth.md)).</span><span class="sxs-lookup"><span data-stu-id="f85ab-113">Call the appropriate **ISCardAuth** method ([**APP\_Auth**](iscardauth-app-auth.md), [**GetChallenge**](iscardauth-getchallenge.md), [**ICC\_Auth**](iscardauth-icc-auth.md), or [**User\_Auth**](iscardauth-user-auth.md)).</span></span>
3.  <span data-ttu-id="f85ab-114">Libérez l’interface **ISCardAuth** .</span><span class="sxs-lookup"><span data-stu-id="f85ab-114">Release the **ISCardAuth** interface.</span></span>

## <a name="members"></a><span data-ttu-id="f85ab-115">Membres</span><span class="sxs-lookup"><span data-stu-id="f85ab-115">Members</span></span>

<span data-ttu-id="f85ab-116">L’interface **ISCardAuth** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="f85ab-116">The **ISCardAuth** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="f85ab-117">**ISCardAuth** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f85ab-117">**ISCardAuth** also has these types of members:</span></span>

-   [<span data-ttu-id="f85ab-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f85ab-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f85ab-119">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f85ab-119">Methods</span></span>

<span data-ttu-id="f85ab-120">L’interface **ISCardAuth** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f85ab-120">The **ISCardAuth** interface has these methods.</span></span>



| <span data-ttu-id="f85ab-121">Méthode</span><span class="sxs-lookup"><span data-stu-id="f85ab-121">Method</span></span>                                          | <span data-ttu-id="f85ab-122">Description</span><span class="sxs-lookup"><span data-stu-id="f85ab-122">Description</span></span>                                                                                    |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f85ab-123">**Authentification de l’application \_**</span><span class="sxs-lookup"><span data-stu-id="f85ab-123">**APP\_Auth**</span></span>](iscardauth-app-auth.md)        | <span data-ttu-id="f85ab-124">Permet à l’application de s’authentifier à l’aide d’un protocole de stimulation/signature.</span><span class="sxs-lookup"><span data-stu-id="f85ab-124">Allows the application to authenticate itself using a challenge/signature protocol.</span></span><br/> |
| [<span data-ttu-id="f85ab-125">**GetChallenge**</span><span class="sxs-lookup"><span data-stu-id="f85ab-125">**GetChallenge**</span></span>](iscardauth-getchallenge.md) | <span data-ttu-id="f85ab-126">Retourne une stimulation de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="f85ab-126">Returns a challenge from the smart card.</span></span><br/>                                            |
| [<span data-ttu-id="f85ab-127">**\_Authentification ICC**</span><span class="sxs-lookup"><span data-stu-id="f85ab-127">**ICC\_Auth**</span></span>](iscardauth-icc-auth.md)        | <span data-ttu-id="f85ab-128">Permet à une application d’authentifier la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="f85ab-128">Allows an application to authenticate the smart card.</span></span><br/>                               |
| [<span data-ttu-id="f85ab-129">**\_Authentification utilisateur**</span><span class="sxs-lookup"><span data-stu-id="f85ab-129">**User\_Auth**</span></span>](iscardauth-user-auth.md)      | <span data-ttu-id="f85ab-130">Autorise l’accès aux services d’authentification des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f85ab-130">Allows access to user authentication services.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="f85ab-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f85ab-131">Requirements</span></span>



| <span data-ttu-id="f85ab-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f85ab-132">Requirement</span></span> | <span data-ttu-id="f85ab-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="f85ab-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f85ab-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f85ab-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f85ab-135">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f85ab-135">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f85ab-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f85ab-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f85ab-137">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f85ab-137">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f85ab-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f85ab-138">End of client support</span></span><br/>    | <span data-ttu-id="f85ab-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f85ab-139">Windows XP</span></span><br/>                                |
| <span data-ttu-id="f85ab-140">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="f85ab-140">End of server support</span></span><br/>    | <span data-ttu-id="f85ab-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f85ab-141">Windows Server 2003</span></span><br/>                       |



 

 
