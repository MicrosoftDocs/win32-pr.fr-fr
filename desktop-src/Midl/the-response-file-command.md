---
title: Commande fichier réponse
description: Un fichier réponse est un fichier texte contenant une ou plusieurs options de ligne de commande du compilateur MIDL.
ms.assetid: ad47ea1a-fe7a-4354-be2f-599ba77685ee
keywords:
- Référence de ligne de commande MIDL, commande de fichier réponse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f624f8bb4fd50fa77df604e5d56f48c9e55c89a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940212"
---
# <a name="the-response-file-command"></a><span data-ttu-id="be5ee-104">Commande fichier réponse</span><span class="sxs-lookup"><span data-stu-id="be5ee-104">The Response File Command</span></span>

<span data-ttu-id="be5ee-105">Un fichier réponse est un fichier texte contenant une ou plusieurs options de ligne de commande du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="be5ee-105">A response file is a text file containing one or more MIDL compiler command-line options.</span></span> <span data-ttu-id="be5ee-106">Contrairement à une ligne de commande, un fichier réponse autorise plusieurs lignes d’options et de noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="be5ee-106">Unlike a command line, a response file allows multiple lines of options and file names.</span></span> <span data-ttu-id="be5ee-107">Cela peut être utile en raison des limitations de votre environnement de génération ou de la commodité de votre processus de génération.</span><span class="sxs-lookup"><span data-stu-id="be5ee-107">This may be useful due to limitations of your build environment, or as a convenience for your build process.</span></span>

## <a name="switch-options"></a><span data-ttu-id="be5ee-108">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="be5ee-108">Switch Options</span></span>

``` syntax
midl @response_file
```

<dl> <dt>

<span data-ttu-id="be5ee-109"><span id="response_file"></span><span id="RESPONSE_FILE"></span>*\_fichier réponse*</span><span class="sxs-lookup"><span data-stu-id="be5ee-109"><span id="response_file"></span><span id="RESPONSE_FILE"></span>*response\_file*</span></span>
</dt> <dd>

<span data-ttu-id="be5ee-110">Spécifie le nom d’un fichier réponse.</span><span class="sxs-lookup"><span data-stu-id="be5ee-110">Specifies the name of a response file.</span></span> <span data-ttu-id="be5ee-111">Le nom du fichier réponse doit suivre immédiatement le caractère @.</span><span class="sxs-lookup"><span data-stu-id="be5ee-111">The response file name must immediately follow the @ character.</span></span> <span data-ttu-id="be5ee-112">Aucun espace blanc n’est autorisé entre le caractère @ et le nom du fichier réponse.</span><span class="sxs-lookup"><span data-stu-id="be5ee-112">No white space is allowed between the @ character and the response file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be5ee-113">Notes</span><span class="sxs-lookup"><span data-stu-id="be5ee-113">Remarks</span></span>

<span data-ttu-id="be5ee-114">Au lieu de placer toutes les options associées à un commutateur sur la ligne de commande, le compilateur MIDL accepte les fichiers réponse qui contiennent des commutateurs et des arguments.</span><span class="sxs-lookup"><span data-stu-id="be5ee-114">As an alternative to placing all options associated with a switch on the command line, the MIDL compiler accepts response files that contain switches and arguments.</span></span> <span data-ttu-id="be5ee-115">Les options d’un fichier réponse sont interprétées comme si elles étaient présentes à cet emplacement dans la ligne de commande MIDL.</span><span class="sxs-lookup"><span data-stu-id="be5ee-115">Options in a response file are interpreted as if they are present in that location in the MIDL command line.</span></span>

<span data-ttu-id="be5ee-116">Chaque argument d’un fichier réponse doit commencer et se terminer sur la même ligne.</span><span class="sxs-lookup"><span data-stu-id="be5ee-116">Each argument in a response file must begin and end on the same line.</span></span> <span data-ttu-id="be5ee-117">Caractère barre oblique inverse ( \) ne peut pas être utilisé pour concaténer des lignes.</span><span class="sxs-lookup"><span data-stu-id="be5ee-117">The backslash character (\) cannot be used to concatenate lines.</span></span> <span data-ttu-id="be5ee-118">Lorsqu’il fait partie d’une chaîne entre guillemets dans le fichier réponse, la barre oblique inverse peut uniquement être utilisée avant une autre barre oblique inverse ou avant un caractère guillemet double (").</span><span class="sxs-lookup"><span data-stu-id="be5ee-118">When it is part of a quoted string in the response file, the backslash character can only be used before another backslash or before a double quotation mark character (").</span></span> <span data-ttu-id="be5ee-119">Lorsqu’il ne fait pas partie d’une chaîne entre guillemets, la barre oblique inverse ne peut être utilisée qu’avant un guillemet double.</span><span class="sxs-lookup"><span data-stu-id="be5ee-119">When it is not part of a quoted string, the backslash character can only be used before a double quotation mark character.</span></span>

<span data-ttu-id="be5ee-120">MIDL prend en charge les arguments de ligne de commande qui incluent un ou plusieurs fichiers réponse associés à d’autres commutateurs de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="be5ee-120">MIDL supports command-line arguments that include one or more response files combined with other command-line switches.</span></span>

<span data-ttu-id="be5ee-121">Le compilateur MIDL ne prend pas en charge les fichiers réponse imbriqués.</span><span class="sxs-lookup"><span data-stu-id="be5ee-121">The MIDL compiler does not support nested response files.</span></span>

## <a name="examples"></a><span data-ttu-id="be5ee-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="be5ee-122">Examples</span></span>

<span data-ttu-id="be5ee-123">**compilateur @midl.rsp**</span><span class="sxs-lookup"><span data-stu-id="be5ee-123">**midl @midl.rsp**</span></span>

<span data-ttu-id="be5ee-124">**MIDL-Oicf @midl1.rsp -env Win32 @midl2.rsp ITF. idl**</span><span class="sxs-lookup"><span data-stu-id="be5ee-124">**midl -Oicf @midl1.rsp -env win32 @midl2.rsp itf.idl**</span></span>

## <a name="related-topics"></a><span data-ttu-id="be5ee-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be5ee-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be5ee-126">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="be5ee-126">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




