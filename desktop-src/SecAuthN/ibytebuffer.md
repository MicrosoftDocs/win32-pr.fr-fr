---
description: L’interface IByteBuffer est fournie pour lire, écrire et gérer les objets de flux. Cet objet est essentiellement un wrapper pour l’objet IStream.
ms.assetid: dbc46d53-a421-45c0-a86b-b8a0a212a672
title: Interface IByteBuffer (scardssp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dfba15dee78134a9787bf7af994f1d4e2b064339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952790"
---
# <a name="ibytebuffer-interface"></a><span data-ttu-id="72d3e-104">Interface IByteBuffer</span><span class="sxs-lookup"><span data-stu-id="72d3e-104">IByteBuffer interface</span></span>

<span data-ttu-id="72d3e-105">\[L’interface **IByteBuffer** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="72d3e-105">\[The **IByteBuffer** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="72d3e-106">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="72d3e-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="72d3e-107">L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="72d3e-107">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="72d3e-108">L’interface **IByteBuffer** est fournie pour lire, écrire et gérer les objets de flux.</span><span class="sxs-lookup"><span data-stu-id="72d3e-108">The **IByteBuffer** interface is provided to read, write and manage stream objects.</span></span> <span data-ttu-id="72d3e-109">Cet objet est essentiellement un wrapper pour l’objet **IStream** .</span><span class="sxs-lookup"><span data-stu-id="72d3e-109">This object essentially is a wrapper for the **IStream** object.</span></span>

## <a name="members"></a><span data-ttu-id="72d3e-110">Membres</span><span class="sxs-lookup"><span data-stu-id="72d3e-110">Members</span></span>

<span data-ttu-id="72d3e-111">L’interface **IByteBuffer** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="72d3e-111">The **IByteBuffer** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="72d3e-112">**IByteBuffer** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="72d3e-112">**IByteBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="72d3e-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="72d3e-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="72d3e-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="72d3e-114">Methods</span></span>

<span data-ttu-id="72d3e-115">L’interface **IByteBuffer** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="72d3e-115">The **IByteBuffer** interface has these methods.</span></span>



| <span data-ttu-id="72d3e-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="72d3e-116">Method</span></span>                                           | <span data-ttu-id="72d3e-117">Description</span><span class="sxs-lookup"><span data-stu-id="72d3e-117">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72d3e-118">**Répliqué**</span><span class="sxs-lookup"><span data-stu-id="72d3e-118">**Clone**</span></span>](ibytebuffer-clone.md)               | <span data-ttu-id="72d3e-119">Clone un objet **IByteBuffer** .</span><span class="sxs-lookup"><span data-stu-id="72d3e-119">Clones an **IByteBuffer** object.</span></span><br/>                                                              |
| [<span data-ttu-id="72d3e-120">**Commit**</span><span class="sxs-lookup"><span data-stu-id="72d3e-120">**Commit**</span></span>](ibytebuffer-commit.md)             | <span data-ttu-id="72d3e-121">Valide une [*transaction*](/windows/desktop/SecGloss/t-gly).</span><span class="sxs-lookup"><span data-stu-id="72d3e-121">Commits a [*transaction*](/windows/desktop/SecGloss/t-gly).</span></span><br/> |
| [<span data-ttu-id="72d3e-122">**CopyTo**</span><span class="sxs-lookup"><span data-stu-id="72d3e-122">**CopyTo**</span></span>](ibytebuffer-copyto.md)             | <span data-ttu-id="72d3e-123">Copie les octets dans un autre objet.</span><span class="sxs-lookup"><span data-stu-id="72d3e-123">Copies bytes to another object.</span></span><br/>                                                                |
| [<span data-ttu-id="72d3e-124">**Initialiser**</span><span class="sxs-lookup"><span data-stu-id="72d3e-124">**Initialize**</span></span>](ibytebuffer-initialize.md)     | <span data-ttu-id="72d3e-125">Initialise l’objet **IByteBuffer** .</span><span class="sxs-lookup"><span data-stu-id="72d3e-125">Initializes the **IByteBuffer** object.</span></span><br/>                                                        |
| [<span data-ttu-id="72d3e-126">**LockRegion**</span><span class="sxs-lookup"><span data-stu-id="72d3e-126">**LockRegion**</span></span>](ibytebuffer-lockregion.md)     | <span data-ttu-id="72d3e-127">Restreint l’accès à une plage d’octets.</span><span class="sxs-lookup"><span data-stu-id="72d3e-127">Restricts access to a range of bytes.</span></span><br/>                                                          |
| [<span data-ttu-id="72d3e-128">**En lecture**</span><span class="sxs-lookup"><span data-stu-id="72d3e-128">**Read**</span></span>](ibytebuffer-read.md)                 | <span data-ttu-id="72d3e-129">Lit les octets dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="72d3e-129">Reads bytes into memory.</span></span><br/>                                                                       |
| [<span data-ttu-id="72d3e-130">**Rétablir**</span><span class="sxs-lookup"><span data-stu-id="72d3e-130">**Revert**</span></span>](ibytebuffer-revert.md)             | <span data-ttu-id="72d3e-131">Ignore les modifications apportées depuis le dernier appel de [**validation**](ibytebuffer-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="72d3e-131">Discards changes since the last [**Commit**](ibytebuffer-commit.md) call.</span></span><br/>                     |
| [<span data-ttu-id="72d3e-132">**Seek**</span><span class="sxs-lookup"><span data-stu-id="72d3e-132">**Seek**</span></span>](ibytebuffer-seek.md)                 | <span data-ttu-id="72d3e-133">Modifie le pointeur de recherche.</span><span class="sxs-lookup"><span data-stu-id="72d3e-133">Changes the seek pointer.</span></span><br/>                                                                      |
| [<span data-ttu-id="72d3e-134">**SetSize**</span><span class="sxs-lookup"><span data-stu-id="72d3e-134">**SetSize**</span></span>](ibytebuffer-setsize.md)           | <span data-ttu-id="72d3e-135">Modifie la taille de l'objet de flux.</span><span class="sxs-lookup"><span data-stu-id="72d3e-135">Changes the size of the stream object.</span></span><br/>                                                         |
| [<span data-ttu-id="72d3e-136">**Stat**</span><span class="sxs-lookup"><span data-stu-id="72d3e-136">**Stat**</span></span>](ibytebuffer-stat.md)                 | <span data-ttu-id="72d3e-137">Récupère des informations statistiques sur un flux.</span><span class="sxs-lookup"><span data-stu-id="72d3e-137">Retrieves statistical information about a stream.</span></span><br/>                                              |
| [<span data-ttu-id="72d3e-138">**UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="72d3e-138">**UnlockRegion**</span></span>](ibytebuffer-unlockregion.md) | <span data-ttu-id="72d3e-139">Supprime la restriction d’accès précédemment définie par [**LockRegion**](ibytebuffer-lockregion.md).</span><span class="sxs-lookup"><span data-stu-id="72d3e-139">Removes access restriction previously set by [**LockRegion**](ibytebuffer-lockregion.md).</span></span><br/>     |
| [<span data-ttu-id="72d3e-140">**Ecrire**</span><span class="sxs-lookup"><span data-stu-id="72d3e-140">**Write**</span></span>](ibytebuffer-write.md)               | <span data-ttu-id="72d3e-141">Écrit des octets dans le flux.</span><span class="sxs-lookup"><span data-stu-id="72d3e-141">Writes bytes to the stream.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="72d3e-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72d3e-142">Requirements</span></span>



| <span data-ttu-id="72d3e-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72d3e-143">Requirement</span></span> | <span data-ttu-id="72d3e-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="72d3e-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72d3e-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72d3e-145">Minimum supported client</span></span><br/> | <span data-ttu-id="72d3e-146">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72d3e-146">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="72d3e-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="72d3e-147">Minimum supported server</span></span><br/> | <span data-ttu-id="72d3e-148">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="72d3e-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="72d3e-149">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="72d3e-149">End of client support</span></span><br/>    | <span data-ttu-id="72d3e-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="72d3e-150">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="72d3e-151">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="72d3e-151">End of server support</span></span><br/>    | <span data-ttu-id="72d3e-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="72d3e-152">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="72d3e-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="72d3e-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="72d3e-154"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="72d3e-154"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="72d3e-155">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="72d3e-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="72d3e-156"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="72d3e-156"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="72d3e-157">DLL</span><span class="sxs-lookup"><span data-stu-id="72d3e-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72d3e-158"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72d3e-158"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="72d3e-159">IID</span><span class="sxs-lookup"><span data-stu-id="72d3e-159">IID</span></span><br/>                      | <span data-ttu-id="72d3e-160">IID \_ IByteBuffer est défini en tant que E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="72d3e-160">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

