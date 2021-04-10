---
title: include (attribut)
description: L’instruction include ACF spécifie un ou plusieurs fichiers d’en-tête à inclure dans le code stub généré.
ms.assetid: f83a704b-2f6e-4498-97ff-593fef2e92dc
keywords:
- inclure MIDL de l’attribut
topic_type:
- apiref
api_name:
- include
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2aab7b7262bceb330e3f4645e4f16035b783197
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100873"
---
# <a name="include-attribute"></a><span data-ttu-id="73ee4-104">include (attribut)</span><span class="sxs-lookup"><span data-stu-id="73ee4-104">include attribute</span></span>

<span data-ttu-id="73ee4-105">L’instruction **include** ACF spécifie un ou plusieurs fichiers d’en-tête à inclure dans le code stub généré.</span><span class="sxs-lookup"><span data-stu-id="73ee4-105">The ACF **include** statement specifies one or more header files to be included in the generated stub code.</span></span>

``` syntax
include filenames;
```

## <a name="parameters"></a><span data-ttu-id="73ee4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73ee4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73ee4-107">*noms*</span><span class="sxs-lookup"><span data-stu-id="73ee4-107">*filenames*</span></span> 
</dt> <dd>

<span data-ttu-id="73ee4-108">Spécifie le nom d’un ou plusieurs fichiers d’en-tête du langage C.</span><span class="sxs-lookup"><span data-stu-id="73ee4-108">Specifies the name of one or more C-language header files.</span></span> <span data-ttu-id="73ee4-109">Utilisez le nom de fichier complet, y compris le. Extension H et mettez chaque nom de fichier entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="73ee4-109">Use the full file name, including the .H extension and enclose each file name in quotation marks.</span></span> <span data-ttu-id="73ee4-110">Séparez les noms de fichiers d’en-tête en langage C par des virgules.</span><span class="sxs-lookup"><span data-stu-id="73ee4-110">Separate multiple C-language header file names with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73ee4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="73ee4-111">Remarks</span></span>

<span data-ttu-id="73ee4-112">À la suite de l’instruction **include** , le code stub généré contient une instruction **\# include** de préprocesseur C.</span><span class="sxs-lookup"><span data-stu-id="73ee4-112">As a result of the **include** statement, the generated stub code will contain a C-preprocessor **\#include** statement.</span></span> <span data-ttu-id="73ee4-113">Vous fournissez le fichier d’en-tête du langage C lors de la compilation des stubs.</span><span class="sxs-lookup"><span data-stu-id="73ee4-113">You supply the C-language header file when compiling the stubs.</span></span> <span data-ttu-id="73ee4-114">Les instructions include s’appuient sur le mécanisme de compilateur C pour rechercher les fichiers inclus dans la structure de répertoires.</span><span class="sxs-lookup"><span data-stu-id="73ee4-114">Include statements rely on the C-compiler mechanism of searching the directory structure for included files.</span></span>

> [!Note]  
> <span data-ttu-id="73ee4-115">Utilisez la directive [**Import**](import.md) plutôt que la directive **include** pour les fichiers système qui contiennent des types de données que vous souhaitez mettre à la disposition du fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="73ee4-115">Use the [**import**](import.md) directive rather than the **include** directive for system files that contain data types you want to make available to the IDL file.</span></span> <span data-ttu-id="73ee4-116">La directive **Import** ignore les prototypes de fonction et vous permet d’utiliser des commutateurs du compilateur MIDL qui optimisent la génération de routines de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="73ee4-116">The **import** directive ignores function prototypes and allows you to use MIDL compiler switches that optimize the generation of support routines.</span></span>

 

## <a name="examples"></a><span data-ttu-id="73ee4-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="73ee4-117">Examples</span></span>

``` syntax
include "local.h";
include "gendefs.h", "protos.h", "mystuff.h";
```

## <a name="see-also"></a><span data-ttu-id="73ee4-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73ee4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73ee4-119">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="73ee4-119">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="73ee4-120">**port**</span><span class="sxs-lookup"><span data-stu-id="73ee4-120">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="73ee4-121">Importation de fichiers et de bibliothèques de types</span><span class="sxs-lookup"><span data-stu-id="73ee4-121">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="73ee4-122">Importation de fichiers d’en-tête système</span><span class="sxs-lookup"><span data-stu-id="73ee4-122">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> </dl>

 

 




