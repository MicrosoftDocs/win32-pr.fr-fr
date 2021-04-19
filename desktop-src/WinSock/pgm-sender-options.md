---
description: Les expéditeurs PGM sont fournis avec certains paramètres par défaut qui affectent les performances de transmission de données, et la durée de mise en mémoire tampon des données pour tenir compte de la perte de paquets et des demandes de retransmission clientes PGM associées.
ms.assetid: 56b15eac-ea0d-4d18-b5f6-2f1a7b1bb25f
title: Options de l’expéditeur PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c2e83ec7b098b9a82f74d4a3e0b6aa3ab03b63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514432"
---
# <a name="pgm-sender-options"></a>Options de l’expéditeur PGM

Les expéditeurs PGM sont fournis avec certains paramètres par défaut qui affectent les performances de transmission de données, et la durée de mise en mémoire tampon des données pour tenir compte de la perte de paquets et des demandes de retransmission clientes PGM associées. Les paragraphes suivants décrivent ces paramètres par défaut.

## <a name="window-size-and-transmission-rate"></a>Taille de la fenêtre et vitesse de transmission

La capacité à définir la taille de la fenêtre et la vitesse de transmission permet aux applications de contrôler la quantité de données que le transport met en mémoire tampon pour la retransmission et la vitesse à laquelle le flux d’octets est transmis.

Les données de retransmission sont stockées dans un fichier. par conséquent, la taille maximale de la fenêtre est limitée par l’espace disque utilisable par le transport. La taille de la fenêtre par défaut est de 10 Mo. Bien qu’il soit possible pour une taille d’envoi ou de message de dépasser la taille de la fenêtre ou de la mémoire tampon, le flux de données reste ininterrompu. l’envoi est mis en attente jusqu’à ce que toutes les données soient envoyées.

> [!Note]  
> L’espace de mémoire tampon maximal est limité par le nombre maximal de paquets qui peuvent être conservés dans la fenêtre à un moment donné, ce qui est égal à 2 ^ 31 – 1.

 

La vitesse de transmission est la sortie combinée des paquets de données d’origine (ODATA), des paquets de données retransmis (RDATA) et des paquets de comptabilité spécifiques au transport (SPMs), exprimés par seconde. Si la limite de débit est définie à 56 kilobits par seconde par seconde par défaut. La taille de fenêtre par défaut est de 10 mégaoctets, avec un taux par défaut de 56 kilobits par seconde. En raison de la relation entre les trois membres de la structure des [**\_ \_ fenêtres d’envoi RM**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window) , la taille de fenêtre par défaut est donc de 1428 secondes. Pour plus d’informations, consultez **\_ \_ fenêtre d’envoi RM** .

## <a name="window-advance-rate"></a>Taux d’avancement de la fenêtre

Le taux d’avancement de la fenêtre est défini par l’option de socket de la fenêtre de l' [ \_ expéditeur \_ \_ \_ RM](socket-options.md) . Cette option permet aux applications de spécifier l’incrément auquel la fenêtre de l’expéditeur PGM est avancée, exprimée sous la forme d’une valeur de pourcentage différente de zéro de la taille de la fenêtre. La valeur par défaut est 15% et le taux maximal est de 50%. Si l’expéditeur PGM a des données de réparation en attente qui tombent dans l’espace de la fenêtre d’incrémentation, la fenêtre est partiellement avancée à mesure que chaque paquet de réparation dans la fenêtre est envoyé.

## <a name="forward-error-correction-fec"></a>Correction des erreurs de transfert (FEC)

La correction des erreurs de transfert est définie par le biais de l' \_ option utiliser le socket FEC du gestionnaire de configuration \_ . Cette option de socket permet à l’expéditeur PGM d’envoyer des paquets de réparation en tant que paquets de parité au lieu de paquets de données normaux. Cela réduit le nombre de paquets de réparation envoyés pour réparer différentes séquences perdues par plusieurs destinataires dans le même groupe de données. L’activation de FEC est uniquement définie sur l’expéditeur PGM. Les récepteurs PGM suivent automatiquement la stratégie définie par l’expéditeur. Pour une discussion détaillée sur FEC, reportez-vous à la RFC PGM qui se trouve sur le site Web [IETF](https://www.ietf.org/) .

 

 



