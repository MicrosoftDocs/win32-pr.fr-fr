---
title: Fonctions système de fichiers DFS
description: Les fonctions système de fichiers DFS (DFS) sont les suivantes.
ms.assetid: 8f86b717-fe26-4550-8b71-8f7df5ca6022
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 463c085115f6d3e88f9a3be80a890caa0aacb340
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483768"
---
# <a name="distributed-file-system-functions"></a><span data-ttu-id="663bb-103">Fonctions système de fichiers DFS</span><span class="sxs-lookup"><span data-stu-id="663bb-103">Distributed File System Functions</span></span>

<span data-ttu-id="663bb-104">Les fonctions système de fichiers DFS (DFS) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="663bb-104">The following are the Distributed File System (DFS) functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="663bb-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="663bb-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="663bb-106">NetDfsAdd</span><span class="sxs-lookup"><span data-stu-id="663bb-106">NetDfsAdd</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsadd)
</dt> <dd>
<span data-ttu-id="663bb-107">Crée un nouveau lien système de fichiers DFS (DFS) ou ajoute des cibles à un lien existant dans un espace de noms DFS.</span><span class="sxs-lookup"><span data-stu-id="663bb-107">Creates a new Distributed File System (DFS) link or adds targets to an existing link in a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-108">NetDfsAddFtRoot</span><span class="sxs-lookup"><span data-stu-id="663bb-108">NetDfsAddFtRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddftroot)
</dt> <dd>
<span data-ttu-id="663bb-109">Crée un nouvel espace de noms de système de fichiers DFS basé sur un domaine (DFS).</span><span class="sxs-lookup"><span data-stu-id="663bb-109">Creates a new domain-based Distributed File System (DFS) namespace.</span></span> <span data-ttu-id="663bb-110">Si l’espace de noms existe déjà, la fonction y ajoute la cible racine spécifiée.</span><span class="sxs-lookup"><span data-stu-id="663bb-110">If the namespace already exists, the function adds the specified root target to it.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-111">NetDfsAddRootTarget</span><span class="sxs-lookup"><span data-stu-id="663bb-111">NetDfsAddRootTarget</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget)
</dt> <dd>
<span data-ttu-id="663bb-112">Crée un espace de noms DFS autonome ou basé sur un domaine ou ajoute une nouvelle cible racine à un espace de noms basé sur un domaine existant.</span><span class="sxs-lookup"><span data-stu-id="663bb-112">Creates a domain-based or stand-alone DFS namespace or adds a new root target to an existing domain-based namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-113">NetDfsAddStdRoot</span><span class="sxs-lookup"><span data-stu-id="663bb-113">NetDfsAddStdRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddstdroot)
</dt> <dd>
<span data-ttu-id="663bb-114">Crée un espace de noms système de fichiers DFS (DFS) autonome.</span><span class="sxs-lookup"><span data-stu-id="663bb-114">Creates a new stand-alone Distributed File System (DFS) namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-115">NetDfsEnum</span><span class="sxs-lookup"><span data-stu-id="663bb-115">NetDfsEnum</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum)
</dt> <dd>
<span data-ttu-id="663bb-116">Énumère les espaces de noms système de fichiers DFS (DFS) hébergés sur un serveur ou les liens DFS d’un espace de noms hébergé par un serveur.</span><span class="sxs-lookup"><span data-stu-id="663bb-116">Enumerates the Distributed File System (DFS) namespaces hosted on a server or DFS links of a namespace hosted by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-117">NetDfsGetClientInfo</span><span class="sxs-lookup"><span data-stu-id="663bb-117">NetDfsGetClientInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> <dd>
<span data-ttu-id="663bb-118">Récupère des informations sur une racine ou un lien système de fichiers DFS (DFS) à partir du cache conservé par le client DFS.</span><span class="sxs-lookup"><span data-stu-id="663bb-118">Retrieves information about a Distributed File System (DFS) root or link from the cache maintained by the DFS client.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-119">NetDfsGetFtContainerSecurity</span><span class="sxs-lookup"><span data-stu-id="663bb-119">NetDfsGetFtContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)
</dt> <dd>
<span data-ttu-id="663bb-120">Récupère le descripteur de sécurité de l’objet conteneur pour les espaces de noms DFS basés sur un domaine dans le domaine de Active Directory spécifié.</span><span class="sxs-lookup"><span data-stu-id="663bb-120">Retrieves the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-121">NetDfsGetInfo</span><span class="sxs-lookup"><span data-stu-id="663bb-121">NetDfsGetInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo)
</dt> <dd>
<span data-ttu-id="663bb-122">Récupère des informations sur la racine ou le lien d’un système de fichiers DFS (DFS) spécifié dans un espace de noms DFS.</span><span class="sxs-lookup"><span data-stu-id="663bb-122">Retrieves information about a specified Distributed File System (DFS) root or link in a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-123">NetDfsGetSecurity</span><span class="sxs-lookup"><span data-stu-id="663bb-123">NetDfsGetSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)
</dt> <dd>
<span data-ttu-id="663bb-124">Récupère le descripteur de sécurité pour l’objet racine de l’espace de noms DFS spécifié.</span><span class="sxs-lookup"><span data-stu-id="663bb-124">Retrieves the security descriptor for the root object of the specified DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-125">NetDfsGetStdContainerSecurity</span><span class="sxs-lookup"><span data-stu-id="663bb-125">NetDfsGetStdContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetstdcontainersecurity)
</dt> <dd>
<span data-ttu-id="663bb-126">Récupère le descripteur de sécurité pour l’objet conteneur de l’espace de noms DFS autonome spécifié.</span><span class="sxs-lookup"><span data-stu-id="663bb-126">Retrieves the security descriptor for the container object of the specified stand-alone DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-127">NetDfsGetSupportedNamespaceVersion</span><span class="sxs-lookup"><span data-stu-id="663bb-127">NetDfsGetSupportedNamespaceVersion</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsupportednamespaceversion)
</dt> <dd>
<span data-ttu-id="663bb-128">Détermine le numéro de version des métadonnées prises en charge.</span><span class="sxs-lookup"><span data-stu-id="663bb-128">Determines the supported metadata version number.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-129">NetDfsMove</span><span class="sxs-lookup"><span data-stu-id="663bb-129">NetDfsMove</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsmove)
</dt> <dd>
<span data-ttu-id="663bb-130">Renomme ou déplace un lien DFS.</span><span class="sxs-lookup"><span data-stu-id="663bb-130">Renames or moves a DFS link.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-131">NetDfsRemove</span><span class="sxs-lookup"><span data-stu-id="663bb-131">NetDfsRemove</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremove)
</dt> <dd>
<span data-ttu-id="663bb-132">Supprime un lien système de fichiers DFS (DFS) ou une cible de lien spécifique d’un lien DFS dans un espace de noms DFS.</span><span class="sxs-lookup"><span data-stu-id="663bb-132">Removes a Distributed File System (DFS) link or a specific link target of a DFS link in a DFS namespace.</span></span> <span data-ttu-id="663bb-133">Lors de la suppression d’une cible de lien spécifique, le lien lui-même est supprimé si la dernière cible de lien du lien est supprimée.</span><span class="sxs-lookup"><span data-stu-id="663bb-133">When removing a specific link target, the link itself is removed if the last link target of the link is removed.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-134">NetDfsRemoveFtRoot</span><span class="sxs-lookup"><span data-stu-id="663bb-134">NetDfsRemoveFtRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftroot)
</dt> <dd>
<span data-ttu-id="663bb-135">Supprime la cible racine spécifiée d’un espace de noms de système de fichiers DFS basé sur un domaine (DFS).</span><span class="sxs-lookup"><span data-stu-id="663bb-135">Removes the specified root target from a domain-based Distributed File System (DFS) namespace.</span></span> <span data-ttu-id="663bb-136">Si la dernière cible racine de l’espace de noms DFS est supprimée, la fonction supprime également l’espace de noms DFS.</span><span class="sxs-lookup"><span data-stu-id="663bb-136">If the last root target of the DFS namespace is being removed, the function also deletes the DFS namespace.</span></span> <span data-ttu-id="663bb-137">Un espace de noms DFS peut être supprimé sans supprimer au préalable tous les liens qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="663bb-137">A DFS namespace can be deleted without first deleting all the links in it.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-138">NetDfsRemoveFtRootForced</span><span class="sxs-lookup"><span data-stu-id="663bb-138">NetDfsRemoveFtRootForced</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced)
</dt> <dd>
<span data-ttu-id="663bb-139">Supprime la cible racine spécifiée d’un espace de noms de système de fichiers DFS basé sur un domaine (DFS), même si le serveur cible racine est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="663bb-139">Removes the specified root target from a domain-based Distributed File System (DFS) namespace, even if the root target server is offline.</span></span> <span data-ttu-id="663bb-140">Si la dernière cible racine de l’espace de noms DFS est supprimée, la fonction supprime également l’espace de noms DFS.</span><span class="sxs-lookup"><span data-stu-id="663bb-140">If the last root target of the DFS namespace is being removed, the function also deletes the DFS namespace.</span></span> <span data-ttu-id="663bb-141">Un espace de noms DFS peut être supprimé sans supprimer au préalable tous les liens qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="663bb-141">A DFS namespace can be deleted without first deleting all the links in it.</span></span>

