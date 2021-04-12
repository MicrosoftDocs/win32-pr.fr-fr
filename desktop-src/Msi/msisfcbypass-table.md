---
description: La table MsiSFCBypass contient une liste de fichiers qui doivent contourner la protection des fichiers Windows lorsque les fichiers sont installés sur Microsoft Windows Me.
ms.assetid: 86de0dc1-ed8f-410c-a411-6c44c8e5c9fd
title: Table MsiSFCBypass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707294e9461aaf321add8a3959682a0db555cc2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319910"
---
# <a name="msisfcbypass-table"></a><span data-ttu-id="b5ed2-103">Table MsiSFCBypass</span><span class="sxs-lookup"><span data-stu-id="b5ed2-103">MsiSFCBypass Table</span></span>

<span data-ttu-id="b5ed2-104">La table MsiSFCBypass contient une liste de fichiers qui doivent contourner la protection des fichiers Windows lorsque les fichiers sont installés sur Microsoft Windows Me.</span><span class="sxs-lookup"><span data-stu-id="b5ed2-104">The MsiSFCBypass Table contains a list of files that should bypass Windows File Protection when the files are installed on Microsoft Windows Me.</span></span>

<span data-ttu-id="b5ed2-105">La table MsiSFCBypass contient la colonne suivante.</span><span class="sxs-lookup"><span data-stu-id="b5ed2-105">The MsiSFCBypass Table has the following column.</span></span>



| <span data-ttu-id="b5ed2-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="b5ed2-106">Column</span></span> | <span data-ttu-id="b5ed2-107">Type</span><span class="sxs-lookup"><span data-stu-id="b5ed2-107">Type</span></span>                         | <span data-ttu-id="b5ed2-108">Clé</span><span class="sxs-lookup"><span data-stu-id="b5ed2-108">Key</span></span> | <span data-ttu-id="b5ed2-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="b5ed2-109">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="b5ed2-110">fichier\_</span><span class="sxs-lookup"><span data-stu-id="b5ed2-110">File\_</span></span> | [<span data-ttu-id="b5ed2-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="b5ed2-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="b5ed2-112">O</span><span class="sxs-lookup"><span data-stu-id="b5ed2-112">Y</span></span>   | <span data-ttu-id="b5ed2-113">N</span><span class="sxs-lookup"><span data-stu-id="b5ed2-113">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b5ed2-114">Colonnes</span><span class="sxs-lookup"><span data-stu-id="b5ed2-114">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b5ed2-115"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_</span><span class="sxs-lookup"><span data-stu-id="b5ed2-115"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="b5ed2-116">Clé étrangère de la [table de fichiers](file-table.md) qui spécifie le fichier qui doit contourner la protection des fichiers Windows lorsque le fichier est installé sur Windows Me.</span><span class="sxs-lookup"><span data-stu-id="b5ed2-116">The foreign key to the [File Table](file-table.md) that specifies the file that should bypass Windows File Protection when the file is installed on Windows Me.</span></span>

</dd> </dl>

 

 



