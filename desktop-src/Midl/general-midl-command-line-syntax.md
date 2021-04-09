---
title: Syntaxe générale de la ligne de commande MIDL
description: Le compilateur MIDL traite un fichier IDL et un fichier de configuration d’application facultatif (ACF) pour générer un jeu de fichiers de sortie.
ms.assetid: 1906b374-d0d1-4ec8-9a00-c5228b4c29ca
keywords:
- Référence de ligne de commande MIDL, syntaxe générale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14baa145c7be03467a24bd4298cf2f502d93b6ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840729"
---
# <a name="general-midl-command-line-syntax"></a><span data-ttu-id="17a82-104">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="17a82-104">General MIDL Command-line Syntax</span></span>

<span data-ttu-id="17a82-105">Le compilateur MIDL traite un fichier IDL et un fichier de configuration d’application facultatif (ACF) pour générer un jeu de fichiers de sortie.</span><span class="sxs-lookup"><span data-stu-id="17a82-105">The MIDL compiler processes an IDL file and an optional application configuration file (ACF) to generate a set of output files.</span></span> <span data-ttu-id="17a82-106">Les attributs spécifiés dans la liste d’attributs d’interface du fichier IDL déterminent si le compilateur génère des fichiers sources pour une interface RPC ou pour une interface OLE personnalisée.</span><span class="sxs-lookup"><span data-stu-id="17a82-106">The attributes specified in the IDL file's interface attribute list determine whether the compiler generates source files for an RPC interface or for a custom OLE interface.</span></span>

## <a name="switch-options"></a><span data-ttu-id="17a82-107">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="17a82-107">Switch Options</span></span>

``` syntax
     midl [command-line-switch [switch-options]] filename
    
```

<dl> <dt>

<span data-ttu-id="17a82-108"><span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*commutateur de ligne de commande*</span><span class="sxs-lookup"><span data-stu-id="17a82-108"><span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*command-line-switch*</span></span>
</dt> <dd>

<span data-ttu-id="17a82-109">Spécifie les commutateurs de ligne de commande du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="17a82-109">Specifies MIDL compiler command-line switches.</span></span> <span data-ttu-id="17a82-110">Les commutateurs peuvent apparaître dans n’importe quelle séquence.</span><span class="sxs-lookup"><span data-stu-id="17a82-110">Switches can appear in any sequence.</span></span>

</dd> <dt>

<span data-ttu-id="17a82-111"><span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*options du commutateur*</span><span class="sxs-lookup"><span data-stu-id="17a82-111"><span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*switch-options*</span></span>
</dt> <dd>

<span data-ttu-id="17a82-112">Spécifie les options associées à chaque commutateur.</span><span class="sxs-lookup"><span data-stu-id="17a82-112">Specifies options associated with each switch.</span></span> <span data-ttu-id="17a82-113">Les options valides sont décrites dans l’entrée de référence pour chaque commutateur du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="17a82-113">Valid options are described in the reference entry for each MIDL compiler switch.</span></span>

</dd> <dt>

<span data-ttu-id="17a82-114"><span id="filename"></span><span id="FILENAME"></span>*extension*</span><span class="sxs-lookup"><span data-stu-id="17a82-114"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="17a82-115">Spécifie le nom du fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="17a82-115">Specifies the name of the IDL file.</span></span> <span data-ttu-id="17a82-116">Ce fichier a généralement l’extension. idl, mais il peut en avoir un autre ou aucun.</span><span class="sxs-lookup"><span data-stu-id="17a82-116">This file usually has the extension .idl, but it can have another or none.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17a82-117">Notes</span><span class="sxs-lookup"><span data-stu-id="17a82-117">Remarks</span></span>

<span data-ttu-id="17a82-118">Les listes suivantes affichent les noms par défaut des fichiers générés pour un fichier IDL nommé Name. idl.</span><span class="sxs-lookup"><span data-stu-id="17a82-118">The following lists show the default names of the files generated for an IDL file named Name.idl.</span></span> <span data-ttu-id="17a82-119">Vous pouvez utiliser des commutateurs de ligne de commande pour remplacer ces noms par défaut.</span><span class="sxs-lookup"><span data-stu-id="17a82-119">You can use command-line switches to override these default names.</span></span> <span data-ttu-id="17a82-120">Notez que le nom du fichier IDL peut avoir une extension autre que. idl ou aucune extension.</span><span class="sxs-lookup"><span data-stu-id="17a82-120">Note that the name of the IDL file can have an extension other than .idl, or no extension at all.</span></span>

