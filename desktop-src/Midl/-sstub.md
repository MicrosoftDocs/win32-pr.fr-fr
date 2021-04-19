---
title: commutateur/sstub
description: Le commutateur/sstub spécifie le nom du fichier stub serveur pour une interface RPC.
ms.assetid: 8e695e81-7c1b-40c0-aeaa-5390512fa099
keywords:
- MIDL du commutateur/sstub
topic_type:
- apiref
api_name:
- /sstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 131be3dd1890967f7107bea64c3dc2634833653d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106513502"
---
# <a name="sstub-switch"></a><span data-ttu-id="f85b4-104">commutateur/sstub</span><span class="sxs-lookup"><span data-stu-id="f85b4-104">/sstub switch</span></span>

<span data-ttu-id="f85b4-105">Le commutateur **/sstub** spécifie le nom du fichier stub serveur pour une interface RPC.</span><span class="sxs-lookup"><span data-stu-id="f85b4-105">The **/sstub** switch specifies the name of the server stub file for an RPC interface.</span></span>

``` syntax
midl /sstub stub_file_name
```

## <a name="switch-options"></a><span data-ttu-id="f85b4-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="f85b4-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="f85b4-107">*\_nom du fichier stub \_*</span><span class="sxs-lookup"><span data-stu-id="f85b4-107">*stub\_file\_name*</span></span> 
</dt> <dd>

<span data-ttu-id="f85b4-108">Spécifie un nom de fichier qui remplace le nom du fichier stub du serveur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f85b4-108">Specifies a file name that overrides the default server stub file name.</span></span> <span data-ttu-id="f85b4-109">Les noms de fichiers peuvent être mis en guillemets explicitement à l’aide de guillemets doubles (") pour empêcher l’interpréteur de commandes d’interpréter les caractères spéciaux.</span><span class="sxs-lookup"><span data-stu-id="f85b4-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f85b4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f85b4-110">Remarks</span></span>

<span data-ttu-id="f85b4-111">Le nom de fichier spécifié remplace le nom de fichier par défaut.</span><span class="sxs-lookup"><span data-stu-id="f85b4-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="f85b4-112">Par défaut, le nom de fichier est obtenu en ajoutant \_ S. C au nom du fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="f85b4-112">By default, the file name is obtained by adding \_S.C to the name of the IDL file.</span></span> <span data-ttu-id="f85b4-113">Ce commutateur n’affecte pas les interfaces OLE.</span><span class="sxs-lookup"><span data-stu-id="f85b4-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="f85b4-114">Lorsque vous importez des fichiers, le nom de fichier spécifié s’applique à un seul fichier stub : le fichier stub qui correspond au fichier IDL spécifié sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="f85b4-114">When you are importing files, the specified file name applies to only one stub file — the stub file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="f85b4-115">Si *le \_ \_ nom du fichier stub* n’inclut pas de chemin d’accès explicite, le fichier est écrit dans le répertoire actif ou dans le répertoire spécifié par le commutateur [**/out**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="f85b4-115">If *stub\_file\_name* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="f85b4-116">Un chemin d’accès explicite dans le *\_ \_ nom du fichier stub* remplace la spécification du commutateur **/out** .</span><span class="sxs-lookup"><span data-stu-id="f85b4-116">An explicit path in *stub\_file\_name* overrides the **/out** switch specification.</span></span>

<span data-ttu-id="f85b4-117">Le commutateur **/Server** None est prioritaire par rapport au commutateur **/sstub**</span><span class="sxs-lookup"><span data-stu-id="f85b4-117">The **/server** none switch takes precedence over the **/sstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="f85b4-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="f85b4-118">Examples</span></span>

<span data-ttu-id="f85b4-119">**MIDL/sstub My \_ sstub. c nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="f85b4-119">**midl /sstub my\_sstub.c filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="f85b4-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f85b4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f85b4-121">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="f85b4-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="f85b4-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="f85b4-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="f85b4-123">**/Header**</span><span class="sxs-lookup"><span data-stu-id="f85b4-123">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="f85b4-124">**/out**</span><span class="sxs-lookup"><span data-stu-id="f85b4-124">**/out**</span></span>](-out.md)
</dt> </dl>

 

 




