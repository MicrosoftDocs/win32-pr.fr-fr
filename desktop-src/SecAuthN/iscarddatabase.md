---
description: L’interface ISCardDatabase fournit les méthodes permettant d’effectuer les opérations de base de données du gestionnaire de ressources de carte à puce.
ms.assetid: 56db3bc0-33c3-4b9c-a4a7-374fc491d8fd
title: Interface ISCardDatabase (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1ae74c813b4d95cc9d02694ca9edb5c030e4f342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544669"
---
# <a name="iscarddatabase-interface"></a><span data-ttu-id="66604-103">Interface ISCardDatabase</span><span class="sxs-lookup"><span data-stu-id="66604-103">ISCardDatabase interface</span></span>

<span data-ttu-id="66604-104">\[L’interface **ISCardDatabase** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="66604-104">\[The **ISCardDatabase** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="66604-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="66604-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="66604-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="66604-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="66604-107">L’interface **ISCardDatabase** fournit les méthodes permettant d’effectuer les opérations de base de données [*du gestionnaire de ressources*](../secgloss/r-gly.md) de [*carte à puce*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="66604-107">The **ISCardDatabase** interface provides the methods for performing the [*smart card*](../secgloss/s-gly.md) [*resource manager's*](../secgloss/r-gly.md) database operations.</span></span> <span data-ttu-id="66604-108">Ces opérations incluent la liste des cartes à puce, des [*lecteurs*](../secgloss/r-gly.md)et des groupes de lecteurs connus, ainsi que la récupération des interfaces prises en charge par une carte à puce et son [*fournisseur de services principal*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="66604-108">These operations include listing known smart cards, [*readers*](../secgloss/r-gly.md), and reader groups, plus retrieving the interfaces supported by a smart card and its [*primary service provider*](../secgloss/p-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="66604-109">L’identificateur du fournisseur de services principal est un GUID COM qui peut être utilisé pour instancier et utiliser les objets COM pour une carte spécifique.</span><span class="sxs-lookup"><span data-stu-id="66604-109">The identifier of the primary service provider is a COM GUID that can be used to instantiate and use the COM objects for a specific card.</span></span>

 

<span data-ttu-id="66604-110">L’exemple suivant illustre une utilisation type de l’interface **ISCardDatabase** .</span><span class="sxs-lookup"><span data-stu-id="66604-110">The following example shows a typical use of the **ISCardDatabase** interface.</span></span> <span data-ttu-id="66604-111">Dans ce cas, l’interface **ISCardDatabase** est utilisée pour répertorier toutes les cartes à puce connues.</span><span class="sxs-lookup"><span data-stu-id="66604-111">In this case, the **ISCardDatabase** interface is used to list all the known smart cards.</span></span>

<span data-ttu-id="66604-112">**Pour soumettre une transaction à une carte spécifique**</span><span class="sxs-lookup"><span data-stu-id="66604-112">**To submit a transaction to a specific card**</span></span>

1.  <span data-ttu-id="66604-113">Créer une interface **ISCardDatabase** .</span><span class="sxs-lookup"><span data-stu-id="66604-113">Create an **ISCardDatabase** interface.</span></span>
2.  <span data-ttu-id="66604-114">Appelez [**ListCards**](iscarddatabase-listcards.md) pour récupérer toutes les cartes à puce connues en fonction d’une [*chaîne ATR*](../secgloss/a-gly.md) ou de leurs interfaces prises en charge.</span><span class="sxs-lookup"><span data-stu-id="66604-114">Call [**ListCards**](iscarddatabase-listcards.md) to retrieve all the known smart cards based on an [*ATR string*](../secgloss/a-gly.md) or their supported interfaces.</span></span>
3.  <span data-ttu-id="66604-115">Libérez l’interface **ISCardDatabase** .</span><span class="sxs-lookup"><span data-stu-id="66604-115">Release the **ISCardDatabase** interface.</span></span>

## <a name="members"></a><span data-ttu-id="66604-116">Membres</span><span class="sxs-lookup"><span data-stu-id="66604-116">Members</span></span>

<span data-ttu-id="66604-117">L’interface **ISCardDatabase** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="66604-117">The **ISCardDatabase** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="66604-118">**ISCardDatabase** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="66604-118">**ISCardDatabase** also has these types of members:</span></span>

-   [<span data-ttu-id="66604-119">Méthodes</span><span class="sxs-lookup"><span data-stu-id="66604-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="66604-120">Méthodes</span><span class="sxs-lookup"><span data-stu-id="66604-120">Methods</span></span>

<span data-ttu-id="66604-121">L’interface **ISCardDatabase** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="66604-121">The **ISCardDatabase** interface has these methods.</span></span>



| <span data-ttu-id="66604-122">Méthode</span><span class="sxs-lookup"><span data-stu-id="66604-122">Method</span></span>                                                          | <span data-ttu-id="66604-123">Description</span><span class="sxs-lookup"><span data-stu-id="66604-123">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66604-124">**GetProviderCardId**</span><span class="sxs-lookup"><span data-stu-id="66604-124">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)   | <span data-ttu-id="66604-125">Récupère l’identificateur du [*fournisseur de services principal*](../secgloss/p-gly.md) pour une carte à puce spécifique.</span><span class="sxs-lookup"><span data-stu-id="66604-125">Retrieves the identifier of the [*primary service provider*](../secgloss/p-gly.md) for a specific smart card.</span></span><br/> |
| [<span data-ttu-id="66604-126">**ListCardInterfaces**</span><span class="sxs-lookup"><span data-stu-id="66604-126">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md) | <span data-ttu-id="66604-127">Récupère les identificateurs d’interface (GUID) de toutes les interfaces prises en charge par une carte à puce spécifique.</span><span class="sxs-lookup"><span data-stu-id="66604-127">Retrieves the interface identifiers (GUIDs) of all the interfaces supported by a specific smart card.</span></span><br/>                                                                                 |
| [<span data-ttu-id="66604-128">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="66604-128">**ListCards**</span></span>](iscarddatabase-listcards.md)                   | <span data-ttu-id="66604-129">Récupère tous les noms de carte à puce qui correspondent à un ensemble spécifique d’identificateurs d’interface (GUID) ou une [*chaîne ATR*](../secgloss/a-gly.md).</span><span class="sxs-lookup"><span data-stu-id="66604-129">Retrieves all the smart card names that match a specific set of interface identifiers (GUIDs) or an [*ATR string*](../secgloss/a-gly.md).</span></span><br/> |
| [<span data-ttu-id="66604-130">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="66604-130">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)     | <span data-ttu-id="66604-131">Récupère les noms des groupes de [*lecteurs*](../secgloss/r-gly.md) que le gestionnaire de ressources a connaissance de.</span><span class="sxs-lookup"><span data-stu-id="66604-131">Retrieves the names of the [*reader groups*](../secgloss/r-gly.md) that the resource manager has knowledge of.</span></span><br/>                        |
| [<span data-ttu-id="66604-132">**ListReaders**</span><span class="sxs-lookup"><span data-stu-id="66604-132">**ListReaders**</span></span>](iscarddatabase-listreaders.md)               | <span data-ttu-id="66604-133">Récupérez les noms des [*lecteurs*](../secgloss/r-gly.md) dont le gestionnaire de ressources a connaissance.</span><span class="sxs-lookup"><span data-stu-id="66604-133">Retrieve the names of the [*readers*](../secgloss/r-gly.md) of which the resource manager has knowledge.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="66604-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66604-134">Requirements</span></span>



| <span data-ttu-id="66604-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66604-135">Requirement</span></span> | <span data-ttu-id="66604-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="66604-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66604-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66604-137">Minimum supported client</span></span><br/> | <span data-ttu-id="66604-138">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66604-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="66604-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66604-139">Minimum supported server</span></span><br/> | <span data-ttu-id="66604-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66604-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="66604-141">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="66604-141">End of client support</span></span><br/>    | <span data-ttu-id="66604-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="66604-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="66604-143">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="66604-143">End of server support</span></span><br/>    | <span data-ttu-id="66604-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="66604-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="66604-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="66604-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="66604-146"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="66604-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="66604-147">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="66604-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="66604-148"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="66604-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="66604-149">DLL</span><span class="sxs-lookup"><span data-stu-id="66604-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66604-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66604-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="66604-151">IID</span><span class="sxs-lookup"><span data-stu-id="66604-151">IID</span></span><br/>                      | <span data-ttu-id="66604-152">IID \_ ISCardDatabase est défini en tant que 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="66604-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



 

 
