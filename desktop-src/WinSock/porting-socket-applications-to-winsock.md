---
description: Cette section décrit les considérations relatives au portage Winsock.
ms.assetid: 41c0c98e-3990-4600-ab9f-fa87edbea402
title: Portage d’applications de socket vers Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97b545c679d9ceb13e3173550dd04b4724309d078b2e8e39fb20419921ba941f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118111867"
---
# <a name="porting-socket-applications-to-winsock"></a>Portage d’applications de socket vers Winsock

Cette section décrit les considérations relatives au portage Winsock.

il existe un nombre limité d’instances dans lesquelles Windows sockets s’est détournés d’un respect strict aux conventions Berkeley, généralement en raison de problèmes d’implémentation dans l’environnement de Windows Microsoft.

lorsqu’un écart par rapport aux conventions Berkeley se produit dans Windows sockets, l’écart est expressément et clairement indiqué. par exemple, si une fonction est spécifique à Windows sockets, cet écart est spécifié avec une expression dans la description de la fonction similaire à ce qui suit :

la fonction **\[ de nom \] de fonction** est une extension spécifique à Microsoft de l’API Windows sockets 2.

cette section fournit des informations sur le portage d’applications de socket Berkeley (BSD) UNIX vers Winsock :

-   [Type de données Socket](socket-data-type-2.md)
-   [Macros Select, FD \_ set et FD \_ xxx](select-and-fd---2.md)
-   [Codes d’erreur-errno, h \_ errno et WSAGetLastError](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
-   [Pointeurs](pointers-2.md)
-   [Fonctions renommées](renamed-functions-2.md)
-   [Nombre maximal de sockets pris en charge](maximum-number-of-sockets-supported-2.md)
-   [Fichiers include](include-files-2.md)
-   [Valeurs de retour en cas d’échec de la fonction](return-values-on-function-failure-2.md)
-   [Sockets bruts](service-provided-raw-sockets-2.md)
-   [Classement des octets](byte-ordering-2.md)
-   [Routines de conversion de Byte-Order étendues](extended-byte-order-conversion-routines-2.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des erreurs Winsock](handling-winsock-errors.md)
</dt> <dt>

[Portage d’applications de socket vers Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Windows Codes d’erreur des sockets](windows-sockets-error-codes-2.md)
</dt> <dt>

[Considérations sur la programmation Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