> [!Note]
> <span data-ttu-id="663bb-142">La fonction [**NetDfsRemoveFtRootForced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) ne met pas à jour le registre sur le serveur cible racine DFS.</span><span class="sxs-lookup"><span data-stu-id="663bb-142">The [**NetDfsRemoveFtRootForced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) function does not update the registry on the DFS root target server.</span></span> <span data-ttu-id="663bb-143">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="663bb-143">For more information, see the Remarks section.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-144">NetDfsRemoveRootTarget</span><span class="sxs-lookup"><span data-stu-id="663bb-144">NetDfsRemoveRootTarget</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveroottarget)
</dt> <dd>
<span data-ttu-id="663bb-145">Supprime une cible racine DFS d’un espace de noms DFS basé sur un domaine.</span><span class="sxs-lookup"><span data-stu-id="663bb-145">Removes a DFS root target from a domain-based DFS namespace.</span></span> <span data-ttu-id="663bb-146">Si la cible racine est la dernière cible racine de l’espace de noms DFS, cette fonction supprime l’espace de noms DFS.</span><span class="sxs-lookup"><span data-stu-id="663bb-146">If the root target is the last root target in the DFS namespace, this function removes the DFS namespace.</span></span> <span data-ttu-id="663bb-147">Cette fonction peut également être utilisée pour supprimer un espace de noms DFS autonome.</span><span class="sxs-lookup"><span data-stu-id="663bb-147">This function can also be used to remove a stand-alone DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-148">NetDfsRemoveStdRoot</span><span class="sxs-lookup"><span data-stu-id="663bb-148">NetDfsRemoveStdRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremovestdroot)
</dt> <dd>
<span data-ttu-id="663bb-149">Supprime un espace de noms système de fichiers DFS (DFS) autonome.</span><span class="sxs-lookup"><span data-stu-id="663bb-149">Deletes a stand-alone Distributed File System (DFS) namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-150">NetDfsSetClientInfo</span><span class="sxs-lookup"><span data-stu-id="663bb-150">NetDfsSetClientInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetclientinfo)
</dt> <dd>
<span data-ttu-id="663bb-151">Modifie les informations relatives à une racine ou un lien système de fichiers DFS (DFS) dans le cache géré par le client DFS.</span><span class="sxs-lookup"><span data-stu-id="663bb-151">Modifies information about a Distributed File System (DFS) root or link in the cache maintained by the DFS client.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-152">NetDfsSetFtContainerSecurity</span><span class="sxs-lookup"><span data-stu-id="663bb-152">NetDfsSetFtContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)
</dt> <dd>
<span data-ttu-id="663bb-153">Définit le descripteur de sécurité de l’objet conteneur pour les espaces de noms DFS basés sur un domaine dans le domaine de Active Directory spécifié.</span><span class="sxs-lookup"><span data-stu-id="663bb-153">Sets the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-154">NetDfsSetInfo</span><span class="sxs-lookup"><span data-stu-id="663bb-154">NetDfsSetInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo)
</dt> <dd>
<span data-ttu-id="663bb-155">Définit ou modifie les informations relatives à une racine système de fichiers DFS (DFS), une cible racine, un lien ou une cible de lien spécifique.</span><span class="sxs-lookup"><span data-stu-id="663bb-155">Sets or modifies information about a specific Distributed File System (DFS) root, root target, link, or link target.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-156">NetDfsSetSecurity</span><span class="sxs-lookup"><span data-stu-id="663bb-156">NetDfsSetSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)
</dt> <dd>
<span data-ttu-id="663bb-157">Définit le descripteur de sécurité pour l’objet racine de l’espace de noms DFS spécifié.</span><span class="sxs-lookup"><span data-stu-id="663bb-157">Sets the security descriptor for the root object of the specified DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="663bb-158">NetDfsSetStdContainerSecurity</span><span class="sxs-lookup"><span data-stu-id="663bb-158">NetDfsSetStdContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity)
</dt> <dd>
<span data-ttu-id="663bb-159">Définit le descripteur de sécurité pour l’objet conteneur de l’espace de noms DFS autonome spécifié.</span><span class="sxs-lookup"><span data-stu-id="663bb-159">Sets the security descriptor for the container object of the specified stand-alone DFS namespace.</span></span>

</dd> </dl>

<span data-ttu-id="663bb-160">Notez qu’une application qui appelle l’une des fonctions peut entraîner indirectement le serveur d’espaces de noms DFS local qui traite l’appel de fonction pour effectuer une synchronisation complète des métadonnées d’espace de noms associées à partir du maître d’émulateur de contrôleur de domaine principal pour ce domaine.</span><span class="sxs-lookup"><span data-stu-id="663bb-160">Note that an application invoking any of the functions may indirectly cause the local DFS Namespace server servicing the function call to perform a full synchronization of the related namespace metadata from the PDC emulator master for that domain.</span></span> <span data-ttu-id="663bb-161">Cette synchronisation complète peut se produire même lorsque le mode d’extensibilité racine est configuré pour cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="663bb-161">This full synchronization could happen even when root scalability mode is configured for that namespace.</span></span>
