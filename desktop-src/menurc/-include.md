---
title: " include"
description: La directive \ include force le compilateur de ressources à traiter le fichier spécifié dans le paramètre filename.
ms.assetid: 9a3505c6-c19f-4c4f-85a4-94fbcfc0f9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8d36f1d0ae24f3dc21d67eec57056872aabdbd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383767"
---
# <a name="-include"></a><span data-ttu-id="23815-103">inclusion</span><span class="sxs-lookup"><span data-stu-id="23815-103">' include'</span></span>

<span data-ttu-id="23815-104">La directive **\# include** force le compilateur de ressources à traiter le fichier spécifié dans le paramètre *filename* .</span><span class="sxs-lookup"><span data-stu-id="23815-104">The **\#include** directive causes the resource compiler to process the file specified in the *filename* parameter.</span></span> <span data-ttu-id="23815-105">Ce fichier doit être un fichier d’en-tête qui définit les constantes utilisées dans le fichier de définition de ressource.</span><span class="sxs-lookup"><span data-stu-id="23815-105">This file should be a header file that defines the constants used in the resource-definition file.</span></span> <span data-ttu-id="23815-106">Le fichier peut utiliser des caractères codés sur un octet, codés sur deux octets ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="23815-106">The file can use single-byte, double-byte, or Unicode characters.</span></span>

``` syntax
#include filename
```

<dl> <dt>

<span data-ttu-id="23815-107"><span id="filename"></span><span id="FILENAME"></span>*extension*</span><span class="sxs-lookup"><span data-stu-id="23815-107"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="23815-108">Nom du fichier à inclure.</span><span class="sxs-lookup"><span data-stu-id="23815-108">Name of the file to be included.</span></span> <span data-ttu-id="23815-109">Si le fichier se trouve dans le répertoire actif, la chaîne doit être placée entre guillemets doubles ; Si le fichier se trouve dans le répertoire spécifié par la variable d’environnement INCLUDe, la chaîne doit être placée dans des caractères inférieur à et supérieur à (<>).</span><span class="sxs-lookup"><span data-stu-id="23815-109">If the file is in the current directory, the string must be enclosed in double quotation marks; if the file is in the directory specified by the INCLUDE environment variable, the string must be enclosed in less-than and greater-than characters (<>).</span></span> <span data-ttu-id="23815-110">Vous devez fournir un chemin d’accès complet placé entre guillemets doubles (") si le fichier ne se trouve pas dans le répertoire actif ou dans le répertoire spécifié par la variable d’environnement INCLUDe.</span><span class="sxs-lookup"><span data-stu-id="23815-110">You must give a full path enclosed in double quotation marks (") if the file is not in the current directory or in the directory specified by the INCLUDE environment variable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23815-111">Notes</span><span class="sxs-lookup"><span data-stu-id="23815-111">Remarks</span></span>

<span data-ttu-id="23815-112">Utilisez l’instruction suivante dans votre fichier d’en-tête pour entourer les instructions qui peuvent être compilées par un compilateur C, mais pas RC :</span><span class="sxs-lookup"><span data-stu-id="23815-112">Use the following statement in your header file to surround statements that can be compiled by a C compiler but not RC:</span></span>

``` syntax
#ifndef RC_INVOKED
```

<span data-ttu-id="23815-113">De cette façon, vous pouvez utiliser les mêmes fichiers include dans vos fichiers. c et. rc.</span><span class="sxs-lookup"><span data-stu-id="23815-113">This way, you can use the same include files in your .c and .rc files.</span></span>

## <a name="example"></a><span data-ttu-id="23815-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="23815-114">Example</span></span>

<span data-ttu-id="23815-115">Cet exemple traite les fichiers d’en-tête Windows. h et MyDefs. h lors de la compilation du fichier de définition de ressource :</span><span class="sxs-lookup"><span data-stu-id="23815-115">This example processes the header files Windows.h and MyDefs.h while compiling the resource-definition file:</span></span>

``` syntax
#include <windows.h>
#include "headers\mydefs.h"
```

## <a name="related-topics"></a><span data-ttu-id="23815-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="23815-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23815-117">Directives de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="23815-117">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




