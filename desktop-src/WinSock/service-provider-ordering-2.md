---
description: L’ordre dans lequel les fournisseurs de services de transport sont installés initialement régit l’ordre dans lequel ils sont énumérés via WSCEnumProtocols et WSCEnumProtocols32 au niveau de l’interface du fournisseur de services, ou via WSAEnumProtocols au niveau de l’interface de l’application. Plus important encore, cet ordre régit également l’ordre dans lequel les protocoles et les fournisseurs de services sont pris en compte lorsqu’un client demande la création d’un socket en fonction de sa famille d’adresses, de son type et de son identificateur de protocole.
ms.assetid: f76c63b3-9952-4aaf-813f-152f4838d3c4
title: Classement des fournisseurs de services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c23d9357d30c94b084bf6288013c38a2d46a4b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863810"
---
# <a name="service-provider-ordering"></a>Classement des fournisseurs de services

L’ordre dans lequel les fournisseurs de services de transport sont installés initialement régit l’ordre dans lequel ils sont énumérés via [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) et [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) au niveau de l’interface du fournisseur de services, ou via [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) au niveau de l’interface de l’application. Plus important encore, cet ordre régit également l’ordre dans lequel les protocoles et les fournisseurs de services sont pris en compte lorsqu’un client demande la création d’un socket en fonction de sa famille d’adresses, de son type et de son identificateur de protocole.

Windows Sockets 2 comprend une applet appelée Sporder.exe qui permet de réorganiser de manière interactive le catalogue des protocoles installés une fois que les protocoles ont déjà été installés. Winsock comprend également une DLL auxiliaire, Sporder.dll, qui exporte une interface procédurale pour la réorganisation des protocoles. Cette interface procédurale se compose d’une procédure unique appelée [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).

La définition d’interface peut être importée dans un programme C ou C++ au moyen du fichier include WebOrder. h. Le point d’entrée peut être lié par le biais du fichier lib WebOrder. lib.

 

 



