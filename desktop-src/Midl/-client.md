---
title: commutateur/client
description: Le commutateur/client indique au compilateur MIDL de générer des fichiers sources C côté client pour une interface RPC.
ms.assetid: bce5af72-2201-4b42-9348-cb97f08b7fdf
keywords:
- MIDL du commutateur/client
topic_type:
- apiref
api_name:
- /client
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf7e17e1893b918d926cd94a93eb8b1c372ee75
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312961"
---
# <a name="client-switch"></a><span data-ttu-id="1baf4-104">commutateur/client</span><span class="sxs-lookup"><span data-stu-id="1baf4-104">/client switch</span></span>

<span data-ttu-id="1baf4-105">Le commutateur **/client** indique au compilateur MIDL de générer des fichiers sources C côté client pour une interface RPC.</span><span class="sxs-lookup"><span data-stu-id="1baf4-105">The **/client** switch directs the MIDL compiler to generate client-side C source files for an RPC interface.</span></span>

``` syntax
midl /client { stub | none }
```

## <a name="switch-options"></a><span data-ttu-id="1baf4-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="1baf4-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span data-ttu-id="1baf4-107"><span id="stub"></span><span id="STUB"></span>stub \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1baf4-107"><span id="stub"></span><span id="STUB"></span>\*\*\*\*stub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1baf4-108">Génère les fichiers côté client.</span><span class="sxs-lookup"><span data-stu-id="1baf4-108">Generates the client-side files.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="1baf4-109"><span id="none"></span><span id="NONE"></span>aucun \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="1baf4-109"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="1baf4-110">Ne génère pas de fichiers côté client.</span><span class="sxs-lookup"><span data-stu-id="1baf4-110">Does not generate any client-side files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1baf4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1baf4-111">Remarks</span></span>

<span data-ttu-id="1baf4-112">Lorsque le commutateur **/client** n’est pas spécifié, le compilateur MIDL génère le fichier stub client.</span><span class="sxs-lookup"><span data-stu-id="1baf4-112">When the **/client** switch is not specified, the MIDL compiler generates the client stub file.</span></span> <span data-ttu-id="1baf4-113">Ce commutateur n’affecte pas les interfaces OLE.</span><span class="sxs-lookup"><span data-stu-id="1baf4-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="1baf4-114">Le commutateur **/client** est prioritaire sur le commutateur [**/cstub**](-cstub.md) .</span><span class="sxs-lookup"><span data-stu-id="1baf4-114">The **/client** switch takes precedence over the [**/cstub**](-cstub.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="1baf4-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="1baf4-115">Examples</span></span>

<span data-ttu-id="1baf4-116">**MIDL/client None nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="1baf4-116">**midl /client none filename.idl**</span></span>

<span data-ttu-id="1baf4-117">**MIDL/client stub nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="1baf4-117">**midl /client stub filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="1baf4-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1baf4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1baf4-119">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="1baf4-119">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="1baf4-120">**/Server**</span><span class="sxs-lookup"><span data-stu-id="1baf4-120">**/server**</span></span>](-server.md)
</dt> <dt>

[<span data-ttu-id="1baf4-121">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="1baf4-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




