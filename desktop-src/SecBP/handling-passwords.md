---
description: Actuellement, les informations d’identification de nom d’utilisateur et de mot de passe sont les informations d’identification les plus courantes utilisées pour l’authentification.
ms.assetid: 1d810f71-9bf5-4c5c-a573-c35081f604cf
title: Gestion des mots de passe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3d3a5ab2bc034500159adb25dab02b47eb43bcd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118890"
---
# <a name="handling-passwords"></a>Gestion des mots de passe

Actuellement, les informations d’identification de nom d’utilisateur et de mot de passe sont les informations d’identification les plus courantes utilisées pour l’authentification. Même si d’autres types d’informations d’identification, tels que les certificats et la biométrie, commencent à se trouver dans le monde des systèmes et de la mise en réseau, ils sont souvent sauvegardés à l’aide de mots de passe. Et, même lorsque les certificats sont utilisés, leurs clés de chiffrement doivent être protégées. Ainsi, les noms d’utilisateur et mots de passe continueront à être utilisés pour les informations d’identification dans le futur.

Étant donné que les mots de passe et les clés de chiffrement vont être quelque temps, il est important que les systèmes logiciels les utilisent de manière sécurisée. Si un réseau ou un système informatique doit rester sécurisé, les mots de passe doivent être protégés contre les attaquants. Cela peut sembler trivial. Toutefois, le système après le système et le réseau après avoir été compromis, car une personne malveillante a pu intercepter les mots de passe des utilisateurs. Les problèmes sont liés aux utilisateurs partageant leurs mots de passe avec une personne, à des logiciels qui peuvent être percés par une personne malveillante.

Il est impossible de stocker des informations confidentielles dans les logiciels de manière entièrement sécurisée. Et étant donné que le stockage des mots de passe et des clés de chiffrement dans un système logiciel ne peut jamais être entièrement sécurisé, il est recommandé de ne pas les stocker dans un système logiciel.

Toutefois, lorsque les mots de passe doivent être stockés dans un système logiciel, ce qui est généralement le cas, certaines précautions peuvent être prises. La précaution principale est de rendre le plus difficile possible pour un intrus de découvrir un mot de passe. Tout comme le verrouillage de vos portes de maison, si une personne est déterminée à s’arrêter, il est presque impossible de les empêcher de le faire. Mais j’espère que le niveau de Difficulté est suffisamment élevé pour que l’intrus serait plus facile à trouver.

Il existe de nombreuses façons de faciliter la découverte des mots de passe par une personne malveillante. Toutefois, l’étendue de ce qui peut être fait est généralement un compromis par rapport à ce que les utilisateurs du réseau ou du système sont prêts à utiliser. Par exemple, prenez le cas où « authentification unique » n’est pas utilisé, et l’utilisateur est invité à entrer un mot de passe chaque fois qu’une application est démarrée. Dans la plupart des cas, cela crée une charge considérable pour les utilisateurs et ils se plaignent probablement. Non seulement cela, mais l’absence d’authentification unique est inefficace et dégrade la productivité des utilisateurs. Ainsi, concrètement, un mot de passe n’est généralement pas collecté auprès d’un utilisateur, sauf au moment de la connexion.

Étant donné que les mots de passe doivent généralement être stockés sur le système logiciel, il est important de s’assurer que les mots de passe restent aussi sécurisés que possible et que la commodité pour les utilisateurs est maintenue. Pour plus d'informations, voir les rubriques suivantes :

-   [Évaluation des menaces par mot de passe](password-threat-assessment.md)
-   [Techniques d’atténuation des menaces](threat-mitigation-techniques.md)

> [!Note]  
> Lorsque vous avez fini d’utiliser les mots de passe dans les applications, effacez les informations sensibles de la mémoire en appelant la fonction [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) .

 

 

 
