---
title: Conversion en VBScript à partir de JScript
description: Conversion en VBScript à partir de JScript
ms.assetid: db1115e1-2abd-4b06-ad8d-c1f917cd3087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f5ac608e94f883edc3b319fd04625e9a08d18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028900"
---
# <a name="translating-to-vbscript-from-jscript"></a><span data-ttu-id="4d84a-103">Conversion en VBScript à partir de JScript</span><span class="sxs-lookup"><span data-stu-id="4d84a-103">Translating to VBScript from JScript</span></span>

<span data-ttu-id="4d84a-104">Dans VBScript **, le...** **Chaque** boucle énumère les membres d’une collection ; en JScript, le **pour**... **in** Loop énumère les membres d’un objet ou d’un tableau JScript.</span><span class="sxs-lookup"><span data-stu-id="4d84a-104">In VBScript, the **For**...**Each** loop enumerates the members of a collection; in JScript, the **for**...**in** loop enumerates the members of a JScript object or array.</span></span> <span data-ttu-id="4d84a-105">Pour énumérer une collection en JScript, utilisez un objet énumérateur.</span><span class="sxs-lookup"><span data-stu-id="4d84a-105">To enumerate a collection in JScript, use an Enumerator object.</span></span>

<span data-ttu-id="4d84a-106">JScript fournit l’objet d’erreur, qui peut être utilisé pour intercepter et gérer les erreurs.</span><span class="sxs-lookup"><span data-stu-id="4d84a-106">JScript provides the Error object, which can be used to trap and handle errors.</span></span> <span data-ttu-id="4d84a-107">L’objet Error est analogue à l’objet Err VBScript.</span><span class="sxs-lookup"><span data-stu-id="4d84a-107">The Error object is analogous to the VBScript Err object.</span></span>

<span data-ttu-id="4d84a-108">En JScript, il existe plusieurs types de données, tels que des nombres, des chaînes, des valeurs booléennes, des objets et l’attribut null.</span><span class="sxs-lookup"><span data-stu-id="4d84a-108">In JScript, there are several data types such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="4d84a-109">VBScript utilise uniquement un type de données **Variant**, qui peut être sous-typé pour représenter des chaînes, des nombres, des valeurs booléennes, etc.</span><span class="sxs-lookup"><span data-stu-id="4d84a-109">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="4d84a-110">Dans JScript, les tableaux peuvent être étendus dynamiquement en définissant une nouvelle valeur pour la propriété Length du tableau.</span><span class="sxs-lookup"><span data-stu-id="4d84a-110">In JScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="4d84a-111">Dans VBScript, les tableaux ne peuvent pas être agrandis ; elles doivent être redimensionnées à l’aide de l’instruction **ReDim** .</span><span class="sxs-lookup"><span data-stu-id="4d84a-111">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="4d84a-112">Les fonctions de prise en charge de VBScript et de JScript.</span><span class="sxs-lookup"><span data-stu-id="4d84a-112">Both VBScript and JScript support functions.</span></span> <span data-ttu-id="4d84a-113">VBScript, toutefois, prend également en charge les sous-routines.</span><span class="sxs-lookup"><span data-stu-id="4d84a-113">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="4d84a-114">Les sous-routines sont similaires aux fonctions, mais ne retournent pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4d84a-114">Subroutines are similar to functions but do not return a value.</span></span>

<span data-ttu-id="4d84a-115">JScript respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="4d84a-115">JScript is case-sensitive.</span></span> <span data-ttu-id="4d84a-116">VBScript n’est pas.</span><span class="sxs-lookup"><span data-stu-id="4d84a-116">VBScript is not.</span></span>

<span data-ttu-id="4d84a-117">JScript est pris en charge par un large éventail de navigateurs Web, y compris Internet Explorer et Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="4d84a-117">JScript is supported by a wide variety of Web browsers, including both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="4d84a-118">Netscape Navigator ne prend pas en charge VBScript.</span><span class="sxs-lookup"><span data-stu-id="4d84a-118">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="4d84a-119">Les tableaux JScript ne sont pas des tableaux du type de variable **Variant SAFEARRAY**.</span><span class="sxs-lookup"><span data-stu-id="4d84a-119">JScript arrays are not arrays of the variable type **VARIANT SAFEARRAY**.</span></span> <span data-ttu-id="4d84a-120">Un script JScript doit utiliser un objet VBArray pour accéder à la variable de **type SAFEARRAY**.</span><span class="sxs-lookup"><span data-stu-id="4d84a-120">A JScript script must use a VBArray object to access the **VARIANT SAFEARRAY** variable.</span></span> <span data-ttu-id="4d84a-121">Les scripts VBScript peuvent accéder directement à des variables de **type SAFEARRAY**.</span><span class="sxs-lookup"><span data-stu-id="4d84a-121">VBScript scripts can access **VARIANT SAFEARRAY** variables directly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d84a-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4d84a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d84a-123">Conversion en VBScript</span><span class="sxs-lookup"><span data-stu-id="4d84a-123">Translating to VBScript</span></span>](translating-to-vbscript.md)
</dt> </dl>

 

 




