---
title: Utilisation de MIDL
description: Création et compilation d’une interface Microsoft Interface Definition Language (MIDL) et d’un appel de procédure distante (RPC).
ms.assetid: 2594e3d6-d44a-4e12-8286-b9700e67702e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22da60f20cba6c558c7f1a67478adef7b407d591
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730013"
---
# <a name="using-midl"></a><span data-ttu-id="38bb6-103">Utilisation de MIDL</span><span class="sxs-lookup"><span data-stu-id="38bb6-103">Using MIDL</span></span>

<span data-ttu-id="38bb6-104">Toutes les interfaces des programmes utilisant RPC doivent être définies en Microsoft Interface Definition Language (MIDL) et compilées avec le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="38bb6-104">All interfaces for programs using RPC must be defined in Microsoft Interface Definition Language (MIDL) and compiled with the MIDL compiler.</span></span> <span data-ttu-id="38bb6-105">Les rubriques suivantes présentent une brève présentation de la création et de la compilation d’une interface MIDL :</span><span class="sxs-lookup"><span data-stu-id="38bb6-105">The following topics present a brief overview of creating and compiling a MIDL interface:</span></span>

-   [<span data-ttu-id="38bb6-106">Définition d’une interface avec MIDL</span><span class="sxs-lookup"><span data-stu-id="38bb6-106">Defining an Interface with MIDL</span></span>](#defining-an-interface-with-midl)
-   [<span data-ttu-id="38bb6-107">Compilation d’un fichier MIDL</span><span class="sxs-lookup"><span data-stu-id="38bb6-107">Compiling a MIDL File</span></span>](#compiling-a-midl-file)

<span data-ttu-id="38bb6-108">Pour une présentation détaillée de ces rubriques, consultez [les fichiers IDL et ACF](the-idl-and-acf-files.md).</span><span class="sxs-lookup"><span data-stu-id="38bb6-108">For a detailed discussion of these topics, see [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

## <a name="defining-an-interface-with-midl"></a><span data-ttu-id="38bb6-109">Définition d’une interface avec MIDL</span><span class="sxs-lookup"><span data-stu-id="38bb6-109">Defining an Interface with MIDL</span></span>

<span data-ttu-id="38bb6-110">Les fichiers MIDL sont des fichiers texte que vous pouvez créer et modifier à l’aide d’un éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="38bb6-110">MIDL files are text files that you can create and edit with a text editor.</span></span> <span data-ttu-id="38bb6-111">Si vous générez un UUID pour votre interface, vous stockez généralement la sortie dans un fichier MIDL de modèle.</span><span class="sxs-lookup"><span data-stu-id="38bb6-111">If you generate a UUID for your interface, you will typically store the output in a template MIDL file.</span></span> <span data-ttu-id="38bb6-112">Pour plus d’informations sur les UUID, consultez [génération d’UUID d’interface](generating-interface-uuids.md).</span><span class="sxs-lookup"><span data-stu-id="38bb6-112">For more information on UUIDs, see [Generating Interface UUIDs](generating-interface-uuids.md).</span></span>

<span data-ttu-id="38bb6-113">Toutes les interfaces dans MIDL suivent le même format.</span><span class="sxs-lookup"><span data-stu-id="38bb6-113">All interfaces in MIDL follow the same format.</span></span> <span data-ttu-id="38bb6-114">Ils commencent par un en-tête qui contient une liste d’attributs d’interface et le nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="38bb6-114">They begin with a header that contains a list of interface attributes and the interface name.</span></span> <span data-ttu-id="38bb6-115">Les attributs sont placés entre crochets.</span><span class="sxs-lookup"><span data-stu-id="38bb6-115">The attributes are enclosed in square brackets.</span></span> <span data-ttu-id="38bb6-116">L’en-tête d’interface est suivi de son corps, qui est placé entre accolades.</span><span class="sxs-lookup"><span data-stu-id="38bb6-116">The interface header is followed by its body, which is enclosed in curly brackets.</span></span> <span data-ttu-id="38bb6-117">Une interface simple est présentée dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="38bb6-117">A simple interface is shown in the following example:</span></span>

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface MyInterface
{
  const unsigned short INT_ARRAY_LEN = 100;

  void MyRemoteProc( 
      [in] int param1,
      [out] int outArray[INT_ARRAY_LEN]
  );
}
```

<span data-ttu-id="38bb6-118">Certains des attributs qui apparaissent généralement dans une définition d’interface MIDL sont l’UUID et le numéro de version de l’interface.</span><span class="sxs-lookup"><span data-stu-id="38bb6-118">Some of the attributes that typically appear in a MIDL interface definition are the UUID and the interface version number.</span></span> <span data-ttu-id="38bb6-119">Le corps de la définition d’interface doit contenir les déclarations de procédure de toutes les procédures distantes dans l’interface.</span><span class="sxs-lookup"><span data-stu-id="38bb6-119">The body of the interface definition must contain the procedure declarations of all of the remote procedures in the interface.</span></span> <span data-ttu-id="38bb6-120">Il peut également contenir les déclarations des types de données et des constantes requis par l’interface.</span><span class="sxs-lookup"><span data-stu-id="38bb6-120">It can also contain the declarations of data types and constants required by the interface.</span></span>

<span data-ttu-id="38bb6-121">Tous les paramètres dans les déclarations de procédure distante doivent être déclarés comme \[ [**in**](/windows/desktop/Midl/in) \] , \[ [**out**](/windows/desktop/Midl/out-idl) \] ou \[ **in**, **out** \] .</span><span class="sxs-lookup"><span data-stu-id="38bb6-121">All parameters in the remote procedure declarations must be declared as \[[**in**](/windows/desktop/Midl/in)\], \[[**out**](/windows/desktop/Midl/out-idl)\], or \[**in**, **out**\].</span></span> <span data-ttu-id="38bb6-122">Ces déclarations spécifient que le programme client transmet les données dans une procédure distante, récupère les données d’une procédure distante, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="38bb6-122">These declarations specify that the client program passes data into a remote procedure, gets data out of a remote procedure, or both.</span></span> <span data-ttu-id="38bb6-123">Pour plus d’informations sur les déclarations de paramètres d’interface, consultez [le corps de l’interface IDL](the-idl-interface-body.md).</span><span class="sxs-lookup"><span data-stu-id="38bb6-123">For more detailed information about interface parameter declarations, see [The IDL Interface Body](the-idl-interface-body.md).</span></span>

## <a name="compiling-a-midl-file"></a><span data-ttu-id="38bb6-124">Compilation d’un fichier MIDL</span><span class="sxs-lookup"><span data-stu-id="38bb6-124">Compiling a MIDL File</span></span>

<span data-ttu-id="38bb6-125">Le compilateur MIDL est un outil en ligne de commande qui est automatiquement installé avec le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="38bb6-125">The MIDL compiler is a command-line tool that is automatically installed with the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="38bb6-126">Appelez-le dans une fenêtre de commande en tapant la commande **MIDL**, suivie du nom d’un fichier MIDL, sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="38bb6-126">Invoke it in a command window by typing the command **midl**, followed by the name of a MIDL file, at the command line.</span></span> <span data-ttu-id="38bb6-127">Assurez-vous que le répertoire contenant le compilateur MIDL se trouve dans votre chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="38bb6-127">Make sure that the directory containing the MIDL compiler is in your path.</span></span> <span data-ttu-id="38bb6-128">L’exemple suivant illustre son utilisation :</span><span class="sxs-lookup"><span data-stu-id="38bb6-128">The following example illustrates its use:</span></span>

<span data-ttu-id="38bb6-129">**MyApp. idl MIDL**</span><span class="sxs-lookup"><span data-stu-id="38bb6-129">**midl MyApp.idl**</span></span>

<span data-ttu-id="38bb6-130">Notez que vous n’avez pas besoin d’inclure l’extension si le nom de fichier a l’extension. idl.</span><span class="sxs-lookup"><span data-stu-id="38bb6-130">Note that you do not have to include the extension if the file name has the .idl extension.</span></span> <span data-ttu-id="38bb6-131">Vous pouvez également utiliser les [commutateurs de ligne de commande](/windows/desktop/Midl/midl-command-line-reference) du compilateur MIDL en les insérant entre la commande **MIDL** et le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="38bb6-131">You can also use the MIDL compiler [command-line switches](/windows/desktop/Midl/midl-command-line-reference) by inserting them between the **midl** command and the file name.</span></span> <span data-ttu-id="38bb6-132">Cela est illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="38bb6-132">This is demonstrated in the following example:</span></span>

<span data-ttu-id="38bb6-133">**MIDL/ACF MyApp. ACF MyApp. idl**</span><span class="sxs-lookup"><span data-stu-id="38bb6-133">**midl /acf MyApp.acf MyApp.idl**</span></span>

<span data-ttu-id="38bb6-134">Dans cet exemple, le compilateur MIDL est exécuté à l’aide du fichier MyApp. idl comme fichier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="38bb6-134">In this example, the MIDL compiler is executed using the file MyApp.idl as the input file.</span></span> <span data-ttu-id="38bb6-135">Le commutateur de ligne de commande **/ACF** indique au compilateur d’utiliser également un fichier de configuration d’application (ACF) pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="38bb6-135">The command line switch **/acf** instructs the compiler to use an application configuration file (ACF) for input as well.</span></span> <span data-ttu-id="38bb6-136">Les fichiers de configuration de l’application sont décrits plus en détail dans [les fichiers IDL et ACF](the-idl-and-acf-files.md).</span><span class="sxs-lookup"><span data-stu-id="38bb6-136">Application configuration files are discussed more thoroughly in [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

<span data-ttu-id="38bb6-137">Pour plus d’informations sur l’utilisation du compilateur MIDL, consultez le [Microsoft Interface Definition Language (MIDL)](/windows/desktop/Midl/midl-start-page), qui contient des informations sur les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="38bb6-137">For more detailed information on using the MIDL compiler, see the [Microsoft Interface Definition Language (MIDL)](/windows/desktop/Midl/midl-start-page), which contains information on the following topics:</span></span>

-   [<span data-ttu-id="38bb6-138">C-Configuration requise pour le préprocesseur pour MIDL</span><span class="sxs-lookup"><span data-stu-id="38bb6-138">C-Preprocessor Requirements for MIDL</span></span>](/windows/desktop/Midl/c-preprocessor-requirements-for-midl)
-   [<span data-ttu-id="38bb6-139">C/C++-considérations relatives au compilateur</span><span class="sxs-lookup"><span data-stu-id="38bb6-139">C/C++-Compiler Considerations</span></span>](/windows/desktop/Midl/c-c-compiler-considerations)
-   [<span data-ttu-id="38bb6-140">Fichiers générés pour une interface RPC</span><span class="sxs-lookup"><span data-stu-id="38bb6-140">Files Generated for an RPC Interface</span></span>](/windows/desktop/Midl/files-generated-for-an-rpc-interface)
-   [<span data-ttu-id="38bb6-141">Informations de référence sur la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="38bb6-141">MIDL Command-line Reference</span></span>](/windows/desktop/Midl/midl-command-line-reference)
-   [<span data-ttu-id="38bb6-142">Référence du langage MIDL</span><span class="sxs-lookup"><span data-stu-id="38bb6-142">MIDL Language Reference</span></span>](/windows/desktop/Midl/midl-language-reference)
-   [<span data-ttu-id="38bb6-143">Erreurs et avertissements du compilateur MIDL</span><span class="sxs-lookup"><span data-stu-id="38bb6-143">MIDL Compiler Errors and Warnings</span></span>](/windows/desktop/Midl/midl-compiler-errors-and-warnings)

 

 