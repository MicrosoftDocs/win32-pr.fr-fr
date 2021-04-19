---
description: Une application peut rechercher dans le répertoire actif tous les noms de fichiers qui correspondent à un modèle donné à l’aide des fonctions FindFirstFile, FindFirstFileEx, FindNextFile et FindClose.
ms.assetid: 7edd6c6e-7e8a-415c-866b-2283e5596a62
title: Recherche d’un ou plusieurs fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c5825b418221b1af429c6c0a731446d627701c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517314"
---
# <a name="searching-for-one-or-more-files"></a><span data-ttu-id="fc6b1-103">Recherche d’un ou plusieurs fichiers</span><span class="sxs-lookup"><span data-stu-id="fc6b1-103">Searching for One or More Files</span></span>

<span data-ttu-id="fc6b1-104">Une application peut rechercher dans le répertoire actif tous les noms de fichiers qui correspondent à un modèle donné à l’aide des fonctions [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)et [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .</span><span class="sxs-lookup"><span data-stu-id="fc6b1-104">An application can search the current directory for all file names that match a given pattern by using the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea), and [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) functions.</span></span> <span data-ttu-id="fc6b1-105">Le modèle doit être un nom de fichier valide et peut inclure des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="fc6b1-105">The pattern must be a valid file name and can include wildcard characters.</span></span>

<span data-ttu-id="fc6b1-106">Les fonctions [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) et [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) créent des handles que **FindFirstFileEx** utilise pour rechercher d’autres fichiers avec le même modèle.</span><span class="sxs-lookup"><span data-stu-id="fc6b1-106">The [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) functions create handles that **FindFirstFileEx** uses to search for other files with the same pattern.</span></span> <span data-ttu-id="fc6b1-107">Toutes les fonctions retournent des informations sur le fichier qui a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="fc6b1-107">All functions return information about the file that was found.</span></span> <span data-ttu-id="fc6b1-108">Ces informations incluent le nom, la taille, les attributs et l’heure du fichier.</span><span class="sxs-lookup"><span data-stu-id="fc6b1-108">This information includes the file name, size, attributes, and time.</span></span>

<span data-ttu-id="fc6b1-109">La fonction [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) permet également à une application de rechercher des fichiers en fonction de critères de recherche supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="fc6b1-109">The [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) function also allows an application to search for files based on additional search criteria.</span></span> <span data-ttu-id="fc6b1-110">La fonction peut limiter les recherches à des noms de périphériques ou de répertoires.</span><span class="sxs-lookup"><span data-stu-id="fc6b1-110">The function can limit searches to device names or directory names.</span></span>

<span data-ttu-id="fc6b1-111">La fonction [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) détruit les handles créés par [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) et [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa).</span><span class="sxs-lookup"><span data-stu-id="fc6b1-111">The [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) function destroys handles created by [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa).</span></span>

<span data-ttu-id="fc6b1-112">Une application peut rechercher un seul fichier sur un chemin d’accès spécifique à l’aide de la fonction [**SearchPath**](/windows/win32/api/processenv/nf-processenv-searchpatha) .</span><span class="sxs-lookup"><span data-stu-id="fc6b1-112">An application can search for a single file on a specific path by using the [**SearchPath**](/windows/win32/api/processenv/nf-processenv-searchpatha) function.</span></span>

 

 
