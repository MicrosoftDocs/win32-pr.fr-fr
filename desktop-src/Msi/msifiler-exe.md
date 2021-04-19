---
description: MsiFiler.exe remplit la table de fichiers avec des versions de fichier, des langues et des tailles basées sur un répertoire source. Il peut également mettre à jour la table MsiFileHash avec des hachages de fichier.
ms.assetid: cc3db60b-0b1d-4582-8b40-0b55f83e00be
title: Msifiler.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d7aeceae7abd8a9786079788e68c7d7bda35ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515009"
---
# <a name="msifilerexe"></a><span data-ttu-id="05b29-104">Msifiler.exe</span><span class="sxs-lookup"><span data-stu-id="05b29-104">Msifiler.exe</span></span>

<span data-ttu-id="05b29-105">MsiFiler.exe remplit la [table de fichiers](file-table.md) avec des versions de fichier, des langues et des tailles basées sur un répertoire source.</span><span class="sxs-lookup"><span data-stu-id="05b29-105">MsiFiler.exe populates the [File table](file-table.md) with file versions, languages, and sizes based upon a source directory.</span></span> <span data-ttu-id="05b29-106">Il peut également mettre à jour la [table MsiFileHash](msifilehash-table.md) avec des hachages de fichier.</span><span class="sxs-lookup"><span data-stu-id="05b29-106">It can also update the [MsiFileHash table](msifilehash-table.md) with file hashes.</span></span>

## <a name="syntax"></a><span data-ttu-id="05b29-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05b29-107">Syntax</span></span>

<span data-ttu-id="05b29-108">**msifiler.exe-d** *{base de données}* **\[ -v \] \[ -h \] \[ -s \] altsource**</span><span class="sxs-lookup"><span data-stu-id="05b29-108">**msifiler.exe -d** *{database}* **\[-v\] \[-h\] \[-s ALTSOURCE\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="05b29-109">Options de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="05b29-109">Command Line Options</span></span>

<span data-ttu-id="05b29-110">Msifiler.exe utilise les options de ligne de commande suivantes qui ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="05b29-110">Msifiler.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="05b29-111">Un séparateur de barre oblique peut également être utilisé à la place d’un tiret.</span><span class="sxs-lookup"><span data-stu-id="05b29-111">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="05b29-112">Option</span><span class="sxs-lookup"><span data-stu-id="05b29-112">Option</span></span> | <span data-ttu-id="05b29-113">Paramètre</span><span class="sxs-lookup"><span data-stu-id="05b29-113">Parameter</span></span>   | <span data-ttu-id="05b29-114">Description</span><span class="sxs-lookup"><span data-stu-id="05b29-114">Description</span></span>                                                                                                                                                                  |
|--------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05b29-115">-d</span><span class="sxs-lookup"><span data-stu-id="05b29-115">-d</span></span>     | <span data-ttu-id="05b29-116">*database*</span><span class="sxs-lookup"><span data-stu-id="05b29-116">*database*</span></span>  | <span data-ttu-id="05b29-117">La base de données (fichier. msi) à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="05b29-117">The database (.msi file) that is to be updated.</span></span>                                                                                                                              |
| <span data-ttu-id="05b29-118">-v</span><span class="sxs-lookup"><span data-stu-id="05b29-118">-v</span></span>     |             | <span data-ttu-id="05b29-119">Utilisez le mode détaillé.</span><span class="sxs-lookup"><span data-stu-id="05b29-119">Use verbose mode.</span></span>                                                                                                                                                            |
| <span data-ttu-id="05b29-120">-H</span><span class="sxs-lookup"><span data-stu-id="05b29-120">-h</span></span>     |             | <span data-ttu-id="05b29-121">Remplissez la [table MsiFileHash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="05b29-121">Populate the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="05b29-122">La table est créée si elle n’existe pas déjà.</span><span class="sxs-lookup"><span data-stu-id="05b29-122">This creates the table if it does not already exist.</span></span> <span data-ttu-id="05b29-123">La table MsiFileHash peut uniquement être utilisée avec des fichiers sans version.</span><span class="sxs-lookup"><span data-stu-id="05b29-123">The MsiFileHash table can only be used with unversioned files.</span></span> |
| <span data-ttu-id="05b29-124">-S</span><span class="sxs-lookup"><span data-stu-id="05b29-124">-s</span></span>     | <span data-ttu-id="05b29-125">*Altsource*</span><span class="sxs-lookup"><span data-stu-id="05b29-125">*ALTSOURCE*</span></span> | <span data-ttu-id="05b29-126">Altsource spécifie un autre répertoire pour rechercher les fichiers.</span><span class="sxs-lookup"><span data-stu-id="05b29-126">ALTSOURCE specifies an alternative directory to find the files.</span></span>                                                                                                              |



 

<span data-ttu-id="05b29-127">Cet outil est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="05b29-127">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="05b29-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="05b29-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05b29-129">Outils de développement Windows Installer</span><span class="sxs-lookup"><span data-stu-id="05b29-129">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="05b29-130">Utilisation de la table Directory</span><span class="sxs-lookup"><span data-stu-id="05b29-130">Using the Directory Table</span></span>](using-the-directory-table.md)
</dt> <dt>

[<span data-ttu-id="05b29-131">Versions, outils et redistribuables publiés</span><span class="sxs-lookup"><span data-stu-id="05b29-131">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



