---
description: L’ordre dans lequel les fournisseurs de services de transport sont installés initialement régit l’ordre dans lequel ils sont énumérés via WSCEnumProtocols et WSCEnumProtocols32 au niveau de l’interface du fournisseur de services, ou via WSAEnumProtocols au niveau de l’interface de l’application. Plus important encore, cet ordre régit également l’ordre dans lequel les protocoles et les fournisseurs de services sont pris en compte lorsqu’un client demande la création d’un socket en fonction de sa famille d’adresses, de son type et de son identificateur de protocole.
ms.assetid: f76c63b3-9952-4aaf-813f-152f4838d3c4
title: Classement des fournisseurs de services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 445fcc0cadafae8fd61ee2e34a872485b67466037c1dc71e34ab173156c8d9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740580"
---
# <a name="service-provider-ordering"></a>Classement des fournisseurs de services

L’ordre dans lequel les fournisseurs de services de transport sont installés initialement régit l’ordre dans lequel ils sont énumérés via [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) et [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) au niveau de l’interface du fournisseur de services, ou via [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) au niveau de l’interface de l’application. Plus important encore, cet ordre régit également l’ordre dans lequel les protocoles et les fournisseurs de services sont pris en compte lorsqu’un client demande la création d’un socket en fonction de sa famille d’adresses, de son type et de son identificateur de protocole.

Windows Sockets 2 comprend une applet appelée Sporder.exe qui permet de réorganiser de manière interactive le catalogue des protocoles installés une fois que les protocoles ont déjà été installés. Winsock comprend également une DLL auxiliaire, Sporder.dll, qui exporte une interface procédurale pour la réorganisation des protocoles. Cette interface procédurale se compose d’une procédure unique appelée [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).

La définition d’interface peut être importée dans un programme C ou C++ au moyen du fichier include WebOrder. h. Le point d’entrée peut être lié par le biais du fichier lib WebOrder. lib.

 

 



