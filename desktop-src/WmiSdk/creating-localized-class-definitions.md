---
description: La création de définitions de classe localisées est un processus en trois étapes.
ms.assetid: e303b894-07c4-44e3-9c57-58b1db16ae9a
ms.tgt_platform: multiple
title: Création de définitions de classes localisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41a183c1478c259b0428cd827088a769e680425
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106527266"
---
# <a name="creating-localized-class-definitions"></a><span data-ttu-id="7519e-103">Création de définitions de classes localisées</span><span class="sxs-lookup"><span data-stu-id="7519e-103">Creating Localized Class Definitions</span></span>

<span data-ttu-id="7519e-104">La création de définitions de classe localisées est un processus en trois étapes.</span><span class="sxs-lookup"><span data-stu-id="7519e-104">Creating localized class definitions is a three-step process.</span></span> <span data-ttu-id="7519e-105">Vous commencez par écrire du code MOF qui définit les classes, y compris tous les qualificateurs qui doivent être localisés.</span><span class="sxs-lookup"><span data-stu-id="7519e-105">You start by writing MOF code that defines the classes, including all qualifiers that must be localized.</span></span> <span data-ttu-id="7519e-106">Ce fichier d’origine est appelé le fichier « Master MOF », car il contient tous les qualificateurs et propriétés qui définissent la classe.</span><span class="sxs-lookup"><span data-stu-id="7519e-106">This original file is called the "master MOF" file because it contains all of the qualifiers and properties that define the class.</span></span>

<span data-ttu-id="7519e-107">Ensuite, utilisez le [compilateur MOF](mofcomp.md) pour créer les versions indépendantes du langage et de la langue du fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="7519e-107">Next, use the [MOF compiler](mofcomp.md) to create the language-neutral and language-specific versions of the MOF file.</span></span> <span data-ttu-id="7519e-108">Le compilateur MOF place la description de la classe de base dans un nouveau fichier MOF et crée une version localisée du fichier MOF qui contient uniquement les propriétés et les qualificateurs qui doivent être localisés.</span><span class="sxs-lookup"><span data-stu-id="7519e-108">The MOF compiler places the basic class description in a new MOF file and creates a localized version of the MOF file that contains only the properties and qualifiers that must be localized.</span></span> <span data-ttu-id="7519e-109">Bien que les versions propres aux langages et aux langues indépendantes du fichier MOF puissent avoir le même nom de fichier, vous devez utiliser une extension de nom de fichier. MFL pour indiquer que le fichier contient des informations localisées.</span><span class="sxs-lookup"><span data-stu-id="7519e-109">Although the language-specific and language-neutral versions of the MOF file can have the same file name, you should use a .mfl file name extension to indicate that the file contains localized information.</span></span> <span data-ttu-id="7519e-110">Vous pouvez localiser le fichier. MFL avec d’autres paramètres régionaux, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7519e-110">You can localize the .mfl file to other locales, if necessary.</span></span> <span data-ttu-id="7519e-111">Le stockage des définitions de classe dans le référentiel CIM nécessite une étape supplémentaire de l’utilisation du compilateur MOF pour compiler à la fois les fichiers MOF de langue neutre et les fichiers MOF spécifiques à une langue.</span><span class="sxs-lookup"><span data-stu-id="7519e-111">Storing the class definitions in the CIM repository requires an additional step of using the MOF compiler to compile both the language-neutral and the language-specific MOF files.</span></span>

<span data-ttu-id="7519e-112">Les étapes suivantes décrivent comment créer et stocker une définition de classe localisée.</span><span class="sxs-lookup"><span data-stu-id="7519e-112">The following steps describe how to create and store a localized class definition.</span></span>

<span data-ttu-id="7519e-113">**Pour créer et stocker une définition de classe localisée**</span><span class="sxs-lookup"><span data-stu-id="7519e-113">**To create and store a localized class definition**</span></span>

