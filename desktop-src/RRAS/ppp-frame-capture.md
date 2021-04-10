---
title: Écriture d’un pilote pour capturer des frames PPP
description: Ce document explique comment développer un pilote capable de capturer des frames PPP dans Windows Vista avant de les compresser/les chiffrer dans le chemin d’envoi ou lorsqu’ils sont décompressés/déchiffrés dans le chemin de réception.
ms.assetid: 1b3fe1b8-2b11-4aed-98e1-464b8c0821ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d592596674cd64af5122303afefcfc81026dad27
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104030855"
---
# <a name="writing-a-driver-to-capture-ppp-frames"></a>Écriture d’un pilote pour capturer des frames PPP

Lorsque les trames de protocole PPP (PPP) sont envoyées via un tunnel PPTP (point-to-Point Tunneling Protocol) avec le chiffrement activé, ou via un tunnel L2TP (Layer 2 Tunneling Protocol) qui utilise IPSec pour le chiffrement, l’utilitaire classique de capture de trames PPP peut uniquement capturer des frames PPP qui ont un champ d’identité de protocole chiffré. Ce document explique comment développer un pilote capable de capturer des frames PPP dans Windows Vista avant de les compresser/les chiffrer dans le chemin d’envoi ou lorsqu’ils sont décompressés/déchiffrés dans le chemin de réception.

1.  Écrire un pilote de protocole NDIS. Pour plus d’informations, consultez [pilotes de protocole ndis 6,0](https://msdn.microsoft.com/library/ms795570.aspx) ou [pilotes de protocole ndis (NDIS 5,1)](https://msdn.microsoft.com/library/ms801145.aspx).
2.  Installez le pilote avec une identité matérielle « MS \_ Netmon ». Pour obtenir des instructions détaillées sur l’installation du pilote avec une identité matérielle spécifique, consultez la [section modèles INF](https://msdn.microsoft.com/library/ms794357.aspx).
    > [!Note]  
    > Chaque ordinateur Windows Vista autorise l’installation d’une seule entité de pilote ayant l' \_ identité matérielle « MS Netmon ». Pour installer un autre pilote avec cette identité, vous devez désinstaller le premier pilote. Un pilote installé sans utiliser l’identité matérielle « MS \_ Netmon » ne peut pas effectuer la liaison nécessaire pour capturer des frames PPP.

     

3.  Le pilote de protocole doit spécifier « ndiswanbh » comme interface de liaison pour la capture des frames PPP. Pour obtenir des instructions détaillées, consultez [spécification des interfaces de liaison](https://msdn.microsoft.com/library/aa937923.aspx).
4.  L’implémentation [ProtocolBindAdapter](https://msdn.microsoft.com/library/ms797311.aspx) dans le pilote doit prendre en charge « NdisMediumWan » dans le cadre de la baie de taille moyenne, afin de pouvoir ouvrir le bord du port ndiswanbh à l’aide de la fonction [NdisOpenAdapter](https://msdn.microsoft.com/library/ms804862.aspx) .
5.  Si la fonction [ProtocolOpenAdapterComplete](https://msdn.microsoft.com/library/ms797287.aspx) est appelée avec l’état \_ NDIS \_ réussite, le pilote de protocole doit définir l’OID du [ \_ \_ \_ \_ filtre de paquets actuel](https://msdn.microsoft.com/library/bb314089.aspx) de l’OID avec les indicateurs [NDIS \_ \_ \_ promiscuité de type](https://msdn.microsoft.com/library/bb314089.aspx) de paquet et [NDIS type de \_ paquet \_ \_ \_ local](https://msdn.microsoft.com/library/bb314089.aspx) sur cette liaison. Une fois cette opération effectuée, le pilote de protocole reçoit les trames PPP déchiffrées de la couche de tramage PPP dans sa fonction [ProtocolReceive](https://msdn.microsoft.com/library/ms797274.aspx) .

> [!Note]  
> Ces informations s’appliquent uniquement aux pilotes sur un ordinateur Windows Vista.

 

 

 




