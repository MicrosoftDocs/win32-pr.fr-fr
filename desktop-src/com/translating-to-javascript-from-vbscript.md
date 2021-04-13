---
title: Conversion en JavaScript à partir de VBScript
description: Conversion en JavaScript à partir de VBScript
ms.assetid: 39a712c5-f8d7-4441-a602-93cda43c24d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff950c58c87e926c8593e5c009db4efbce0a371
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309366"
---
# <a name="translating-to-javascript-from-vbscript"></a><span data-ttu-id="2ac2c-103">Conversion en JavaScript à partir de VBScript</span><span class="sxs-lookup"><span data-stu-id="2ac2c-103">Translating to JavaScript from VBScript</span></span>

<span data-ttu-id="2ac2c-104">En JavaScript, il existe plusieurs types de données, tels que des nombres, des chaînes, des valeurs booléennes, des objets et l’attribut null.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-104">In JavaScript, there are several data types such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="2ac2c-105">VBScript utilise uniquement un type de données **Variant**, qui peut être sous-typé pour représenter des chaînes, des nombres, des valeurs booléennes, etc.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-105">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="2ac2c-106">En JavaScript, les tableaux peuvent être étendus dynamiquement en définissant une nouvelle valeur pour la propriété Length du tableau.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-106">In JavaScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="2ac2c-107">Dans VBScript, les tableaux ne peuvent pas être agrandis ; elles doivent être redimensionnées à l’aide de l’instruction **ReDim** .</span><span class="sxs-lookup"><span data-stu-id="2ac2c-107">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="2ac2c-108">Les fonctions de prise en charge de VBScript et JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-108">Both VBScript and JavaScript support functions.</span></span> <span data-ttu-id="2ac2c-109">VBScript, toutefois, prend également en charge les sous-routines.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-109">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="2ac2c-110">Les sous-routines sont similaires aux fonctions, mais ne retournent pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-110">Subroutines are similar to functions but do not return a value.</span></span>

<span data-ttu-id="2ac2c-111">JavaScript respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-111">JavaScript is case-sensitive.</span></span> <span data-ttu-id="2ac2c-112">VBScript n’est pas.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-112">VBScript is not.</span></span>

<span data-ttu-id="2ac2c-113">JavaScript est pris en charge par un large éventail de navigateurs Web, y compris Internet Explorer et Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-113">JavaScript is supported by a wide variety of Web browsers, including both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="2ac2c-114">VBScript est pris en charge uniquement par Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-114">VBScript is only supported by Internet Explorer.</span></span>

<span data-ttu-id="2ac2c-115">VBScript fournit la prise en charge de la gestion des erreurs via son objet Err.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-115">VBScript provides error handling support through its Err object.</span></span> <span data-ttu-id="2ac2c-116">JavaScript ne fournit pas actuellement de méthode de recouvrement et de gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="2ac2c-116">JavaScript does not currently provide a means of trapping and handling errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ac2c-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2ac2c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ac2c-118">Conversion en JavaScript</span><span class="sxs-lookup"><span data-stu-id="2ac2c-118">Translating to JavaScript</span></span>](translating-to-javascript.md)
</dt> </dl>

 

 




