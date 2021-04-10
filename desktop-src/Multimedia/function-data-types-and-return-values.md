---
title: Types de données de fonction et valeurs de retour
description: Types de données de fonction et valeurs de retour
ms.assetid: a17ec8bb-4369-463f-8c67-11457a18595b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28bd7484c3d968e92da5fcd19ee738da1ee811a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939884"
---
# <a name="function-data-types-and-return-values"></a><span data-ttu-id="3c7b1-103">Types de données de fonction et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="3c7b1-103">Function Data Types and Return Values</span></span>

<span data-ttu-id="3c7b1-104">Les fonctions et macros AVIFile utilisent des gestionnaires de fichiers et de flux implémentés avec la technologie OLE.</span><span class="sxs-lookup"><span data-stu-id="3c7b1-104">The AVIFile functions and macros use file and stream handlers implemented with OLE technology.</span></span> <span data-ttu-id="3c7b1-105">Le type de données standard d’une fonction OLE est **STDAPI**, et la fonction retourne une valeur **HRESULT** (zéro en cas de réussite ou une erreur).</span><span class="sxs-lookup"><span data-stu-id="3c7b1-105">The standard data type of an OLE function is **STDAPI**, and the function returns an **HRESULT** value (zero for success or an error otherwise).</span></span> <span data-ttu-id="3c7b1-106">Si une fonction retourne une valeur autre qu’un **HRESULT**, le type du prototype de la fonction a une syntaxe légèrement différente qui incorpore le type de valeur de retour entre parenthèses à la suite de « STDAPI \_ ».</span><span class="sxs-lookup"><span data-stu-id="3c7b1-106">If a function returns a value other than an **HRESULT**, the type of the function's prototype has a slightly different syntax that embeds the return value type in parentheses following "STDAPI\_".</span></span> <span data-ttu-id="3c7b1-107">Par exemple, une fonction qui retourne une valeur de données de **type long** utilise **STDAPI \_ (long)** dans l’instruction prototype.</span><span class="sxs-lookup"><span data-stu-id="3c7b1-107">For example, a function that returns a **LONG** data value uses **STDAPI\_(LONG)** in the prototype statement.</span></span>

 

 




