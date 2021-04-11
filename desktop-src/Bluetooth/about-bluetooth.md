---
title: À propos de Bluetooth
description: Bluetooth est un protocole standard qui permet la connectivité sans fil pour une multitude d’appareils, notamment des ordinateurs, des imprimantes, des téléphones portables et des appareils portables.
ms.assetid: 424168a1-e55c-4947-9a80-8594b4d83bbd
keywords:
- Bluetooth Bluetooth, Description
- Bluetooth Bluetooth, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b704bb3245adcd75948f7f9fbb411697c7c45f0
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104030851"
---
# <a name="about-bluetooth"></a>À propos de Bluetooth

Bluetooth est un protocole standard qui permet la connectivité sans fil pour une multitude d’appareils, notamment des ordinateurs, des imprimantes, des téléphones portables et des appareils portables.

Les principales fonctionnalités de Bluetooth sont les suivantes :

-   Protocole sans fil à faible consommation d’énergie et à faible coût avec prise en charge standard et acceptation mondiale.
-   Interface de programmation définie et familière que les développeurs peuvent utiliser pour développer ou porter rapidement sur des applications.
-   Un site Web officiel et une organisation coopérative à l’ensemble du secteur qui explique, encourage et standardise la technologie Bluetooth. Pour plus d’informations, consultez [www.Bluetooth.com](https://www.bluetooth.com/).

Bluetooth sur Windows fournit des services essentiels similaires à ceux exposés par le protocole de contrôle de transmission (TCP/IP). À l’instar de nombreux protocoles et services de mise en réseau, la connectivité Bluetooth et le transfert de données sont programmés via des appels de fonction Windows Sockets, à l’aide de techniques de programmation Windows Sockets courantes et d’extensions Bluetooth spécifiques. Toutefois, étant donné que des différences significatives existent entre un réseau câblé, un réseau fixe et un réseau ad hoc sans fil, Bluetooth fournit des extensions telles que la détection de service/appareil et la notification qui permettent aux applications de fonctionner correctement dans l’environnement sans fil. Ces extensions vous permettent également d’effectuer un Portage simple vers des technologies similaires, telles que IrDA, ou de futurs transports sans fil.

Microsoft assure la prise en charge de Bluetooth sur Windows XP avec Service Pack 1 (SP1) et versions ultérieures, sur Windows XP Embedded avec Service Pack 2 et sur Windows CE. Les applications Bluetooth qui s’exécutent sur Windows XP doivent pouvoir s’exécuter sur une image d’exécution basée sur Windows XP Embedded qui comprend les dépendances requises. Pour plus d’informations sur Windows XP Embedded, consultez la documentation de l’aide de Windows XP Embedded sur MSDN. Pour plus d’informations sur la programmation de Windows CE, consultez le kit de développement logiciel (SDK) Windows CE.

Microsoft propose deux approches pour la programmation de Bluetooth sur Windows :

-   Utilisation de l’interface Windows Sockets
-   Gestion des appareils directement à l’aide des interfaces Bluetooth à l’aide d’interfaces

Cette section fournit des informations générales sur ces deux approches dans les rubriques suivantes. Pour plus d’informations sur l’utilisation des éléments de l’API Windows Sockets pour programmer Bluetooth, consultez la page [programmation Bluetooth avec Windows Sockets](bluetooth-programming-with-windows-sockets.md).



| Section                                                                                | Content                                                           |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Prise en charge de Windows Sockets pour Bluetooth](windows-sockets-support-for-bluetooth.md)     | Décrit la relation entre Bluetooth et Windows Sockets. |
| [Gestion des appareils et des services Bluetooth](managing-bluetooth-devices-and-services.md) | Décrit comment gérer des appareils et des services Bluetooth.           |



 

 

 




