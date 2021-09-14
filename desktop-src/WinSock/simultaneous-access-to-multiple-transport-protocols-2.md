---
description: un protocole de transport doit être correctement installé sur le système et enregistré auprès de Windows sockets pour être accessible à une application.
ms.assetid: 45b20f66-4e12-44df-b64b-c96cd5b24cd4
title: Accès simultané à plusieurs protocoles de transport
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e4b9d97743691bc527c455881cd0da5803b62b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292075"
---
# <a name="simultaneous-access-to-multiple-transport-protocols"></a>Accès simultané à plusieurs protocoles de transport

un protocole de transport doit être correctement installé sur le système et enregistré auprès de Windows sockets pour être accessible à une application. La \_ bibliothèque Ws232.dll exporte un ensemble de fonctions pour faciliter le processus d’inscription. Cela comprend la création d’une nouvelle inscription et la suppression d’une inscription existante.

Lorsque de nouvelles inscriptions sont créées, l’appelant (autrement dit, le script d’installation du fournisseur de la pile) fournit une ou plusieurs structures d' [**\_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) renseignées contenant un ensemble complet d’informations sur le protocole. pour plus d’informations, consultez [Windowss SPI 2](about-the-winsock-spi.md). toute pile de transport installée de cette manière est appelée fournisseur de service de sockets Windows.

sur Windows XP avec service pack 2 (SP2), Windows Server 2003 avec service pack 1 (SP1) et Windows Vista et versions ultérieures. le catalogue Winsock qui contient une liste de fournisseurs de transport et d’espaces de noms installés peut être affiché dans une invite de commandes avec la commande suivante :

**netsh Winsock-afficher le catalogue**

le kit de développement logiciel (SDK) Microsoft Windows comprend *Sporder.exe*, qui permet à l’utilisateur d’afficher et de modifier l’ordre dans lequel les fournisseurs de services sont énumérés. À l’aide de *Sporder.exe*, un utilisateur peut établir manuellement une pile de protocole TCP/IP particulière comme fournisseur TCP/IP par défaut si plusieurs piles de ce type sont présentes.

L’application *Sporder.exe* utilise des fonctions exportées de *Sporder.dll* pour réorganiser les fournisseurs de services. Par conséquent, les applications d’installation peuvent utiliser l’interface fournie par *Sporder.dll* pour réorganiser par programmation des fournisseurs de services.

-   [Protocoles et chaînes de protocole en couches](layered-protocols-and-protocol-chains-2.md)
-   [Utilisation de plusieurs protocoles](using-multiple-protocols-2.md)
-   [Plusieurs restrictions de fournisseur sur SELECT](multiple-provider-restrictions-on-select-2.md)

 

 
