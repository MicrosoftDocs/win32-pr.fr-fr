---
title: commutateur/Header
description: Le commutateur/Header spécifie le nom du fichier d’en-tête.
ms.assetid: d36cb6c9-df57-4ef4-aff3-9968ac8ac001
keywords:
- MIDL du commutateur/Header
topic_type:
- apiref
api_name:
- /header
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816310f0b584f3c30d351e0d036e1f18c2f23962
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380890"
---
# <a name="header-switch"></a><span data-ttu-id="1b810-104">commutateur/Header</span><span class="sxs-lookup"><span data-stu-id="1b810-104">/header switch</span></span>

<span data-ttu-id="1b810-105">Le commutateur **/header** spécifie le nom du fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="1b810-105">The **/header** switch specifies the name of the header file.</span></span>

``` syntax
midl /header filename
```

## <a name="switch-options"></a><span data-ttu-id="1b810-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="1b810-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="1b810-107">*extension*</span><span class="sxs-lookup"><span data-stu-id="1b810-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="1b810-108">Spécifie un nom de fichier d’en-tête qui remplace le nom du fichier d’en-tête par défaut.</span><span class="sxs-lookup"><span data-stu-id="1b810-108">Specifies a header file name that overrides the default header file name.</span></span> <span data-ttu-id="1b810-109">Les noms de fichiers peuvent être mis en guillemets explicitement à l’aide de guillemets doubles (") pour empêcher l’interpréteur de commandes d’interpréter des caractères spéciaux.</span><span class="sxs-lookup"><span data-stu-id="1b810-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b810-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1b810-110">Remarks</span></span>

<span data-ttu-id="1b810-111">Le nom de fichier spécifié remplace le nom de fichier par défaut.</span><span class="sxs-lookup"><span data-stu-id="1b810-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="1b810-112">Le nom de fichier par défaut est obtenu en remplaçant l’extension de nom de fichier IDL (généralement. idl) par l’extension de nom de fichier. h.</span><span class="sxs-lookup"><span data-stu-id="1b810-112">The default file name is obtained by replacing the IDL file name extension (usually .idl) with the file name extension .h.</span></span> <span data-ttu-id="1b810-113">Pour les interfaces OLE, le commutateur **/header** remplace le nom par défaut du fichier d’en-tête d’interface.</span><span class="sxs-lookup"><span data-stu-id="1b810-113">For OLE interfaces, the **/header** switch overrides the default name of the interface header file.</span></span>

<span data-ttu-id="1b810-114">Lorsque vous importez des fichiers, le nom de fichier spécifié s’applique à un seul fichier d’en-tête : le fichier d’en-tête qui correspond au fichier IDL spécifié sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="1b810-114">When you are importing files, the specified file name applies to only one header file — the header file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="1b810-115">Si *filename* n’inclut pas de chemin d’accès explicite, le fichier est écrit dans le répertoire actif ou dans le répertoire spécifié par le commutateur [**/out**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="1b810-115">If *filename* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="1b810-116">Un chemin d’accès explicite dans *filename* remplace la spécification du commutateur **/out** .</span><span class="sxs-lookup"><span data-stu-id="1b810-116">An explicit path in *filename* overrides the **/out** switch specification.</span></span>

## <a name="examples"></a><span data-ttu-id="1b810-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="1b810-117">Examples</span></span>

<span data-ttu-id="1b810-118">**MIDL/Header « bar. h » NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="1b810-118">**midl /header "bar.h" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="1b810-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b810-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b810-120">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="1b810-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="1b810-121">**/h**</span><span class="sxs-lookup"><span data-stu-id="1b810-121">**/h**</span></span>](-h.md)
</dt> <dt>

[<span data-ttu-id="1b810-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="1b810-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="1b810-123">**/out**</span><span class="sxs-lookup"><span data-stu-id="1b810-123">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="1b810-124">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="1b810-124">**/sstub**</span></span>](-sstub.md)
</dt> <dt>

[<span data-ttu-id="1b810-125">**/proxy**</span><span class="sxs-lookup"><span data-stu-id="1b810-125">**/proxy**</span></span>](-proxy.md)
</dt> </dl>

 

 




