---
description: Le type de données AnyPath est une chaîne de texte contenant un chemin d’accès complet ou un chemin d’accès relatif.
ms.assetid: fe8a4d2a-1960-40af-a0e4-4d65accdd388
title: AnyPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ab6265874616bb0bb1a2f61098cdbabfa8ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527634"
---
# <a name="anypath"></a><span data-ttu-id="b9d79-103">AnyPath</span><span class="sxs-lookup"><span data-stu-id="b9d79-103">AnyPath</span></span>

<span data-ttu-id="b9d79-104">Le type de données AnyPath est une chaîne de texte contenant un chemin d’accès complet ou un chemin d’accès relatif.</span><span class="sxs-lookup"><span data-stu-id="b9d79-104">The AnyPath data type is a text string containing either a full path or a relative path.</span></span> <span data-ttu-id="b9d79-105">Lorsque vous spécifiez un chemin d’accès relatif, vous pouvez inclure un nom de fichier long avec le nom de fichier Short en séparant les noms courts et longs par une barre verticale ( \| ).</span><span class="sxs-lookup"><span data-stu-id="b9d79-105">When specifying a relative path, you can include a long file name with the short file name by separating the short and long names with a vertical bar (\|).</span></span> <span data-ttu-id="b9d79-106">Notez que vous ne pouvez pas spécifier plusieurs niveaux d’un répertoire ou des chemins d’accès complets de cette façon.</span><span class="sxs-lookup"><span data-stu-id="b9d79-106">Note that you cannot specify multiple levels of a directory or fully qualified paths in this way.</span></span> <span data-ttu-id="b9d79-107">Le chemin d’accès peut contenir des propriétés placées entre crochets ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="b9d79-107">The path may contain properties enclosed within square brackets (\[ \]).</span></span>

<span data-ttu-id="b9d79-108">Exemples de données AnyPath valides :</span><span class="sxs-lookup"><span data-stu-id="b9d79-108">Examples of valid AnyPath data:</span></span>

-   <span data-ttu-id="b9d79-109">\\\\fichier \\ temporaire de partage de serveur \\</span><span class="sxs-lookup"><span data-stu-id="b9d79-109">\\\\server\\share\\temp</span></span>
-   <span data-ttu-id="b9d79-110">c : \\ temp</span><span class="sxs-lookup"><span data-stu-id="b9d79-110">c:\\temp</span></span>
-   <span data-ttu-id="b9d79-111">\\modèle</span><span class="sxs-lookup"><span data-stu-id="b9d79-111">\\temp</span></span>
-   <span data-ttu-id="b9d79-112">Project ~ 1 \| État du projet</span><span class="sxs-lookup"><span data-stu-id="b9d79-112">projec~1\|Project Status</span></span>

<span data-ttu-id="b9d79-113">Exemples de données AnyPath non valides :</span><span class="sxs-lookup"><span data-stu-id="b9d79-113">Examples of invalid AnyPath data:</span></span>

-   <span data-ttu-id="b9d79-114">c : \\ temp \\ Project ~ 1 \| c : \\ État du \\ projet Temp One</span><span class="sxs-lookup"><span data-stu-id="b9d79-114">c:\\temp\\projec~1\|c:\\temp one\\Project Status</span></span>
-   <span data-ttu-id="b9d79-115">\\\\État du projet Temp Project ~ 1 \| \\ temp \\</span><span class="sxs-lookup"><span data-stu-id="b9d79-115">\\temp\\projec~1\|\\temp one\\Project Status</span></span>

 

 



