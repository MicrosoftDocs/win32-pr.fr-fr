---
description: Un gestionnaire d’exceptions basé sur des frames vous permet de gérer la possibilité qu’une exception se produise dans une certaine séquence de code. Un gestionnaire d’exceptions basé sur des frames se compose des éléments suivants.
ms.assetid: 07aac772-f917-48b7-91a9-3b5d4cb43600
title: Gestion des exceptions basée sur des frames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afb72118aca7653e9bc15e7f4ff4b75e46b1abad5bab7dee4a3397ae5f98e1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573119"
---
# <a name="frame-based-exception-handling"></a>Gestion des exceptions basée sur des frames

Un *Gestionnaire d’exceptions basé sur des frames* vous permet de gérer la possibilité qu’une exception se produise dans une certaine séquence de code. Un gestionnaire d’exceptions basé sur des frames se compose des éléments suivants.

-   Corps protégé du code
-   Expression de filtre
-   Bloc de gestionnaire d’exceptions

Les gestionnaires d’exceptions basés sur des frames sont déclarés dans une syntaxe spécifique au langage. Par exemple, dans le compilateur d’optimisation Microsoft C/C++, elles sont implémentées à l’aide de **\_ \_ try** et **\_ \_ except**. Pour plus d’informations, consultez [syntaxe du gestionnaire](handler-syntax.md).

Le *corps de code gardé* est un ensemble d’une ou plusieurs instructions pour lesquelles l’expression de filtre et le bloc de gestionnaire d’exceptions fournissent une protection de gestion des exceptions. Le corps protégé peut être un bloc de code, un ensemble de blocs imbriqués ou une procédure ou une fonction entière. À l’aide du compilateur d’optimisation Microsoft C/C++, un corps protégé est placé entre accolades ( {} ) à la suite du mot clé **\_ \_ try** .

L' *expression de filtre* d’un gestionnaire d’exceptions basé sur des frames est une expression qui est évaluée par le système lorsqu’une exception se produit dans le corps protégé. Cette évaluation produit l’une des actions suivantes par le système.

-   Le système arrête la recherche d’un gestionnaire d’exceptions, restaure l’état de l’ordinateur et continue l’exécution du thread au point où l’exception s’est produite.
-   Le système poursuit la recherche d’un gestionnaire d’exceptions.
-   Le système transfère le contrôle au gestionnaire d’exceptions, et l’exécution du thread continue de manière séquentielle dans le frame de pile dans lequel le gestionnaire d’exceptions est trouvé. Si le gestionnaire n’est pas dans le frame de pile dans lequel l’exception s’est produite, le système déroule la pile, en laissant le frame de pile actuel et tous les autres frames de pile jusqu’à ce qu’il soit renvoyé au frame de pile du gestionnaire d’exceptions. Avant l’exécution d’un gestionnaire d’exceptions, les gestionnaires de terminaisons sont exécutés pour tous les corps protégés du code qui se sont terminés suite au transfert de contrôle au gestionnaire d’exceptions. Pour plus d’informations sur les gestionnaires de terminaisons, reportez-vous à [gestion des arrêts](termination-handling.md).

L’expression de filtre peut être une expression simple, ou elle peut appeler une *fonction de filtre* qui tente de gérer l’exception. Vous pouvez appeler les fonctions [**GetExceptionCode**](getexceptioncode.md) et [**GetExceptionInformation**](getexceptioninformation.md) à partir d’une expression de filtre pour obtenir des informations sur l’exception filtrée. **GetExceptionCode** retourne un code qui identifie le type d’exception et **GetExceptionInformation** retourne un pointeur vers une structure [**de \_ pointeurs d’exception**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) qui contient des pointeurs vers des structures d' [**\_ enregistrement**](/windows/desktop/api/WinNT/ns-winnt-exception_record) de [**contexte**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) et d’exception.

Ces fonctions ne peuvent pas être appelées à partir d’une fonction de filtre, mais leurs valeurs de retour peuvent être passées comme paramètres à une fonction de filtre. [**GetExceptionCode**](getexceptioncode.md) peut être utilisé dans le bloc de gestionnaire d’exceptions, mais [**GetExceptionInformation**](getexceptioninformation.md) ne peut pas être, car les informations vers lesquelles il pointe se trouvent généralement sur la pile et sont détruites lorsque le contrôle est transféré à un gestionnaire d’exceptions. Toutefois, une application peut copier les informations dans un stockage sécurisé pour les mettre à la disposition du gestionnaire d’exceptions.

L’avantage d’une fonction de filtre est qu’elle peut gérer une exception et retourner une valeur qui amène le système à continuer l’exécution à partir du point auquel l’exception s’est produite. Avec un bloc de gestionnaire d’exceptions, en revanche, l’exécution continue de manière séquentielle à partir du gestionnaire d’exceptions plutôt qu’à partir du point de l’exception.

La gestion d’une exception peut être aussi simple qu’une erreur et la définition d’un indicateur qui sera examiné ultérieurement, en imprimant un message d’avertissement ou d’erreur, ou en effectuant une autre action limitée. Si l’exécution peut être poursuivie, il peut également être nécessaire de modifier l’état de l’ordinateur en modifiant l’enregistrement de contexte. Pour obtenir un exemple de fonction de filtre qui gère une exception de défaut de page, consultez [utilisation des fonctions de mémoire virtuelle](../memory/using-the-memory-management-functions.md).

La fonction [**UnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) peut être utilisée comme fonction de filtre dans une expression de filtre. Elle retourne \_ \_ le gestionnaire d’exécution d’exception, sauf si le processus est en cours de débogage. dans ce cas, elle retourne l’exception \_ Continuer la \_ recherche.

 

 
