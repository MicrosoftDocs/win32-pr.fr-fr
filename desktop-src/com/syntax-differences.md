---
title: Différences de syntaxe
description: La modification la plus apparente à mesure que vous passez d’un langage de programmation à l’autre est la modification de la syntaxe.
ms.assetid: 179efb69-3794-4a06-b770-2b3dc8409172
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3a9c2123d8b94f9fc6fe79d4ab48188830c7a1
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463762"
---
# <a name="syntax-differences"></a><span data-ttu-id="b6aa3-103">Différences de syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6aa3-103">Syntax Differences</span></span>

<span data-ttu-id="b6aa3-104">La modification la plus apparente à mesure que vous passez d’un langage de programmation à l’autre est la modification de la syntaxe.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-104">The most apparent change as you move between programming languages is the change in syntax.</span></span>

<span data-ttu-id="b6aa3-105">Prenons l’exemple de la méthode Add de l’objet EnhEvents, tel qu’il est déclaré dans trois langages différents.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-105">Consider the EnhEvents object's Add method, shown as it is declared in three different languages.</span></span>

``` syntax
object.Add(Time As Double, Name As String) As Variant

HRESULT Add(
  double Time, 
  BSTR Name, 
  VARIANT* pVal
);
 
public com.ms.com.Variant Add( 
  double Time, 
  java.lang.String Name
);
 
```

<span data-ttu-id="b6aa3-106">Bien que la syntaxe de chaque langage exprime différemment la méthode, la fonctionnalité est la même.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-106">Although the syntax of each language expresses the method differently, the functionality is the same.</span></span> <span data-ttu-id="b6aa3-107">Dans chaque langue, la méthode Add prend les paramètres *Time* et *Name* et retourne un objet EnhEvent.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-107">In each language, the Add method takes the parameters *Time* and *Name* and returns an EnhEvent object.</span></span> <span data-ttu-id="b6aa3-108">Dans l’exemple C++, la méthode retourne l’objet à l’aide d’un troisième paramètre de sortie, *pval*.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-108">In the C++ example, the method returns the object by using a third, output parameter, *pVal*.</span></span>

<span data-ttu-id="b6aa3-109">En règle générale, les fonctionnalités d’un objet COM sont les mêmes dans les langages de programmation.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-109">Typically, the functionality of a COM object is the same across programming languages.</span></span> <span data-ttu-id="b6aa3-110">Pour cette raison, la documentation d’un objet COM est utile même si l’objet est documenté dans un autre langage de programmation que celui que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-110">Because of this, documentation for a COM object is useful even if the object is documented in another programming language than the one you are using.</span></span> <span data-ttu-id="b6aa3-111">Les descriptions des fonctionnalités, paramètres et valeurs de retour de l’objet sont, à quelques exceptions près, valides pour tous les langages.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-111">The descriptions of the object's functionality, parameters, and return values are, with few exceptions, valid for all languages.</span></span>

<span data-ttu-id="b6aa3-112">Pour plus d’informations sur la conversion de la syntaxe d’un objet COM en un autre langage de programmation, consultez traduction de la [syntaxe d’objet com pour les langages de programmation](translating-com-object-syntax-for-programming-languages.md).</span><span class="sxs-lookup"><span data-stu-id="b6aa3-112">For information about how to convert the syntax of a COM object to another programming language, see [Translating COM Object Syntax for Programming Languages](translating-com-object-syntax-for-programming-languages.md).</span></span>

<span data-ttu-id="b6aa3-113">Les différences syntaxiques entre les langages de script JavaScript, JScript et VBScript sont moins prononcées que les différences de syntaxe entre les langages de programmation présentés précédemment.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-113">The syntax differences among the scripting languages JavaScript, JScript, and VBScript are less pronounced than the syntax differences among the programming languages shown preceding.</span></span> <span data-ttu-id="b6aa3-114">Par exemple, considérez la fonction Square telle qu’elle est implémentée dans chacun de ces trois langages de script :</span><span class="sxs-lookup"><span data-stu-id="b6aa3-114">For example, consider the square function as it is implemented in each of these three scripting languages:</span></span>

``` syntax
Function square(x)
  square = x*x
End Function
 
function square(x){ return x*x; }
 
function square(x){ return x*x; }
 
```

<span data-ttu-id="b6aa3-115">Notez que les langages de script, contrairement aux langages de programmation, sont faiblement typés.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-115">Notice that the scripting languages, unlike the programming languages, are weakly typed.</span></span> <span data-ttu-id="b6aa3-116">En d’autres termes, il n’est pas nécessaire de spécifier le type de données d’un paramètre ou d’une valeur de retour lorsque vous déclarez une fonction.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-116">In other words, you do not have to specify the data type of a parameter or return value when you declare a function.</span></span> <span data-ttu-id="b6aa3-117">Au lieu de cela, les variables sont automatiquement converties vers le type de données approprié.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-117">Instead, the variables are automatically cast to the appropriate data type.</span></span> <span data-ttu-id="b6aa3-118">Dans le cas de VBScript, toutes les variables sont du même type de données, **Variant**.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-118">In the case of VBScript, all variables are of the same data type, **Variant**.</span></span>

<span data-ttu-id="b6aa3-119">La syntaxe JavaScript et JScript pour Square est la même.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-119">The JavaScript and JScript syntax for square is the same.</span></span> <span data-ttu-id="b6aa3-120">JScript est en grande partie compatible avec JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-120">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="b6aa3-121">Toutefois, JScript comprend certains objets qui ne sont actuellement pas pris en charge par JavaScript, tels que **ActiveXObject**, **Enumerator**, **Error**, **Global** et **VBArray**.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-121">However, JScript includes some objects not currently supported by JavaScript, such as **ActiveXObject**, **Enumerator**, **Error**, **Global**, and **VBArray**.</span></span> <span data-ttu-id="b6aa3-122">Pour plus d’informations sur ces objets, consultez la [Référence du langage JScript](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="b6aa3-122">For more information about these objects, see the [JScript Language Reference](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100)).</span></span>

<span data-ttu-id="b6aa3-123">Sur la surface, la syntaxe JavaScript et JScript ressemble à la syntaxe Java.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-123">On the surface, JavaScript and JScript syntax resembles Java syntax.</span></span> <span data-ttu-id="b6aa3-124">Cette similarité est superficielle uniquement.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-124">This similarity is only superficial.</span></span> <span data-ttu-id="b6aa3-125">Le langage Java a été développé indépendamment à la fois à partir de JavaScript et de JScript et n’est pas associé à l’un ou l’autre.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-125">The Java language was developed independently from both JavaScript and JScript and is not related to either.</span></span>

<span data-ttu-id="b6aa3-126">VBScript, en revanche, est un sous-ensemble du langage de programmation Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-126">VBScript, on the other hand, is a subset of the Visual Basic programming language.</span></span> <span data-ttu-id="b6aa3-127">Pour cette raison, la syntaxe VBScript est un sous-ensemble de Visual Basic syntaxe et est souvent interchangeable avec la syntaxe Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b6aa3-127">Because of this, VBScript syntax is a subset of Visual Basic syntax and is often interchangeable with Visual Basic syntax.</span></span>

<span data-ttu-id="b6aa3-128">Pour plus d’informations sur l’utilisation d’objets COM dans des langages de script, consultez [écriture de scripts avec des objets com](scripting-with-com-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b6aa3-128">For information on using COM objects in scripting languages, see [Scripting with COM Objects](scripting-with-com-objects.md).</span></span>

 

 