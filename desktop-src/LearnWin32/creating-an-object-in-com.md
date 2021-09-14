---
title: Création d’un objet dans COM
description: Pour utiliser une interface COM, votre programme crée d’abord une instance d’un objet qui implémente cette interface.
ms.assetid: 75f2115d-d49d-4e4e-8f99-67a231559ba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f96e4d9c2afbac028bfcefffcec6a070c78c8b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094414"
---
# <a name="creating-an-object-in-com"></a>Création d’un objet dans COM

Une fois qu’un thread a initialisé la bibliothèque COM, il est possible que le thread utilise des interfaces COM. Pour utiliser une interface COM, votre programme crée d’abord une instance d’un objet qui implémente cette interface.

En général, il existe deux façons de créer un objet COM :

-   Le module qui implémente l’objet peut fournir une fonction spécifiquement conçue pour créer des instances de cet objet.
-   En guise d’alternative, COM fournit une fonction de création générique nommée [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Par exemple, prenez l' `Shape` objet hypothétique de la rubrique [qu’est-ce qu’une interface com ?](what-is-a-com-interface-.md). Dans cet exemple, l' `Shape` objet implémente une interface nommée `IDrawable` . La bibliothèque de graphiques qui implémente l' `Shape` objet peut exporter une fonction avec la signature suivante.


```C++
// Not an actual Windows function. 

HRESULT CreateShape(IDrawable** ppShape);
```



À partir de cette fonction, vous pouvez créer un nouvel `Shape` objet comme suit.


```C++
IDrawable *pShape;

HRESULT hr = CreateShape(&pShape);
if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



Le paramètre *ppShape* est de type pointeur vers pointeur vers `IDrawable` . Si vous n’avez pas déjà vu ce modèle, l’indirection double peut être curieuse.

Tenez compte des exigences de la `CreateShape` fonction. La fonction doit renvoyer un `IDrawable` pointeur à l’appelant. Mais la valeur de retour de la fonction est déjà utilisée pour le code d’erreur/de réussite. Par conséquent, le pointeur doit être retourné par l’intermédiaire d’un argument à la fonction. L’appelant passera une variable de type `IDrawable*` à la fonction, et la fonction remplacera cette variable par un nouveau `IDrawable` pointeur. En C++, il existe deux façons pour une fonction de remplacer une valeur de paramètre : passer par référence ou passer par adresse. COM utilise la dernière adresse, directe. Et l’adresse d’un pointeur est un pointeur vers un pointeur, donc le type de paramètre doit être `IDrawable**` .

Voici un diagramme pour vous aider à visualiser ce qui se passe.

![diagramme qui montre une indirection de pointeur double](images/com03.png)

La `CreateShape` fonction utilise l’adresse de *pShape* ( `&pShape` ) pour écrire une nouvelle valeur de pointeur dans *pShape*.

## <a name="cocreateinstance-a-generic-way-to-create-objects"></a>CoCreateInstance : méthode générique pour créer des objets

La fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fournit un mécanisme générique pour la création d’objets. Pour comprendre **CoCreateInstance**, gardez à l’esprit que deux objets COM peuvent implémenter la même interface, et qu’un objet peut implémenter deux ou plusieurs interfaces. Par conséquent, une fonction générique qui crée des objets a besoin de deux éléments d’information.

-   L’objet à créer.
-   Interface à récupérer à partir de l’objet.

Mais comment faire pour indiquer ces informations lorsque nous appelons la fonction ? Dans COM, un objet ou une interface est identifié en lui assignant un nombre 128 bits, appelé *identificateur global unique* (Guid). Les GUID sont générés d’une manière qui les rend effectivement uniques. Les GUID sont une solution au problème de la création d’identificateurs uniques sans autorité d’inscription centrale. Les GUID sont parfois appelés *identificateurs uniques universels* (UUID). Avant COM, elles étaient utilisées dans DCE/RPC (environnement de calcul distribué/appel de procédure distante). Plusieurs algorithmes existent pour la création de nouveaux GUID. Tous ces algorithmes garantissent une unicité stricte, mais la probabilité de créer deux fois la même valeur GUID est très faible, en réalité zéro. Les GUID peuvent être utilisés pour identifier n’importe quel type d’entité, pas seulement les objets et les interfaces. Toutefois, il s’agit de la seule utilisation qui nous concerne dans ce module.

Par exemple, la `Shapes` bibliothèque peut déclarer deux constantes GUID :


```C++
extern const GUID CLSID_Shape;
extern const GUID IID_IDrawable; 
```



(Vous pouvez supposer que les valeurs numériques 128 bits réelles pour ces constantes sont définies ailleurs.) La **\_ forme de CLSID** constante identifie l' `Shape` objet, tandis que le **\_ IDrawable IID** de constante identifie l' `IDrawable` interface. Le préfixe « CLSID » signifie *identificateur de classe* et le préfixe *IID* signifie *identificateur d’interface*. Il s’agit des conventions d’affectation de noms standard dans COM.

À partir de ces valeurs, vous devez créer une nouvelle instance de la façon suivante `Shape` :


```C++
IDrawable *pShape;
hr = CoCreateInstance(CLSID_Shape, NULL, CLSCTX_INPROC_SERVER, IID_Drawable,
     reinterpret_cast<void**>(&pShape));

if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



La fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) a cinq paramètres. Le premier et le quatrième paramètres sont l’identificateur de classe et l’identificateur d’interface. En effet, ces paramètres indiquent à la fonction « créer l’objet de forme et me donnent un pointeur vers l’interface IDrawable ».

