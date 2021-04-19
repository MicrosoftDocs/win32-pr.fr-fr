---
description: Pour qu’un protocole de transport soit accessible via Windows Sockets, il doit être correctement installé sur le système et enregistré auprès de Windows Sockets.
ms.assetid: 0f0b22e4-81b7-43a7-bc2f-7124fa32d925
title: Configuration et installation du transport
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea980740f727e39338c7568f4cc30a961b5484df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516459"
---
# <a name="transport-configuration-and-installation"></a>Configuration et installation du transport

Pour qu’un protocole de transport soit accessible via Windows Sockets, il doit être correctement installé sur le système et enregistré auprès de Windows Sockets. Lorsqu’un fournisseur de services de transport est installé en invoquant le programme d’installation d’un fournisseur, les informations de configuration doivent être ajoutées à une base de données de configuration pour fournir au \_ service Ws232.dll informations nécessaires concernant le fournisseur de services. L' \_32.dll Ws2 exporte plusieurs fonctions d’installation, [**WSCInstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider) et [**WSCInstallProviderAndChains**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains), pour que le programme d’installation du fournisseur fournisse les informations pertinentes sur le fournisseur de services à installer. Ces informations incluent, par exemple, le nom et le chemin d’accès à la DLL du fournisseur de services, ainsi qu’une liste de structures d' [**\_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) que ce fournisseur peut prendre en charge. Le \_32.dll Ws2 fournit également une fonction, [**WSCDeinstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider), pour le programme de désinstallation d’un fournisseur afin de supprimer toutes les informations pertinentes de la base de données de configuration gérée par le \_32.dll Ws2. L’emplacement et le format exacts de ces informations de configuration sont privés pour le \_32.dll Ws2 et ne peuvent être manipulés que par les fonctions mentionnées ci-dessus.

Sur les plateformes 64 bits, il existe des fonctions similaires qui fonctionnent sur les catalogues 32 bits et 64 bits. Ces fonctions incluent [**WSCInstallProvider64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider64_32), [**WSCInstallProviderAndChains64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains64_32)et [**WSCDeinstallProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider32).

L’ordre dans lequel les fournisseurs de services de transport sont installés initialement régit l’ordre dans lequel ils sont énumérés via [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) et [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) au niveau de l’interface du fournisseur de services, ou via [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) au niveau de l’interface de l’application. Plus important encore, cet ordre régit également l’ordre dans lequel les protocoles et les fournisseurs de services sont pris en compte lorsqu’un client demande la création d’un socket en fonction de sa famille d’adresses, de son type et de son identificateur de protocole. Windows Sockets 2 comprend une applet appelée Sporder.exe qui permet de réorganiser de manière interactive le catalogue des protocoles installés une fois que les protocoles ont déjà été installés. Windows Sockets 2 comprend également une DLL auxiliaire, Sporder.dll, qui exporte une interface procédurale pour réorganiser les protocoles. Cette interface procédurale se compose d’une procédure unique appelée [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).

## <a name="installing-layered-protocols-and-protocol-chains"></a>Installation de protocoles et de chaînes de protocole en couches

La structure d' [**\_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) fournie avec chaque protocole à installer indique si le protocole est un protocole de base, un protocole en couche ou une chaîne de protocole. La valeur du paramètre *ProtocolChain. ChainLen* est interprétée comme indiqué dans le tableau suivant.

| Valeur | Signification                                           |
|-------|---------------------------------------------------|
| 0     | Protocole superposé.                                 |
| 1     | Protocole de base (ou chaîne avec un seul composant). |
| >1 | Chaîne de protocole.                                   |



 

L’installation de chaînes de protocole ne peut se produire qu’après l’installation réussie de tous les composants constitutifs (protocoles de base et protocoles en couches). La structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour une chaîne de protocole utilise le paramètre *ProtocolChain* pour décrire la longueur de la chaîne et l’identité de chaque composant. Les protocoles individuels qui composent une chaîne sont répertoriés dans l’ordre dans le tableau ProtocolChain. ChainEntries, avec l’élément avant toute chose du tableau correspondant au premier fournisseur superposé. Les protocoles sont identifiés par leurs valeurs *CatalogEntryID* , qui sont affectées par l' \_32.dll Ws2 à l’heure d’installation du protocole et se trouvent dans la structure **WSAPROTOCOL \_ info** pour chaque protocole.

Les valeurs des autres paramètres de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) de la chaîne de protocole doivent être choisies pour refléter les attributs et les identificateurs qui caractérisent le mieux la chaîne de protocole dans son ensemble. Lorsque vous sélectionnez ces valeurs, les développeurs doivent garder à l’esprit que les communications sur les chaînes de protocole ne peuvent se produire que lorsque les deux points de terminaison ont des chaînes de protocole compatibles installées et que les applications doivent être en mesure de reconnaître la structure d' **\_ informations WSAPROTOCOL** correspondante.

Lorsqu’un protocole de base est installé, il n’est pas nécessaire de créer des entrées dans le tableau *ProtocolChain. ChainEntries* . Il est implicitement compris que le seul composant de cette chaîne est déjà identifié dans le paramètre *CatalogEntryID* de la même structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) . Notez également que les chaînes de protocole peuvent ne pas inclure plusieurs instances du même protocole en couches.

 

 
