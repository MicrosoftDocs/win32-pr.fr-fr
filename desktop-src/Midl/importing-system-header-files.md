---
title: Importation de fichiers d’en-tête système
description: S’il est souvent possible d’utiliser la directive \ include pour inclure des fichiers d’en-tête dans votre fichier IDL, ce n’est pas recommandé.
ms.assetid: ff524965-424d-416d-97cd-c2780ebf69ef
keywords:
- importation de MIDL, fichiers d’en-tête système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26df7ca983fa21ae8e604446f0221c302c73099
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761588"
---
# <a name="importing-system-header-files"></a><span data-ttu-id="e880e-104">Importation de fichiers d’en-tête système</span><span class="sxs-lookup"><span data-stu-id="e880e-104">Importing System Header Files</span></span>

<span data-ttu-id="e880e-105">S’il est souvent possible d’utiliser la directive **\# include** pour inclure des fichiers d’en-tête dans votre fichier IDL, ce n’est pas recommandé.</span><span class="sxs-lookup"><span data-stu-id="e880e-105">While it is often possible to use the **\#include** directive to include header files in your IDL file, it is not recommended.</span></span> <span data-ttu-id="e880e-106">Le compilateur MIDL génère des stubs pour toutes les fonctions définies dans le fichier IDL en cours de compilation.</span><span class="sxs-lookup"><span data-stu-id="e880e-106">The MIDL compiler will generate stubs for all functions defined in the IDL file being compiled.</span></span> <span data-ttu-id="e880e-107">En général, un fichier d’en-tête contient un certain nombre de prototypes que vous n’avez pas besoin d’inclure dans vos fichiers stub, et un **\# include** place efficacement toutes ces définitions dans votre fichier IDL principal.</span><span class="sxs-lookup"><span data-stu-id="e880e-107">Usually a header file contains a number of prototypes that you neither need nor want to include in your stub files, and a **\#include** effectively puts all those definitions into your main IDL file.</span></span> <span data-ttu-id="e880e-108">En outre, si des types non accessibles à distance sont définis dans le fichier d’en-tête, le fichier IDL peut ne pas se compiler.</span><span class="sxs-lookup"><span data-stu-id="e880e-108">Furthermore, if there are nonremotable types defined in the header file, the IDL file may not compile.</span></span>

<span data-ttu-id="e880e-109">Il existe deux façons d’inclure des définitions de types à partir de fichiers d’en-tête dans un fichier IDL :</span><span class="sxs-lookup"><span data-stu-id="e880e-109">There are two ways to include type definitions from header files in an IDL file:</span></span>

-   <span data-ttu-id="e880e-110">Utilisez la directive [**Import**](import.md) pour inclure les types de données définis dans un fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="e880e-110">Use the [**import**](import.md) directive to include data types defined in a header file.</span></span> <span data-ttu-id="e880e-111">Contrairement à la directive **\# include** du langage C, la directive **Import** sélectionne uniquement les définitions de type et de constante et ignore les prototypes de procédure.</span><span class="sxs-lookup"><span data-stu-id="e880e-111">Unlike the C-language **\#include** directive, the **import** directive only picks up type and constant definitions and ignores procedure prototypes.</span></span> <span data-ttu-id="e880e-112">Cette approche fonctionne tant que votre fichier IDL principal ne fait pas référence à des types non accessibles à distance définis dans le fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="e880e-112">This approach will work as long as your main IDL file does not reference any nonremotable types defined in the header file.</span></span>
-   <span data-ttu-id="e880e-113">Créez un fichier IDL d’assistance avec une interface factice qui comprend les fichiers d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="e880e-113">Create a helper IDL file with a dummy interface that includes the header files.</span></span> <span data-ttu-id="e880e-114">Ensuite, utilisez la directive [**Import**](import.md) pour inclure le fichier d’assistance.</span><span class="sxs-lookup"><span data-stu-id="e880e-114">Then, use the [**import**](import.md) directive to include the helper file.</span></span> <span data-ttu-id="e880e-115">De cette façon, seuls les [**typedef**](typedef.md)s s’affichent dans les stubs compilés.</span><span class="sxs-lookup"><span data-stu-id="e880e-115">In this way, only the [**typedef**](typedef.md)s will appear in the compiled stubs.</span></span> <span data-ttu-id="e880e-116">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="e880e-116">For example:</span></span>

```syntax
//in helper.idl:
interface dummy
{ 
   #include "kitchensink.h"
   #include "system.h"
}

//in main.idl:
import "helper.idl";
```
