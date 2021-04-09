---
description: La méthode Connect de l’objet Merge peut être utilisée pour connecter un module à une fonctionnalité supplémentaire qui a été fusionnée dans la base de données ou qui sera fusionnée dans la base de données. La fonctionnalité doit exister avant d’appeler cette méthode.
ms.assetid: 8b59de42-bc3f-468b-a410-8f935ff73345
title: Connexion d’un module de fusion à plusieurs fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57b49f1ee27b4c8d3aa5d0b3ac1b0d7b8b8e11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867045"
---
# <a name="connecting-a-merge-module-to-multiple-features"></a><span data-ttu-id="977e2-104">Connexion d’un module de fusion à plusieurs fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="977e2-104">Connecting a Merge Module to Multiple Features</span></span>

<span data-ttu-id="977e2-105">La méthode [**Connect**](merge-connect.md) de l' [objet Merge](merge-object.md) peut être utilisée pour connecter un module à une fonctionnalité supplémentaire qui a été fusionnée dans la base de données ou qui sera fusionnée dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="977e2-105">The [**Connect**](merge-connect.md) method of the [Merge Object](merge-object.md) can be used to connect a module to an additional feature that has been merged into the database or that will be merged into the database.</span></span> <span data-ttu-id="977e2-106">La fonctionnalité doit exister avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="977e2-106">The feature must exist before calling this method.</span></span>

<span data-ttu-id="977e2-107">Un module de fusion ne doit jamais remettre un composant contenant des fichiers système à la fonctionnalité principale d’une application, car cela peut entraîner la validation et la réparation de l’application par le programme d’installation chaque fois que le fichier système est utilisé.</span><span class="sxs-lookup"><span data-stu-id="977e2-107">A merge module should never deliver a component containing system files to the main feature of an application, because this may cause the Installer to validate and repair the application each time the system file is used.</span></span> <span data-ttu-id="977e2-108">Un fichier. msi destiné à accepter des composants d’un module de fusion doit être créé afin que tous les composants qui contiennent des fichiers système appartiennent uniquement à des fonctionnalités qui sont séparées de la fonctionnalité principale de l’application.</span><span class="sxs-lookup"><span data-stu-id="977e2-108">A .msi file that is intended to accept components from a merge module should be authored so that any components that contain system files only belong to features that are separate from the main feature of the application.</span></span>

<span data-ttu-id="977e2-109">Si votre package utilise un module de fusion contenant des fichiers système qui lient tous les composants du module de fusion à la fonctionnalité principale de l’application, une tentative d’utilisation du fichier système peut déclencher le programme d’installation pour essayer de réparer la fonctionnalité principale de l’application.</span><span class="sxs-lookup"><span data-stu-id="977e2-109">If your package uses a merge module containing system files that link all the components from the merge module to the main feature of the application, an attempt to use the system file may trigger the Installer to try and repair the main feature of the application.</span></span> <span data-ttu-id="977e2-110">Si la fonctionnalité principale ne peut pas être réparée, l’installation peut échouer.</span><span class="sxs-lookup"><span data-stu-id="977e2-110">If the main feature cannot be repaired, the installation may fail.</span></span>

 

 



