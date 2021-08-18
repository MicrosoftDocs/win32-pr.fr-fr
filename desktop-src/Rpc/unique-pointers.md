---
title: Pointeurs uniques
description: Dans les programmes C, plusieurs pointeurs peuvent contenir l’adresse des données.
ms.assetid: da4f466d-2c59-4e48-b6c5-1a49b933621a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3adb39d2505daa623f23f47c936fb73d0ecff6e0ad7749c951f9926fd66f33d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010990"
---
# <a name="unique-pointers"></a>Pointeurs uniques

Dans les programmes C, plusieurs pointeurs peuvent contenir l’adresse des données. Les pointeurs sont dits pour créer un [*alias*](a-glos.md) pour les données. Les alias sont également créés lorsque des pointeurs pointent vers des variables déclarées. Le fragment de code suivant illustre ces deux méthodes d’alias :


```C++
int iAnInteger=50;

// The next statement makes ipAnIntegerPointer an
// alias for iAnInteger.
int *ipAnIntegerPointer = &iAnInteger;

// This statement creates an alias for ipAnIntegerPointer.
int *ipAnotherIntegerPointer = ipAnIntegerPointer;
```



Dans un programme C standard, vous pouvez spécifier une arborescence binaire à l’aide de la définition suivante :


```C++
typedef struct _treetype 
{
    long               lValue;
    struct _treetype * left;
    struct _treetype * right;
} TREETYPE;

TREETYPE * troot;
```



Plusieurs pointeurs peuvent accéder au contenu d’un nœud d’arbre. Cela est généralement parfait pour les applications non distribuées. Toutefois, ce style de programmation génère du code de prise en charge RPC plus complexe. Les stubs client et serveur requièrent le code supplémentaire pour gérer les données et les pointeurs. Le code stub sous-jacent doit résoudre les différents pointeurs vers les adresses et déterminer la copie des données qui représente la version la plus récente.

La quantité de traitement peut être réduite si vous vous assurez que votre pointeur est la seule façon dont l’application peut accéder à cette zone de mémoire. Le pointeur peut toujours avoir la plupart des fonctionnalités d’un pointeur C. Par exemple, elle peut être modifiée entre les valeurs **null** et non **null** , ou rester inchangée. L'exemple suivant illustre ce comportement. Le pointeur est **null** avant l’appel et pointe vers une chaîne valide après l’appel :

![modification du pointeur entre les valeurs NULL et non null](images/prog-a01.png)

Par défaut, le compilateur MIDL applique l' \[ [](/windows/desktop/Midl/unique) \] attribut de pointeur unique à tous les pointeurs qui ne sont pas des paramètres. Ce paramètre par défaut peut être modifié à l’aide de l' \[ attribut [ \_ par défaut du pointeur](/windows/desktop/Midl/pointer-default) \] .

Un pointeur unique présente les caractéristiques suivantes :

-   Elle peut avoir la valeur **null**.
-   Elle peut passer de **null** à non **null** pendant l’appel. Lorsque la valeur devient non **null**, une nouvelle mémoire est allouée au retour.
-   Elle peut passer d’une valeur non **null** à une **valeur null** pendant l’appel. Lorsque la valeur est remplacée par **null**, l’application est responsable de la libération de la mémoire.
-   La valeur peut passer d’une valeur non **null** à une autre.
-   Le stockage vers lequel pointe un pointeur unique est inaccessible par tout autre pointeur ou nom dans l’opération.
-   Les données de retour sont écrites dans le stockage existant si le pointeur n’a pas la valeur **null**.

L’exemple suivant montre comment définir un pointeur unique.

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, unique] char *ach);
}
```

Dans cet exemple, le paramètre *ach* est un pointeur unique vers des données caractères qui est envoyé à un serveur à traiter avec la routine RemoteFn.

 

 