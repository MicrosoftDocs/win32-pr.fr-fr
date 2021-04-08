---
title: commutateur/dlldata
description: Le commutateur/dlldata est utilisé pour spécifier le nom de fichier du fichier dlldata généré pour une DLL de proxy. Le nom de fichier par défaut dlldata. c est utilisé si le commutateur/dlldata n’est pas spécifié.
ms.assetid: 5211498b-c641-447f-9514-a98766e26ea9
keywords:
- MIDL du commutateur/dlldata
topic_type:
- apiref
api_name:
- /dlldata
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e9c1d7f27c56f81905081fd9ef24c8c490391b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678661"
---
# <a name="dlldata-switch"></a><span data-ttu-id="bb668-105">commutateur/dlldata</span><span class="sxs-lookup"><span data-stu-id="bb668-105">/dlldata switch</span></span>

<span data-ttu-id="bb668-106">Le commutateur **/dlldata** est utilisé pour spécifier le nom de fichier du fichier dlldata généré pour une dll de proxy.</span><span class="sxs-lookup"><span data-stu-id="bb668-106">The **/dlldata** switch is used to specify the file name for the generated dlldata file for a proxy DLL.</span></span> <span data-ttu-id="bb668-107">Le nom de fichier par défaut dlldata. c est utilisé si le commutateur **/dlldata** n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="bb668-107">The default file name Dlldata.c is used if the **/dlldata** switch is not specified.</span></span>

``` syntax
midl /dlldata file-name
```

## <a name="switch-options"></a><span data-ttu-id="bb668-108">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="bb668-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="bb668-109">*nom de fichier*</span><span class="sxs-lookup"><span data-stu-id="bb668-109">*file-name*</span></span> 
</dt> <dd>

<span data-ttu-id="bb668-110">Nom du fichier source C que le compilateur MIDL génère pour la DLL du proxy.</span><span class="sxs-lookup"><span data-stu-id="bb668-110">The name of the C source file the MIDL compiler will generate for the proxy DLL.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb668-111">Notes</span><span class="sxs-lookup"><span data-stu-id="bb668-111">Remarks</span></span>

<span data-ttu-id="bb668-112">Le fichier spécifié par le *nom de fichier* doit être lié à la dll du proxy.</span><span class="sxs-lookup"><span data-stu-id="bb668-112">The file specified by *file-name* must be linked to the proxy DLL.</span></span> <span data-ttu-id="bb668-113">Le fichier dlldata contient des points d’entrée et des structures de données requis par la fabrique de classe pour la DLL du proxy.</span><span class="sxs-lookup"><span data-stu-id="bb668-113">The dlldata file contains entry points and data structures required by the class factory for the proxy DLL.</span></span> <span data-ttu-id="bb668-114">Ces structures de données spécifient les interfaces d’objet contenues dans la DLL du proxy.</span><span class="sxs-lookup"><span data-stu-id="bb668-114">These data structures specify the object interfaces contained in the proxy DLL.</span></span> <span data-ttu-id="bb668-115">Le fichier dlldata spécifie également l’identificateur de classe de la fabrique de classe pour la DLL du proxy.</span><span class="sxs-lookup"><span data-stu-id="bb668-115">The dlldata file also specifies the class identifier of the class factory for the proxy DLL.</span></span> <span data-ttu-id="bb668-116">Il s’agit toujours de l’UUID (IID) de la première interface du premier fichier proxy (par ordre alphabétique).</span><span class="sxs-lookup"><span data-stu-id="bb668-116">This is always the UUID (IID) of the first interface of the first proxy file (by alphabetical order).</span></span>

<span data-ttu-id="bb668-117">Le même fichier dlldata doit être spécifié lors de l’appel de MIDL sur tous les fichiers IDL qui seront placés dans une DLL proxy particulière.</span><span class="sxs-lookup"><span data-stu-id="bb668-117">The same dlldata file should be specified when invoking MIDL on all the IDL files that will go into a particular proxy DLL.</span></span> <span data-ttu-id="bb668-118">Le fichier dlldata est créé ou mis à jour lors de chaque compilation MIDL, générant de façon incrémentielle une liste des interfaces qui seront insérées dans la DLL du proxy.</span><span class="sxs-lookup"><span data-stu-id="bb668-118">The dlldata file is created or updated during each MIDL compilation, incrementally building a list of the interfaces that will go into the proxy DLL.</span></span>

## <a name="examples"></a><span data-ttu-id="bb668-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="bb668-119">Examples</span></span>

<span data-ttu-id="bb668-120">**MIDL/dlldata données. c**</span><span class="sxs-lookup"><span data-stu-id="bb668-120">**midl /dlldata data.c**</span></span>

## <a name="see-also"></a><span data-ttu-id="bb668-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb668-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb668-122">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="bb668-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




