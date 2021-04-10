---
title: commutateur/h
description: L’option/h est fonctionnellement équivalente à l’option/Header.
ms.assetid: 1b74d5f2-6624-4b71-832d-fb55a0e84c86
keywords:
- /h Switch MIDL
topic_type:
- apiref
api_name:
- /h
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ff2cd7aa5e4b8386e0c9faecfaccd860207403
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030333"
---
# <a name="h-switch"></a><span data-ttu-id="5ad1b-104">commutateur/h</span><span class="sxs-lookup"><span data-stu-id="5ad1b-104">/h switch</span></span>

<span data-ttu-id="5ad1b-105">L’option **/h** est fonctionnellement équivalente à l’option [**/header**](-header.md) .</span><span class="sxs-lookup"><span data-stu-id="5ad1b-105">The **/h** option is functionally equivalent to the [**/header**](-header.md) option.</span></span>

``` syntax
midl /h filename
```

## <a name="switch-options"></a><span data-ttu-id="5ad1b-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="5ad1b-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="5ad1b-107">*extension*</span><span class="sxs-lookup"><span data-stu-id="5ad1b-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="5ad1b-108">Spécifie un nom de fichier d’en-tête qui remplace le nom du fichier d’en-tête par défaut.</span><span class="sxs-lookup"><span data-stu-id="5ad1b-108">Specifies a header file name that overrides the default header file name.</span></span> <span data-ttu-id="5ad1b-109">Les noms de fichiers peuvent être mis en guillemets explicitement à l’aide de guillemets doubles (") pour empêcher l’interpréteur de commandes d’interpréter des caractères spéciaux.</span><span class="sxs-lookup"><span data-stu-id="5ad1b-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ad1b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="5ad1b-110">Remarks</span></span>

<span data-ttu-id="5ad1b-111">Le commutateur **/h** spécifie *filename* comme nom pour un fichier d’en-tête qui contient toutes les définitions contenues dans le fichier IDL, sans la syntaxe IDL.</span><span class="sxs-lookup"><span data-stu-id="5ad1b-111">The **/h** switch specifies *filename* as the name for a header file that contains all the definitions contained in the IDL file, without the IDL syntax.</span></span> <span data-ttu-id="5ad1b-112">Ce fichier peut être utilisé en tant que fichier d’en-tête C ou C++.</span><span class="sxs-lookup"><span data-stu-id="5ad1b-112">This file can be used as a C or C++ header file.</span></span>

## <a name="examples"></a><span data-ttu-id="5ad1b-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="5ad1b-113">Examples</span></span>

<span data-ttu-id="5ad1b-114">**MIDL/h tlibhead. h nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="5ad1b-114">**midl /h tlibhead.h filename.idl**</span></span>

<span data-ttu-id="5ad1b-115">**MIDL/h « MIDL. h » NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="5ad1b-115">**midl /h "midl.h" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="5ad1b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ad1b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ad1b-117">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="5ad1b-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="5ad1b-118">**/Header**</span><span class="sxs-lookup"><span data-stu-id="5ad1b-118">**/header**</span></span>](-header.md)
</dt> </dl>

 

 




