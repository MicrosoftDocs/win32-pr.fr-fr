---
title: commutateur/cstub
description: Le commutateur/cstub spécifie le nom du fichier stub client pour une interface RPC.
ms.assetid: f2c9e083-3511-4e72-b1d1-14a3a662ffaf
keywords:
- MIDL du commutateur/cstub
topic_type:
- apiref
api_name:
- /cstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 878f6eee47deaac3887c3f9936c18b0185cc807a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312958"
---
# <a name="cstub-switch"></a><span data-ttu-id="d6df9-104">commutateur/cstub</span><span class="sxs-lookup"><span data-stu-id="d6df9-104">/cstub switch</span></span>

<span data-ttu-id="d6df9-105">Le commutateur **/cstub** spécifie le nom du fichier stub client pour une interface RPC.</span><span class="sxs-lookup"><span data-stu-id="d6df9-105">The **/cstub** switch specifies the name of the client stub file for an RPC interface.</span></span>

``` syntax
midl /cstub stub_file_name
```

## <a name="switch-options"></a><span data-ttu-id="d6df9-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="d6df9-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="d6df9-107">*\_nom du fichier stub \_*</span><span class="sxs-lookup"><span data-stu-id="d6df9-107">*stub\_file\_name*</span></span> 
</dt> <dd>

<span data-ttu-id="d6df9-108">Spécifie un nom de fichier qui remplace le nom du fichier stub client par défaut.</span><span class="sxs-lookup"><span data-stu-id="d6df9-108">Specifies a file name that overrides the default client stub file name.</span></span> <span data-ttu-id="d6df9-109">Les noms de fichiers peuvent être mis en guillemets explicitement à l’aide de guillemets doubles (") pour empêcher l’interpréteur de commandes d’interpréter les caractères spéciaux.</span><span class="sxs-lookup"><span data-stu-id="d6df9-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6df9-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d6df9-110">Remarks</span></span>

<span data-ttu-id="d6df9-111">Le nom de fichier spécifié remplace le nom de fichier par défaut.</span><span class="sxs-lookup"><span data-stu-id="d6df9-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="d6df9-112">Par défaut, le nom de fichier est obtenu en ajoutant l’extension \_ c. c au nom du fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="d6df9-112">By default, the file name is obtained by adding the extension \_c.c to the name of the IDL file.</span></span> <span data-ttu-id="d6df9-113">Ce commutateur n’affecte pas les interfaces OLE.</span><span class="sxs-lookup"><span data-stu-id="d6df9-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="d6df9-114">Lorsque vous importez des fichiers, le nom de fichier spécifié s’applique à un seul fichier stub : le fichier stub qui correspond au fichier IDL spécifié sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="d6df9-114">When you are importing files, the specified file name applies to only one stub file — the stub file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="d6df9-115">Si *le \_ \_ nom du fichier stub* n’inclut pas de chemin d’accès explicite, le fichier est écrit dans le répertoire actif ou dans le répertoire spécifié par le commutateur [**/out**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="d6df9-115">If *stub\_file\_name* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="d6df9-116">Un chemin d’accès explicite dans le *\_ \_ nom du fichier stub* remplace la spécification du commutateur **/out** .</span><span class="sxs-lookup"><span data-stu-id="d6df9-116">An explicit path in *stub\_file\_name* overrides the **/out** switch specification.</span></span>

<span data-ttu-id="d6df9-117">Le commutateur **/client** None est prioritaire sur le commutateur **/cstub** .</span><span class="sxs-lookup"><span data-stu-id="d6df9-117">The **/client** none switch takes precedence over the **/cstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="d6df9-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="d6df9-118">Examples</span></span>

<span data-ttu-id="d6df9-119">**MIDL/cstub My \_ cstub. c nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="d6df9-119">**midl /cstub my\_cstub.c filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="d6df9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6df9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6df9-121">**/Header**</span><span class="sxs-lookup"><span data-stu-id="d6df9-121">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="d6df9-122">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="d6df9-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="d6df9-123">**/out**</span><span class="sxs-lookup"><span data-stu-id="d6df9-123">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="d6df9-124">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="d6df9-124">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




