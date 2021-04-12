---
description: Vous devez compiler votre fichier MOF maître pour créer les fichiers MOF propres à une langue et spécifiques à une langue.
ms.assetid: ae2fa320-8294-4991-be30-403088c34b7a
ms.tgt_platform: multiple
title: Compilation des fichiers MOF localisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ab1341a37269ba98fdbbdecaa64b5e5a119703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319682"
---
# <a name="compiling-localized-mof-files"></a><span data-ttu-id="4fa42-103">Compilation des fichiers MOF localisés</span><span class="sxs-lookup"><span data-stu-id="4fa42-103">Compiling Localized MOF Files</span></span>

<span data-ttu-id="4fa42-104">Vous devez compiler votre fichier MOF maître pour créer les fichiers MOF propres à une langue et spécifiques à une langue.</span><span class="sxs-lookup"><span data-stu-id="4fa42-104">You must compile your master MOF file to create the language-neutral and language-specific MOF files.</span></span>

<span data-ttu-id="4fa42-105">Tapez la commande suivante à l’invite de commandes pour compiler un fichier MOF maître.</span><span class="sxs-lookup"><span data-stu-id="4fa42-105">Type the following command at a command prompt to compile a master MOF file.</span></span>

<span data-ttu-id="4fa42-106">**mofcomp-MOF : Lnmof. mof-MFL : Lsmof. MFL-amendement : MS \_ 409 Mastermof. mof**</span><span class="sxs-lookup"><span data-stu-id="4fa42-106">**mofcomp -MOF:Lnmof.mof -MFL:Lsmof.mfl -Amendment:MS\_409 Mastermof.mof**</span></span>

<span data-ttu-id="4fa42-107">Lorsque vous exécutez cette commande, le compilateur MOF crée deux fichiers MOF à partir du fichier Mastermof. mof d’origine.</span><span class="sxs-lookup"><span data-stu-id="4fa42-107">When you run this command, the MOF compiler creates two MOF files from the original Mastermof.mof file.</span></span> <span data-ttu-id="4fa42-108">Le compilateur MOF produit une version indépendante du langage, Lnmof. mof, dans laquelle tous les éléments spécifiques au langage sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="4fa42-108">The MOF compiler produces a language-neutral version, Lnmof.mof, in which all language-specific items are removed.</span></span> <span data-ttu-id="4fa42-109">Une deuxième version propre à la langue, Lsmof. mof, est également créée. ce fichier contient uniquement les éléments qui ont été marqués avec la version de qualificateur [**modifiée**](qualifier-flavors.md) dans le fichier Mastermof. mof.</span><span class="sxs-lookup"><span data-stu-id="4fa42-109">A second, language-specific version, Lsmof.mof, is also created; this file contains only items that were marked with the [**Amended**](qualifier-flavors.md) Qualifier Flavor in the Mastermof.mof file.</span></span>

<span data-ttu-id="4fa42-110">L’exemple de code suivant montre le contenu du fichier MOF indépendant du langage (Lnmof. MOF) qui est généré.</span><span class="sxs-lookup"><span data-stu-id="4fa42-110">The following code example shows the contents of the language-neutral MOF file (Lnmof.mof) that is generated.</span></span>

``` syntax
#pragma namespace("\\\\.\\root")

Instance of __Namespace
{
  Name = "TEST";
};
#pragma namespace("\\\\.\\root\\TEST")

[LOCALE(1033)] 
class myclass
{
  [key] string Name;
  uint64 Value;
  uint64 Timestamp;
};
```

<span data-ttu-id="4fa42-111">L’exemple de code suivant affiche le contenu du fichier MOF spécifique au langage (Lsmof. MFL) qui est généré.</span><span class="sxs-lookup"><span data-stu-id="4fa42-111">The following code example shows the contents of the language-specific MOF file (Lsmof.mfl) that is generated.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\TEST")
instance of __namespace{ name="ms_409";};
#pragma namespace("\\\\.\\root\\TEST\\ms_409")

[Description("Localized version of MyClass for American English") :
    Amended, LOCALE(0x409)] 

class myclass
{
    [DisplayName("User Name") : Amended,
    Description("The Name property contains the name of the user") : 
    Amended, key]
     string Name;

