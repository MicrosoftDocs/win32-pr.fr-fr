---
title: À propos de Bluetooth
description: Bluetooth est un protocole standard qui permet la connectivité sans fil pour une multitude d’appareils, notamment des ordinateurs, des imprimantes, des téléphones portables et des appareils portables.
ms.assetid: 424168a1-e55c-4947-9a80-8594b4d83bbd
keywords:
- Bluetooth Bluetooth, description
- Bluetooth Bluetooth, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b704bb3245adcd75948f7f9fbb411697c7c45f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126940951"
---
# <a name="about-bluetooth"></a>À propos de Bluetooth

Bluetooth est un protocole standard qui permet la connectivité sans fil pour une multitude d’appareils, notamment des ordinateurs, des imprimantes, des téléphones portables et des appareils portables.

les principales fonctionnalités de Bluetooth sont les suivantes :

-   Protocole sans fil à faible consommation d’énergie et à faible coût avec prise en charge standard et acceptation mondiale.
-   Interface de programmation définie et familière que les développeurs peuvent utiliser pour développer ou porter rapidement sur des applications.
-   un site Web officiel et une organisation coopérative à l’ensemble du secteur qui explique, encourage et standardise la technologie Bluetooth. Pour plus d’informations, consultez [www.Bluetooth.com](https://www.bluetooth.com/).

Bluetooth sur Windows fournit des services principaux similaires à ceux exposés par le protocole de contrôle de Transmission (tcp/IP). à l’instar de nombreux protocoles et services de mise en réseau, la connectivité Bluetooth et le transfert de données sont programmés via des appels de fonction Windows sockets, à l’aide de techniques de programmation Windows sockets courantes et d’extensions de Bluetooth spécifiques. toutefois, étant donné qu’il existe des différences significatives entre un réseau câblé, un réseau fixe et un réseau ad hoc sans fil, Bluetooth fournit des extensions telles que la détection de service/appareil et la notification qui permettent aux applications de fonctionner correctement dans l’environnement sans fil. Ces extensions vous permettent également d’effectuer un Portage simple vers des technologies similaires, telles que IrDA, ou de futurs transports sans fil.

Microsoft assure la prise en charge de Bluetooth sur Windows xp avec service pack 1 (SP1) et versions ultérieures, sur Windows xp embedded avec service pack 2 et sur Windows CE. Bluetooth applications qui s’exécutent sur Windows xp doivent pouvoir s’exécuter sur une image d’exécution basée sur Windows XP embedded qui comprend les dépendances requises. pour plus d’informations sur Windows xp embedded, consultez la documentation d’aide Windows xp embedded sur MSDN. pour plus d’informations sur la programmation de Windows CE, consultez le kit de développement logiciel (SDK) Windows CE.

Microsoft propose deux approches pour la programmation de Bluetooth sur Windows :

-   utilisation de l’interface de sockets Windows
-   gestion directe des appareils à l’aide d’interfaces de Bluetooth

Cette section fournit des informations générales sur ces deux approches dans les rubriques suivantes. pour plus d’informations sur l’utilisation des éléments de l’API Windows sockets pour programmer des Bluetooth, consultez [Bluetooth programmation avec Windows sockets](bluetooth-programming-with-windows-sockets.md).



| Section                                                                                | Contenu                                                           |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Prise en charge de Windows Sockets pour Bluetooth](windows-sockets-support-for-bluetooth.md)     | décrit la relation entre Bluetooth et les sockets Windows. |
| [gestion des appareils et des Services Bluetooth](managing-bluetooth-devices-and-services.md) | décrit comment gérer des appareils et des services Bluetooth.           |



 

 

 




