---
description: Création du fichier de ressources de la langue de base
ms.assetid: 770e1f4b-5258-4b6b-afa4-5c19743daaaa
title: Création du fichier de ressources de la langue de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96d566625025c105e123e0e2edf9f4f20721274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035126"
---
# <a name="creating-the-base-language-resource-file"></a><span data-ttu-id="b6933-103">Création du fichier de ressources de la langue de base</span><span class="sxs-lookup"><span data-stu-id="b6933-103">Creating the Base Language Resource File</span></span>

<span data-ttu-id="b6933-104">Les ressources pour les éléments d’interface utilisateur sont définies pour le langage de base pris en charge par l’application, par exemple l’anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="b6933-104">Resources for user interface elements are defined for the basic language that the application supports, for example, English (United States).</span></span> <span data-ttu-id="b6933-105">Un fichier de ressources Win32 PE est un exemple de fichier. RC créé à l’aide du compilateur RC.</span><span class="sxs-lookup"><span data-stu-id="b6933-105">An example of a Win32 PE resource file is an .rc file, created using RC Compiler.</span></span> <span data-ttu-id="b6933-106">Pour plus d’informations sur la création de fichiers. RC, consultez [à propos des fichiers de ressources](../menurc/about-resource-files.md).</span><span class="sxs-lookup"><span data-stu-id="b6933-106">For details of .rc file creation, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

<span data-ttu-id="b6933-107">Si vous utilisez un fichier. RC pour les ressources linguistiques de base, vous avez la possibilité d’utiliser un fichier de configuration de ressources pour une représentation XML des données de configuration de ressource.</span><span class="sxs-lookup"><span data-stu-id="b6933-107">If using an .rc file for the base language resources, you have the option of using a resource configuration file for an XML representation of resource configuration data.</span></span> <span data-ttu-id="b6933-108">Pour créer ce fichier, consultez [préparation d’un fichier de configuration de ressource](preparing-a-resource-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="b6933-108">To create this file, see [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>

<span data-ttu-id="b6933-109">Vous pouvez également utiliser un fichier PE non Win32 pour définir les ressources linguistiques de base.</span><span class="sxs-lookup"><span data-stu-id="b6933-109">You can also use a non-Win32 PE file to define base language resources.</span></span> <span data-ttu-id="b6933-110">Par exemple, vous pouvez utiliser un fichier. XML ou. txt à cet effet.</span><span class="sxs-lookup"><span data-stu-id="b6933-110">For example, you might use an .xml file or .txt file for this purpose.</span></span>

> [!Note]  
> <span data-ttu-id="b6933-111">Quand vous définissez des ressources de langue de base à l’aide d’un fichier PE non Win32, vous ne pouvez pas utiliser le compilateur RC pour la définition de ressource.</span><span class="sxs-lookup"><span data-stu-id="b6933-111">When you define base language resources using a non-Win32 PE file, you cannot use RC Compiler for resource definition.</span></span> <span data-ttu-id="b6933-112">Au lieu de cela, vous définissez votre propre format de ressource, et votre application doit fournir ses propres fonctionnalités pour rechercher et charger les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="b6933-112">Instead, you define your own resource format, and your application must provide its own functionality to find and load the required resources.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b6933-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b6933-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6933-114">Préparation des ressources</span><span class="sxs-lookup"><span data-stu-id="b6933-114">Preparing Resources</span></span>](preparing-resources.md)
</dt> <dt>

[<span data-ttu-id="b6933-115">Préparation d’un fichier de configuration de ressource</span><span class="sxs-lookup"><span data-stu-id="b6933-115">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)
</dt> </dl>

 

 
