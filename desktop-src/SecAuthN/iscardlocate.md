---
description: L’interface ISCardLocate fournit des services permettant de localiser une carte à puce par son nom.
ms.assetid: add00705-69d5-4562-a74f-94c6864f6bd8
title: Interface ISCardLocate (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate
- ISCardLocate.ConfigureCardGuidSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e65a8315e796db032dfa6e9cb8898d19437bad05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530581"
---
# <a name="iscardlocate-interface"></a><span data-ttu-id="bb8fd-103">Interface ISCardLocate</span><span class="sxs-lookup"><span data-stu-id="bb8fd-103">ISCardLocate interface</span></span>

<span data-ttu-id="bb8fd-104">\[L’interface **ISCardLocate** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="bb8fd-104">\[The **ISCardLocate** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bb8fd-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="bb8fd-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bb8fd-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="bb8fd-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="bb8fd-107">L’interface **ISCardLocate** fournit des services permettant de localiser une [*carte à puce*](../secgloss/s-gly.md) par son nom.</span><span class="sxs-lookup"><span data-stu-id="bb8fd-107">The **ISCardLocate** interface provides services for locating a [*smart card*](../secgloss/s-gly.md) by its name.</span></span>

<span data-ttu-id="bb8fd-108">Cette interface peut afficher l' [*interface utilisateur*](../secgloss/u-gly.md) de la carte à puce, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="bb8fd-108">This interface can display the smart card [*user interface*](../secgloss/u-gly.md) if it is required.</span></span>

<span data-ttu-id="bb8fd-109">Le scénario suivant illustre une utilisation type de l’interface **ISCardLocate** .</span><span class="sxs-lookup"><span data-stu-id="bb8fd-109">The following scenario shows a typical use of the **ISCardLocate** interface.</span></span> <span data-ttu-id="bb8fd-110">L’interface **ISCardLocate** est utilisée pour générer une [*unité de données de protocole d’application*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="bb8fd-110">The **ISCardLocate** interface is used to build an [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

<span data-ttu-id="bb8fd-111">**Pour rechercher une carte spécifique à l’aide de son nom**</span><span class="sxs-lookup"><span data-stu-id="bb8fd-111">**To locate a specific card using its name**</span></span>

1.  <span data-ttu-id="bb8fd-112">Créer une interface **ISCardLocate** .</span><span class="sxs-lookup"><span data-stu-id="bb8fd-112">Create an **ISCardLocate** interface.</span></span>
2.  <span data-ttu-id="bb8fd-113">Appelez [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) pour rechercher un nom de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="bb8fd-113">Call [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) to search for a smart card name.</span></span>
3.  <span data-ttu-id="bb8fd-114">Appelez [**FindCard**](iscardlocate-findcard.md) pour rechercher la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="bb8fd-114">Call [**FindCard**](iscardlocate-findcard.md) to search for the smart card.</span></span>
4.  <span data-ttu-id="bb8fd-115">interpréter les résultats ;</span><span class="sxs-lookup"><span data-stu-id="bb8fd-115">Interpret the results.</span></span>
5.  <span data-ttu-id="bb8fd-116">Libérez l’interface **ISCardLocate** .</span><span class="sxs-lookup"><span data-stu-id="bb8fd-116">Release the **ISCardLocate** interface.</span></span>

## <a name="members"></a><span data-ttu-id="bb8fd-117">Membres</span><span class="sxs-lookup"><span data-stu-id="bb8fd-117">Members</span></span>

<span data-ttu-id="bb8fd-118">L’interface **ISCardLocate** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="bb8fd-118">The **ISCardLocate** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="bb8fd-119">**ISCardLocate** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bb8fd-119">**ISCardLocate** also has these types of members:</span></span>

-   [<span data-ttu-id="bb8fd-120">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bb8fd-120">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bb8fd-121">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bb8fd-121">Methods</span></span>

<span data-ttu-id="bb8fd-122">L’interface **ISCardLocate** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="bb8fd-122">The **ISCardLocate** interface has these methods.</span></span>



| <span data-ttu-id="bb8fd-123">Méthode</span><span class="sxs-lookup"><span data-stu-id="bb8fd-123">Method</span></span>                                                                  | <span data-ttu-id="bb8fd-124">Description</span><span class="sxs-lookup"><span data-stu-id="bb8fd-124">Description</span></span>                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| <span data-ttu-id="bb8fd-125">**ConfigureCardGuidSearch**</span><span class="sxs-lookup"><span data-stu-id="bb8fd-125">**ConfigureCardGuidSearch**</span></span>                                             | <span data-ttu-id="bb8fd-126">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="bb8fd-126">Reserved for future use.</span></span><br/>                                        |
| [<span data-ttu-id="bb8fd-127">**ConfigureCardNameSearch**</span><span class="sxs-lookup"><span data-stu-id="bb8fd-127">**ConfigureCardNameSearch**</span></span>](iscardlocate-configurecardnamesearch.md) | <span data-ttu-id="bb8fd-128">Spécifie le nom de la carte à utiliser dans la recherche.</span><span class="sxs-lookup"><span data-stu-id="bb8fd-128">Specifies the card name to be used in the search.</span></span><br/>               |
| [<span data-ttu-id="bb8fd-129">**FindCard**</span><span class="sxs-lookup"><span data-stu-id="bb8fd-129">**FindCard**</span></span>](iscardlocate-findcard.md)                               | <span data-ttu-id="bb8fd-130">Recherche la carte à puce et ouvre une connexion valide à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="bb8fd-130">Searches for the smart card and opens a valid connection to it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bb8fd-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb8fd-131">Requirements</span></span>



| <span data-ttu-id="bb8fd-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb8fd-132">Requirement</span></span> | <span data-ttu-id="bb8fd-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb8fd-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb8fd-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb8fd-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bb8fd-135">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb8fd-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bb8fd-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb8fd-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bb8fd-137">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb8fd-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bb8fd-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="bb8fd-138">End of client support</span></span><br/>    | <span data-ttu-id="bb8fd-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bb8fd-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="bb8fd-140">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="bb8fd-140">End of server support</span></span><br/>    | <span data-ttu-id="bb8fd-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bb8fd-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="bb8fd-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb8fd-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb8fd-143"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb8fd-143"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb8fd-144">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="bb8fd-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="bb8fd-145"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bb8fd-145"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bb8fd-146">DLL</span><span class="sxs-lookup"><span data-stu-id="bb8fd-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb8fd-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb8fd-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bb8fd-148">IID</span><span class="sxs-lookup"><span data-stu-id="bb8fd-148">IID</span></span><br/>                      | <span data-ttu-id="bb8fd-149">IID \_ ISCardLocate est défini en tant que 1461AACD-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="bb8fd-149">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



 

 
