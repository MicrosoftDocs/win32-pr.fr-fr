---
description: L’interface utilisateur de Windows permet aux utilisateurs d’accéder à un large éventail d’objets nécessaires pour exécuter des applications et gérer le système d’exploitation.
title: Shell Windows
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1d0d4ed7-9b85-4d70-bf1f-82567a1687fb
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 448e1d5265ec34ce1889ca36f234622e2b082553
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973323"
---
# <a name="windows-shell"></a><span data-ttu-id="cba5a-103">Shell Windows</span><span class="sxs-lookup"><span data-stu-id="cba5a-103">Windows Shell</span></span>

<span data-ttu-id="cba5a-104">L’interface utilisateur de Windows permet aux utilisateurs d’accéder à un large éventail d’objets nécessaires pour exécuter des applications et gérer le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="cba5a-104">The Windows UI provides users with access to a wide variety of objects necessary for running applications and managing the operating system.</span></span> <span data-ttu-id="cba5a-105">Les plus nombreux et les plus familiers de ces objets sont les dossiers et les fichiers qui résident sur les lecteurs de disque de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="cba5a-105">The most numerous and familiar of these objects are the folders and files that reside on computer disk drives.</span></span> <span data-ttu-id="cba5a-106">Il existe également un certain nombre d’objets virtuels qui permettent à l’utilisateur d’effectuer des tâches telles que l’envoi de fichiers à des imprimantes distantes ou l’accès à la corbeille.</span><span class="sxs-lookup"><span data-stu-id="cba5a-106">There are also a number of virtual objects that allow the user to perform tasks such as sending files to remote printers or accessing the Recycle Bin.</span></span> <span data-ttu-id="cba5a-107">L’interpréteur de commandes organise ces objets dans un espace de noms hiérarchique et fournit aux utilisateurs et aux applications un moyen cohérent et efficace d’accéder aux objets et de les gérer.</span><span class="sxs-lookup"><span data-stu-id="cba5a-107">The Shell organizes these objects into a hierarchical namespace and provides users and applications with a consistent and efficient way to access and manage objects.</span></span>

## <a name="shell-development-scenarios"></a><span data-ttu-id="cba5a-108">Scénarios de développement de Shell</span><span class="sxs-lookup"><span data-stu-id="cba5a-108">Shell Development Scenarios</span></span>

<span data-ttu-id="cba5a-109">Les scénarios de développement suivants sont liés au développement d’applications :</span><span class="sxs-lookup"><span data-stu-id="cba5a-109">The following development scenarios relate to application development:</span></span>

-   <span data-ttu-id="cba5a-110">Extension de l’interpréteur de commandes, qui consiste à créer une source de données (plutôt que de consommer le modèle de données Shell)</span><span class="sxs-lookup"><span data-stu-id="cba5a-110">Extending the Shell, which consists of creating a data source (versus consuming the Shell data model)</span></span>
-   <span data-ttu-id="cba5a-111">Implémentation d’un sous-ensemble des tâches de la source de données Shell</span><span class="sxs-lookup"><span data-stu-id="cba5a-111">Implementing a subset of the Shell data source tasks</span></span>
-   <span data-ttu-id="cba5a-112">Prise en charge des bibliothèques et des affichages d’éléments dans l’Explorateur Windows</span><span class="sxs-lookup"><span data-stu-id="cba5a-112">Supporting libraries and item views in Windows Explorer</span></span>
-   <span data-ttu-id="cba5a-113">Utilisation de la boîte de dialogue fichier commun</span><span class="sxs-lookup"><span data-stu-id="cba5a-113">Using the common file dialog</span></span>
-   <span data-ttu-id="cba5a-114">Implémentation des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="cba5a-114">Implementing Control Panel items</span></span>
-   <span data-ttu-id="cba5a-115">Gestion des notifications</span><span class="sxs-lookup"><span data-stu-id="cba5a-115">Managing notifications</span></span>

<span data-ttu-id="cba5a-116">Les scénarios de développement suivants sont liés à la propriété de format de fichier :</span><span class="sxs-lookup"><span data-stu-id="cba5a-116">The following development scenarios relate to file format ownership:</span></span>

-   <span data-ttu-id="cba5a-117">Implémentation d’un sous-ensemble des tâches de la source de données Shell</span><span class="sxs-lookup"><span data-stu-id="cba5a-117">Implementing a subset of the Shell data source tasks</span></span>
-   <span data-ttu-id="cba5a-118">Implémentation d’un gestionnaire</span><span class="sxs-lookup"><span data-stu-id="cba5a-118">Implementing any handler</span></span>
-   <span data-ttu-id="cba5a-119">Prise en charge de Desktop Search</span><span class="sxs-lookup"><span data-stu-id="cba5a-119">Supporting desktop search</span></span>

