---
title: Recherche de fichiers
description: Par défaut, RC recherche d’abord les fichiers d’en-tête et les fichiers de ressources (tels que les fichiers icône et curseur) dans le répertoire actif, puis dans les répertoires spécifiés par la variable d’environnement INCLUDe.
ms.assetid: 6c8c905d-b0f6-4665-9a93-62617ff30137
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078a04a4cf2f3461d03c7026e0f1d73d8fd38665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511843"
---
# <a name="searching-for-files"></a><span data-ttu-id="cb000-103">Recherche de fichiers</span><span class="sxs-lookup"><span data-stu-id="cb000-103">Searching for Files</span></span>

<span data-ttu-id="cb000-104">Par défaut, RC recherche d’abord les fichiers d’en-tête et les fichiers de ressources (tels que les fichiers icône et curseur) dans le répertoire actif, puis dans les répertoires spécifiés par la variable d’environnement INCLUDe.</span><span class="sxs-lookup"><span data-stu-id="cb000-104">By default, RC searches for header files and resource files (such as icon and cursor files) first in the current directory and then in the directories specified by the INCLUDE environment variable.</span></span> <span data-ttu-id="cb000-105">(La variable d’environnement PATH n’a aucun effet sur les recherches de répertoires RC.)</span><span class="sxs-lookup"><span data-stu-id="cb000-105">(The PATH environment variable has no effect on which directories RC searches.)</span></span>

## <a name="adding-a-directory-to-search"></a><span data-ttu-id="cb000-106">Ajout d’un répertoire dans lequel effectuer la recherche</span><span class="sxs-lookup"><span data-stu-id="cb000-106">Adding a Directory to Search</span></span>

<span data-ttu-id="cb000-107">Vous pouvez utiliser l’option **/i** pour ajouter un répertoire à la liste des recherches de répertoires RC.</span><span class="sxs-lookup"><span data-stu-id="cb000-107">You can use the **/i** option to add a directory to the list of directories RC searches.</span></span> <span data-ttu-id="cb000-108">Le compilateur recherche ensuite dans les répertoires dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="cb000-108">The compiler then searches the directories in the following order:</span></span>

1.  <span data-ttu-id="cb000-109">Répertoire actif</span><span class="sxs-lookup"><span data-stu-id="cb000-109">The current directory</span></span>
2.  <span data-ttu-id="cb000-110">Le ou les répertoires que vous spécifiez à l’aide de l’option **/i** , dans l’ordre dans lequel ils apparaissent sur la ligne de commande RC</span><span class="sxs-lookup"><span data-stu-id="cb000-110">The directory or directories you specify by using the **/i** option, in the order in which they appear on the RC command line</span></span>
3.  <span data-ttu-id="cb000-111">Liste des répertoires spécifiés par la variable d’environnement INCLUDe, dans l’ordre dans lequel la variable les répertorie, sauf si vous spécifiez l’option **/x**</span><span class="sxs-lookup"><span data-stu-id="cb000-111">The list of directories specified by the INCLUDE environment variable, in the order in which the variable lists them, unless you specify the **/x** option</span></span>

<span data-ttu-id="cb000-112">L’exemple suivant compile le fichier de définition de ressource MyApp. RC :</span><span class="sxs-lookup"><span data-stu-id="cb000-112">The following example compiles the resource-definition file MyApp.rc:</span></span>

<span data-ttu-id="cb000-113">**RC/i c : \\ source \\ Stuff/i d : \\ ressources MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="cb000-113">**rc /i c:\\source\\stuff /i d:\\resources myapp.rc**</span></span>

<span data-ttu-id="cb000-114">Lors de la compilation du script MyApp. RC, RC recherche d’abord les fichiers d’en-tête et les fichiers de ressources dans le répertoire actif, puis dans C : \\ source \\ Stuff et D : Resources \\ , puis dans les répertoires spécifiés par la variable d’environnement include.</span><span class="sxs-lookup"><span data-stu-id="cb000-114">When compiling the script MyApp.rc, RC searches for header files and resource files first in the current directory, then in C:\\Source\\Stuff and D:\\Resources, and then in the directories specified by the INCLUDE environment variable.</span></span>

## <a name="ignoring-the-include-environment-variable"></a><span data-ttu-id="cb000-115">La variable d’environnement INCLUDe est ignorée</span><span class="sxs-lookup"><span data-stu-id="cb000-115">Ignoring the INCLUDE Environment Variable</span></span>

<span data-ttu-id="cb000-116">Vous pouvez empêcher RC d’utiliser la variable d’environnement INCLUDe lors de la détermination des répertoires dans lesquels effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="cb000-116">You can prevent RC from using the INCLUDE environment variable when determining the directories to search.</span></span> <span data-ttu-id="cb000-117">Pour ce faire, utilisez l’option **/x** .</span><span class="sxs-lookup"><span data-stu-id="cb000-117">To do so, use the **/x** option.</span></span> <span data-ttu-id="cb000-118">Le compilateur recherche ensuite des fichiers uniquement dans le répertoire actif et dans les répertoires que vous spécifiez à l’aide de l’option **/i** .</span><span class="sxs-lookup"><span data-stu-id="cb000-118">The compiler then searches for files only in the current directory and in any directories you specify by using the **/i** option.</span></span>

<span data-ttu-id="cb000-119">La commande suivante compile le fichier de script MyApp. RC :</span><span class="sxs-lookup"><span data-stu-id="cb000-119">The following command compiles the script file MyApp.rc:</span></span>

<span data-ttu-id="cb000-120">**RC/x/i c : \\ source source \\ MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="cb000-120">**rc /x /i c:\\source\\stuff myapp.rc**</span></span>

<span data-ttu-id="cb000-121">Lors de la compilation du script MyApp. RC, RC recherche d’abord les fichiers d’en-tête et les fichiers de ressources dans le répertoire actif, puis dans C : \\ source \\ .</span><span class="sxs-lookup"><span data-stu-id="cb000-121">When compiling the script MyApp.rc, RC searches for header files and resource files first in the current directory and then in C:\\Source\\Stuff.</span></span> <span data-ttu-id="cb000-122">Elle ne recherche pas dans les répertoires spécifiés par la variable d’environnement INCLUDe.</span><span class="sxs-lookup"><span data-stu-id="cb000-122">It does not search the directories specified by the INCLUDE environment variable.</span></span>

 

 




