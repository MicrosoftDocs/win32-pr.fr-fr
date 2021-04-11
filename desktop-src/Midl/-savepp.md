---
title: commutateur/savePP
description: Quand la directive/savePP est spécifiée, le compilateur MIDL ne supprime pas la sortie du préprocesseur C/C++.
ms.assetid: 65a687a5-55ec-4e76-bcfc-38c0a317b85b
keywords:
- MIDL du commutateur/savePP
topic_type:
- apiref
api_name:
- /savePP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d3ab7032768cacfab6415548a09def453ab4f9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030255"
---
# <a name="savepp-switch"></a><span data-ttu-id="f8479-104">commutateur/savePP</span><span class="sxs-lookup"><span data-stu-id="f8479-104">/savePP switch</span></span>

<span data-ttu-id="f8479-105">Quand la directive **/savePP** est spécifiée, le compilateur MIDL ne supprime pas la sortie du préprocesseur C/C++.</span><span class="sxs-lookup"><span data-stu-id="f8479-105">When the **/savePP** directive is specified, the MIDL compiler does not delete the output of the C/C++ preprocessor.</span></span>

``` syntax
midl /savePP
```

## <a name="switch-options"></a><span data-ttu-id="f8479-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="f8479-106">Switch Options</span></span>

<span data-ttu-id="f8479-107">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f8479-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8479-108">Notes</span><span class="sxs-lookup"><span data-stu-id="f8479-108">Remarks</span></span>

<span data-ttu-id="f8479-109">Ce commutateur permet aux développeurs de discerner ce qui est analysé par le compilateur MIDL et est utile pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="f8479-109">This switch enables developers to discern what is being parsed by the MIDL compiler, and is useful for debugging.</span></span> <span data-ttu-id="f8479-110">La sortie du préprocesseur est écrite dans un ou plusieurs fichiers temporaires dans le répertoire indiqué par la variable d’environnement TEMP.</span><span class="sxs-lookup"><span data-stu-id="f8479-110">The output of the preprocessor is written to one or more temporary files in the directory indicated by the TEMP environment variable.</span></span> <span data-ttu-id="f8479-111">Le nom du fichier de sortie, ou fichiers, suit une convention d’affectation de noms de MID \* . tmp.</span><span class="sxs-lookup"><span data-stu-id="f8479-111">The name of the output file, or files, follows a naming convention of MID\*.tmp.</span></span> <span data-ttu-id="f8479-112">Notez qu’une seule compilation peut générer plusieurs flux d’entrée prétraités ; Cela est dû au fait que l’importation d’un fichier IDL, par opposition à l’utilisation de **\# include**, entraîne une exécution de préprocesseur distincte.</span><span class="sxs-lookup"><span data-stu-id="f8479-112">Note that a single compile may generate several preprocessed input streams; this is because importing an IDL file, as opposed to using **\#include**, causes a separate preprocessor run.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8479-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8479-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8479-114">**/CPP \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="f8479-114">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="f8479-115">**/CPP \_ opt**</span><span class="sxs-lookup"><span data-stu-id="f8479-115">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="f8479-116">/non \_ CPP,/nocpp</span><span class="sxs-lookup"><span data-stu-id="f8479-116">/no\_cpp, /nocpp</span></span>](-no-cpp-nocpp.md)
</dt> </dl>

 

 




