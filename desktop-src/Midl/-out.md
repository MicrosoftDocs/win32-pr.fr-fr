---
title: /out (commutateur)
description: Le commutateur/out spécifie le répertoire par défaut dans lequel le compilateur MIDL écrit les fichiers de sortie.
ms.assetid: 37cfe989-137a-4336-8c66-e6b9c23473df
keywords:
- MIDL du commutateur/out
topic_type:
- apiref
api_name:
- /out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d688f17957170c6f3a8887030ea2c67140c0ff8c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106543613"
---
# <a name="out-switch"></a><span data-ttu-id="0b164-104">/out (commutateur)</span><span class="sxs-lookup"><span data-stu-id="0b164-104">/out switch</span></span>

<span data-ttu-id="0b164-105">Le commutateur **/out** spécifie le répertoire par défaut dans lequel le compilateur MIDL écrit les fichiers de sortie.</span><span class="sxs-lookup"><span data-stu-id="0b164-105">The **/out** switch specifies the default directory where the MIDL compiler writes output files.</span></span>

``` syntax
midl /out path-specification
```

## <a name="switch-options"></a><span data-ttu-id="0b164-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="0b164-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="0b164-107">*Path-Specification*</span><span class="sxs-lookup"><span data-stu-id="0b164-107">*path-specification*</span></span> 
</dt> <dd>

<span data-ttu-id="0b164-108">Spécifie le chemin d’accès au répertoire dans lequel le stub, l’en-tête et les fichiers de commutateur sont générés.</span><span class="sxs-lookup"><span data-stu-id="0b164-108">Specifies the path to the directory in which the stub, header, and switch files are generated.</span></span> <span data-ttu-id="0b164-109">Une spécification de lecteur, un chemin d’accès absolu au répertoire ou les deux peuvent être spécifiés.</span><span class="sxs-lookup"><span data-stu-id="0b164-109">A drive specification, an absolute directory path, or both can be specified.</span></span> <span data-ttu-id="0b164-110">Les chemins d’accès peuvent être explicitement placés entre guillemets doubles (") pour empêcher l’interpréteur de commandes d’interpréter les caractères spéciaux.</span><span class="sxs-lookup"><span data-stu-id="0b164-110">Paths can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b164-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0b164-111">Remarks</span></span>

<span data-ttu-id="0b164-112">Le répertoire de sortie peut être spécifié avec une lettre de lecteur, un nom de chemin d’accès absolu, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="0b164-112">The output directory can be specified with a drive letter, an absolute path name, or both.</span></span> <span data-ttu-id="0b164-113">L’option **/out** peut être utilisée avec n’importe quel commutateur qui active la spécification de fichier de sortie individuelle.</span><span class="sxs-lookup"><span data-stu-id="0b164-113">The **/out** option can be used with any of the switches that enable individual output file specification.</span></span>

<span data-ttu-id="0b164-114">Lorsque le commutateur **/out** n’est pas spécifié, les fichiers sont écrits dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="0b164-114">When the **/out** switch is not specified, files are written to the current directory.</span></span>

<span data-ttu-id="0b164-115">Le répertoire par défaut spécifié par le commutateur **/out** peut être substitué par un nom de chemin d’accès explicite spécifié dans le cadre du commutateur [**/cstub**](-cstub.md), [**/header**](-header.md), [**/proxy**](-proxy.md)ou [**/sstub**](-sstub.md) .</span><span class="sxs-lookup"><span data-stu-id="0b164-115">The default directory specified by the **/out** switch can be overridden by an explicit path name specified as part of the [**/cstub**](-cstub.md), [**/header**](-header.md), [**/proxy**](-proxy.md), or [**/sstub**](-sstub.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="0b164-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="0b164-116">Examples</span></span>

<span data-ttu-id="0b164-117">**MIDL/out c : \\ mydir \\ mysubdir \\ SubDir2 plus profond nom de fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="0b164-117">**midl /out c:\\mydir\\mysubdir\\subdir2 deeper filename.idl**</span></span>

<span data-ttu-id="0b164-118">**MIDL/out c : nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="0b164-118">**midl /out c: filename.idl**</span></span>

<span data-ttu-id="0b164-119">**MIDL/out \\ mydir \\ mysubdir \\ un autre nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="0b164-119">**midl /out \\mydir\\mysubdir\\another filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="0b164-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b164-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b164-121">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="0b164-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="0b164-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="0b164-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="0b164-123">**/Header**</span><span class="sxs-lookup"><span data-stu-id="0b164-123">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="0b164-124">**/proxy**</span><span class="sxs-lookup"><span data-stu-id="0b164-124">**/proxy**</span></span>](-proxy.md)
</dt> <dt>

[<span data-ttu-id="0b164-125">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="0b164-125">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




