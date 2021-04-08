---
title: commutateur/no_def_idir
description: Lorsque les répertoires sont spécifiés avec le commutateur/I, le \_ commutateur/non Def \_ idir demande au compilateur MIDL de rechercher uniquement les répertoires spécifiés à l’aide du commutateur/i.
ms.assetid: 9a396de4-332d-4832-8e8b-291690cd3a10
keywords:
- /commutateur no_def_idir MIDL
topic_type:
- apiref
api_name:
- /no_def_idir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62ed845c73c36fbbfe4ea7dea952ee4541b043a7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841469"
---
# <a name="no_def_idir-switch"></a><span data-ttu-id="87961-104">\_commutateur/non Def \_ idir</span><span class="sxs-lookup"><span data-stu-id="87961-104">/no\_def\_idir switch</span></span>

<span data-ttu-id="87961-105">Lorsque les répertoires sont spécifiés avec le commutateur [**/i**](-i.md) , le commutateur **/non \_ Def \_ idir** demande au compilateur MIDL de rechercher uniquement les répertoires spécifiés à l’aide du commutateur **/i** , en ignorant le répertoire actif, ainsi que les répertoires spécifiés par la variable d’environnement include.</span><span class="sxs-lookup"><span data-stu-id="87961-105">When directories are specified with the [**/I**](-i.md) switch, the **/no\_def\_idir** switch instructs the MIDL compiler to search only the directories specified with the **/I** switch, ignoring the current directory as well as the directories specified by the INCLUDE environment variable.</span></span>

``` syntax
midl /no_def_idir
```

## <a name="switch-options"></a><span data-ttu-id="87961-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="87961-106">Switch Options</span></span>

<span data-ttu-id="87961-107">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="87961-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="87961-108">Notes</span><span class="sxs-lookup"><span data-stu-id="87961-108">Remarks</span></span>

<span data-ttu-id="87961-109">Quand aucun répertoire n’est spécifié avec le commutateur [**/i**](-i.md) , le commutateur **/non \_ Def \_ idir** demande au compilateur MIDL de rechercher uniquement le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="87961-109">When no directories are specified with the [**/I**](-i.md) switch, the **/no\_def\_idir** switch instructs the MIDL compiler to search only the current directory.</span></span>

## <a name="examples"></a><span data-ttu-id="87961-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="87961-110">Examples</span></span>

``` syntax
; search only the current directory 
midl /no_def_idir filename.idl  

; search only the specified directories 
midl /no_def_idir /I c:\c700\include filename.idl 
```

## <a name="see-also"></a><span data-ttu-id="87961-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87961-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87961-112">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="87961-112">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="87961-113">**/acf**</span><span class="sxs-lookup"><span data-stu-id="87961-113">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="87961-114">**/I**</span><span class="sxs-lookup"><span data-stu-id="87961-114">**/I**</span></span>](-i.md)
</dt> </dl>

 

 




