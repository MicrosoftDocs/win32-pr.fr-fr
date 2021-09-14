---
description: Fournit une brève introduction à quelques types de situations de dépassement de mémoire tampon et propose des idées et des ressources pour vous aider à éviter de créer de nouveaux risques et à atténuer les risques existants.
ms.assetid: 713fd6de-16af-49d2-8940-763c4a6e414b
title: Éviter les dépassements de mémoire tampon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8a3456384e799380fa0041172fb2b2ea09c0c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011192"
---
# <a name="avoiding-buffer-overruns"></a>Éviter les dépassements de mémoire tampon

Un dépassement de mémoire tampon est l’une des sources les plus courantes de risque de sécurité. Un dépassement de mémoire tampon est essentiellement causé par le traitement d’une entrée externe non vérifiée en tant que données dignes de confiance. Le fait de copier ces données, à l’aide d’opérations telles que [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), **strcat**, **strcpy** ou **wcscpy**, peut créer des résultats imprévus, ce qui permet d’endommager le système. Dans le meilleur des cas, votre application s’arrête avec un vidage de base, une erreur de segmentation ou une violation d’accès. Dans le pire des cas, une personne malveillante peut exploiter le dépassement de mémoire tampon en introduisant et en exécutant d’autres codes malveillants dans votre processus. La copie non vérifiée, les données d’entrée dans une mémoire tampon basée sur la pile est la cause la plus courante d’erreurs exploitables.

Les dépassements de mémoire tampon peuvent se produire de différentes façons. La liste suivante fournit une brève introduction à quelques types de situations de dépassement de mémoire tampon et propose des idées et des ressources pour vous aider à éviter de créer de nouveaux risques et à atténuer les risques existants :

<dl> <dt>

<span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Dépassements de mémoire tampon statiques
</dt> <dd>

Un dépassement de mémoire tampon statique se produit lorsqu’une mémoire tampon, qui a été déclarée sur la pile, est écrite dans avec plus de données qu’elle n’a été allouée à conserver. Les versions moins évidentes de cette erreur se produisent lorsque des données d’entrée utilisateur non vérifiées sont copiées directement dans une variable statique, provoquant ainsi une corruption potentielle de la pile.

</dd> <dt>

<span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Dépassements de tas
</dt> <dd>

Les dépassements de tas, comme les dépassements de mémoire tampon statiques, peuvent entraîner une altération de la mémoire et de la pile. Étant donné que les dépassements de tas se produisent dans la mémoire du tas plutôt que sur la pile, certaines personnes les considèrent comme étant moins capables de provoquer de sérieux problèmes. Néanmoins, les dépassements de tas requièrent des soins de programmation réels et sont tout aussi capables d’autoriser les risques système en cas de dépassements de mémoire tampon statique.

</dd> <dt>

<span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Erreurs d’indexation de tableau
</dt> <dd>

Les erreurs d’indexation de tableau sont également une source de dépassements de mémoire. La vérification des limites soignées et la gestion des index vous aideront à éviter ce type de dépassement de mémoire.

</dd> </dl>

La prévention des dépassements de mémoire tampon consiste principalement à écrire un code correct. Validez toujours toutes vos entrées et effectuez une défaillance normale si nécessaire. Pour plus d’informations sur l’écriture de code sécurisé, consultez les ressources suivantes :

-   Maguire, Steve \[ 1993 \] , *écrivant du code solide*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.
-   Howard, Michael et LeBlanc, David \[ 2003 \] , *écriture de code sécurisé*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.

> [!Note]  
> Ces ressources peuvent ne pas être disponibles dans certains langages et pays.

 

Coffre la gestion des chaînes est un problème à long terme qui continue à être résolu à la fois en suivant les bonnes pratiques de programmation et souvent en utilisant et en réservant les systèmes existants avec des fonctions de gestion de chaînes sécurisées. un exemple d’un tel ensemble de fonctions pour l’interpréteur de commandes Windows démarre avec [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata).

 

 
