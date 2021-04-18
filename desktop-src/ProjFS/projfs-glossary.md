---
title: Glossaire du système de fichiers projeté de Windows
description: Termes spéciaux utilisés dans ProjFS.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: c6eac8faa83e2c898e4b1a3ada5c24ef81151b22
ms.sourcegitcommit: a48b68a75323edfb902eb04fbe6d0ecba6988c21
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/21/2020
ms.locfileid: "106512490"
---
# <a name="windows-projected-file-system-glossary"></a><span data-ttu-id="18f5c-103">Glossaire du système de fichiers projeté de Windows</span><span class="sxs-lookup"><span data-stu-id="18f5c-103">Windows Projected File System glossary</span></span>

<span data-ttu-id="18f5c-104">Termes spéciaux utilisés dans ProjFS.</span><span class="sxs-lookup"><span data-stu-id="18f5c-104">Special terms used in ProjFS.</span></span>

<dl>
<dt>

<span data-ttu-id="18f5c-105"><span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**magasin de stockage**</span><span class="sxs-lookup"><span data-stu-id="18f5c-105"><span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**backing store**</span></span>
</dt>
<dd>

<span data-ttu-id="18f5c-106">Données hiérarchiques gérées par le fournisseur et projetées dans le système de fichiers sous forme de fichiers et de répertoires.</span><span class="sxs-lookup"><span data-stu-id="18f5c-106">Provider-maintained hierarchical data that is projected into the file system as files and directories.</span></span>
</dd>

<dt>

<span data-ttu-id="18f5c-107"><span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**espace réservé de modification**</span><span class="sxs-lookup"><span data-stu-id="18f5c-107"><span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**dirty placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="18f5c-108">Fichier ou répertoire modifié localement et n’est plus un cache de son état dans le magasin du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="18f5c-108">A file or directory that has been locally modified and is no longer a cache of its state in the provider's store.</span></span>  <span data-ttu-id="18f5c-109">Consultez [l’état du cache dans la racine de virtualisation](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="18f5c-109">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="18f5c-110"><span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**fichier/répertoire complet**</span><span class="sxs-lookup"><span data-stu-id="18f5c-110"><span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**full file/directory**</span></span>
</dt>
<dd>

<span data-ttu-id="18f5c-111">Un fichier ou un répertoire qui a été créé dans le système de fichiers local, ou un fichier qui a été modifié, ce qui n’est plus un cache de son état dans le magasin de stockage.</span><span class="sxs-lookup"><span data-stu-id="18f5c-111">A file or directory that was created in the local file system, or a file that has been modified, making it no longer a cache of its state in the backing store.</span></span>  <span data-ttu-id="18f5c-112">Consultez [l’état du cache dans la racine de virtualisation](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="18f5c-112">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="18f5c-113"><span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**espace réservé hydraté**</span><span class="sxs-lookup"><span data-stu-id="18f5c-113"><span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**hydrated placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="18f5c-114">Fichier dont le contenu et les métadonnées ont été mis en cache sur le disque.</span><span class="sxs-lookup"><span data-stu-id="18f5c-114">A file whose content and metadata have been cached to disk.</span></span>  <span data-ttu-id="18f5c-115">Consultez [l’état du cache dans la racine de virtualisation](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="18f5c-115">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="18f5c-116"><span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**Situé**</span><span class="sxs-lookup"><span data-stu-id="18f5c-116"><span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="18f5c-117">Fichier ou répertoire qui n’est pas entièrement présent sur le disque.</span><span class="sxs-lookup"><span data-stu-id="18f5c-117">A file or directory that is not fully present on disk.</span></span>  <span data-ttu-id="18f5c-118">Consultez [l’état du cache dans la racine de virtualisation](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="18f5c-118">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="18f5c-119"><span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**objet tombstone**</span><span class="sxs-lookup"><span data-stu-id="18f5c-119"><span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**tombstone**</span></span>
</dt>
<dd>

<span data-ttu-id="18f5c-120">Espace réservé masqué spécial qui représente un élément qui a été supprimé du système de fichiers local.</span><span class="sxs-lookup"><span data-stu-id="18f5c-120">A special hidden placeholder that represents an item that has been deleted from the local file system.</span></span>  <span data-ttu-id="18f5c-121">Consultez [l’état du cache dans la racine de virtualisation](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="18f5c-121">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="18f5c-122"><span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**fichier/répertoire virtuel**</span><span class="sxs-lookup"><span data-stu-id="18f5c-122"><span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**virtual file/directory**</span></span>
</dt>
<dd>

<span data-ttu-id="18f5c-123">Fichier ou répertoire qui n’existe pas physiquement sur le disque, mais qui est projeté dans les résultats de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="18f5c-123">A file or directory that does not physically exist on disk, but is projected into enumeration results.</span></span>  <span data-ttu-id="18f5c-124">Consultez [l’état du cache dans la racine de virtualisation](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="18f5c-124">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="18f5c-125"><span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**instance de virtualisation**</span><span class="sxs-lookup"><span data-stu-id="18f5c-125"><span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**virtualization instance**</span></span>
</dt>
<dd>

<span data-ttu-id="18f5c-126">Objet en mémoire qui gère la communication entre le fournisseur et ProjFS pour l’ensemble des fichiers et répertoires situés sous une racine de virtualisation particulière.</span><span class="sxs-lookup"><span data-stu-id="18f5c-126">An in-memory object that manages communication between the provider and ProjFS for the set of files and directories located under a particular virtualization root.</span></span>
</dd>

<dt>

<span data-ttu-id="18f5c-127"><span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**racine de virtualisation**</span><span class="sxs-lookup"><span data-stu-id="18f5c-127"><span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**virtualization root**</span></span>
</dt>
<dd>

<span data-ttu-id="18f5c-128">Répertoire dans le système de fichiers sous lequel les données du fournisseur sont projetées.</span><span class="sxs-lookup"><span data-stu-id="18f5c-128">A directory in the file system under which the provider's data is projected.</span></span>
</dd>

</dl>

<!--
<dt>

<span id="projfs.glossary_"></span><span id="PROJFS.GLOSSARY_"></span>**TERM**
</dt>
<dd>

DEFINITION
</dd>
-->