---
title: import (attribut)
description: La directive import spécifie un autre fichier IDL, ODL ou d’en-tête contenant les définitions que vous souhaitez référencer à partir de votre fichier IDL principal.
ms.assetid: b52fb2c7-ce60-474f-8833-7a821844f747
keywords:
- MIDL d’attribut d’importation
topic_type:
- apiref
api_name:
- import
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ff13c069c6bba819720a9d1120a42c25af4b51
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314766"
---
# <a name="import-attribute"></a><span data-ttu-id="6e132-104">import (attribut)</span><span class="sxs-lookup"><span data-stu-id="6e132-104">import attribute</span></span>

<span data-ttu-id="6e132-105">La directive **Import** spécifie un autre fichier IDL, ODL ou d’en-tête contenant les définitions que vous souhaitez référencer à partir de votre fichier IDL principal.</span><span class="sxs-lookup"><span data-stu-id="6e132-105">The **import** directive specifies another IDL, ODL, or header file containing definitions you wish to reference from your main IDL file.</span></span>

``` syntax
import "filename" [[ , ... ]] ;
```

## <a name="parameters"></a><span data-ttu-id="6e132-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e132-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e132-107">*extension*</span><span class="sxs-lookup"><span data-stu-id="6e132-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="6e132-108">Spécifie le nom du fichier d’en-tête, IDL ou ODL à importer.</span><span class="sxs-lookup"><span data-stu-id="6e132-108">Specifies the name of the header, IDL, or ODL file to import.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e132-109">Notes</span><span class="sxs-lookup"><span data-stu-id="6e132-109">Remarks</span></span>

<span data-ttu-id="6e132-110">Avec la directive **Import** , toutes les instructions IDL dans le fichier importé, telles que typedefs, déclarations de constantes et définitions d’interface, deviennent disponibles pour l’importation. Fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="6e132-110">With the **import** directive, all IDL statements in the imported file, such as typedefs, constant declarations, and interface definitions become available to the importing .IDL file.</span></span>

<span data-ttu-id="6e132-111">Le fichier importé est traité séparément (ce qui signifie que le préprocesseur CPP est appelé indépendamment) à partir du fichier IDL d’importation.</span><span class="sxs-lookup"><span data-stu-id="6e132-111">The imported file is processed separately (meaning that CPP preprocessor is invoked independently) from the importing IDL file.</span></span> <span data-ttu-id="6e132-112">De cette façon, les directives de préprocesseur, telles que \# define, ne reportent pas d’un fichier d’en-tête ou d’un fichier IDL importé vers le fichier IDL d’importation.</span><span class="sxs-lookup"><span data-stu-id="6e132-112">In this way, pre-processor directives, such as \#define, do not carry over from an imported header or IDL file to the importing IDL file.</span></span>

<span data-ttu-id="6e132-113">À l’instar de la macro de préprocesseur du langage C **\# include**, la directive **Import** indique au compilateur d’inclure les types de données définis dans les fichiers IDL importés.</span><span class="sxs-lookup"><span data-stu-id="6e132-113">Like the C-language preprocessor macro **\#include**, the **import** directive tells the compiler to include data types that were defined in the imported IDL files.</span></span> <span data-ttu-id="6e132-114">Contrairement à la directive **\# include** , la directive **Import** ignore les prototypes de procédure, car aucun stub n’est généré pour quoi que ce soit dans le fichier importé.</span><span class="sxs-lookup"><span data-stu-id="6e132-114">Unlike the **\#include** directive, the **import** directive ignores procedure prototypes, since no stubs are generated for anything in the imported file.</span></span>

<span data-ttu-id="6e132-115">Pour obtenir des informations spécifiques sur l’utilisation de l' **importation** pour inclure des fichiers d’en-tête dans un fichier IDL, consultez [importation de fichiers d’en-tête système](importing-system-header-files.md).</span><span class="sxs-lookup"><span data-stu-id="6e132-115">For specific information on using **import** to include header files in an IDL file, see [Importing System Header Files](importing-system-header-files.md).</span></span>

<span data-ttu-id="6e132-116">En-tête du langage C (. H) généré pour l’interface ne contient pas directement les types importés, mais génère à la place une directive **\# include** pour le fichier d’en-tête correspondant à l’interface importée.</span><span class="sxs-lookup"><span data-stu-id="6e132-116">The C-language header (.H) file generated for the interface does not directly contain the imported types but instead generates a **\#include** directive for the header file corresponding to the imported interface.</span></span> <span data-ttu-id="6e132-117">Par exemple, lorsque vous importez la BASE. IDL dans votre dérivé. IDL, le fichier d’en-tête généré est dérivé. H contiendra la directive **\# include** base. H.</span><span class="sxs-lookup"><span data-stu-id="6e132-117">For example, when you import BASE.IDL into your DERIVED.IDL, the generated header file DERIVED.H will contain the directive **\#include** BASE.H.</span></span>

