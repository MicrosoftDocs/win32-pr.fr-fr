---
title: commutateur/use_epv
description: Le \_ commutateur/utilisez EPV indique au compilateur MIDL de générer le code stub du serveur qui appelle la routine de l’application serveur via un vecteur de point d’entrée (EPV), plutôt que par un appel statique. L’utilisation de cet attribut n’est pas recommandée.
ms.assetid: 2853d836-ded3-412a-916b-1143968123a2
keywords:
- /commutateur use_epv MIDL
topic_type:
- apiref
api_name:
- /use_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec73b5cb9833c15a77c96a784e1ded88d266f9a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106512094"
---
# <a name="use_epv-switch"></a><span data-ttu-id="bd55a-105">\_commutateur/utilisez EPV</span><span class="sxs-lookup"><span data-stu-id="bd55a-105">/use\_epv switch</span></span>

<span data-ttu-id="bd55a-106">Le commutateur **/Utilisez \_ EPV** indique au compilateur MIDL de générer le code stub du serveur qui appelle la routine de l’application serveur via un vecteur de point d’entrée (EPV), plutôt que par un appel statique.</span><span class="sxs-lookup"><span data-stu-id="bd55a-106">The **/use\_epv** switch directs the MIDL compiler to generate server stub code that calls the server application routine through an entry-point vector (epv), rather than by a static call.</span></span> <span data-ttu-id="bd55a-107">L’utilisation de cet attribut n’est pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="bd55a-107">The use of this attribute is not recommended.</span></span>

``` syntax
midl /use_epv
```

## <a name="switch-options"></a><span data-ttu-id="bd55a-108">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="bd55a-108">Switch Options</span></span>

<span data-ttu-id="bd55a-109">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="bd55a-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd55a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="bd55a-110">Remarks</span></span>

<span data-ttu-id="bd55a-111">En règle générale, les applications requièrent une liaison statique à la routine d’application serveur.</span><span class="sxs-lookup"><span data-stu-id="bd55a-111">Typically, applications require static linkage to the server application routine.</span></span> <span data-ttu-id="bd55a-112">Le compilateur MIDL génère ce type d’appel par défaut.</span><span class="sxs-lookup"><span data-stu-id="bd55a-112">The MIDL compiler generates such a call by default.</span></span> <span data-ttu-id="bd55a-113">Toutefois, si une application requiert que le stub serveur appelle la routine d’application serveur à l’aide de EPV, le commutateur **/Utilisez \_ EPV** doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="bd55a-113">However, if an application requires the server stub to call the server application routine by using the epv, the **/use\_epv** switch must be specified.</span></span> <span data-ttu-id="bd55a-114">Quand le commutateur **/Utilisez \_ EPV** est spécifié, le compilateur MIDL génère un EPV par défaut.</span><span class="sxs-lookup"><span data-stu-id="bd55a-114">When the **/use\_epv** switch is specified, the MIDL compiler generates a default epv.</span></span> <span data-ttu-id="bd55a-115">Ce EPV par défaut est ensuite utilisé si l’application n’enregistre pas un autre EPV via l’appel [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) .</span><span class="sxs-lookup"><span data-stu-id="bd55a-115">This default epv is then used if the application does not register another epv through the [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) call.</span></span>

## <a name="examples"></a><span data-ttu-id="bd55a-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="bd55a-116">Examples</span></span>

<span data-ttu-id="bd55a-117">**MIDL/utilisez \_ EPV** *nom de fichier \* \* *. idl**</span><span class="sxs-lookup"><span data-stu-id="bd55a-117">**midl /use\_epv** *filename\*\*\*.idl*\*</span></span>

## <a name="see-also"></a><span data-ttu-id="bd55a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd55a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd55a-119">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="bd55a-119">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="bd55a-120">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="bd55a-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="bd55a-121">**/non \_ par défaut \_ EPV**</span><span class="sxs-lookup"><span data-stu-id="bd55a-121">**/no\_default\_epv**</span></span>](-no-default-epv.md)
</dt> <dt>

[<span data-ttu-id="bd55a-122">**RpcServerRegisterIf**</span><span class="sxs-lookup"><span data-stu-id="bd55a-122">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 