Affectez au second paramètre la **valeur null**. (Pour plus d’informations sur la signification de ce paramètre, consultez la rubrique [Aggregation](/windows/desktop/com/aggregation) dans la documentation com.) Le troisième paramètre prend un ensemble d’indicateurs dont l’objectif principal est de spécifier le *contexte d’exécution* de l’objet. Le contexte d’exécution spécifie si l’objet s’exécute dans le même processus que l’application ; dans un processus différent sur le même ordinateur ; ou sur un ordinateur distant. Le tableau suivant indique les valeurs les plus courantes pour ce paramètre.



| Indicateur                       | Description                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_serveur INPROC \_ CLSCTX** | Même processus.                                                                                                                                                      |
| **\_serveur local \_ CLSCTX**  | Processus différent, même ordinateur.                                                                                                                                  |
| **\_serveur distant \_ CLSCTX** | Ordinateur différent.                                                                                                                                                |
| **CLSCTX \_ tout**            | Utilisez l’option la plus efficace prise en charge par l’objet. (Le classement, du plus efficace au moins efficace, est : in-process, out-of-process et Cross-Computer.) |



 

La documentation d’un composant particulier peut vous indiquer le contexte d’exécution pris en charge par l’objet. Si ce n’est pas le cas, utilisez **CLSCTX \_ All**. Si vous demandez un contexte d’exécution que l’objet ne prend pas en charge, la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) retourne le code d’erreur **RegDB \_ E \_ CLASSNOTREG**. Ce code d’erreur peut également indiquer que le CLSID ne correspond à aucun composant inscrit sur l’ordinateur de l’utilisateur.

Le cinquième paramètre de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) reçoit un pointeur vers l’interface. Comme **CoCreateInstance** est un mécanisme générique, ce paramètre ne peut pas être fortement typé. Au lieu de cela, le type de données est **void \* \*** et l’appelant doit contraindre l’adresse du pointeur en **type \* \* void** . C’est l’objectif de la **\_ conversion réinterprétée** dans l’exemple précédent.

Il est essentiel de vérifier la valeur de retour de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Si la fonction retourne un code d’erreur, le pointeur d’interface COM n’est pas valide et toute tentative de déréférencement peut entraîner le blocage de votre programme.

En interne, la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) utilise diverses techniques pour créer un objet. Dans le cas le plus simple, il recherche l’identificateur de classe dans le registre. L’entrée de registre pointe vers un fichier DLL ou EXE qui implémente l’objet. **CoCreateInstance** peut également utiliser des informations provenant d’un catalogue com+ ou d’un manifeste côte à côte (SxS). Quels que soient les détails, les détails sont transparents pour l’appelant. Pour plus d’informations sur les détails internes de **CoCreateInstance**, consultez [clients et serveurs com](/windows/desktop/com/com-clients-and-servers).

L' `Shapes` exemple que nous utilisons est quelque peu fictif. passons maintenant à un exemple concret de com en action : affichage de la boîte de dialogue **ouvrir** pour que l’utilisateur sélectionne un fichier.

## <a name="next"></a>Suivant

[Exemple : la boîte de dialogue Ouvrir](example--the-open-dialog-box.md)

 

 