---
description: Fournit des services pour définir le code des IVT (vérification du détenteur de la carte) et pour vérifier l’utilisateur.
ms.assetid: fa40c21c-1584-475e-89f6-f81f67e3b942
title: Interface ISCardVerify
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify
api_type:
- COM
api_location: ''
ms.openlocfilehash: f929028f96faaab6ddb03538e854db01196ae180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757017"
---
# <a name="iscardverify-interface"></a><span data-ttu-id="9acc6-103">Interface ISCardVerify</span><span class="sxs-lookup"><span data-stu-id="9acc6-103">ISCardVerify interface</span></span>

<span data-ttu-id="9acc6-104">\[L’interface **ISCardVerify** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="9acc6-104">\[The **ISCardVerify** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9acc6-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="9acc6-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9acc6-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="9acc6-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9acc6-107">La définition d’interface suivante est fournie en tant que norme qui peut être suivie lors du développement d’un [*fournisseur de services*](../secgloss/c-gly.md)de [*carte à puce*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="9acc6-107">The following interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="9acc6-108">L’interface **ISCardVerify** fournit des services pour définir le code des IVT (vérification du détenteur de la carte) et pour vérifier l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9acc6-108">The **ISCardVerify** interface provides services for setting CHV (card holder verification) code and for verifying the user.</span></span>

<span data-ttu-id="9acc6-109">La classe **ISCardVerify** est définie pour les applications qui implémentent la stratégie IVT propre à l’application et qui ont une connaissance détaillée de l’implémentation interne de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="9acc6-109">The **ISCardVerify** class is defined for applications that implement application-specific CHV policy, and that have a detailed knowledge of the smart card's internal implementation.</span></span>

<span data-ttu-id="9acc6-110">Voici une utilisation courante de l’interface **ISCardVerify** .</span><span class="sxs-lookup"><span data-stu-id="9acc6-110">Following is a typical use of the **ISCardVerify** interface.</span></span>

<span data-ttu-id="9acc6-111">La procédure suivante utilise **ISCardVerify** pour modifier le code des IVT.</span><span class="sxs-lookup"><span data-stu-id="9acc6-111">The following procedure uses **ISCardVerify** to change the CHV code.</span></span>

<span data-ttu-id="9acc6-112">**Pour modifier le code IVT d’une carte à puce**</span><span class="sxs-lookup"><span data-stu-id="9acc6-112">**To change the CHV code of a smart card**</span></span>

1.  <span data-ttu-id="9acc6-113">Créez une interface **ISCardVerify** (à l’aide de la méthode d’interface [**ISCardManage**](iscardmanage.md) correspondante).</span><span class="sxs-lookup"><span data-stu-id="9acc6-113">Create an **ISCardVerify** interface (through the corresponding [**ISCardManage**](iscardmanage.md) interface method).</span></span>
2.  <span data-ttu-id="9acc6-114">Appelez la méthode [**ChangeCode**](iscardverify-changecode.md) et fournissez un nouveau code, en spécifiant s’il est local ou global et s’il est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="9acc6-114">Call the [**ChangeCode**](iscardverify-changecode.md) method and provide new code, specifying if it is local or global and if it is enabled or disabled.</span></span>
3.  <span data-ttu-id="9acc6-115">Libérez l’interface **ISCardVerify** .</span><span class="sxs-lookup"><span data-stu-id="9acc6-115">Release the **ISCardVerify** interface.</span></span>

## <a name="members"></a><span data-ttu-id="9acc6-116">Membres</span><span class="sxs-lookup"><span data-stu-id="9acc6-116">Members</span></span>

<span data-ttu-id="9acc6-117">L’interface **ISCardVerify** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="9acc6-117">The **ISCardVerify** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="9acc6-118">**ISCardVerify** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9acc6-118">**ISCardVerify** also has these types of members:</span></span>

-   [<span data-ttu-id="9acc6-119">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9acc6-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9acc6-120">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9acc6-120">Methods</span></span>

<span data-ttu-id="9acc6-121">L’interface **ISCardVerify** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9acc6-121">The **ISCardVerify** interface has these methods.</span></span>



| <span data-ttu-id="9acc6-122">Méthode</span><span class="sxs-lookup"><span data-stu-id="9acc6-122">Method</span></span>                                                        | <span data-ttu-id="9acc6-123">Description</span><span class="sxs-lookup"><span data-stu-id="9acc6-123">Description</span></span>                                                                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9acc6-124">**ChangeCode**</span><span class="sxs-lookup"><span data-stu-id="9acc6-124">**ChangeCode**</span></span>](iscardverify-changecode.md)                 | <span data-ttu-id="9acc6-125">Modifie le code IVT actuel.</span><span class="sxs-lookup"><span data-stu-id="9acc6-125">Changes the current CHV code.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="9acc6-126">**ResetSecurityState**</span><span class="sxs-lookup"><span data-stu-id="9acc6-126">**ResetSecurityState**</span></span>](iscardverify-resetsecuritystate.md) | <span data-ttu-id="9acc6-127">Réinitialise le [*contexte de sécurité*](../secgloss/s-gly.md) de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="9acc6-127">Resets the [*security context*](../secgloss/s-gly.md) of the smart card.</span></span><br/> |
| <span data-ttu-id="9acc6-128">[**Verrouillage**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9acc6-128">[**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span></span>                       | <span data-ttu-id="9acc6-129">Réactive le contexte de [*sécurité*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9acc6-129">Re-enables the [*security context*](../secgloss/s-gly.md).</span></span><br/>               |
| [<span data-ttu-id="9acc6-130">**Vérifier**</span><span class="sxs-lookup"><span data-stu-id="9acc6-130">**Verify**</span></span>](iscardverify-verify.md)                         | <span data-ttu-id="9acc6-131">Authentifie l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9acc6-131">Authenticates the user.</span></span><br/>                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="9acc6-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9acc6-132">Requirements</span></span>



| <span data-ttu-id="9acc6-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9acc6-133">Requirement</span></span> | <span data-ttu-id="9acc6-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="9acc6-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9acc6-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9acc6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9acc6-136">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9acc6-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="9acc6-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9acc6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9acc6-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9acc6-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9acc6-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="9acc6-139">End of client support</span></span><br/>    | <span data-ttu-id="9acc6-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9acc6-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="9acc6-141">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="9acc6-141">End of server support</span></span><br/>    | <span data-ttu-id="9acc6-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9acc6-142">Windows Server 2003</span></span><br/>                       |



 

 
