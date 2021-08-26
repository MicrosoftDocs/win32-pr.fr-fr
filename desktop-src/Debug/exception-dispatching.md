---
description: Lorsqu’une exception matérielle ou logicielle se produit, le processeur arrête l’exécution au point où l’exception s’est produite et transfère le contrôle au système.
ms.assetid: 35a1b9bd-8da9-47e6-beda-e0b159bd840d
title: Distribution des exceptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b7b4f73c9d2c3fbaf15b4390ee6ecc6b9aa06b50524ec080fc45319d3b94767
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912729"
---
# <a name="exception-dispatching"></a>Distribution des exceptions

Lorsqu’une exception matérielle ou logicielle se produit, le processeur arrête l’exécution au point où l’exception s’est produite et transfère le contrôle au système. Tout d’abord, le système enregistre à la fois l’état de l’ordinateur du thread actuel et les informations qui décrivent l’exception. Le système tente alors de trouver un gestionnaire d’exceptions pour gérer l’exception.

L’état de l’ordinateur du thread dans lequel l’exception s’est produite est enregistré dans une structure de [**contexte**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) . Ces informations (appelées « *enregistrement de contexte*») permettent au système de continuer l’exécution au point de l’exception si l’exception est correctement gérée. La description de l’exception (appelée **enregistrement d’exception**) est enregistrée dans une structure d' [**\_ enregistrement d’exception**](/windows/desktop/api/WinNT/ns-winnt-exception_record) . Étant donné qu’il stocke les informations dépendantes de l’ordinateur de l’enregistrement de contexte indépendamment des informations indépendantes de l’ordinateur de l’enregistrement d’exception, le mécanisme de gestion des exceptions est portable sur différentes plateformes.

Les informations dans les enregistrements de contexte et d’exception sont disponibles au moyen de la fonction [**GetExceptionInformation**](getexceptioninformation.md) et peuvent être mises à la disposition de tous les gestionnaires d’exceptions qui sont exécutés à la suite de l’exception. L’enregistrement d’exception contient les informations suivantes.

-   Code d’exception qui identifie le type d’exception.
-   Indicateurs indiquant si l’exception est continue. Toute tentative de poursuite de l’exécution après une exception qui n’est pas continue génère une autre exception.
-   Pointeur vers un autre enregistrement d’exception. Cela facilite la création d’une liste liée d’exceptions si des exceptions imbriquées se produisent.
-   Adresse à laquelle l’exception s’est produite.
-   Tableau d’arguments qui fournissent des informations supplémentaires sur l’exception.

Quand une exception se produit dans le code en mode utilisateur, le système utilise l’ordre de recherche suivant pour trouver un gestionnaire d’exceptions :

1.  Si le processus est en cours de débogage, le système avertit le débogueur. Pour plus d’informations, consultez [gestion des exceptions du débogueur](debugger-exception-handling.md).
2.  Si le processus n’est pas en cours de débogage ou si le débogueur associé ne gère pas l’exception, le système tente de localiser un gestionnaire d’exceptions basé sur des frames en recherchant les frames de pile du thread dans lequel l’exception s’est produite. Le système recherche d’abord le frame de pile actuel, puis effectue une recherche dans l’ordre inverse des frames de pile précédents.
3.  Si aucun gestionnaire de trames n’est trouvé, ou si aucun gestionnaire basé sur des trames ne gère l’exception, mais que le processus est en cours de débogage, le système notifie le débogueur une deuxième fois.
4.  Si le processus n’est pas en cours de débogage ou si le débogueur associé ne gère pas l’exception, le système fournit la gestion par défaut en fonction du type d’exception. Pour la plupart des exceptions, l’action par défaut consiste à appeler la fonction [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) .

Quand une exception se produit dans le code en mode noyau, le système recherche un gestionnaire d’exceptions dans les frames de pile de la pile du noyau. Si un gestionnaire est introuvable ou qu’aucun gestionnaire ne gère l’exception, le système est arrêté comme si la fonction [**exitwindows**](/windows/win32/api/winuser/nf-winuser-exitwindows) avait été appelée.

 

 