<span data-ttu-id="6e132-118">Les règles suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="6e132-118">The following rules apply:</span></span>

-   <span data-ttu-id="6e132-119">Le mot clé **Import** est facultatif et peut apparaître zéro, une ou plusieurs fois dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="6e132-119">The **import** keyword is optional and can appear zero or more times in the IDL file.</span></span>
-   <span data-ttu-id="6e132-120">Chaque mot clé **Import** peut être associé à plusieurs noms de fichier.</span><span class="sxs-lookup"><span data-stu-id="6e132-120">Each **import** keyword can be associated with more than one file name.</span></span>
-   <span data-ttu-id="6e132-121">Séparez les noms de fichiers par des virgules.</span><span class="sxs-lookup"><span data-stu-id="6e132-121">Separate multiple file names with commas.</span></span>
-   <span data-ttu-id="6e132-122">Vous devez placer le nom de fichier entre guillemets et mettre fin à l’instruction d’importation avec un point-virgule (;).</span><span class="sxs-lookup"><span data-stu-id="6e132-122">You must enclose the file name within quotation marks and end the import statement with a semicolon (;).</span></span>
-   <span data-ttu-id="6e132-123">Vous pouvez importer une interface qui n’a pas d’attributs dans un autre fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="6e132-123">You can import an interface that has no attributes into another IDL file.</span></span> <span data-ttu-id="6e132-124">Toutefois, l’interface doit contenir uniquement des types de données ; elle ne peut pas contenir de procédures.</span><span class="sxs-lookup"><span data-stu-id="6e132-124">However, the interface must contain only datatypes; it cannot contain any procedures.</span></span> <span data-ttu-id="6e132-125">Si même une procédure est contenue dans l’interface importée, vous devez spécifier un attribut [**local**](local.md) ou [**UUID**](uuid.md) .</span><span class="sxs-lookup"><span data-stu-id="6e132-125">If even one procedure is contained in the imported interface, you must specify a [**local**](local.md) or [**UUID**](uuid.md) attribute.</span></span>
-   <span data-ttu-id="6e132-126">La fonction d' **importation** est idempotentÂ â €, c’est-à-dire que l’importation d’une interface plus d’une fois n’a aucun effet supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="6e132-126">The **import** function is idempotentÂ â€”Â that is, importing an interface more than once has no additional effect.</span></span>

> [!Note]  
> <span data-ttu-id="6e132-127">Le comportement de la directive **Import** est indépendant du mode compilateur MIDL commutateurs [**/ms. \_ ext**](-ms-ext.md) (valeur par défaut), [**/OSF**](-osf.md)et [**/app \_**](-app-config.md).</span><span class="sxs-lookup"><span data-stu-id="6e132-127">The behavior of the **import** directive is independent of the MIDL compiler mode switches [**/ms\_ext**](-ms-ext.md) (the default), [**/osf**](-osf.md), and [**/app\_config**](-app-config.md).</span></span> <span data-ttu-id="6e132-128">Toutefois, le mode de compilateur (**/OSF** ou **/ms. \_ ext**) peut affecter la décoration d’attribut de pointeur sur les types importés.</span><span class="sxs-lookup"><span data-stu-id="6e132-128">However, the compiler mode (**/osf** or **/ms\_ext**) can affect pointer attribute decoration on imported types.</span></span> <span data-ttu-id="6e132-129">Pour plus d’informations [, consultez héritage de type d’attribut de pointeur](/windows/desktop/Rpc/pointer-attribute-type-inheritance).</span><span class="sxs-lookup"><span data-stu-id="6e132-129">For details see [Pointer-Attribute Type Inheritance](/windows/desktop/Rpc/pointer-attribute-type-inheritance).</span></span>

 

## <a name="examples"></a><span data-ttu-id="6e132-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="6e132-130">Examples</span></span>

``` syntax
import "myoldodl.odl";  
import "unknwn.idl";
import "part1.idl", "part2.idl", "part3.idl"; 
```

## <a name="see-also"></a><span data-ttu-id="6e132-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e132-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e132-132">**configuration de/App \_**</span><span class="sxs-lookup"><span data-stu-id="6e132-132">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="6e132-133">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="6e132-133">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="6e132-134">**importlib**</span><span class="sxs-lookup"><span data-stu-id="6e132-134">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="6e132-135">**inclusion**</span><span class="sxs-lookup"><span data-stu-id="6e132-135">**include**</span></span>](include.md)
</dt> <dt>

[<span data-ttu-id="6e132-136">Importation de fichiers d’en-tête système</span><span class="sxs-lookup"><span data-stu-id="6e132-136">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> <dt>

[<span data-ttu-id="6e132-137">Importation de fichiers et de bibliothèques de types</span><span class="sxs-lookup"><span data-stu-id="6e132-137">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="6e132-138">**/ms. \_ ext**</span><span class="sxs-lookup"><span data-stu-id="6e132-138">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="6e132-139">**/osf**</span><span class="sxs-lookup"><span data-stu-id="6e132-139">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 