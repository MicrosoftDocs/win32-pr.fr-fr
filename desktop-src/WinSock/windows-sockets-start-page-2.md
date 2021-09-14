---
description: Windows Sockets 2 (Winsock) permet aux programmeurs de créer des applications Internet, intranet et réseau avancées pour transmettre des données d’application sur le câble, indépendamment du protocole réseau utilisé.
ms.assetid: 1ec8758a-40fd-4c98-b839-c2409ef712d6
title: Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df253572d2fca117dbc8b45b451f8c3bacc2f360
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918924"
---
# <a name="windows-sockets-2"></a>Windows Sockets 2

## <a name="purpose"></a>Objectif

Windows Sockets 2 (Winsock) permet aux programmeurs de créer des applications Internet, intranet et réseau avancées pour transmettre des données d’application sur le câble, indépendamment du protocole réseau utilisé. avec Winsock, les programmeurs ont accès aux fonctionnalités avancées de mise en réseau de Microsoft® Windows® telles que la multidiffusion et la qualité de Service (QoS).

Winsock suit le modèle WOSA (Open System Architecture) Windows. Il définit une interface de fournisseur de services (SPI) standard entre l’interface de programmation d’applications (API), ses fonctions exportées et les piles de protocole. Elle utilise le paradigme Sockets qui a été répandu pour la première fois par Berkeley Software Distribution (BSD) UNIX. il a été ensuite adapté pour Windows dans Windows sockets 1,1, avec lequel les applications Windows sockets 2 sont à compatibilité descendante. Programmation Winsock précédemment centrée sur TCP/IP. Certaines pratiques de programmation qui fonctionnaient avec TCP/IP ne fonctionnent pas avec tous les protocoles. par conséquent, l’API Windows sockets 2 ajoute des fonctions quand cela est nécessaire pour gérer plusieurs protocoles.

## <a name="developer-audience"></a>Développeurs concernés

Windows Sockets 2 est conçu pour être utilisé par les programmeurs C/C++. vous devez être familiarisé avec la mise en réseau Windows.

## <a name="run-time-requirements"></a>Conditions d’exécution

Windows sockets 2 peut être utilisé sur toutes les plates-formes Windows. lorsque certaines implémentations ou fonctionnalités de Windows des restrictions de plateforme sockets 2 existent, elles sont clairement notées dans la documentation.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                             | Description                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Nouveautés de Windows Sockets](what-s-new-for-windows-sockets-2.md)<br/>                 | informations sur les nouvelles fonctionnalités de Windows sockets.<br/>                                                                                                                                                                                                                                 |
| [Prise en charge du protocole réseau Winsock dans Windows](network-protocol-support-in-windows.md)<br/> | informations sur la prise en charge du protocole réseau pour les sockets Windows sur différentes versions de Windows.<br/>                                                                                                                                                                                    |
| [À propos de Winsock](about-winsock.md)<br/>                                                     | informations générales sur les considérations relatives à la programmation de Windows sockets, sur l’architecture et les fonctionnalités disponibles pour les développeurs.<br/>                                                                                                                                                       |
| [Utilisation de Winsock](using-winsock.md)<br/>                                                     | procédures et techniques de programmation utilisées avec Windows sockets. Cette section comprend des techniques de programmation de base de Winsock, telles que [prise en main avec Winsock](getting-started-with-winsock.md), ainsi que des techniques avancées utiles aux développeurs Winsock expérimentés.<br/> |
| [Informations de référence sur Winsock](winsock-reference.md)<br/>                                             | Documentation de l’API Windows sockets.<br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assistance IP](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[Qualité de service](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> </dl>

 

 
