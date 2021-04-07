---
title: Erreurs et avertissements du compilateur MIDL
description: Lors de l’utilisation du compilateur MIDL, les erreurs et les avertissements peuvent être provoqués par une utilisation incorrecte des commutateurs de ligne de commande ou par le contenu des fichiers IDL et ACF.
ms.assetid: 5c8d5a28-e559-4893-932f-b2306aefa932
keywords:
- Microsoft Interface Definition Language MIDL, référence
- MIDL du compilateur MIDL, Erreurs
- MIDL du compilateur, Erreurs
- Erreurs MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae531528f83f3731b4449c7aba012f3228edd9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839077"
---
# <a name="midl-compiler-errors-and-warnings"></a><span data-ttu-id="cb3c5-107">Erreurs et avertissements du compilateur MIDL</span><span class="sxs-lookup"><span data-stu-id="cb3c5-107">MIDL Compiler Errors and Warnings</span></span>

<span data-ttu-id="cb3c5-108">Lors de l’utilisation du compilateur MIDL, les erreurs et les avertissements peuvent être provoqués par une utilisation incorrecte des commutateurs de ligne de commande ou par le contenu des fichiers IDL et ACF.</span><span class="sxs-lookup"><span data-stu-id="cb3c5-108">When using the MIDL compiler, errors and warnings can be caused by improper use of the command-line switches or by the content of the IDL and ACF files.</span></span> <span data-ttu-id="cb3c5-109">Si l’erreur est due à l’entrée incorrecte des commutateurs de ligne de commande, un message d’erreur ou d’avertissement peut spécifier le nom d’un ou plusieurs commutateurs du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="cb3c5-109">If the error is due to improperly entering the command-line switches, an error or warning message may specify the name of one or more MIDL compiler mode switches.</span></span> <span data-ttu-id="cb3c5-110">Par exemple, vous pouvez inclure certains attributs ACF dans un fichier IDL lorsque vous utilisez le commutateur/de **\_ configuration d’application** , mais ce fichier IDL génère une erreur si vous compilez sans utiliser le commutateur/**app \_ config** .</span><span class="sxs-lookup"><span data-stu-id="cb3c5-110">For example, you can include certain ACF attributes in an IDL file when you use the /**app\_config** switch, but that IDL file will generate an error if you compile without using the /**app\_config** switch.</span></span>

<span data-ttu-id="cb3c5-111">Les erreurs dans les fichiers IDL et ACF se répartissent en deux catégories : les erreurs interceptées par le préprocesseur et les erreurs reconnues par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="cb3c5-111">Errors in the IDL and ACF files fall into two categories: errors caught by the preprocessor and errors recognized by the compiler.</span></span> <span data-ttu-id="cb3c5-112">Cette section répertorie les messages d’erreur du compilateur et du préprocesseur MIDL.</span><span class="sxs-lookup"><span data-stu-id="cb3c5-112">This section lists the MIDL preprocessor and compiler error messages.</span></span> <span data-ttu-id="cb3c5-113">Il décrit également leurs formats et leurs causes.</span><span class="sxs-lookup"><span data-stu-id="cb3c5-113">It also describes their formats and causes.</span></span>

-   [<span data-ttu-id="cb3c5-114">Formats des messages d’erreur et d’avertissement</span><span class="sxs-lookup"><span data-stu-id="cb3c5-114">Error and Warning Message Formats</span></span>](error-and-warning-message-formats.md)
-   [<span data-ttu-id="cb3c5-115">Erreurs de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="cb3c5-115">Preprocessor Errors</span></span>](preprocessor-errors.md)
-   [<span data-ttu-id="cb3c5-116">Erreurs du compilateur</span><span class="sxs-lookup"><span data-stu-id="cb3c5-116">Compiler Errors</span></span>](compiler-errors.md)

 

 




