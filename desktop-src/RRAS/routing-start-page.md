---
title: Routage
description: Les API de routage permettent de créer des applications pour administrer les fonctionnalités de routage du système d’exploitation.
ms.assetid: 66e1bbb4-73c8-40fc-9575-ffe76d4b697b
keywords:
- Routage RAS
- Routage RAS, page de démarrage
- RAS RRAS
- RAS RRAS, voir routage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e3b2a92a6c54f47693d657315ec0a48e660061
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013855"
---
# <a name="routing"></a>Routage

## <a name="purpose"></a>Objectif

Les API de routage permettent de créer des applications pour administrer les fonctionnalités de routage du système d’exploitation.

## <a name="where-applicable"></a>Le cas échéant

Le routage permet à un ordinateur de fonctionner en tant que routeur réseau.

## <a name="developer-audience"></a>Développeurs concernés

Les API de routage sont conçues pour être utilisées par les programmeurs C/C++. Les programmeurs doivent également être familiarisés avec les concepts de mise en réseau.

## <a name="run-time-requirements"></a>Conditions d’exécution

Le routage est une technologie serveur. toutes les fonctionnalités du routage sont intégrées à Windows serveur 2000 et au Windows server 2003. les applications de routage ne peuvent pas s’exécuter sur Windows NT Workstation 4,0 ou sur des systèmes d’exploitation clients, tels que Windows 95. Pour plus d’informations sur les systèmes d’exploitation qui prennent en charge une fonction particulière, reportez-vous aux sections relatives à la configuration requise dans la documentation.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                               | Description                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Gestion de routeur](about-router-management.md)<br/>                                         | l’API d’administration de routeur permet aux développeurs de créer des applications pour gérer le service de routeur sur un ordinateur exécutant Windows serveur 2000 et les systèmes d’exploitation ultérieurs.<br/>                                                                                                                                                     |
| [Bases d’informations de gestion et gestionnaires de routeur](/windows/desktop/RRAS/about-router-management-with-mib)<br/> | Les API MIB (Management Information base) pour la gestion de routeur permettent d’interroger et de définir les valeurs des variables MIB exportées par l’un des gestionnaires de routeur ou l’un des protocoles de routage utilisés par le service gestionnaires de routeur. À l’aide de cette API, le routeur prend en charge le protocole SNMP (simple Network Management Protocol).<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions de l’assistance IP](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[Accès à distance](remote-access-start-page.md)
</dt> <dt>

[Protocoles de routage](routing-protocols-start-page.md)
</dt> </dl>

 

