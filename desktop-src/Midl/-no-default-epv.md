---
title: commutateur/no_default_epv
description: Le \_ commutateur EPV par défaut de/non \_ indique au compilateur MIDL qu’il ne doit pas générer de vecteur de point d’entrée par défaut (EPV). L’utilisation de cet attribut n’est pas recommandée.
ms.assetid: 160b5fd3-cd9c-4f51-8c35-6cddab120021
keywords:
- /commutateur no_default_epv MIDL
topic_type:
- apiref
api_name:
- /no_default_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a6e39319c5f03c1cd41959a009307b07bef66f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940879"
---
# <a name="no_default_epv-switch"></a><span data-ttu-id="233e4-105">\_ \_ commutateur EPV par défaut</span><span class="sxs-lookup"><span data-stu-id="233e4-105">/no\_default\_epv switch</span></span>

<span data-ttu-id="233e4-106">Le **commutateur \_ \_ EPV par défaut de/non** indique au compilateur MIDL qu’il ne doit pas générer de vecteur de point d’entrée par défaut (EPV).</span><span class="sxs-lookup"><span data-stu-id="233e4-106">The **/no\_default\_epv** switch directs the MIDL compiler not to generate a default entry-point vector (epv).</span></span> <span data-ttu-id="233e4-107">L’utilisation de cet attribut n’est pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="233e4-107">The use of this attribute is not recommended.</span></span>

``` syntax
midl /no_default_epv
```

## <a name="switch-options"></a><span data-ttu-id="233e4-108">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="233e4-108">Switch Options</span></span>

<span data-ttu-id="233e4-109">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="233e4-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="233e4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="233e4-110">Remarks</span></span>

<span data-ttu-id="233e4-111">Dans ce cas, l’application doit inscrire un EPV avec l’appel [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) .</span><span class="sxs-lookup"><span data-stu-id="233e4-111">In this case, the application must register an epv with the [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) call.</span></span> <span data-ttu-id="233e4-112">Comparez ce commutateur avec le commutateur [**/Utilisez \_ EPV**](-use-epv.md) .</span><span class="sxs-lookup"><span data-stu-id="233e4-112">Compare this switch with the [**/use\_epv**](-use-epv.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="233e4-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="233e4-113">Examples</span></span>

<span data-ttu-id="233e4-114">**MIDL/non \_ par défaut \_ EPV nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="233e4-114">**midl /no\_default\_epv filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="233e4-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="233e4-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="233e4-116">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="233e4-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="233e4-117">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="233e4-117">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="233e4-118">**/Utilisez \_ EPV**</span><span class="sxs-lookup"><span data-stu-id="233e4-118">**/use\_epv**</span></span>](-use-epv.md)
</dt> <dt>

[<span data-ttu-id="233e4-119">**RpcServerRegisterIf**</span><span class="sxs-lookup"><span data-stu-id="233e4-119">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 