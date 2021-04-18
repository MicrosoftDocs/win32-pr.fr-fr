---
title: Conversion en VBScript à partir de JavaScript
description: Conversion en VBScript à partir de JavaScript
ms.assetid: f302e032-4e94-42f1-839b-022dab538760
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eda8169a665dc93133f7ac933de12ecc612f3e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509185"
---
# <a name="translating-to-vbscript-from-javascript"></a><span data-ttu-id="cf7fe-103">Conversion en VBScript à partir de JavaScript</span><span class="sxs-lookup"><span data-stu-id="cf7fe-103">Translating to VBScript from JavaScript</span></span>

<span data-ttu-id="cf7fe-104">En JavaScript, il existe plusieurs types de données, tels que des nombres, des chaînes, des valeurs booléennes, des objets et l’attribut null.</span><span class="sxs-lookup"><span data-stu-id="cf7fe-104">In JavaScript, there are several data types, such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="cf7fe-105">VBScript utilise uniquement un type de données **Variant**, qui peut être sous-typé pour représenter des chaînes, des nombres, des valeurs booléennes, etc.</span><span class="sxs-lookup"><span data-stu-id="cf7fe-105">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="cf7fe-106">En JavaScript, les tableaux peuvent être étendus dynamiquement en définissant une nouvelle valeur pour la propriété Length du tableau.</span><span class="sxs-lookup"><span data-stu-id="cf7fe-106">In JavaScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="cf7fe-107">Dans VBScript, les tableaux ne peuvent pas être agrandis ; elles doivent être redimensionnées à l’aide de l’instruction **ReDim** .</span><span class="sxs-lookup"><span data-stu-id="cf7fe-107">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="cf7fe-108">Les fonctions de prise en charge de VBScript et JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cf7fe-108">Both VBScript and JavaScript support functions.</span></span> <span data-ttu-id="cf7fe-109">VBScript, toutefois, prend également en charge les sous-routines.</span><span class="sxs-lookup"><span data-stu-id="cf7fe-109">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="cf7fe-110">Les sous-routines sont similaires aux fonctions, sauf qu’elles ne retournent pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="cf7fe-110">Subroutines are similar to functions, except they do not return a value.</span></span>

<span data-ttu-id="cf7fe-111">JavaScript respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="cf7fe-111">JavaScript is case-sensitive.</span></span> <span data-ttu-id="cf7fe-112">VBScript n’est pas.</span><span class="sxs-lookup"><span data-stu-id="cf7fe-112">VBScript is not.</span></span>

<span data-ttu-id="cf7fe-113">JavaScript est pris en charge par un large éventail de navigateurs Web, y compris Internet Explorer et Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="cf7fe-113">JavaScript is supported by a wide variety of Web browsers, including both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="cf7fe-114">Netscape Navigator ne prend pas en charge VBScript.</span><span class="sxs-lookup"><span data-stu-id="cf7fe-114">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="cf7fe-115">VBScript prend en charge la gestion des erreurs via son objet Err.</span><span class="sxs-lookup"><span data-stu-id="cf7fe-115">VBScript supports error handling through its Err object.</span></span> <span data-ttu-id="cf7fe-116">JavaScript ne fournit pas actuellement de méthode de recouvrement et de gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="cf7fe-116">JavaScript does not currently provide a means of trapping and handling errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf7fe-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cf7fe-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf7fe-118">Conversion en VBScript</span><span class="sxs-lookup"><span data-stu-id="cf7fe-118">Translating to VBScript</span></span>](translating-to-vbscript.md)
</dt> </dl>

 

 




