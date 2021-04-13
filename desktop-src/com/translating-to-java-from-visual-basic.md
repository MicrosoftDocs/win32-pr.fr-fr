---
title: Conversion en Java à partir de Visual Basic
description: Conversion en Java à partir de Visual Basic
ms.assetid: 2bd61efc-f4f4-46f7-aa5a-f6cefc54d86b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84d02071641901c5217069d997c22fa04c94cef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379654"
---
# <a name="translating-to-java-from-visual-basic"></a><span data-ttu-id="d9748-103">Conversion en Java à partir de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d9748-103">Translating to Java from Visual Basic</span></span>

<span data-ttu-id="d9748-104">Par défaut, Visual Basic transmet les paramètres par référence.</span><span class="sxs-lookup"><span data-stu-id="d9748-104">By default, Visual Basic passes parameters by reference.</span></span> <span data-ttu-id="d9748-105">Les paramètres qui sont destinés à être passés par valeur uniquement sont spécifiés par le mot clé **ByVal**.</span><span class="sxs-lookup"><span data-stu-id="d9748-105">Parameters that are meant to be passed by value only are specified by the keyword **ByVal**.</span></span>

<span data-ttu-id="d9748-106">Java ne prend pas en charge les tableaux multidimensionnels.</span><span class="sxs-lookup"><span data-stu-id="d9748-106">Java does not support multidimensional arrays.</span></span> <span data-ttu-id="d9748-107">Les méthodes qui acceptent ou retournent des tableaux multidimensionnels ne sont pas disponibles à partir de Java.</span><span class="sxs-lookup"><span data-stu-id="d9748-107">Methods that accept or return multidimensional arrays are not available from Java.</span></span>

<span data-ttu-id="d9748-108">Java et Visual Basic diffèrent légèrement selon la façon dont ils représentent des propriétés.</span><span class="sxs-lookup"><span data-stu-id="d9748-108">Java and Visual Basic differ slightly in how they represent properties.</span></span> <span data-ttu-id="d9748-109">En Java, les propriétés sont représentées sous la forme d’un ensemble de fonctions d’accesseur, une qui définit la valeur de la propriété et une qui récupère la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="d9748-109">In Java, properties are represented as a set of accessor functions, one that sets the property value and one that retrieves the property value.</span></span> <span data-ttu-id="d9748-110">Dans Visual Basic, les propriétés sont représentées sous la forme d’un seul élément qui peut être utilisé pour récupérer ou définir la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="d9748-110">In Visual Basic, properties are represented as a single item that can be used to retrieve or set the property value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9748-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d9748-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9748-112">Conversion en Java</span><span class="sxs-lookup"><span data-stu-id="d9748-112">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




