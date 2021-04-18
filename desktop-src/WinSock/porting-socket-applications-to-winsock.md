---
description: Cette section décrit les considérations relatives au portage Winsock.
ms.assetid: 41c0c98e-3990-4600-ab9f-fa87edbea402
title: Portage d’applications de socket vers Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2b3480d5572405d33b3a3532892a48633caa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519295"
---
# <a name="porting-socket-applications-to-winsock"></a>Portage d’applications de socket vers Winsock

Cette section décrit les considérations relatives au portage Winsock.

Il existe un nombre limité d’instances dans lesquelles Windows Sockets s’est détournée d’un respect strict aux conventions Berkeley, généralement en raison de problèmes d’implémentation dans l’environnement Microsoft Windows.

Lorsqu’un écart par rapport aux conventions Berkeley se produit dans Windows Sockets, l’écart est expressément et clairement indiqué. Par exemple, si une fonction est spécifique à Windows Sockets, cet écart est spécifié avec une expression dans la description de la fonction similaire à ce qui suit :

La fonction **\[ de nom \] de fonction** est une extension spécifique à Microsoft de l’API Windows Sockets 2.

Cette section fournit des informations sur le portage d’applications de sockets UNIX Berkeley (BSD) vers Winsock :

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

[Codes d’erreur de Windows Sockets](windows-sockets-error-codes-2.md)
</dt> <dt>

[Considérations sur la programmation Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



