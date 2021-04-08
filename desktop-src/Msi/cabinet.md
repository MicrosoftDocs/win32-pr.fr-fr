---
description: Le type de données Cabinet doit être utilisé dans la colonne Cabinet de la table Media.
ms.assetid: 149c74ea-4342-45dd-8da4-4dfa7f4317a0
title: CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814473ef4d21d5445b5b5319278a5e25a7f5540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864422"
---
# <a name="cabinet"></a><span data-ttu-id="31599-103">CAB</span><span class="sxs-lookup"><span data-stu-id="31599-103">Cabinet</span></span>

<span data-ttu-id="31599-104">Le type de données Cabinet doit être utilisé dans la colonne Cabinet de la [table Media](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="31599-104">The Cabinet data type must be used in the Cabinet column of the [Media table](media-table.md).</span></span>

<span data-ttu-id="31599-105">Si le nom du fichier cab est précédé du signe dièse, le fichier cab est stocké en tant que flux de données à l’intérieur du package.</span><span class="sxs-lookup"><span data-stu-id="31599-105">If the cabinet name is preceded by the number sign, the cabinet is stored as a data stream inside the package.</span></span> <span data-ttu-id="31599-106">La chaîne de caractères qui suit \# est un [identificateur](identifier.md) pour ce flux de données.</span><span class="sxs-lookup"><span data-stu-id="31599-106">The character string which follows the \# is an [Identifier](identifier.md) for this data stream.</span></span> <span data-ttu-id="31599-107">Notez que si le fichier cab est stocké en tant que flux de données, le nom d’un fichier cab est sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="31599-107">Note that if the cabinet is stored as a data stream, the name of a cabinet is case-sensitive.</span></span>

<span data-ttu-id="31599-108">Si le nom du fichier CAB n’est pas précédé du signe dièse \# , le fichier cab est stocké dans un fichier séparé situé à la racine de l’arborescence source spécifiée par la [table Directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="31599-108">If the cabinet name is not preceded by the number sign \#, the cabinet is stored in a separate file located at the root of the source tree specified by the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="31599-109">Le fichier cab doit utiliser la syntaxe de nom de fichier abrégé composée d’un nom de huit caractères, d’un point et d’une extension de trois caractères.</span><span class="sxs-lookup"><span data-stu-id="31599-109">The cabinet file must use the short file name syntax consisting of an eight character name, a period, and a three character extension.</span></span> <span data-ttu-id="31599-110">Le type de données cabinet ne peut pas utiliser la \| syntaxe de Short longname pour les noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="31599-110">The Cabinet data type cannot use the short\|longname syntax for file names.</span></span> <span data-ttu-id="31599-111">Si le fichier cab est stocké sous la forme d’un fichier distinct, le nom du fichier CAB ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="31599-111">If the cabinet file is stored as a separate file, the name of the cabinet file is not case-sensitive.</span></span>

<span data-ttu-id="31599-112">Pour économiser de l’espace disque, le programme d’installation supprime toutes les armoires incorporées dans le fichier. msi avant la mise en cache du package d’installation sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="31599-112">To conserve disk space, the installer removes any cabinets embedded in the .msi file before caching the installation package on the user's computer.</span></span>

<span data-ttu-id="31599-113">Voir [inclusion d’un fichier cab dans une installation](including-a-cabinet-file-in-an-installation.md).</span><span class="sxs-lookup"><span data-stu-id="31599-113">See [Including a Cabinet File in an Installation](including-a-cabinet-file-in-an-installation.md).</span></span>

 

 



