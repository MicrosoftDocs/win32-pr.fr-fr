---
description: Un mailslot est un pseudofile qui réside en mémoire, et vous utilisez des fonctions de fichier standard pour y accéder.
ms.assetid: 9a68905d-c235-4c72-bc71-1cccdf5cdadc
title: À propos des mailslots
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bd83fc0d952577efdb149d4c7f25fffbab9784f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538215"
---
# <a name="about-mailslots"></a>À propos des mailslots

Un mailslot est un pseudofile qui réside en mémoire, et vous utilisez des fonctions de fichier standard pour y accéder. Les données d’un message mailslot peuvent se présenter sous n’importe quelle forme, mais elles ne peuvent pas être supérieures à 424 octets lors de leur envoi entre des ordinateurs. Contrairement aux fichiers sur disque, les mailslots sont temporaires. Lorsque tous les descripteurs d’un mailslot sont fermés, le mailslot et toutes les données qu’il contient sont supprimés.

Un *serveur mailslot* est un processus qui crée un mailslot et en possède un. Quand le serveur crée un mailslot, il reçoit un handle mailslot. Ce descripteur doit être utilisé lorsqu’un processus lit des messages de la mailslot. Seul le processus qui crée un mailslot ou a obtenu le descripteur par un autre mécanisme (tel que l’héritage) peut lire à partir de la mailslot. Tous les mailslots sont locaux au processus qui les crée. Un processus ne peut pas créer de mailslot distant.

Un *client mailslot* est un processus qui écrit un message sur un mailslot. Tout processus qui porte le nom d’un mailslot peut y placer un message. Les nouveaux messages suivent tous les messages existants dans le mailslot.

Les mailslots peuvent diffuser des messages au sein d’un domaine. Si plusieurs processus d’un domaine créent chacun un mailslot en utilisant le même nom, tous les messages adressés à ce mailslot et envoyés au domaine sont reçus par les processus participants. Étant donné qu’un processus peut contrôler à la fois un handle de serveur mailslot et le descripteur du client récupéré lorsque le mailslot est ouvert pour une opération d’écriture, les applications peuvent facilement implémenter une fonctionnalité simple de transmission de messages dans un domaine.

Pour envoyer des messages d’une taille supérieure à 424 octets entre les ordinateurs, utilisez à la place des [canaux nommés](named-pipes.md) ou des [sockets Windows](/windows/desktop/WinSock/windows-sockets-start-page-2) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Noms des mailslot](mailslot-names.md)
</dt> <dt>

[Opérations mailslot](mailslot-operations.md)
</dt> </dl>

 

 
