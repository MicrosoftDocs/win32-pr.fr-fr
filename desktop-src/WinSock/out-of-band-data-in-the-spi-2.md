---
description: Les fournisseurs de services qui prennent en charge l’abstraction de données hors bande (OOB) pour les sockets de type flux de données doivent adhérer à la sémantique de cette section.
ms.assetid: 83ed881f-8474-445e-8fb5-9635138a63dd
title: Données hors bande dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858e2845e9fbe198dc7af7a70edfad8a4ac429f8f1abe84289b87a779f6e478b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741049"
---
# <a name="out-of-band-data-in-the-spi"></a>Données hors bande dans le SPI

Les fournisseurs de services qui prennent en charge l’abstraction de données hors bande (OOB) pour les sockets de type flux de données doivent adhérer à la sémantique de cette section. Nous décrirons la gestion des données OOB de manière indépendante du protocole. Pour plus d’informations sur les données OOB implémentées à l’aide de données urgentes dans les fournisseurs de services TCP/IP, reportez-vous aux [annexes Winsock](winsock-annexes.md) . Dans l’exemple suivant, l’utilisation de [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) s’applique également à [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)).

 

 