<span data-ttu-id="cba5a-120">Les scénarios de développement suivants sont liés à la propriété du stockage des données :</span><span class="sxs-lookup"><span data-stu-id="cba5a-120">The following development scenarios relate to data storage ownership:</span></span>

-   <span data-ttu-id="cba5a-121">Prise en charge de Desktop Search et OpenSearch</span><span class="sxs-lookup"><span data-stu-id="cba5a-121">Supporting desktop search and OpenSearch</span></span>
-   <span data-ttu-id="cba5a-122">Implémentation d’un sous-ensemble des tâches de la source de données Shell (dossiers virtuels)</span><span class="sxs-lookup"><span data-stu-id="cba5a-122">Implementing a subset of the Shell data source tasks (virtual folders)</span></span>
-   <span data-ttu-id="cba5a-123">Bibliothèques de prise en charge dans l’Explorateur Windows</span><span class="sxs-lookup"><span data-stu-id="cba5a-123">Supporting libraries in Windows Explorer</span></span>

<span data-ttu-id="cba5a-124">Le scénario de développement suivant est associé à la prise en charge des appareils :</span><span class="sxs-lookup"><span data-stu-id="cba5a-124">The following development scenario relates to device support:</span></span>

-   <span data-ttu-id="cba5a-125">Exécution automatique et lecture automatique</span><span class="sxs-lookup"><span data-stu-id="cba5a-125">Auto run and auto play</span></span>

## <a name="windows-shell-sdk-documentation"></a><span data-ttu-id="cba5a-126">Documentation du kit de développement logiciel (SDK) Windows Shell</span><span class="sxs-lookup"><span data-stu-id="cba5a-126">Windows Shell SDK Documentation</span></span>

<span data-ttu-id="cba5a-127">Cette documentation est divisée en trois sections principales :</span><span class="sxs-lookup"><span data-stu-id="cba5a-127">This documentation is broken into three major sections:</span></span>