<span data-ttu-id="17a82-121">Par défaut (autrement dit, si la liste d’attributs d’interface ne contient pas l' [**objet**](object.md) ou l’attribut [**local**](local.md) ), le compilateur génère les fichiers suivants pour une [interface RPC](files-generated-for-an-rpc-interface.md):</span><span class="sxs-lookup"><span data-stu-id="17a82-121">By default (that is, if the interface attribute list does not contain the [**object**](object.md) or [**local**](local.md) attribute), the compiler generates the following files for an [RPC interface](files-generated-for-an-rpc-interface.md):</span></span>

-   <span data-ttu-id="17a82-122">Stub client (nom \_ c. c)</span><span class="sxs-lookup"><span data-stu-id="17a82-122">Client stub (name\_c.c)</span></span>
-   <span data-ttu-id="17a82-123">Serveur stub (nom \_ s. c)</span><span class="sxs-lookup"><span data-stu-id="17a82-123">Server stub (name\_s.c)</span></span>
-   <span data-ttu-id="17a82-124">Fichier d’en-tête (Name. h)</span><span class="sxs-lookup"><span data-stu-id="17a82-124">Header file (name.h)</span></span>

<span data-ttu-id="17a82-125">Lorsque l’attribut d' [**objet**](object.md) apparaît dans la liste attribut d’interface, le compilateur génère les fichiers suivants pour une interface com :</span><span class="sxs-lookup"><span data-stu-id="17a82-125">When the [**object**](object.md) attribute appears in the interface attribute list, the compiler generates the following files for a COM interface:</span></span>

-   <span data-ttu-id="17a82-126">Fichier de proxy d’interface (nom \_ p. c)</span><span class="sxs-lookup"><span data-stu-id="17a82-126">Interface proxy file (name\_p.c)</span></span>
-   <span data-ttu-id="17a82-127">Fichier d’en-tête d’interface (Name. h)</span><span class="sxs-lookup"><span data-stu-id="17a82-127">Interface header file (name.h)</span></span>
-   <span data-ttu-id="17a82-128">Fichier UUID de l’interface (nom \_ I. c)</span><span class="sxs-lookup"><span data-stu-id="17a82-128">Interface UUID file (name\_I.c)</span></span>

<span data-ttu-id="17a82-129">Lorsque l’attribut [**local**](local.md) apparaît dans la liste d’attributs de l’interface, le compilateur génère uniquement le fichier d’en-tête d’interface, Name. h.</span><span class="sxs-lookup"><span data-stu-id="17a82-129">When the [**local**](local.md) attribute appears in the interface attribute list, the compiler generates only the interface header file, Name.h.</span></span>

<span data-ttu-id="17a82-130">Le compilateur MIDL fourni avec Microsoft RPC appelle le préprocesseur C en fonction des besoins pour traiter le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="17a82-130">The MIDL compiler provided with Microsoft RPC invokes the C preprocessor as needed to process the IDL file.</span></span> <span data-ttu-id="17a82-131">Il n’appelle pas automatiquement le compilateur C pour compiler les fichiers générés.</span><span class="sxs-lookup"><span data-stu-id="17a82-131">It does not automatically invoke the C compiler to compile generated files.</span></span>

> [!Note]  
> <span data-ttu-id="17a82-132">Le compilateur MIDL fourni avec Microsoft RPC utilise une syntaxe de ligne de commande différente de celle du compilateur IDL DCE.</span><span class="sxs-lookup"><span data-stu-id="17a82-132">The MIDL compiler provided with Microsoft RPC uses a different command-line syntax than the DCE IDL compiler.</span></span>

 

<span data-ttu-id="17a82-133">Le compilateur MIDL bascule [**/env**](-env.md), [**/Server**](-server.md), [**/sstub**](-sstub.md)et [**/out**](-out.md) sur le fichier stub du serveur.</span><span class="sxs-lookup"><span data-stu-id="17a82-133">The MIDL compiler switches [**/env**](-env.md), [**/server**](-server.md), [**/sstub**](-sstub.md), and [**/out**](-out.md) affect the server stub file.</span></span>

<span data-ttu-id="17a82-134">À compter de la version 6.0.359 de MIDL, l’option de ligne de commande par défaut pour le compilateur MIDL est [**/Oicf**](-oi.md)Â  [**/Robust**](-robust.md).</span><span class="sxs-lookup"><span data-stu-id="17a82-134">Starting with MIDL version 6.0.359, the default command line option for the MIDL compiler is [**/Oicf**](-oi.md)Â  [**/robust**](-robust.md).</span></span> <span data-ttu-id="17a82-135">Pour désactiver/Robust, spécifiez l’option [**/non \_ robustesse**](-no-robust.md) .</span><span class="sxs-lookup"><span data-stu-id="17a82-135">To disable /robust, specify the [**/no\_robust**](-no-robust.md) option.</span></span>

## <a name="the-header-file"></a><span data-ttu-id="17a82-136">Fichier d’en-tête</span><span class="sxs-lookup"><span data-stu-id="17a82-136">The Header File</span></span>

<span data-ttu-id="17a82-137">Le fichier d’en-tête contient les définitions de tous les types de données et opérations déclarés dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="17a82-137">The header file contains definitions of all the data types and operations declared in the IDL file.</span></span> <span data-ttu-id="17a82-138">Le fichier d’en-tête doit être inclus par tous les modules d’application qui appellent les opérations définies, implémentent les opérations définies ou manipulent les types définis.</span><span class="sxs-lookup"><span data-stu-id="17a82-138">The header file must be included by all application modules that call the defined operations, implement the defined operations, or manipulate the defined types.</span></span>

<span data-ttu-id="17a82-139">Le compilateur MIDL bascule [**/header**](-header.md) et [**/out**](-out.md) sur le fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="17a82-139">The MIDL compiler switches [**/header**](-header.md) and [**/out**](-out.md) affect the header file.</span></span>

 

 




