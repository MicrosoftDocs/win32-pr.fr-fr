---
title: commutateur/IID
description: Le commutateur/IID spécifie le nom du fichier d’identificateur d’interface pour une interface COM, en remplaçant le nom par défaut obtenu en ajoutant \_ i. c au nom de fichier IDL.
ms.assetid: 051593f5-e612-4b19-94e5-d7885dbede21
keywords:
- MIDL du commutateur/IID
topic_type:
- apiref
api_name:
- /iid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631a28f1bc5a1a24253c9416104df9941cd8da33
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380888"
---
# <a name="iid-switch"></a><span data-ttu-id="2365c-104">commutateur/IID</span><span class="sxs-lookup"><span data-stu-id="2365c-104">/iid switch</span></span>

<span data-ttu-id="2365c-105">Le commutateur **/IID** spécifie le nom du fichier d’identificateur d’interface pour une interface com, en remplaçant le nom par défaut obtenu en ajoutant \_ i. c au nom de fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="2365c-105">The **/iid** switch specifies the name of the interface identifier file for a COM interface, overriding the default name obtained by adding \_i.c to the IDL file name.</span></span>

``` syntax
midl /iid filename
```

## <a name="switch-options"></a><span data-ttu-id="2365c-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="2365c-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="2365c-107">*extension*</span><span class="sxs-lookup"><span data-stu-id="2365c-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="2365c-108">Spécifie un nom de fichier d’identificateur d’interface qui remplace le nom de fichier de l’identificateur d’interface par défaut pour une interface COM.</span><span class="sxs-lookup"><span data-stu-id="2365c-108">Specifies an interface identifier file name that overrides the default interface identifier file name for a COM interface.</span></span> <span data-ttu-id="2365c-109">Les noms de fichiers peuvent être mis en guillemets explicitement à l’aide de guillemets doubles (") pour empêcher l’interpréteur de commandes d’interpréter les caractères spéciaux.</span><span class="sxs-lookup"><span data-stu-id="2365c-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2365c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="2365c-110">Remarks</span></span>

<span data-ttu-id="2365c-111">Le commutateur **/IID** n’affecte pas les interfaces RPC.</span><span class="sxs-lookup"><span data-stu-id="2365c-111">The **/iid** switch does not affect RPC interfaces.</span></span>

<span data-ttu-id="2365c-112">Si *filename* n’inclut pas de chemin d’accès explicite, le fichier est écrit dans le répertoire actif ou dans le répertoire spécifié par le commutateur [**/out**](-out.md) .</span><span class="sxs-lookup"><span data-stu-id="2365c-112">If *filename* does not include an explicit path, the file is written to the current directory or to the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="2365c-113">Un chemin d’accès explicite dans *filename* remplace la spécification du commutateur **/out** .</span><span class="sxs-lookup"><span data-stu-id="2365c-113">An explicit path in *filename* overrides the **/out** switch specification.</span></span>

## <a name="examples"></a><span data-ttu-id="2365c-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="2365c-114">Examples</span></span>

<span data-ttu-id="2365c-115">**MIDL/IID "My \_ IID. c" nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="2365c-115">**midl /iid "my\_iid.c" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="2365c-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2365c-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2365c-117">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="2365c-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="2365c-118">**/Header**</span><span class="sxs-lookup"><span data-stu-id="2365c-118">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="2365c-119">**/out**</span><span class="sxs-lookup"><span data-stu-id="2365c-119">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="2365c-120">**/proxy**</span><span class="sxs-lookup"><span data-stu-id="2365c-120">**/proxy**</span></span>](-proxy.md)
</dt> </dl>

 

 