-   <span data-ttu-id="cba5a-128">Le [Guide du développeur de l’interpréteur](intro.md) de commandes fournit des informations conceptuelles sur le fonctionnement de l’interpréteur de commandes et sur l’utilisation de l’API de l’interpréteur de commandes dans votre application.</span><span class="sxs-lookup"><span data-stu-id="cba5a-128">The [Shell Developer's Guide](intro.md) provides conceptual material about how the Shell works and how to use the Shell's API in your application.</span></span>
-   <span data-ttu-id="cba5a-129">La section informations de référence sur le [Shell](shell-reference-bumper.md) documente les éléments de programmation qui composent les différentes API de Shell.</span><span class="sxs-lookup"><span data-stu-id="cba5a-129">The [Shell Reference](shell-reference-bumper.md) section documents programming elements that make up the various Shell APIs.</span></span>
-   <span data-ttu-id="cba5a-130">Les [exemples de Shell](samples-entry.md) fournissent des liens vers des exemples de code connexes.</span><span class="sxs-lookup"><span data-stu-id="cba5a-130">[Shell Samples](samples-entry.md) provides links to related code samples.</span></span>

<span data-ttu-id="cba5a-131">Le tableau suivant présente la section Référence de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="cba5a-131">The following table provides an outline of the Shell Reference section.</span></span> <span data-ttu-id="cba5a-132">Sauf indication contraire, tous les éléments de programmation sont documentés dans le C++ non managé.</span><span class="sxs-lookup"><span data-stu-id="cba5a-132">Unless otherwise noted, all programming elements are documented in unmanaged C++.</span></span>



| <span data-ttu-id="cba5a-133">Section</span><span class="sxs-lookup"><span data-stu-id="cba5a-133">Section</span></span>                                                               | <span data-ttu-id="cba5a-134">Description</span><span class="sxs-lookup"><span data-stu-id="cba5a-134">Description</span></span>                                                                                                          |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cba5a-135">Classes de Shell</span><span class="sxs-lookup"><span data-stu-id="cba5a-135">Shell Classes</span></span>](classes.md)                                          | <span data-ttu-id="cba5a-136">Cette section décrit la sélection des classes de shell Windows.</span><span class="sxs-lookup"><span data-stu-id="cba5a-136">This section describes select Windows Shell classes.</span></span>                                                                 |
| [<span data-ttu-id="cba5a-137">Interfaces Shell</span><span class="sxs-lookup"><span data-stu-id="cba5a-137">Shell Interfaces</span></span>](interfaces.md)                                    | <span data-ttu-id="cba5a-138">Cette section décrit les interfaces COM (Component Object Model) du shell Windows.</span><span class="sxs-lookup"><span data-stu-id="cba5a-138">This section describes the Windows Shell Component Object Model (COM) interfaces.</span></span>                                    |
| [<span data-ttu-id="cba5a-139">Fonctions Shell</span><span class="sxs-lookup"><span data-stu-id="cba5a-139">Shell Functions</span></span>](functions.md)                                      | <span data-ttu-id="cba5a-140">Cette section décrit les fonctions de l’interpréteur de commandes Windows.</span><span class="sxs-lookup"><span data-stu-id="cba5a-140">This section describes the Windows Shell functions.</span></span>                                                                  |
| [<span data-ttu-id="cba5a-141">Fonctions de rappel de l’interpréteur de commandes</span><span class="sxs-lookup"><span data-stu-id="cba5a-141">Shell Callback Functions</span></span>](callbacks.md)                             | <span data-ttu-id="cba5a-142">Cette section décrit les modèles des fonctions de rappel de l’interpréteur de commandes Windows.</span><span class="sxs-lookup"><span data-stu-id="cba5a-142">This section describes the Windows Shell callback functions templates.</span></span>                                               |
| [<span data-ttu-id="cba5a-143">Constantes, énumérations et indicateurs de Shell</span><span class="sxs-lookup"><span data-stu-id="cba5a-143">Shell Constants, Enumerations, and Flags</span></span>](consts-enums-flags.md)    | <span data-ttu-id="cba5a-144">Cette section décrit les constantes, énumérations et indicateurs de l’interpréteur de commandes Windows utilisés dans les API de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="cba5a-144">This section describes the Windows Shell constants, enumerations, and flags used in the Shell APIs.</span></span>                  |
| [<span data-ttu-id="cba5a-145">Fonctions utilitaires légères de l’interpréteur de commandes</span><span class="sxs-lookup"><span data-stu-id="cba5a-145">Shell Lightweight Utility Functions</span></span>](shlwapi.md)                    | <span data-ttu-id="cba5a-146">Cette section décrit les fonctions de l’utilitaire léger Windows Shell fournies dans Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="cba5a-146">This section describes the Windows Shell lightweight utility functions provided in Shlwapi.dll.</span></span>                      |
| [<span data-ttu-id="cba5a-147">Macros de Shell</span><span class="sxs-lookup"><span data-stu-id="cba5a-147">Shell Macros</span></span>](macros.md)                                            | <span data-ttu-id="cba5a-148">Cette section décrit les macros de l’utilitaire Windows Shell.</span><span class="sxs-lookup"><span data-stu-id="cba5a-148">This section describes the Windows Shell utility macros.</span></span>                                                             |
| [<span data-ttu-id="cba5a-149">Messages et notifications de l’interpréteur de commandes</span><span class="sxs-lookup"><span data-stu-id="cba5a-149">Shell Messages and Notifications</span></span>](messages.md)                      | <span data-ttu-id="cba5a-150">Cette section décrit les messages et les notifications envoyés par les éléments de l’interpréteur de commandes Windows.</span><span class="sxs-lookup"><span data-stu-id="cba5a-150">This section describes the messages and notifications sent by elements of the Windows Shell.</span></span>                         |
| [<span data-ttu-id="cba5a-151">Objets Shell pour l’écriture de scripts et Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="cba5a-151">Shell Objects for Scripting and Microsoft Visual Basic</span></span>](objects.md) | <span data-ttu-id="cba5a-152">Cette section décrit les objets Windows implémentés par le Shell pour une utilisation dans les scripts et les Visual Basic Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cba5a-152">This section describes the Windows objects implemented by the Shell for use in scripting and Microsoft Visual Basic.</span></span> |
| [<span data-ttu-id="cba5a-153">Objets Shell pour C++</span><span class="sxs-lookup"><span data-stu-id="cba5a-153">Shell Objects for C++</span></span>](objects-cpp.md)                              | <span data-ttu-id="cba5a-154">Cette section décrit les objets Windows C++ implémentés par l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="cba5a-154">This section describes the C++ Windows objects implemented by the Shell.</span></span>                                             |
| [<span data-ttu-id="cba5a-155">Schémas de Shell</span><span class="sxs-lookup"><span data-stu-id="cba5a-155">Shell Schemas</span></span>](schemas.md)                                          | <span data-ttu-id="cba5a-156">Cette section décrit les schémas de manifeste de bibliothèque, de propriété et de transfert utilisés par le shell Windows.</span><span class="sxs-lookup"><span data-stu-id="cba5a-156">This section describes library, property, and transfer manifest schemas used by the Windows Shell.</span></span>                   |
| [<span data-ttu-id="cba5a-157">Structures de Shell</span><span class="sxs-lookup"><span data-stu-id="cba5a-157">Shell Structures</span></span>](structures.md)                                    | <span data-ttu-id="cba5a-158">Cette section décrit les structures de shell Windows utilisées dans les API de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="cba5a-158">This section describes the Windows Shell structures used in the Shell APIs.</span></span>                                          |



 

 

 



