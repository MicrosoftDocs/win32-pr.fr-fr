---
description: L’API Internet Protocol Helper (assistance IP) permet d’extraire et de modifier les paramètres de configuration réseau de l’ordinateur local.
ms.assetid: 4896a9f8-0486-4380-bf49-d1c9ef114acc
title: Assistance IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6262543d1644fbe62858f2c90064f42d2c1348b2f3c56033813f453d33470ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146772"
---
# <a name="ip-helper"></a>Assistance IP

## <a name="purpose"></a>Objectif

L’API Internet Protocol Helper (assistance IP) permet d’extraire et de modifier les paramètres de configuration réseau de l’ordinateur local.

## <a name="where-applicable"></a>Le cas échéant

L’API d’assistance IP est applicable dans tout environnement informatique dans lequel la manipulation par programmation de la configuration réseau et TCP/IP est utile. Les applications typiques incluent les protocoles de routage IP et les agents SNMP (simple Network Management Protocol).

## <a name="developer-audience"></a>Développeurs concernés

L’API d’assistance IP est conçue pour être utilisée par les programmeurs C/C++. les programmeurs doivent également être familiarisés avec les concepts de mise en réseau Windows et TCP/IP.

## <a name="run-time-requirements"></a>Conditions d’exécution

l’API d’assistance IP peut être utilisée sur toutes les plates-formes Windows. Tous les systèmes d’exploitation ne prennent pas en charge toutes les fonctions. lorsque certaines implémentations ou fonctionnalités de Windows des restrictions de plateforme sockets 2 existent, elles sont clairement notées dans la documentation. Si une fonction d’assistance IP est appelée sur une plateforme qui ne prend pas en charge la fonction, l’erreur \_ non \_ prise en charge est retournée. Pour plus d’informations sur les systèmes d’exploitation qui prennent en charge une fonction particulière, reportez-vous aux sections relatives à la configuration requise dans la documentation.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                              | Description                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Nouveautés du programme d’assistance IP](what-s-new-in-ip-helper.md)<br/>  | Informations sur les nouvelles fonctionnalités de l’assistance IP.<br/>                                                                                                                                                             |
| [À propos de l’assistance IP](about-ip-helper.md)<br/>                  | Informations générales sur les considérations et les fonctionnalités de programmation d’assistance IP disponibles pour les développeurs.<br/>                                                                                               |
| [Utilisation de l’assistance IP](using-ip-helper.md)<br/>                  | Procédures et techniques de programmation utilisées avec l’assistance IP. Cette section comprend des techniques de base de programmation d’assistance IP, telles que [prise en main avec IP Helper](getting-started-with-ip-helper.md).<br/> |
| [Informations de référence sur l’assistance IP](ip-helper-function-reference.md)<br/> | Documentation de référence pour les fonctions, structures et énumérations d’assistance IP.<br/>                                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Sockets 2](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[Service de routage et d’accès à distance](../rras/routing-start-page.md)
</dt> </dl>

 

