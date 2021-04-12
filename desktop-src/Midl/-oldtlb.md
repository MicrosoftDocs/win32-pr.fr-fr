---
title: commutateur/oldtlb
description: Le commutateur/oldtlb indique au compilateur MIDL de générer une bibliothèque de types de format ancien.
ms.assetid: cf5fe000-7262-4812-a6ab-f12a558ac068
keywords:
- MIDL du commutateur/oldtlb
topic_type:
- apiref
api_name:
- /oldtlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a08e468d0acff16aa1df4a45fcacafeb676b00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381841"
---
# <a name="oldtlb-switch"></a><span data-ttu-id="1bb5b-104">commutateur/oldtlb</span><span class="sxs-lookup"><span data-stu-id="1bb5b-104">/oldtlb switch</span></span>

<span data-ttu-id="1bb5b-105">Le commutateur **/oldtlb** indique au compilateur MIDL de générer une bibliothèque de types de format ancien.</span><span class="sxs-lookup"><span data-stu-id="1bb5b-105">The **/oldtlb** switch directs the MIDL compiler to generate an old-format type library.</span></span>

``` syntax
midl /oldtlb
```

## <a name="switch-options"></a><span data-ttu-id="1bb5b-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="1bb5b-106">Switch Options</span></span>

<span data-ttu-id="1bb5b-107">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1bb5b-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bb5b-108">Notes</span><span class="sxs-lookup"><span data-stu-id="1bb5b-108">Remarks</span></span>

<span data-ttu-id="1bb5b-109">Le commutateur **/oldtlb** remplace la valeur par défaut et indique au compilateur MIDL de générer des bibliothèques de types anciennes, même sur les versions actuelles de Windows, à l’aide de [CreateTypeLib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) au lieu de [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2).</span><span class="sxs-lookup"><span data-stu-id="1bb5b-109">The **/oldtlb** switch overrides the default and directs the MIDL compiler to generate old-format type libraries even on current versions of Windows by using [CreateTypeLib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) instead of [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2).</span></span>

## <a name="examples"></a><span data-ttu-id="1bb5b-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="1bb5b-110">Examples</span></span>

<span data-ttu-id="1bb5b-111">**MIDL/oldtlb NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="1bb5b-111">**midl /oldtlb filename.idl**</span></span>

<span data-ttu-id="1bb5b-112">**MIDL/oldtlb myoldodl. ODL**</span><span class="sxs-lookup"><span data-stu-id="1bb5b-112">**midl /oldtlb myoldodl.odl**</span></span>

## <a name="see-also"></a><span data-ttu-id="1bb5b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bb5b-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bb5b-114">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="1bb5b-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="1bb5b-115">**/newtlb**</span><span class="sxs-lookup"><span data-stu-id="1bb5b-115">**/newtlb**</span></span>](-newtlb.md)
</dt> </dl>

 

 