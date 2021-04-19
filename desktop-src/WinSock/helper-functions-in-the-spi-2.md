---
description: NSPGetServiceClassInfo
ms.assetid: 6fbe9c0c-ac1f-4f2b-a542-eae2195b1335
title: Fonctions d’assistance dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e687529bf1ede1598225708cf288e49bb7e9b5c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536330"
---
# <a name="helper-functions-in-the-spi"></a>Fonctions d’assistance dans le SPI

-   [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo)

La fonction [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) récupère les informations de schéma de la classe de service qui ont été conservées par un fournisseur d’espaces de noms. Il est également utilisé par la DLL Windows Sockets 2 dans son implémentation de [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida).

Les macros suivantes définies dans le fichier d’en-tête *Svcguid. h* et peuvent faciliter le mappage entre les classes de service bien connues et ces espaces de noms.

| Nom de macro                                                                              | Description                                                                                                                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| **SVCID \_ TCP (port)**<br/> **\_UDP SVCID (port)**<br/>                         | À partir d’un port TCP ou UDP pour le protocole Internet, retourne le GUID.                                                                               |
| **EST \_ SVCID \_ TCP (Guid)**<br/> **EST \_ SVCID \_ UDP (Guid)**<br/>                 | Retourne la **valeur true** si le GUID pour TCP ou UDP se trouve dans la plage autorisée.                                                                         |
| **PORT \_ de \_ SVCID \_ TCP (Guid)**<br/> **PORT \_ du \_ SVCID \_ UDP (Guid)**<br/> | Retourne le port TCP ou UDP associé au GUID.                                                                                              |
| **SVCID \_ NetWare (sapid)**<br/>                                                    | Compte tenu de l’identificateur SAP (Service Advertising Protocol), retourne le GUID. Cette macro est utilisée avec l’espace de noms SAP au sein d’un environnement NetWare. |
| **SAPId \_ à partir de \_ SVCID \_ NetWare (Guid)**<br/>                                        | Retourne l’identificateur SAP SAP associé au GUID. Cette macro est utilisée avec l’espace de noms SAP au sein d’un environnement NetWare.               |
| **IS \_ SVCID \_ NetWare (Guid)**<br/>                                                 | Retourne la **valeur true** si le GUID pour NetWare se trouve dans la plage autorisée. Cette macro est utilisée avec l’espace de noms SAP au sein d’un environnement NetWare.    |



 

> [!Note]  
> Le fichier d’en-tête *Svcguid. h* n’est pas automatiquement inclus dans le fichier d’en-tête *Winsock2. h* .

 

 

 




