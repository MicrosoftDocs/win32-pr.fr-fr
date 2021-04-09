---
title: commutateur/RPCSS
description: Le commutateur/RPCSS, lorsqu’il est spécifié, agit comme si l' \_ attribut Enable Allocate était spécifié pour toutes les opérations de l’interface. L’utilisation de cet attribut n’est pas recommandée.
ms.assetid: a4507779-7d07-4517-8592-39f0d9460bc3
keywords:
- MIDL du commutateur/RPCSS
topic_type:
- apiref
api_name:
- /rpcss
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dabdd6340005c4e56080dc91bdd372a858e0e7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030086"
---
# <a name="rpcss-switch"></a><span data-ttu-id="04353-105">commutateur/RPCSS</span><span class="sxs-lookup"><span data-stu-id="04353-105">/rpcss switch</span></span>

<span data-ttu-id="04353-106">Le commutateur **/RPCSS** , lorsqu’il est spécifié, agit comme si l’attribut [**Enable \_ allocate**](enable-allocate.md) était spécifié pour toutes les opérations de l’interface.</span><span class="sxs-lookup"><span data-stu-id="04353-106">The **/rpcss** switch, when specified, acts as though the [**enable\_allocate**](enable-allocate.md) attribute was specified on all operations of the interface.</span></span> <span data-ttu-id="04353-107">L’utilisation de cet attribut n’est pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="04353-107">The usage of this attribute is not recommended.</span></span>

``` syntax
midl /rpcss
```

## <a name="switch-options"></a><span data-ttu-id="04353-108">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="04353-108">Switch Options</span></span>

<span data-ttu-id="04353-109">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="04353-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="04353-110">Notes</span><span class="sxs-lookup"><span data-stu-id="04353-110">Remarks</span></span>

<span data-ttu-id="04353-111">En mode par défaut, le package RpcSs est activé uniquement si la procédure ou l’interface a l’attribut [**Enable \_ allocate**](enable-allocate.md) ou si le commutateur **/RPCSS** est spécifié sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="04353-111">In default mode, the RpcSs package is enabled only if either the procedure or interface has the [**enable\_allocate**](enable-allocate.md) attribute or the **/rpcss** switch is specified on the command line.</span></span> <span data-ttu-id="04353-112">En mode **/OSF** , le stub côté serveur Active le package d’allocation rpcss.</span><span class="sxs-lookup"><span data-stu-id="04353-112">In **/osf** mode, the server-side stub enables the RpcSs allocation package.</span></span>

## <a name="examples"></a><span data-ttu-id="04353-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="04353-113">Examples</span></span>

<span data-ttu-id="04353-114">**MIDL/RPCSS NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="04353-114">**midl /rpcss filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="04353-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04353-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04353-116">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="04353-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="04353-117">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="04353-117">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="04353-118">**activer l' \_ allocation**</span><span class="sxs-lookup"><span data-stu-id="04353-118">**enable\_allocate**</span></span>](enable-allocate.md)
</dt> <dt>

[<span data-ttu-id="04353-119">**/osf**</span><span class="sxs-lookup"><span data-stu-id="04353-119">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 




