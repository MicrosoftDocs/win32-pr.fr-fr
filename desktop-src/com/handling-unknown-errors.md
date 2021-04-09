---
title: Gestion des erreurs inconnues
description: Gestion des erreurs inconnues
ms.assetid: d6a4cc60-8320-4b67-9f2e-7c4bea6c37fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c3d9e70b89a9a78be62d2940ad8a69ac34c8f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029773"
---
# <a name="handling-unknown-errors"></a>Gestion des erreurs inconnues

Il est légal de retourner un code d’état uniquement à partir de l’implémentation d’une méthode d’interface approuvée comme légitimement retournée. Si vous ne respectez pas cette règle, l’éventualité d’un conflit entre les valeurs de code d’erreur renvoyées et celles approuvées par l’application est incompatible. Portez une attention particulière à ce problème potentiel lors de la propagation des codes d’erreur à partir de fonctions appelées en interne.

Les applications qui appellent des interfaces doivent traiter tout code d’erreur retourné inconnu (par opposition à un code de réussite) comme synonyme de E \_ inattendue. Cette pratique de gestion des codes d’erreur inconnus est requise par les clients des interfaces et fonctions définies par COM. Étant donné que la pratique de programmation consiste à gérer quelques codes d’erreur spécifiques en détail et à traiter le reste de façon générique, cette exigence de gestion des codes d’erreur inattendus ou inconnus est facilement respectée.

Il est important de gérer toutes les erreurs possibles lors de l’appel d’une méthode d’interface. Si vous ne le faites pas, votre application risque de se bloquer, de corrompre les données ou de devenir vulnérable aux attaques de sécurité. L’exemple de code suivant montre la méthode recommandée pour gérer les erreurs inconnues :


```C++
HRESULT hr; 
hr = xxMethod(); 
 
switch (GetScode(hr))  
{ 
    case NOERROR: 
      // Method returned success. 
      break; 
 
    case x1: 
      // Handle error x1 here.
      break; 
 
    case x2: 
      // Handle error x2 here.
      break; 
 
    case E_UNEXPECTED: 
    default: 
      // Handle unexpected errors here. 
      break; 
} 
 
```



La vérification des erreurs suivante est souvent utilisée avec les routines qui ne retournent pas d’éléments spéciaux (autres que S \_ OK ou une erreur inattendue) :


```C++
if (xxMethod() == NOERROR) 
{
    // Handle success here.
} 
else 
{
    // Handle failure here.
} 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des erreurs dans COM](error-handling-in-com.md)
</dt> </dl>

 

 




