---
description: Windows Sockets 2 offre un ensemble étendu d’opérations qui peuvent se produire en coïncidant avec l’établissement d’une connexion de Socket. Les conditions requises par le fournisseur de services pour implémenter ces fonctionnalités sont décrites ci-dessous.
ms.assetid: fbc7055e-ea25-4d17-8039-f0fef300353c
title: Amélioration des fonctionnalités au moment de la connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33c6d7ee928fe7e97f535363e9e842285eef7fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113083"
---
# <a name="enhanced-functionality-at-connect-time"></a>Amélioration des fonctionnalités au moment de la connexion

Windows Sockets 2 offre un ensemble étendu d’opérations qui peuvent se produire en coïncidant avec l’établissement d’une connexion de Socket. Les conditions requises par le fournisseur de services pour implémenter ces fonctionnalités sont décrites ci-dessous.

## <a name="conditional-acceptance"></a>Acceptation conditionnelle

Comme décrit précédemment, [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) appelle une fonction de condition fournie par le client qui utilise des paramètres d’entrée pour fournir des informations sur la demande de connexion en attente. Ces informations peuvent être utilisées par le client pour accepter ou refuser une demande de connexion en fonction des informations de l’appelant, telles que l’identificateur de l’appelant, la qualité de service (QoS), etc. Si la fonction condition retourne l' \_ acceptation CF, un nouveau socket est créé avec les mêmes propriétés que le socket d’écoute et un handle vers le nouveau socket est retourné. Si la fonction condition retourne CF \_ Reject, la demande de connexion doit être rejetée. Si la fonction condition retourne CF \_ Defer, la décision accepter/refuser ne peut pas être effectuée immédiatement et le fournisseur de services doit conserver la demande de connexion dans la file d’attente du Backlog. Le client doit appeler **WSPAccept** à nouveau, lorsqu’il est prêt à prendre une décision et organiser la fonction condition pour qu’elle retourne les fonctions d' \_ acceptation ou de \_ rejet cf. Alors qu’une demande de connexion différée est en haut de la file d’attente des travaux en souffrance, le fournisseur de services n’émet aucune indication supplémentaire pour les demandes de connexion en attente.

## <a name="exchanging-user-data-at-connect-time"></a>Échange de données utilisateur au moment de la connexion

Certains protocoles autorisent l’échange d’une petite quantité de données utilisateur au moment de la connexion. Si ces données ont été reçues de l’hôte qui se connecte, elles sont placées dans une mémoire tampon du fournisseur de services, et un pointeur vers cette mémoire tampon avec une valeur de longueur est fourni au client Winsock SPI via des paramètres d’entrée pour la fonction de condition [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) . Si le client Winsock SPI a des données de réponse à retourner à l’hôte qui se connecte, il peut le copier dans une mémoire tampon fournie par le fournisseur de services. Un pointeur vers cette mémoire tampon et un entier indiquant la taille de la mémoire tampon sont également fournis comme paramètres d’entrée de la fonction de condition (si pris en charge par le protocole).

## <a name="establishing-socket-groups"></a>Établissement des groupes de Sockets

Toutes les utilisation des groupes de sockets sont réservées.

 

 



