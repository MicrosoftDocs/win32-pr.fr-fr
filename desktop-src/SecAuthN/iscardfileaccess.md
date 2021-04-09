---
description: La définition d’interface suivante est fournie en tant que norme qui peut être suivie lors du développement d’un fournisseur de services de carte à puce.
ms.assetid: 68cc0bbe-ce8e-4da1-b907-596caa95a39c
title: Interface ISCardFileAccess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess
api_type:
- COM
api_location: ''
ms.openlocfilehash: fcfcdc75bcf10b922a242574bfabe267c949fa52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866258"
---
# <a name="iscardfileaccess-interface"></a><span data-ttu-id="dab1b-103">Interface ISCardFileAccess</span><span class="sxs-lookup"><span data-stu-id="dab1b-103">ISCardFileAccess interface</span></span>

<span data-ttu-id="dab1b-104">\[L’interface **ISCardFileAccess** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="dab1b-104">\[The **ISCardFileAccess** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dab1b-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="dab1b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dab1b-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="dab1b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="dab1b-107">La définition d’interface suivante est fournie en tant que norme qui peut être suivie lors du développement d’un [*fournisseur de services*](../secgloss/c-gly.md)de [*carte à puce*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="dab1b-107">The following interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="dab1b-108">L’interface **ISCardFileAccess** peut être utilisée pour implémenter une interface de haut niveau sur un système de fichiers à base de cartes avec un système de fichiers de cartes sous-jacent basé sur la structure définie dans la norme ISO/IEC 7816-4.</span><span class="sxs-lookup"><span data-stu-id="dab1b-108">The **ISCardFileAccess** interface can be used to implement a high-level interface to a card-based file system with an underlying card file system based on the structure defined in ISO/IEC 7816-4.</span></span> <span data-ttu-id="dab1b-109">D’autres implémentations sont possibles, mais elles sont supposées être les plus courantes.</span><span class="sxs-lookup"><span data-stu-id="dab1b-109">Other implementations are possible, but this is expected to be the most common.</span></span>

<span data-ttu-id="dab1b-110">L’interface **ISCardFileAccess** peut être utilisée pour exposer des entités de système de fichiers de manière très familière aux développeurs d’applications dans l’environnement de PC.</span><span class="sxs-lookup"><span data-stu-id="dab1b-110">The **ISCardFileAccess** interface can be used to expose file system entities in a manner very familiar to application developers in the PC environment.</span></span> <span data-ttu-id="dab1b-111">Il fournit des mécanismes pour localiser des fichiers spécifiques et effectuer des opérations courantes, telles que la sélection, la lecture, l’écriture, la création et la suppression.</span><span class="sxs-lookup"><span data-stu-id="dab1b-111">It provides mechanisms for locating specific files and performing common operations such as selecting, reading, writing, creating and deleting.</span></span> <span data-ttu-id="dab1b-112">Il encapsule et masque une grande partie des détails de bas niveau liés à l’exécution de ces opérations au niveau de la carte.</span><span class="sxs-lookup"><span data-stu-id="dab1b-112">It encapsulates and masks much of the low-level detail involved in performing these operations at the card level.</span></span>

<span data-ttu-id="dab1b-113">Voici une utilisation courante de l’interface **ISCardFileAccess** .</span><span class="sxs-lookup"><span data-stu-id="dab1b-113">Following is a typical use of the **ISCardFileAccess** interface.</span></span> <span data-ttu-id="dab1b-114">Dans ce cas, l’interface **ISCardFileAccess** est utilisée pour sélectionner, ouvrir et écrire dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="dab1b-114">In this case, the **ISCardFileAccess** interface is used to select, open, and write to a file.</span></span>

<span data-ttu-id="dab1b-115">**Pour écrire dans un fichier**</span><span class="sxs-lookup"><span data-stu-id="dab1b-115">**To write to a file**</span></span>

1.  <span data-ttu-id="dab1b-116">Appelez [**ISCardManage :: CreateFileAccess**](iscardmanage-createfileaccess.md) pour créer une interface **ISCardFileAccess** .</span><span class="sxs-lookup"><span data-stu-id="dab1b-116">Call [**ISCardManage::CreateFileAccess**](iscardmanage-createfileaccess.md) to create an **ISCardFileAccess** interface.</span></span>
2.  <span data-ttu-id="dab1b-117">Appelez [**Open**](iscardfileaccess-open.md) pour sélectionner et ouvrir le fichier.</span><span class="sxs-lookup"><span data-stu-id="dab1b-117">Call [**Open**](iscardfileaccess-open.md) to select and open the file.</span></span>
3.  <span data-ttu-id="dab1b-118">Appelez [**Write**](iscardfileaccess-write.md).</span><span class="sxs-lookup"><span data-stu-id="dab1b-118">Call [**Write**](iscardfileaccess-write.md).</span></span>
4.  <span data-ttu-id="dab1b-119">Appelez [**Close**](iscardfileaccess-close.md).</span><span class="sxs-lookup"><span data-stu-id="dab1b-119">Call [**Close**](iscardfileaccess-close.md).</span></span>
5.  <span data-ttu-id="dab1b-120">Libérez l’interface **ISCardFileAccess** .</span><span class="sxs-lookup"><span data-stu-id="dab1b-120">Release the **ISCardFileAccess** interface.</span></span>

## <a name="members"></a><span data-ttu-id="dab1b-121">Membres</span><span class="sxs-lookup"><span data-stu-id="dab1b-121">Members</span></span>

<span data-ttu-id="dab1b-122">L’interface **ISCardFileAccess** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="dab1b-122">The **ISCardFileAccess** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="dab1b-123">**ISCardFileAccess** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dab1b-123">**ISCardFileAccess** also has these types of members:</span></span>

-   [<span data-ttu-id="dab1b-124">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dab1b-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dab1b-125">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dab1b-125">Methods</span></span>

<span data-ttu-id="dab1b-126">L’interface **ISCardFileAccess** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="dab1b-126">The **ISCardFileAccess** interface has these methods.</span></span>



| <span data-ttu-id="dab1b-127">Méthode</span><span class="sxs-lookup"><span data-stu-id="dab1b-127">Method</span></span>                                                              | <span data-ttu-id="dab1b-128">Description</span><span class="sxs-lookup"><span data-stu-id="dab1b-128">Description</span></span>                                                                                                                                  |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dab1b-129">**ChangeDir**</span><span class="sxs-lookup"><span data-stu-id="dab1b-129">**ChangeDir**</span></span>](iscardfileaccess-changedir.md)                     | <span data-ttu-id="dab1b-130">Remplace le répertoire de carte à puce actuel par le nouveau répertoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="dab1b-130">Changes the current smart card directory to the new specified directory.</span></span><br/>                                                          |
| [<span data-ttu-id="dab1b-131">**Fermer**</span><span class="sxs-lookup"><span data-stu-id="dab1b-131">**Close**</span></span>](iscardfileaccess-close.md)                             | <span data-ttu-id="dab1b-132">Ferme le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="dab1b-132">Closes the specified file.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="dab1b-133">**Créés**</span><span class="sxs-lookup"><span data-stu-id="dab1b-133">**Create**</span></span>](iscardfileaccess-create.md)                           | <span data-ttu-id="dab1b-134">Crée un fichier à un emplacement donné dans le système de fichiers ICC.</span><span class="sxs-lookup"><span data-stu-id="dab1b-134">Creates a file at a given location within the ICC file system.</span></span><br/>                                                                    |
| [<span data-ttu-id="dab1b-135">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="dab1b-135">**Delete**</span></span>](iscardfileaccess-delete.md)                           | <span data-ttu-id="dab1b-136">Supprime un fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="dab1b-136">Deletes a specified file.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="dab1b-137">**Répertoire**</span><span class="sxs-lookup"><span data-stu-id="dab1b-137">**Directory**</span></span>](iscardfileaccess-directory.md)                     | <span data-ttu-id="dab1b-138">Récupère une liste de fichiers.</span><span class="sxs-lookup"><span data-stu-id="dab1b-138">Retrieves a list of files.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="dab1b-139">**GetCurrentDir**</span><span class="sxs-lookup"><span data-stu-id="dab1b-139">**GetCurrentDir**</span></span>](iscardfileaccess-getcurrentdir.md)             | <span data-ttu-id="dab1b-140">Retourne un chemin d’accès absolu au répertoire actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="dab1b-140">Returns an absolute path to the currently selected directory.</span></span><br/>                                                                     |
| [<span data-ttu-id="dab1b-141">**GetFileCapabilities**</span><span class="sxs-lookup"><span data-stu-id="dab1b-141">**GetFileCapabilities**</span></span>](iscardfileaccess-getfilecapabilities.md) | <span data-ttu-id="dab1b-142">Récupère les fonctionnalités de fichier.</span><span class="sxs-lookup"><span data-stu-id="dab1b-142">Retrieves file capabilities.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="dab1b-143">**GetProperties**</span><span class="sxs-lookup"><span data-stu-id="dab1b-143">**GetProperties**</span></span>](iscardfileaccess-getproperties.md)             | <span data-ttu-id="dab1b-144">Récupère les données primitives référencées par des balises pour l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="dab1b-144">Retrieves the primitive data referred by tags for the specified object.</span></span><br/>                                                           |
| [<span data-ttu-id="dab1b-145">**Invalidate**</span><span class="sxs-lookup"><span data-stu-id="dab1b-145">**Invalidate**</span></span>](iscardfileaccess-invalidate.md)                   | <span data-ttu-id="dab1b-146">Rend le fichier spécifié non valide.</span><span class="sxs-lookup"><span data-stu-id="dab1b-146">Makes the specified file not valid.</span></span><br/>                                                                                               |
| [<span data-ttu-id="dab1b-147">**Afficher**</span><span class="sxs-lookup"><span data-stu-id="dab1b-147">**Open**</span></span>](iscardfileaccess-open.md)                               | <span data-ttu-id="dab1b-148">Ouvre le fichier spécifié pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="dab1b-148">Opens the specified file for further use.</span></span><br/>                                                                                         |
| [<span data-ttu-id="dab1b-149">**En lecture**</span><span class="sxs-lookup"><span data-stu-id="dab1b-149">**Read**</span></span>](iscardfileaccess-read.md)                               | <span data-ttu-id="dab1b-150">Lit et retourne les données spécifiées à partir d’un fichier donné.</span><span class="sxs-lookup"><span data-stu-id="dab1b-150">Reads and returns the specified data from a given file.</span></span><br/>                                                                           |
| [<span data-ttu-id="dab1b-151">**Réhabiliter**</span><span class="sxs-lookup"><span data-stu-id="dab1b-151">**Rehabilitate**</span></span>](iscardfileaccess-rehabilitate.md)               | <span data-ttu-id="dab1b-152">Rend un fichier (EF ou DF) qui a été précédemment rendu non valide à l’aide de la commande Invalidate, accessible par l’application.</span><span class="sxs-lookup"><span data-stu-id="dab1b-152">Makes a file (EF or DF), which has been previously made not valid by using the Invalidate command, accessible by the application.</span></span><br/> |
| [<span data-ttu-id="dab1b-153">**Seek**</span><span class="sxs-lookup"><span data-stu-id="dab1b-153">**Seek**</span></span>](iscardfileaccess-seek.md)                               | <span data-ttu-id="dab1b-154">Sélectionne l’objet à partir duquel l’autorisation de lecture/écriture sera effectuée.</span><span class="sxs-lookup"><span data-stu-id="dab1b-154">Selects the object from which read/write permission will be done.</span></span><br/>                                                                 |
| [<span data-ttu-id="dab1b-155">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="dab1b-155">**SetProperties**</span></span>](iscardfileaccess-setproperties.md)             | <span data-ttu-id="dab1b-156">Définit les données primitives référencées par des balises pour l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="dab1b-156">Sets the primitive data referred by tags for the specified object.</span></span><br/>                                                                |
| [<span data-ttu-id="dab1b-157">**Ecrire**</span><span class="sxs-lookup"><span data-stu-id="dab1b-157">**Write**</span></span>](iscardfileaccess-write.md)                             | <span data-ttu-id="dab1b-158">Écrit des données dans un fichier ouvert en cours.</span><span class="sxs-lookup"><span data-stu-id="dab1b-158">Writes data to a current opened file.</span></span><br/>                                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="dab1b-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dab1b-159">Requirements</span></span>



| <span data-ttu-id="dab1b-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dab1b-160">Requirement</span></span> | <span data-ttu-id="dab1b-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="dab1b-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dab1b-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dab1b-162">Minimum supported client</span></span><br/> | <span data-ttu-id="dab1b-163">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dab1b-163">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="dab1b-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dab1b-164">Minimum supported server</span></span><br/> | <span data-ttu-id="dab1b-165">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dab1b-165">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="dab1b-166">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="dab1b-166">End of client support</span></span><br/>    | <span data-ttu-id="dab1b-167">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dab1b-167">Windows XP</span></span><br/>                                |
| <span data-ttu-id="dab1b-168">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="dab1b-168">End of server support</span></span><br/>    | <span data-ttu-id="dab1b-169">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dab1b-169">Windows Server 2003</span></span><br/>                       |



 

 
