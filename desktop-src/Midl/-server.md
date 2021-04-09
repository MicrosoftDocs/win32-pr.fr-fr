---
title: commutateur/Server
description: Le commutateur/Server indique au compilateur MIDL de générer des fichiers sources C côté serveur pour une interface RPC.
ms.assetid: c5ca6a47-e8b0-4a13-ba73-2d35a9ac8240
keywords:
- MIDL du commutateur/Server
topic_type:
- apiref
api_name:
- /server
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31449133fa795a90d1f11d8c06b960b74909548d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030254"
---
# <a name="server-switch"></a><span data-ttu-id="8f09e-104">commutateur/Server</span><span class="sxs-lookup"><span data-stu-id="8f09e-104">/server switch</span></span>

<span data-ttu-id="8f09e-105">Le commutateur **/Server** indique au compilateur MIDL de générer des fichiers sources C côté serveur pour une interface RPC.</span><span class="sxs-lookup"><span data-stu-id="8f09e-105">The **/server** switch directs the MIDL compiler to generate server-side C source files for an RPC interface.</span></span>

``` syntax
midl /server { stub | none }
```

## <a name="switch-options"></a><span data-ttu-id="8f09e-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="8f09e-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span data-ttu-id="8f09e-107"><span id="stub"></span><span id="STUB"></span>stub \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="8f09e-107"><span id="stub"></span><span id="STUB"></span>\*\*\*\*stub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="8f09e-108">Génère les fichiers côté serveur.</span><span class="sxs-lookup"><span data-stu-id="8f09e-108">Generates the server-side files.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="8f09e-109"><span id="none"></span><span id="NONE"></span>aucun \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="8f09e-109"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="8f09e-110">Ne génère pas de fichiers côté serveur.</span><span class="sxs-lookup"><span data-stu-id="8f09e-110">Does not generate server-side files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f09e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8f09e-111">Remarks</span></span>

<span data-ttu-id="8f09e-112">Lorsque le commutateur **/Server** n’est pas spécifié, le compilateur MIDL génère le fichier stub serveur.</span><span class="sxs-lookup"><span data-stu-id="8f09e-112">When the **/server** switch is not specified, the MIDL compiler generates the server stub file.</span></span> <span data-ttu-id="8f09e-113">Ce commutateur n’affecte pas les interfaces OLE.</span><span class="sxs-lookup"><span data-stu-id="8f09e-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="8f09e-114">L’option **None** n’entraîne pas la génération de fichiers.</span><span class="sxs-lookup"><span data-stu-id="8f09e-114">The **none** option causes no files to be generated.</span></span>

<span data-ttu-id="8f09e-115">Le commutateur **/Server** est prioritaire par rapport au commutateur **/sstub**</span><span class="sxs-lookup"><span data-stu-id="8f09e-115">The **/server** switch takes precedence over the **/sstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="8f09e-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="8f09e-116">Examples</span></span>

<span data-ttu-id="8f09e-117">**MIDL/Server aucun**</span><span class="sxs-lookup"><span data-stu-id="8f09e-117">**midl /server none**</span></span>

<span data-ttu-id="8f09e-118">**stub/Server MIDL**</span><span class="sxs-lookup"><span data-stu-id="8f09e-118">**midl /server stub**</span></span>

## <a name="see-also"></a><span data-ttu-id="8f09e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f09e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f09e-120">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="8f09e-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="8f09e-121">**/client**</span><span class="sxs-lookup"><span data-stu-id="8f09e-121">**/client**</span></span>](-client.md)
</dt> <dt>

[<span data-ttu-id="8f09e-122">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="8f09e-122">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




