---
description: Les données hors bande (OOB) sont un canal de transmission logiquement indépendant associé à une paire de sockets de flux connectés.
ms.assetid: 30f667cd-5be9-45f2-9d55-bff04834078f
title: Protocole IndependentOut-of-band Data in the SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a55e186e34e401e56017097271d5f036f2666bdc51f8bc27c6692be7e12874e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993609"
---
# <a name="protocol-independentout-of-band-data-in-the-spi"></a>Protocole IndependentOut-of-band Data in the SPI

Les données hors bande (OOB) sont un canal de transmission logiquement indépendant associé à une paire de sockets de flux connectés. Les données OOB peuvent être fournies à l’utilisateur indépendamment des données normales. L’abstraction définit que les fonctionnalités de données OOB doivent prendre en charge la remise fiable d’au moins un bloc de données OOB à la fois. Ce bloc de données peut contenir au moins un octet de données, et au moins un bloc de données OOB peut être en attente de remise à l’utilisateur à un moment donné. Pour les protocoles de communication qui prennent en charge la signalisation intrabande (c’est-à-dire, TCP, où les données urgentes sont fournies en séquence avec les données normales), le système extrait normalement les données OOB du flux de données normal et les stocke séparément (en laissant un intervalle dans le flux de données normal). Cela permet aux utilisateurs de choisir de recevoir les données OOB dans l’ordre et de les recevoir hors séquence sans avoir à mettre en mémoire tampon toutes les données intermédiaires. Il est possible de lire des données OOB.

Un utilisateur peut déterminer s’il existe des données OOB en attente de lecture à l’aide de la fonction [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) (SIOCATMARK). pour les protocoles où le concept de la position du bloc de données OOB dans le flux de données normal est explicite (c’est-à-dire, TCP), un fournisseur de services Windows sockets conservera un marqueur conceptuel indiquant la position du dernier octet des données OOB dans le flux de données normal. Cela n’est pas nécessaire pour l’implémentation de la fonctionnalité **WSPIoctl** (SIOCATMARK) : la présence ou l’absence de données oobles est tout ce qui est nécessaire.

Pour les protocoles où le concept de la position du bloc de données OOB dans le flux de données normal est significatif, une application peut préférer traiter les données hors bande en ligne, dans le cadre du flux de données normal. Pour ce faire, définissez l’option de socket de sorte que \_ OOBINLINE (voir la section [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))). Pour les autres protocoles où les blocs de données OOB sont véritablement indépendants du flux de données normal, toute tentative de définition de SO \_ OOBINLINE génère une erreur. Une application peut utiliser la commande SIOCATMARK WSPIoctl pour déterminer si des données OOB non lues sont précédées de la marque. Par exemple, il peut l’utiliser pour se resynchroniser avec son homologue en s’assurant que toutes les données jusqu’à la marque dans le flux de données sont ignorées lorsque cela est approprié.

Avec SO \_ OOBINLINE désactivé (par défaut) :

-   Le fournisseur de services Winsock notifie un client d’un \_ événement OOB FD, si le client s’est inscrit pour la notification avec [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)), exactement de la même façon que FD \_ Read est utilisé pour notifier la présence de données normales. Autrement dit, FD \_ OOB est publié à l’arrivée des données OOB et aucune donnée OOB n’a été mise en file d’attente, et également lorsque les données sont lues à l’aide de l’indicateur de message \_ OOB, et certaines données OOB restent lues après le retour de l’opération de lecture. Les \_ messages de lecture FD ne sont pas publiés pour les données OOB.
-   Le fournisseur de services Winsock retourne à partir de [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) avec le jeu de Sockets *exceptfds* approprié si les données OOB sont mises en file d’attente sur le Socket.
-   Le client peut appeler [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) avec MSG \_ OOB pour lire le bloc de données urgent à tout moment. Le bloc de données OOB déplace la file d’attente.
-   Le client peut appeler [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) sans msg \_ OOB pour lire le flux de données normal. Le bloc de données OOB n’apparaîtra pas dans le flux de données avec des données normales. Si les données OOB restent après un appel à **WSPRecv**, le fournisseur de services notifie le client avec FD \_ OOB ou via *exceptfds* lors de l’utilisation de [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)).
-   Pour les protocoles où les données OOB ont une position dans le flux de données normal, une seule opération [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) ne s’étend pas sur cette position. Un **WSPRecv** renvoie les données normales avant la marque, et un deuxième **WSPRecv** est requis pour commencer à lire les données après la marque.

Avec SO \_ OOBINLINE activé :

-   Les \_ messages OOB FD ne sont pas publiés pour les données OOB. dans le cadre des fonctions [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) et [**WSPASYNCSELECT**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) , les données OOB sont traitées comme des données normales et indiquées par la définition du socket dans *readfds* ou par l’envoi d’un \_ message FD Read respectivement.
-   Le client ne peut pas appeler [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) avec l' \_ indicateur OOB MSG défini pour lire le bloc de données OOB : le code d’erreur WSAEINVAL est retourné.
-   Le client peut appeler [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) sans l’indicateur de message \_ OOB défini. Toute donnée OOB sera remise dans son ordre correct dans le flux de données normal. Les données OOB ne seront jamais mélangées avec des données normales : il doit y avoir trois demandes de lecture pour prendre en compte les données OOB. La première retourne les données normales avant le bloc de données OOB, le second retourne les données OOB, le troisième retourne les données normales qui suivent les données OOB. En d’autres termes, les limites du bloc de données OOB sont conservées.

La routine [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) est particulièrement bien adaptée pour gérer la notification de la présence de données OOB lorsque \_ OOBINLINE est désactivé.

 

 
