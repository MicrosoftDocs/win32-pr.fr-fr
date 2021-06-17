---
description: 'Vous avez deux possibilités lors de la compilation d’un fichier MOF : à l’aide de l’utilitaire de ligne de commande ou à l’aide d’une interface de programmation.'
ms.assetid: 1760f1bd-7027-4201-97a2-ca902f945b52
ms.tgt_platform: multiple
title: Exécution du compilateur MOF sur un fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f62834944e995c3e7f3763c460d72f9f70aa66
ms.sourcegitcommit: 7eadd92b1da5eb4eab7d516a5a768e7f7fc02d4c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/16/2021
ms.locfileid: "112230238"
---
# <a name="running-the-mof-compiler-on-a-file"></a><span data-ttu-id="d2ab2-103">Exécution du compilateur MOF sur un fichier</span><span class="sxs-lookup"><span data-stu-id="d2ab2-103">Running the MOF Compiler on a File</span></span>

<span data-ttu-id="d2ab2-104">Vous avez deux possibilités lors de la compilation d’un fichier MOF : à l’aide de l’utilitaire de ligne de commande ou à l’aide d’une interface de programmation.</span><span class="sxs-lookup"><span data-stu-id="d2ab2-104">You have two choices when compiling a MOF file: using the command-line utility or using a programmatic interface.</span></span>

<span data-ttu-id="d2ab2-105">Tant que vous n’avez pas exécuté le compilateur MOF, [**Mofcomp.exe**](mofcomp.md), un fournisseur n’est pas inscrit auprès de WMI et les classes qu’il a créées dans le fichier MOF ne sont pas disponibles dans l' [*espace de stockage WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="d2ab2-105">Until you run the MOF compiler, [**Mofcomp.exe**](mofcomp.md), a provider is not registered with WMI and the classes it created in the MOF file are not available in the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="d2ab2-106">La procédure suivante décrit comment compiler un fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="d2ab2-106">The following procedure describes how to compile a MOF file.</span></span>

<span data-ttu-id="d2ab2-107">**Pour exécuter le compilateur MOF sur un fichier à partir de la ligne de commande**</span><span class="sxs-lookup"><span data-stu-id="d2ab2-107">**To run the MOF compiler on a file from the command line**</span></span>

1.  <span data-ttu-id="d2ab2-108">Appelez le compilateur MOF à partir de la ligne de commande, en utilisant la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="d2ab2-108">Call the MOF compiler from the command line, using the following syntax.</span></span>

    <span data-ttu-id="d2ab2-109">**mofcomp** _MOFfile_**. mof**</span><span class="sxs-lookup"><span data-stu-id="d2ab2-109">**mofcomp** _MOFfile_**.mof**</span></span>

    <span data-ttu-id="d2ab2-110">Le compilateur MOF prend en charge différents commutateurs pour contrôler les situations de traitement spéciales.</span><span class="sxs-lookup"><span data-stu-id="d2ab2-110">The MOF compiler supports a variety of switches to control special processing situations.</span></span> <span data-ttu-id="d2ab2-111">Tous les commutateurs sont facultatifs, et toute combinaison de commutateurs est autorisée.</span><span class="sxs-lookup"><span data-stu-id="d2ab2-111">All of the switches are optional, and any combination of switches is allowed.</span></span> <span data-ttu-id="d2ab2-112">Toutefois, il n’est pas judicieux d’utiliser certains commutateurs en combinaison avec d’autres.</span><span class="sxs-lookup"><span data-stu-id="d2ab2-112">However, it does not make sense to use some of the switches in combination with others.</span></span> <span data-ttu-id="d2ab2-113">Par exemple, pour combiner les commutateurs **-Class : updateonly** et **-Class : CreateOnly** , le compilateur n’effectue aucune action.</span><span class="sxs-lookup"><span data-stu-id="d2ab2-113">For example, to combine the **-class:updateonly** and **-class:createonly** switches results in the compiler not performing any action.</span></span>

    <span data-ttu-id="d2ab2-114">Par défaut, Mofcomp.exe stocke les classes compilées dans l' \\ espace de noms WMI par défaut racine.</span><span class="sxs-lookup"><span data-stu-id="d2ab2-114">By default, Mofcomp.exe stores the compiled classes in the root\\default WMI namespace.</span></span> <span data-ttu-id="d2ab2-115">Notez que l’espace de noms par défaut pour Mofcomp.exe n’est pas le même que l’espace de noms par défaut pour les scripts.</span><span class="sxs-lookup"><span data-stu-id="d2ab2-115">Note that the default namespace for Mofcomp.exe is not the same as the default namespace for scripting.</span></span> <span data-ttu-id="d2ab2-116">L’espace de noms par défaut pour les scripts est spécifié dans le contrôle WMI sous l’onglet Avancé. Pour plus d’informations, consultez [définition de la sécurité de l’espace de noms avec le contrôle WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="d2ab2-116">The default namespace for scripting is specified in the WMI Control on the Advanced tab. For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>

    <span data-ttu-id="d2ab2-117">Vous pouvez modifier l’espace de noms qui reçoit les classes de deux manières.</span><span class="sxs-lookup"><span data-stu-id="d2ab2-117">You can change the namespace that receives the classes in two ways.</span></span>

    1.  <span data-ttu-id="d2ab2-118">Utilisez le commutateur **-N** pour la commande **mofcomp** .</span><span class="sxs-lookup"><span data-stu-id="d2ab2-118">Use the **-N** switch for the **mofcomp** command.</span></span>
    2.  <span data-ttu-id="d2ab2-119">Insérez l' \# [**espace de noms du pragma**](pragma-namespace.md) de commande du préprocesseur dans le fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="d2ab2-119">Insert the preprocessor command \#[**pragma namespace**](pragma-namespace.md) in the MOF file.</span></span>

2.  <span data-ttu-id="d2ab2-120">Si vous le souhaitez, vous pouvez compiler un fichier MOF par programme.</span><span class="sxs-lookup"><span data-stu-id="d2ab2-120">Optionally, you can compile a MOF file programmatically.</span></span> <span data-ttu-id="d2ab2-121">Pour plus d’informations, consultez [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).</span><span class="sxs-lookup"><span data-stu-id="d2ab2-121">For more information, see [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2ab2-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d2ab2-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2ab2-123">Compilation des fichiers MOF</span><span class="sxs-lookup"><span data-stu-id="d2ab2-123">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="d2ab2-124">**mofcomp**</span><span class="sxs-lookup"><span data-stu-id="d2ab2-124">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="d2ab2-125">Commandes de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="d2ab2-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



