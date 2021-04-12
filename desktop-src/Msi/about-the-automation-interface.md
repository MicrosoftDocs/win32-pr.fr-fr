---
description: Un objet d’installation doit être créé initialement pour charger la prise en charge d’Automation requise pour accéder aux composants du programme d’installation via COM.
ms.assetid: 113ed443-a866-43d4-86bd-fc3b244f2edb
title: À propos de l’interface d’automatisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655a01a4daccb805bec4a858337c1dce48f0fb82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202570"
---
# <a name="about-the-automation-interface"></a><span data-ttu-id="e5ec6-103">À propos de l’interface d’automatisation</span><span class="sxs-lookup"><span data-stu-id="e5ec6-103">About the Automation Interface</span></span>

<span data-ttu-id="e5ec6-104">Un [**objet d’installation**](installer-object.md) doit être créé initialement pour charger la prise en charge d’Automation requise pour accéder aux composants du programme d’installation via com.</span><span class="sxs-lookup"><span data-stu-id="e5ec6-104">An [**Installer object**](installer-object.md) must be created initially to load the automation support required to access the installer components through COM.</span></span> <span data-ttu-id="e5ec6-105">Cet objet fournit des wrappers pour créer les objets de niveau supérieur et accéder à leurs méthodes.</span><span class="sxs-lookup"><span data-stu-id="e5ec6-105">This object provides wrappers to create the top-level objects and access their methods.</span></span> <span data-ttu-id="e5ec6-106">Ces wrappers fournissent simplement des traductions de paramètres pour exposer les fonctions du programme d’installation d’une manière cohérente avec Microsoft Visual Basic sans modifier le comportement des méthodes.</span><span class="sxs-lookup"><span data-stu-id="e5ec6-106">These wrappers simply provide parameter translations to expose the installer functions in a manner consistent with Microsoft Visual Basic without changing the behavior of the methods.</span></span>

<span data-ttu-id="e5ec6-107">Dans la mesure du possible, une paire de méthodes C++ d’extraction et de définition sont exposées à Visual Basic en tant que propriété unique.</span><span class="sxs-lookup"><span data-stu-id="e5ec6-107">Whenever possible, a pair of Get and Set C++ methods are exposed to Visual Basic as a single property.</span></span> <span data-ttu-id="e5ec6-108">Dans certains cas, les méthodes C++ qui prennent un argument d’index sont exposées en tant que propriété indexée.</span><span class="sxs-lookup"><span data-stu-id="e5ec6-108">In some cases C++ methods taking an index argument are exposed as an indexed property.</span></span> <span data-ttu-id="e5ec6-109">De nombreuses méthodes C++ retournent le résultat via un paramètre, car la valeur de retour est utilisée pour le retour d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e5ec6-109">Many C++ methods return the result through a parameter because the return value is used for the error return.</span></span> <span data-ttu-id="e5ec6-110">Toutefois, dans Visual Basic, les erreurs sont gérées par un mécanisme distinct, et le résultat est toujours passé dans la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="e5ec6-110">However, in Visual Basic, errors are handled by a separate mechanism, and the result is always passed in the return value.</span></span>

<span data-ttu-id="e5ec6-111">Pour plus d’informations sur l’utilisation d’Automation et la création de l’objet installer, consultez [utilisation de l’interface Automation](using-the-automation-interface.md).</span><span class="sxs-lookup"><span data-stu-id="e5ec6-111">For information about using automation and creating the Installer object, see [Using the Automation Interface](using-the-automation-interface.md).</span></span>

<span data-ttu-id="e5ec6-112">Pour obtenir des documents de référence pour les objets Windows Installer, consultez Référence de l' [interface Automation](automation-interface-reference.md).</span><span class="sxs-lookup"><span data-stu-id="e5ec6-112">For reference material for the Windows Installer objects, see [Automation Interface Reference](automation-interface-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5ec6-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e5ec6-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5ec6-114">Exemples de scripts Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e5ec6-114">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 



