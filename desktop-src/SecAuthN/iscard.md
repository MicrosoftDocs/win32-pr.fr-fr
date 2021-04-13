---
description: Vous permet d’ouvrir et de gérer une connexion à une carte à puce.
ms.assetid: f49f76e6-eed9-4e85-b48f-29f7bad40218
title: Interface ISCard (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7dbbeccdf6c3fa9d586c841de661ed351ec37d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528150"
---
# <a name="iscard-interface"></a><span data-ttu-id="cb751-103">Interface ISCard</span><span class="sxs-lookup"><span data-stu-id="cb751-103">ISCard interface</span></span>

<span data-ttu-id="cb751-104">\[L’interface **ISCard** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="cb751-104">\[The **ISCard** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cb751-105">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="cb751-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="cb751-106">L’interface **ISCard** vous permet d’ouvrir et de gérer une connexion à une [*carte à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cb751-106">The **ISCard** interface lets you open and manage a connection to a [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="cb751-107">Chaque connexion à une carte requiert une seule instance correspondante de l’interface **ISCard** .</span><span class="sxs-lookup"><span data-stu-id="cb751-107">Each connection to a card requires a single, corresponding instance of the **ISCard** interface.</span></span>

<span data-ttu-id="cb751-108">Le gestionnaire de [*ressources*](../secgloss/r-gly.md) de carte à puce doit être disponible chaque fois qu’une instance de **ISCard** est créée.</span><span class="sxs-lookup"><span data-stu-id="cb751-108">The smart card [*resource manager*](../secgloss/r-gly.md) must be available whenever an instance of **ISCard** is created.</span></span> <span data-ttu-id="cb751-109">Si ce service n’est pas disponible, la création de l’interface échoue.</span><span class="sxs-lookup"><span data-stu-id="cb751-109">If this service is unavailable, creation of the interface will fail.</span></span>

<span data-ttu-id="cb751-110">L’exemple suivant illustre une utilisation type de l’interface **ISCard** .</span><span class="sxs-lookup"><span data-stu-id="cb751-110">The following example shows a typical use of the **ISCard** interface.</span></span> <span data-ttu-id="cb751-111">L’interface **ISCard** est utilisée pour la connexion à la carte à puce, l’envoi d’une [*transaction*](../secgloss/t-gly.md)et la libération de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="cb751-111">The **ISCard** interface is used to connect to the smart card, submit a [*transaction*](../secgloss/t-gly.md), and release the smart card.</span></span>

<span data-ttu-id="cb751-112">**Pour soumettre une transaction à une carte spécifique**</span><span class="sxs-lookup"><span data-stu-id="cb751-112">**To submit a transaction to a specific card**</span></span>

1.  <span data-ttu-id="cb751-113">Créer une interface **ISCard** .</span><span class="sxs-lookup"><span data-stu-id="cb751-113">Create an **ISCard** interface.</span></span>
2.  <span data-ttu-id="cb751-114">Connectez-vous à une carte à puce en spécifiant un [*lecteur*](../secgloss/r-gly.md) de carte à puce ou en utilisant un handle valide précédemment établi.</span><span class="sxs-lookup"><span data-stu-id="cb751-114">Attach to a smart card by specifying a smart card [*reader*](../secgloss/r-gly.md) or by using a previously established, valid handle.</span></span>
3.  <span data-ttu-id="cb751-115">Créer des commandes de transaction avec des interfaces de carte à puce [**ISCardCmd**](iscardcmd.md)et [**ISCardISO7816**](iscardiso7816.md) .</span><span class="sxs-lookup"><span data-stu-id="cb751-115">Create transaction commands with [**ISCardCmd**](iscardcmd.md), and [**ISCardISO7816**](iscardiso7816.md) smart card interfaces.</span></span>
4.  <span data-ttu-id="cb751-116">Utilisez **ISCard** pour envoyer les commandes de transaction en vue de leur traitement par la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="cb751-116">Use **ISCard** to submit the transaction commands for processing by the smart card.</span></span>
5.  <span data-ttu-id="cb751-117">Utilisez **ISCard** pour libérer la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="cb751-117">Use **ISCard** to release the smart card.</span></span>
6.  <span data-ttu-id="cb751-118">Libérez l’interface **ISCard** .</span><span class="sxs-lookup"><span data-stu-id="cb751-118">Release the **ISCard** interface.</span></span>

## <a name="members"></a><span data-ttu-id="cb751-119">Membres</span><span class="sxs-lookup"><span data-stu-id="cb751-119">Members</span></span>

<span data-ttu-id="cb751-120">L’interface **ISCard** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="cb751-120">The **ISCard** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="cb751-121">**ISCard** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cb751-121">**ISCard** also has these types of members:</span></span>

-   [<span data-ttu-id="cb751-122">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cb751-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="cb751-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cb751-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cb751-124">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cb751-124">Methods</span></span>

<span data-ttu-id="cb751-125">L’interface **ISCard** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="cb751-125">The **ISCard** interface has these methods.</span></span>



| <span data-ttu-id="cb751-126">Méthode</span><span class="sxs-lookup"><span data-stu-id="cb751-126">Method</span></span>                                          | <span data-ttu-id="cb751-127">Description</span><span class="sxs-lookup"><span data-stu-id="cb751-127">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb751-128">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="cb751-128">**AttachByHandle**</span></span>](iscard-attachbyhandle.md) | <span data-ttu-id="cb751-129">Attache un objet à un handle de carte à puce ouvert et configuré.</span><span class="sxs-lookup"><span data-stu-id="cb751-129">Attaches an object to an open and configured smart card handle.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="cb751-130">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="cb751-130">**AttachByReader**</span></span>](iscard-attachbyreader.md) | <span data-ttu-id="cb751-131">Ouvre la carte à puce dans le lecteur nommé.</span><span class="sxs-lookup"><span data-stu-id="cb751-131">Opens the smart card in the named reader.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="cb751-132">**Dissocié**</span><span class="sxs-lookup"><span data-stu-id="cb751-132">**Detach**</span></span>](iscard-detach.md)                 | <span data-ttu-id="cb751-133">Ferme la connexion ouverte à la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="cb751-133">Closes the open connection to the smart card.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="cb751-134">**LockSCard**</span><span class="sxs-lookup"><span data-stu-id="cb751-134">**LockSCard**</span></span>](iscard-lockscard.md)           | <span data-ttu-id="cb751-135">Réclame un accès exclusif à la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="cb751-135">Claims exclusive access to the smart card.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="cb751-136">**Rattacher**</span><span class="sxs-lookup"><span data-stu-id="cb751-136">**ReAttach**</span></span>](iscard-reattach.md)             | <span data-ttu-id="cb751-137">Réinitialise et réinitialise la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="cb751-137">Resets and reinitializes the smart card.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="cb751-138">**Libellé**</span><span class="sxs-lookup"><span data-stu-id="cb751-138">**Transaction**</span></span>](iscard-transaction.md)       | <span data-ttu-id="cb751-139">Exécute une opération d’écriture et de lecture sur l’objet de commande de carte à puce ([*unité de données de protocole d’application*](../secgloss/a-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="cb751-139">Executes a write and read operation on the smart card command ([*application protocol data unit*](../secgloss/a-gly.md)) object.</span></span><br/> |
| [<span data-ttu-id="cb751-140">**UnlockScard**</span><span class="sxs-lookup"><span data-stu-id="cb751-140">**UnlockScard**</span></span>](iscard-unlockscard.md)       | <span data-ttu-id="cb751-141">Libère l’accès exclusif à la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="cb751-141">Releases exclusive access to the smart card.</span></span><br/>                                                                                                                                                                         |



 

### <a name="properties"></a><span data-ttu-id="cb751-142">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cb751-142">Properties</span></span>

<span data-ttu-id="cb751-143">L’interface **ISCard** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="cb751-143">The **ISCard** interface has these properties.</span></span>



| <span data-ttu-id="cb751-144">Propriété</span><span class="sxs-lookup"><span data-stu-id="cb751-144">Property</span></span>                                               | <span data-ttu-id="cb751-145">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="cb751-145">Access type</span></span>          | <span data-ttu-id="cb751-146">Description</span><span class="sxs-lookup"><span data-stu-id="cb751-146">Description</span></span>                                                                                                                                                                                    |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb751-147">**Atr**</span><span class="sxs-lookup"><span data-stu-id="cb751-147">**Atr**</span></span>](iscard-get-atr.md)<br/>               | <span data-ttu-id="cb751-148">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb751-148">Read-only</span></span><br/> | <span data-ttu-id="cb751-149">Récupère la [*chaîne ATR*](../secgloss/a-gly.md) de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="cb751-149">Retrieves the [*ATR string*](../secgloss/a-gly.md) of the smart card.</span></span><br/>                                                                   |
| [<span data-ttu-id="cb751-150">**CardHandle**</span><span class="sxs-lookup"><span data-stu-id="cb751-150">**CardHandle**</span></span>](iscard-get-cardhandle.md)<br/> | <span data-ttu-id="cb751-151">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb751-151">Read-only</span></span><br/> | <span data-ttu-id="cb751-152">Récupère le handle de la carte à puce connectée.</span><span class="sxs-lookup"><span data-stu-id="cb751-152">Retrieves the handle for the connected smart card.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="cb751-153">**Context**</span><span class="sxs-lookup"><span data-stu-id="cb751-153">**Context**</span></span>](iscard-get-context.md)<br/>       | <span data-ttu-id="cb751-154">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb751-154">Read-only</span></span><br/> | <span data-ttu-id="cb751-155">Récupère le handle de [*contexte du gestionnaire de ressources*](../secgloss/r-gly.md) actuel.</span><span class="sxs-lookup"><span data-stu-id="cb751-155">Retrieves the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span><br/>                            |
| [<span data-ttu-id="cb751-156">**Protocol**</span><span class="sxs-lookup"><span data-stu-id="cb751-156">**Protocol**</span></span>](iscard-get-protocol.md)<br/>     | <span data-ttu-id="cb751-157">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb751-157">Read-only</span></span><br/> | <span data-ttu-id="cb751-158">Récupère l’identificateur du protocole en cours d’utilisation sur la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="cb751-158">Retrieves the identifier of the protocol currently in use on the smart card.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="cb751-159">**Statu**</span><span class="sxs-lookup"><span data-stu-id="cb751-159">**Status**</span></span>](iscard-get-status.md)<br/>         | <span data-ttu-id="cb751-160">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="cb751-160">Read-only</span></span><br/> | <span data-ttu-id="cb751-161">Récupère l' [*État*](../secgloss/s-gly.md) actuel de la [*carte à puce*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="cb751-161">Retrieves the current [*state*](../secgloss/s-gly.md) the [*smart card*](../secgloss/s-gly.md) is in.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cb751-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb751-162">Requirements</span></span>



| <span data-ttu-id="cb751-163">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb751-163">Requirement</span></span> | <span data-ttu-id="cb751-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb751-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb751-165">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb751-165">Minimum supported client</span></span><br/> | <span data-ttu-id="cb751-166">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb751-166">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cb751-167">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb751-167">Minimum supported server</span></span><br/> | <span data-ttu-id="cb751-168">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb751-168">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cb751-169">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="cb751-169">End of client support</span></span><br/>    | <span data-ttu-id="cb751-170">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cb751-170">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="cb751-171">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="cb751-171">End of server support</span></span><br/>    | <span data-ttu-id="cb751-172">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cb751-172">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="cb751-173">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb751-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb751-174"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb751-174"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="cb751-175">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="cb751-175">Type library</span></span><br/>             | <dl> <span data-ttu-id="cb751-176"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cb751-176"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cb751-177">DLL</span><span class="sxs-lookup"><span data-stu-id="cb751-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb751-178"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb751-178"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cb751-179">IID</span><span class="sxs-lookup"><span data-stu-id="cb751-179">IID</span></span><br/>                      | <span data-ttu-id="cb751-180">IID \_ ISCard est défini en tant que 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="cb751-180">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



 

 
