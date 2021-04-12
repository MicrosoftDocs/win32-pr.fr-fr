---
description: Les modules de fusion sont essentiellement simplifiés. msi, qui est l’extension de nom de fichier d’un package d’installation Windows Installer. Un module de fusion standard a une extension de nom de fichier. msm.
ms.assetid: 580fe58a-4636-4f9a-a68d-4fd0e281e949
title: À propos des modules de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70d416b89f0979d5651480a05052e95b4d32e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319045"
---
# <a name="about-merge-modules"></a><span data-ttu-id="7b876-104">À propos des modules de fusion</span><span class="sxs-lookup"><span data-stu-id="7b876-104">About Merge Modules</span></span>

<span data-ttu-id="7b876-105">Les modules de fusion sont essentiellement simplifiés. msi, qui est l’extension de nom de fichier d’un package d’installation Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7b876-105">Merge modules are essentially simplified .msi files, which is the file name extension for a Windows Installer installation package.</span></span> <span data-ttu-id="7b876-106">Un module de fusion standard a une extension de nom de fichier. msm.</span><span class="sxs-lookup"><span data-stu-id="7b876-106">A standard merge module has an .msm file name extension.</span></span>

<span data-ttu-id="7b876-107">Un module de fusion ne peut pas être installé seul, car il n’a pas de tables de base de données vitales présentes dans une base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="7b876-107">A merge module cannot be installed alone because its lacks some vital database tables that are present in an installation database.</span></span> <span data-ttu-id="7b876-108">Les modules de fusion contiennent également des tables supplémentaires qui sont uniques à eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="7b876-108">Merge modules also contain additional tables that are unique to themselves.</span></span> <span data-ttu-id="7b876-109">Pour installer les informations fournies par un module de fusion avec une application, le module doit d’abord être fusionné dans le fichier. msi de l’application.</span><span class="sxs-lookup"><span data-stu-id="7b876-109">To install the information delivered by a merge module with an application, the module must first be merged into the application's .msi file.</span></span>

<span data-ttu-id="7b876-110">Un module de fusion se compose des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="7b876-110">A merge module consists of the following parts:</span></span>

-   <span data-ttu-id="7b876-111">Une [base de données de module de fusion](merge-module-database.md) contenant les propriétés d’installation et la logique d’installation fournies par le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="7b876-111">A [Merge Module Database](merge-module-database.md) containing the installation properties and setup logic being delivered by the merge module.</span></span>
-   <span data-ttu-id="7b876-112">[Référence du flux de données de résumé du module de fusion](merge-module-summary-information-stream-reference.md) décrivant le module.</span><span class="sxs-lookup"><span data-stu-id="7b876-112">A [Merge Module Summary Information Stream Reference](merge-module-summary-information-stream-reference.md) describing the module.</span></span>
-   <span data-ttu-id="7b876-113">Fichier CAB [ inetMergeModule.CAB](mergemodule-cabinet.md) stocké en tant que flux à l’intérieur du module de fusion.</span><span class="sxs-lookup"><span data-stu-id="7b876-113">A [MergeModule.CABinet](mergemodule-cabinet.md) cabinet file stored as a stream inside the merge module.</span></span> <span data-ttu-id="7b876-114">Ce fichier cab contient tous les fichiers requis par les composants fournis par le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="7b876-114">This cabinet contains all the files required by the components delivered by the merge module.</span></span>

<span data-ttu-id="7b876-115">Les [modules de fusion à plusieurs langues](multiple-language-merge-modules.md) peuvent fournir des composants à un package d’installation dans plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="7b876-115">[Multiple language merge modules](multiple-language-merge-modules.md) can deliver components to an installation package in multiple languages.</span></span> <span data-ttu-id="7b876-116">Dans un module de fusion à plusieurs langues, la base de données contient les propriétés d’installation et la logique pour plusieurs langues et l’armoire MergeModule.CABinet inclut tous les fichiers nécessaires pour installer les composants avec toutes les langues prises en charge par le module.</span><span class="sxs-lookup"><span data-stu-id="7b876-116">In a multiple language merge module the database contains the installation properties and logic for more than one language and the MergeModule.CABinet cabinet includes all the files necessary to install components with all the languages supported by the module.</span></span>

 

 



