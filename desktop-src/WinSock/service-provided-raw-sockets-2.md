---
description: Un socket brut est un type de socket qui autorise l’accès au fournisseur de transport sous-jacent. L’utilisation de sockets bruts lors du Portage d’applications vers Winsock n’est pas recommandée pour plusieurs raisons.
ms.assetid: b78c75b7-255c-4e85-9a88-0efb3b5f0e51
title: Sockets bruts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209c884e85327a7a8c1d21292d9342a0c032747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114907"
---
# <a name="raw-sockets"></a>Sockets bruts

Un socket brut est un type de socket qui autorise l’accès au fournisseur de transport sous-jacent. L’utilisation de sockets bruts lors du Portage d’applications vers Winsock n’est pas recommandée pour plusieurs raisons.

La spécification Windows Sockets ne requiert pas qu’un fournisseur de services Winsock prenne en charge les sockets bruts, autrement dit, les sockets de type **chaussette \_ RAW**. Toutefois, les fournisseurs de services sont encouragés à fournir une prise en charge des sockets bruts. Une application compatible avec Windows Sockets qui souhaite utiliser des sockets bruts doit tenter d’ouvrir le socket avec l’appel de [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) et, si elle échoue, tente d’utiliser un autre type de socket ou indique l’échec de l’utilisateur.

Sur Windows 7, Windows Server 2008 R2, Windows Vista et Windows XP avec Service Pack 2 (SP2), la possibilité d’envoyer du trafic sur des sockets bruts a été restreinte de plusieurs façons. Pour plus d’informations, consultez [sockets bruts TCP/IP](tcp-ip-raw-sockets-2.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Portage d’applications de socket vers Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**socle**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[Sockets bruts TCP/IP](tcp-ip-raw-sockets-2.md)
</dt> <dt>

[Considérations sur la programmation Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



