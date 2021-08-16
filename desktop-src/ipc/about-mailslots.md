---
description: Un mailslot est un pseudofile qui réside en mémoire, et vous utilisez des fonctions de fichier standard pour y accéder.
ms.assetid: 9a68905d-c235-4c72-bc71-1cccdf5cdadc
title: À propos des mailslots
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d009b2e667e5feebedeb4b842fc3f6e1630b39069e717ce08f5d0441ebe25aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756517"
---
# <a name="about-mailslots"></a>À propos des mailslots

Un mailslot est un pseudofile qui réside en mémoire, et vous utilisez des fonctions de fichier standard pour y accéder. Les données d’un message mailslot peuvent se présenter sous n’importe quelle forme, mais elles ne peuvent pas être supérieures à 424 octets lors de leur envoi entre des ordinateurs. Contrairement aux fichiers sur disque, les mailslots sont temporaires. Lorsque tous les descripteurs d’un mailslot sont fermés, le mailslot et toutes les données qu’il contient sont supprimés.

Un *serveur mailslot* est un processus qui crée un mailslot et en possède un. Quand le serveur crée un mailslot, il reçoit un handle mailslot. Ce descripteur doit être utilisé lorsqu’un processus lit des messages de la mailslot. Seul le processus qui crée un mailslot ou a obtenu le descripteur par un autre mécanisme (tel que l’héritage) peut lire à partir de la mailslot. Tous les mailslots sont locaux au processus qui les crée. Un processus ne peut pas créer de mailslot distant.

Un *client mailslot* est un processus qui écrit un message sur un mailslot. Tout processus qui porte le nom d’un mailslot peut y placer un message. Les nouveaux messages suivent tous les messages existants dans le mailslot.

Les mailslots peuvent diffuser des messages au sein d’un domaine. Si plusieurs processus d’un domaine créent chacun un mailslot en utilisant le même nom, tous les messages adressés à ce mailslot et envoyés au domaine sont reçus par les processus participants. Étant donné qu’un processus peut contrôler à la fois un handle de serveur mailslot et le descripteur du client récupéré lorsque le mailslot est ouvert pour une opération d’écriture, les applications peuvent facilement implémenter une fonctionnalité simple de transmission de messages dans un domaine.

pour envoyer des messages d’une taille supérieure à 424 octets entre les ordinateurs, utilisez des [canaux nommés](named-pipes.md) ou des [sockets Windows](/windows/desktop/WinSock/windows-sockets-start-page-2) à la place.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Noms des mailslot](mailslot-names.md)
</dt> <dt>

[Opérations mailslot](mailslot-operations.md)
</dt> </dl>

 

 
