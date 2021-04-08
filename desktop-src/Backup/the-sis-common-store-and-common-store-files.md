---
title: Le magasin commun SIS et les fichiers Common-Store
description: Tous les fichiers de sauvegarde gérés par la sauvegarde SIS (Single-Instance Store) sont appelés des fichiers de stockage commun.
ms.assetid: c6231c30-9d5a-428d-a94d-9dc8db933432
keywords:
- Sauvegarde des magasins courants
- Sauvegarde SIS (Single-Instance Store), magasins courants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2f86b778b0a8db916fe580b8f833214523eb2e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842537"
---
# <a name="the-sis-common-store-and-common-store-files"></a><span data-ttu-id="33485-105">Le magasin commun SIS et les fichiers Common-Store</span><span class="sxs-lookup"><span data-stu-id="33485-105">The SIS Common Store and Common-Store Files</span></span>

<span data-ttu-id="33485-106">Tous les fichiers de sauvegarde gérés par la sauvegarde SIS (Single-Instance Store) sont appelés des *fichiers de stockage commun*.</span><span class="sxs-lookup"><span data-stu-id="33485-106">All backing files maintained by single-instance store (SIS) backup are called *common-store files*.</span></span> <span data-ttu-id="33485-107">Un *magasin commun* existe sur chaque volume géré par SIS et contient tous les fichiers du magasin commun qui existent sur ce volume.</span><span class="sxs-lookup"><span data-stu-id="33485-107">One *common store* exists on each SIS-maintained volume and contains all of the common-store files that exist on that volume.</span></span> <span data-ttu-id="33485-108">Ce répertoire se trouve dans le répertoire racine du volume et est nommé « \\ SIS Common Store ».</span><span class="sxs-lookup"><span data-stu-id="33485-108">This directory is located in the root directory of the volume and is named "\\SIS Common Store".</span></span> <span data-ttu-id="33485-109">Le magasin commun est implémenté en tant que répertoire protégé contre l’accès utilisateur normal, car les fichiers du magasin commun sont conçus pour être accessibles directement uniquement par les fonctions d’API de sauvegarde SIS, et non pour les applications de sauvegarde et de restauration.</span><span class="sxs-lookup"><span data-stu-id="33485-109">The common store is implemented as a directory that is protected against normal user access, because common-store files are intended to be accessed directly only by SIS backup API functions and not backup and restore applications.</span></span>

<span data-ttu-id="33485-110">Les propriétés d’un fichier de magasin commun sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="33485-110">The properties of a common-store file are the following:</span></span>

-   <span data-ttu-id="33485-111">Un fichier de magasin commun peut avoir un ou plusieurs liens pointant vers celui-ci.</span><span class="sxs-lookup"><span data-stu-id="33485-111">A common-store file may have one or more links pointing to it.</span></span>
-   <span data-ttu-id="33485-112">Une fois créé, le contenu d’un fichier de magasin commun ne change jamais.</span><span class="sxs-lookup"><span data-stu-id="33485-112">After it is created, the contents of a common-store file never change.</span></span>
-   <span data-ttu-id="33485-113">Les noms des fichiers de stockage commun sont globalement uniques, c’est-à-dire qu’ils sont uniques sur tous les volumes de tous les systèmes du monde, et la liaison entre un nom de fichier de magasin commun et ses données est globalement statique.</span><span class="sxs-lookup"><span data-stu-id="33485-113">The names of common-store files are globally unique—that is, they are unique across all volumes across all systems in the world, and the binding between a common-store file name and its data is globally static.</span></span>

<span data-ttu-id="33485-114">Lorsque SIS est activé sur un volume, une copie des fichiers dupliqués est alors créée dans le magasin commun, et tous les fichiers dupliqués sont remplacés par [des liens SIS](sis-links-and-reparse-points.md) pointant vers le fichier de magasin commun.</span><span class="sxs-lookup"><span data-stu-id="33485-114">When SIS is enabled on a volume, one copy of the duplicate files is then created to the common store, and all of the duplicate files are replaced with [SIS links](sis-links-and-reparse-points.md) pointing to the common-store file.</span></span> <span data-ttu-id="33485-115">Pour plus d’informations, consultez [activation ou désactivation de SIS sur un volume](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) dans la documentation technet.</span><span class="sxs-lookup"><span data-stu-id="33485-115">For more information, see [Enabling or Disabling SIS on a Volume](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) in the TechNet documentation.</span></span>

<span data-ttu-id="33485-116">Lorsque vous accédez à l’un des liens SIS pour une opération d’écriture, le filtre SIS restaure d’abord le contenu d’origine du fichier de liaison SIS à partir du fichier de magasin commun, le point d’analyse reliant le fichier de liaison SIS au magasin commun est supprimé, puis l’opération d’écriture est effectuée sur le fichier de destination d’origine.</span><span class="sxs-lookup"><span data-stu-id="33485-116">When one of the SIS links is accessed for a write operation, the SIS filter first restores the original contents of the SIS link file from the common-store file, the reparse point linking the SIS link file to the common store is removed, and then the write operation is performed on the original destination file.</span></span>

<span data-ttu-id="33485-117">Le fichier du magasin commun est supprimé uniquement lorsque le dernier lien SIS qui pointe vers celui-ci est supprimé.</span><span class="sxs-lookup"><span data-stu-id="33485-117">The common-store file is removed only when the last SIS link pointing to it is deleted.</span></span>

 

 