1.  <span data-ttu-id="7519e-114">Créez le fichier MOF maître qui définit les classes que vous souhaitez localiser.</span><span class="sxs-lookup"><span data-stu-id="7519e-114">Create the master MOF file that defines the classes that you want localized.</span></span>

    <span data-ttu-id="7519e-115">Enregistrez ce code MOF dans un fichier appelé Mastermof. mof.</span><span class="sxs-lookup"><span data-stu-id="7519e-115">Save this MOF code in a file called Mastermof.mof.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root")

    instance of __Namespace
    {
        Name = "TEST" ;
    } ;

    #pragma namespace("\\\\.\\root\\TEST")

    [Description("Localized version of MyClass for American English") 
        : Amended, LOCALE(0x409)] 

    class myclass
    {
        [DisplayName("User Name") : Amended,
        Description("The Name property contains the name of the user") : 
        Amended, key]
         string Name;

        uint64 Value; // non-localized value field

          [DisplayName("Time Stamp") : Amended,
        Description("This property shows when the object was created") : 
        Amended] 
         uint64 Timestamp;
    };
    ```

2.  <span data-ttu-id="7519e-116">Créez des versions indépendantes de la langue et de la langue du fichier MOF en compilant le fichier MasterMOF. mof.</span><span class="sxs-lookup"><span data-stu-id="7519e-116">Create language-neutral and language-specific versions of the MOF file by compiling the MasterMOF.mof file.</span></span>

    <span data-ttu-id="7519e-117">Tapez la commande suivante à l’invite de commandes pour compiler le fichier MasterMOF. mof.</span><span class="sxs-lookup"><span data-stu-id="7519e-117">Type the following command at a command prompt to compile the MasterMOF.mof file.</span></span>

    <span data-ttu-id="7519e-118">**mofcomp-MOF : Lnmof. mof-MFL : Lsmof. MFL-amendement : MS \_ 409 Mastermof. mof**</span><span class="sxs-lookup"><span data-stu-id="7519e-118">**mofcomp -MOF:Lnmof.mof -MFL:Lsmof.mfl -Amendment:MS\_409 Mastermof.mof**</span></span>

3.  <span data-ttu-id="7519e-119">Compilez les fichiers indépendants du langage (Lnmof. MOF) et les fichiers spécifiques à la langue (Lsmof. MFL) et stockez les informations de classe dans le référentiel CIM.</span><span class="sxs-lookup"><span data-stu-id="7519e-119">Compile the language-neutral (Lnmof.mof) and language-specific (Lsmof.mfl) files and store the class information in the CIM repository.</span></span>

    <span data-ttu-id="7519e-120">Tapez les commandes suivantes à l’invite de commandes pour stocker les informations de classe dans le référentiel CIM.</span><span class="sxs-lookup"><span data-stu-id="7519e-120">Type the following commands at a command prompt to store the class information in the CIM repository.</span></span>

    <span data-ttu-id="7519e-121">**Mofcomp Lnmof. mof**</span><span class="sxs-lookup"><span data-stu-id="7519e-121">**Mofcomp Lnmof.mof**</span></span>

    <span data-ttu-id="7519e-122">**Mofcomp Lsmof. MFL**</span><span class="sxs-lookup"><span data-stu-id="7519e-122">**Mofcomp Lsmof.mfl**</span></span>

    <span data-ttu-id="7519e-123">Une fois que vous avez compilé ces fichiers, vous aurez une définition de classe indépendante du langage dans l' \\ espace de noms de test racine et une définition de classe localisée dans l' \\ espace de \\ noms MS 409 de test racine \_ .</span><span class="sxs-lookup"><span data-stu-id="7519e-123">After you compile these files, you will have a language-neutral class definition in the root\\test namespace and a localized class definition in the root\\test\\ms\_409 namespace.</span></span> <span data-ttu-id="7519e-124">Pour plus d’informations sur la compilation des fichiers MOF localisés, consultez [compilation des fichiers MOF localisés](compiling-localized-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="7519e-124">For more information about compiling localized MOF files, see [Compiling Localized MOF files](compiling-localized-mof-files.md).</span></span>

 

 



