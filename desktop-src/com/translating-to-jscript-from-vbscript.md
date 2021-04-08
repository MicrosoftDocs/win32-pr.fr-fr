---
title: Conversion en JScript à partir de VBScript
description: Conversion en JScript à partir de VBScript
ms.assetid: cdf04a01-8bc3-4f37-872b-3a0aae962f26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18c2ccb11ffa4f5f000d8cfc73f7db6f857cf6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671554"
---
# <a name="translating-to-jscript-from-vbscript"></a><span data-ttu-id="7f6dc-103">Conversion en JScript à partir de VBScript</span><span class="sxs-lookup"><span data-stu-id="7f6dc-103">Translating to JScript from VBScript</span></span>

<span data-ttu-id="7f6dc-104">Dans VBScript **, le...** **Chaque** boucle énumère les membres d’une collection ; en JScript, le **pour**... **in** Loop énumère les membres d’un objet ou d’un tableau JScript.</span><span class="sxs-lookup"><span data-stu-id="7f6dc-104">In VBScript, the **For**...**Each** loop enumerates the members of a collection; in JScript, the **for**...**in** loop enumerates the members of a JScript object or array.</span></span> <span data-ttu-id="7f6dc-105">Pour énumérer une collection en JScript, utilisez un objet énumérateur.</span><span class="sxs-lookup"><span data-stu-id="7f6dc-105">To enumerate a collection in JScript, use an Enumerator object.</span></span>

<span data-ttu-id="7f6dc-106">En JScript, il existe plusieurs types de données, tels que des nombres, des chaînes, des valeurs booléennes, des objets et l’attribut null.</span><span class="sxs-lookup"><span data-stu-id="7f6dc-106">In JScript, there are several data types such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="7f6dc-107">VBScript utilise uniquement un type de données **Variant**, qui peut être sous-typé pour représenter des chaînes, des nombres, des valeurs booléennes, etc.</span><span class="sxs-lookup"><span data-stu-id="7f6dc-107">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="7f6dc-108">Dans JScript, les tableaux peuvent être étendus dynamiquement en définissant une nouvelle valeur pour la propriété Length du tableau.</span><span class="sxs-lookup"><span data-stu-id="7f6dc-108">In JScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="7f6dc-109">Dans VBScript, les tableaux ne peuvent pas être agrandis ; elles doivent être redimensionnées à l’aide de l’instruction **ReDim** .</span><span class="sxs-lookup"><span data-stu-id="7f6dc-109">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="7f6dc-110">Les fonctions de prise en charge de VBScript et de JScript.</span><span class="sxs-lookup"><span data-stu-id="7f6dc-110">Both VBScript and JScript support functions.</span></span> <span data-ttu-id="7f6dc-111">VBScript, toutefois, prend également en charge les sous-routines.</span><span class="sxs-lookup"><span data-stu-id="7f6dc-111">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="7f6dc-112">Les sous-routines sont similaires aux fonctions, mais ne retournent pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7f6dc-112">Subroutines are similar to functions but do not return a value.</span></span>

<span data-ttu-id="7f6dc-113">JScript respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="7f6dc-113">JScript is case-sensitive.</span></span> <span data-ttu-id="7f6dc-114">VBScript n’est pas.</span><span class="sxs-lookup"><span data-stu-id="7f6dc-114">VBScript is not.</span></span>

<span data-ttu-id="7f6dc-115">JScript est pris en charge par Internet Explorer et Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="7f6dc-115">JScript is supported by both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="7f6dc-116">Netscape Navigator ne prend pas en charge VBScript.</span><span class="sxs-lookup"><span data-stu-id="7f6dc-116">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="7f6dc-117">JScript fournit l’objet d’erreur, qui peut être utilisé pour intercepter et gérer les erreurs.</span><span class="sxs-lookup"><span data-stu-id="7f6dc-117">JScript provides the Error object, which can be used to trap and handle errors.</span></span> <span data-ttu-id="7f6dc-118">L’objet Error est analogue à l’objet Err VBScript.</span><span class="sxs-lookup"><span data-stu-id="7f6dc-118">The Error object is analogous to the VBScript Err object.</span></span>

<span data-ttu-id="7f6dc-119">Les tableaux JScript ne sont pas des tableaux du type de variable **Variant SAFEARRAY**.</span><span class="sxs-lookup"><span data-stu-id="7f6dc-119">JScript arrays are not arrays of the variable type **VARIANT SAFEARRAY**.</span></span> <span data-ttu-id="7f6dc-120">Si votre script reçoit une variable **Variant SAFEARRAY** à partir d’un objet com ou d’un script VBScript, il doit utiliser un objet VBArray pour accéder à la variable de **type SAFEARRAY** .</span><span class="sxs-lookup"><span data-stu-id="7f6dc-120">If your script receives a **VARIANT SAFEARRAY** variable from a COM object or VBScript script, it must use a VBArray object to access the **VARIANT SAFEARRAY** variable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f6dc-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7f6dc-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f6dc-122">Traduire en JScript</span><span class="sxs-lookup"><span data-stu-id="7f6dc-122">Translating to JScript</span></span>](translating-to-jscript.md)
</dt> </dl>

 

 




