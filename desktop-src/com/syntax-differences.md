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
# <a name="syntax-differences"></a>Différences de syntaxe

La modification la plus apparente à mesure que vous passez d’un langage de programmation à l’autre est la modification de la syntaxe.

Prenons l’exemple de la méthode Add de l’objet EnhEvents, tel qu’il est déclaré dans trois langages différents.

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

Bien que la syntaxe de chaque langage exprime différemment la méthode, la fonctionnalité est la même. Dans chaque langue, la méthode Add prend les paramètres *Time* et *Name* et retourne un objet EnhEvent. Dans l’exemple C++, la méthode retourne l’objet à l’aide d’un troisième paramètre de sortie, *pval*.

En règle générale, les fonctionnalités d’un objet COM sont les mêmes dans les langages de programmation. Pour cette raison, la documentation d’un objet COM est utile même si l’objet est documenté dans un autre langage de programmation que celui que vous utilisez. Les descriptions des fonctionnalités, paramètres et valeurs de retour de l’objet sont, à quelques exceptions près, valides pour tous les langages.

Pour plus d’informations sur la conversion de la syntaxe d’un objet COM en un autre langage de programmation, consultez traduction de la [syntaxe d’objet com pour les langages de programmation](translating-com-object-syntax-for-programming-languages.md).

Les différences syntaxiques entre les langages de script JavaScript, JScript et VBScript sont moins prononcées que les différences de syntaxe entre les langages de programmation présentés précédemment. Par exemple, considérez la fonction Square telle qu’elle est implémentée dans chacun de ces trois langages de script :

``` syntax
Function square(x)
  square = x*x
End Function
 
function square(x){ return x*x; }
 
function square(x){ return x*x; }
 
```

Notez que les langages de script, contrairement aux langages de programmation, sont faiblement typés. En d’autres termes, il n’est pas nécessaire de spécifier le type de données d’un paramètre ou d’une valeur de retour lorsque vous déclarez une fonction. Au lieu de cela, les variables sont automatiquement converties vers le type de données approprié. Dans le cas de VBScript, toutes les variables sont du même type de données, **Variant**.

La syntaxe JavaScript et JScript pour Square est la même. JScript est en grande partie compatible avec JavaScript. Toutefois, JScript comprend certains objets qui ne sont actuellement pas pris en charge par JavaScript, tels que **ActiveXObject**, **Enumerator**, **Error**, **Global** et **VBArray**. Pour plus d’informations sur ces objets, consultez la [Référence du langage JScript](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100)).

Sur la surface, la syntaxe JavaScript et JScript ressemble à la syntaxe Java. Cette similarité est superficielle uniquement. Le langage Java a été développé indépendamment à la fois à partir de JavaScript et de JScript et n’est pas associé à l’un ou l’autre.

VBScript, en revanche, est un sous-ensemble du langage de programmation Visual Basic. Pour cette raison, la syntaxe VBScript est un sous-ensemble de Visual Basic syntaxe et est souvent interchangeable avec la syntaxe Visual Basic.

Pour plus d’informations sur l’utilisation d’objets COM dans des langages de script, consultez [écriture de scripts avec des objets com](scripting-with-com-objects.md).

 

 