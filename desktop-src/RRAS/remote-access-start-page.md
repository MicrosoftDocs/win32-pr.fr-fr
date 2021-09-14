---
title: Accès à distance
description: Utilisez le service d’accès à distance (RAS) pour créer des applications clientes.
ms.assetid: 4e6c04d4-f989-4248-901f-ec15f61582da
keywords:
- RAS du service d’accès à distance
- RAS RAS
- RAS du service d’accès à distance, page de démarrage
- RAS RAS, voir accès à distance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a4b1c06656b51395c8c4fc666e59d6115bd839
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011432"
---
# <a name="remote-access"></a>Accès à distance

## <a name="purpose"></a>Objectif

Utilisez le service d’accès à distance (RAS) pour créer des applications clientes. Ces applications affichent les boîtes de dialogue courantes RAS, gèrent les connexions et les appareils d’accès à distance et manipulent les entrées d’annuaire téléphonique. RAS fournit également la nouvelle génération de fonctionnalités serveur pour le service d’accès à distance (RAS) pour Windows. La fonctionnalité de serveur RRAS suit et s’appuie sur le service d’accès à distance (RAS).

## <a name="where-applicable"></a>Le cas échéant

Le service d’accès à distance est applicable dans n’importe quel environnement informatique qui utilise une liaison de réseau étendu (WAN) ou un réseau privé virtuel (VPN). RAS permet de connecter un ordinateur client distant à un serveur réseau via une liaison de réseau étendu (WAN) ou un réseau privé virtuel (VPN). L’ordinateur distant fonctionne alors sur le réseau local du serveur comme si l’ordinateur distant était directement connecté au réseau local. L’API RAS permet aux programmeurs d’accéder par programme aux fonctionnalités de RAS.

## <a name="developer-audience"></a>Développeurs concernés

L’API RAS est conçue pour être utilisée par les programmeurs C/C++. les programmeurs Microsoft Visual Basic peuvent également trouver l’API utile. Les programmeurs doivent être familiarisés avec les concepts de mise en réseau.

## <a name="run-time-requirements"></a>Conditions d’exécution

Certaines fonctions de l’API RAS sont uniquement prises en charge sur les serveurs réseau et les autres fonctions sont prises en charge uniquement sur les clients réseau. Pour plus d’informations sur les systèmes d’exploitation qui prennent en charge une fonction particulière, reportez-vous aux sections relatives à la configuration requise dans la documentation.

La [fonctionnalité RAS améliorée](function-comparison-windows-2000-versus-rras-redistributable.md) de RRAS est disponible pour Windows NT Server 4,0 en installant le [package redistribuable RRAS](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp). toutes les fonctionnalités du service RRAS sont incorporées dans Windows serveur 2000, Windows server 2003 et Windows server 2008. les applications RRAS ne peuvent pas s’exécuter sur Windows NT Workstation 4,0 ou sur des systèmes d’exploitation clients, tels que Windows 95. Pour plus d’informations sur les systèmes d’exploitation qui prennent en charge une fonction particulière, reportez-vous aux sections relatives à la configuration requise dans la documentation.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                             | Description                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Service d’accès à distance](about-remote-access-service.md)<br/>                               | Le service d’accès à distance (RAS) fournit des fonctionnalités d’accès à distance aux applications clientes sur des ordinateurs exécutant Windows.<br/>                                                                                          |
| [Administration du service d’accès à distance](about-remote-access-service-administration.md)<br/> | L’administration du service d’accès à distance fournit un ensemble de fonctions permettant d’administrer les autorisations et les ports des utilisateurs sur les serveurs RAS. À l’aide de ces fonctions, vous pouvez développer une application d’administration de serveur RAS.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Routage](routing-start-page.md)
</dt> <dt>

[Protocoles de routage](routing-protocols-start-page.md)
</dt> </dl>

 

 