    [DisplayName("Time Stamp") : Amended,
    Description("This property shows when the object was created") : 
    Amended] 
     uint64 Timestamp;
};
```

<span data-ttu-id="4fa42-112">La compilation d’un fichier MOF avec le qualificateur [**modifié**](qualifier-flavors.md) génère uniquement des fichiers MOF indépendants du langage et propres aux langages. le référentiel CIM n’est pas mis à jour avec les nouvelles informations de classe.</span><span class="sxs-lookup"><span data-stu-id="4fa42-112">Compiling a MOF file with the [**Amended**](qualifier-flavors.md) qualifier only generates separate language-neutral and language-specific MOF files; the CIM repository is not updated with the new class information.</span></span> <span data-ttu-id="4fa42-113">Vous devez utiliser le compilateur MOF pour compiler les deux fichiers MOF générés par la première compilation avant que toutes les informations de classe ne soient disponibles pour WMI.</span><span class="sxs-lookup"><span data-stu-id="4fa42-113">You must use the MOF compiler to compile the two MOF files that the first compilation produced before any class information is available to WMI.</span></span>

<span data-ttu-id="4fa42-114">Quand vous compilez un fichier MOF maître, seuls les qualificateurs avec la version [**modifiée**](qualifier-flavors.md) sont déplacés vers le fichier MOF propre au langage.</span><span class="sxs-lookup"><span data-stu-id="4fa42-114">When you compile a master MOF file, only qualifiers with the [**Amended**](qualifier-flavors.md) flavor are moved to the language-specific MOF file.</span></span> <span data-ttu-id="4fa42-115">Les qualificateurs qui n’ont pas la version **modifiée** ne sont pas localisés et n’existent que dans la définition de la classe de base dans le fichier MOF indépendant du langage.</span><span class="sxs-lookup"><span data-stu-id="4fa42-115">Qualifiers that do not have the **Amended** flavor are not localized and only exist in the basic class definition in the language-neutral MOF file.</span></span> <span data-ttu-id="4fa42-116">Les qualificateurs non localisés peuvent être utilisés pour les descriptions par défaut si les descriptions localisées ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="4fa42-116">Nonlocalized qualifiers can be used for default descriptions if localized descriptions are not available.</span></span>

<span data-ttu-id="4fa42-117">Vous pouvez utiliser la commande [pragma Amendement](pragma-amendment.md) [**au lieu de spécifier**](qualifier-flavors.md) Changed en tant que commutateur pour le compilateur MOF.</span><span class="sxs-lookup"><span data-stu-id="4fa42-117">You can use the [pragma amendment](pragma-amendment.md) command instead of specifying [**Amended**](qualifier-flavors.md) as a switch to the MOF compiler.</span></span> <span data-ttu-id="4fa42-118">L’une ou l’autre de ces options est équivalente à la demande de versions spécifiques à une langue et indépendantes du langage d’un fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="4fa42-118">Either of these options are equivalent to requesting language-specific and language-neutral versions of a MOF file.</span></span> <span data-ttu-id="4fa42-119">Si vous utilisez la commande pragma amendement ou l’option de ligne de commande **modifiée** , vous devez spécifier le nom des fichiers de sortie à l’aide des options **-MFL** et **-MOF** à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="4fa42-119">If you use either the pragma amendment command or the **Amended** command-line option, you must specify the name of the output files using the **-MFL** and **-MOF** options at the command prompt.</span></span>

> [!Note]  
> <span data-ttu-id="4fa42-120">Le fichier MOF indépendant du langage généré par le compilateur MOF contient l’équivalent décimal de l’ID de paramètres régionaux, même si cette valeur a été entrée au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="4fa42-120">The language-neutral MOF file that the MOF compiler generates contains the decimal equivalent of the locale ID, even if this value was entered in hexadecimal.</span></span> <span data-ttu-id="4fa42-121">Dans l’exemple ci-dessus, le compilateur a converti la valeur 0x40C en nombre décimal 1033 pour le fichier de sortie Lnmof. mof.</span><span class="sxs-lookup"><span data-stu-id="4fa42-121">In the example above, the compiler has converted the value 0x409 to the decimal number 1033 for the Lnmof.mof output file.</span></span>

 

 

 



