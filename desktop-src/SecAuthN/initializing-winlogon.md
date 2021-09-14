---
description: Lorsque Winlogon s’initialise, il enregistre la séquence de touches de sécurité (SAS) CTRL + ALT + SUPPR avec le système, puis il crée trois bureaux au sein de la station Windows WinSta0.
ms.assetid: 874aa12b-e213-4857-9600-698c28dfda37
title: Initialisation de Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 768983d308228e73316c797fb67b035d491a1582
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011286"
---
# <a name="initializing-winlogon"></a>Initialisation de Winlogon

Lorsque [Winlogon](winlogon.md) s’initialise, il enregistre la séquence de touches de [*sécurité*](../secgloss/s-gly.md) (SAS) Ctrl + Alt + Suppr avec le système, puis il crée trois bureaux au sein de la station Windows WinSta0.

L’inscription de CTRL + ALT + SUPPR fait de cette initialisation le premier processus, garantissant ainsi qu’aucune autre application n’a raccordé cette séquence clé.

WinSta0 est le nom de l’objet de station Windows qui représente l’écran, le clavier et la souris physiques. Winlogon crée les postes de travail suivants dans l’objet WinSta0.



| Bureau              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bureau Winlogon     | Il s’agit du bureau utilisé par Winlogon et [*Gina*](../secgloss/g-gly.md) pour l’identification et l’authentification interactives, ainsi que pour d’autres boîtes de dialogue sécurisées. Winlogon bascule automatiquement vers ce bureau lorsqu’il reçoit une notification d’événement SAS.                                                                                                                                                                                                                                                                                                                                                                          |
| Application Desktop  | Chaque fois qu’un utilisateur se connecte avec succès, un bureau d’application est créé pour cette [*session*](../secgloss/l-gly.md). Le Bureau de l’application est également appelé Bureau par défaut ou utilisateur. Ce bureau est l’endroit où l’activité de l’utilisateur a lieu. Le Bureau de l’application est protégé ; seul le système et la session interactive Logon y ont accès. Notez que seule une instance particulière de l’utilisateur connecté a accès au bureau. Si l’utilisateur interactif active un processus à l’aide du contrôleur de service, cette application de service n’aura pas accès au bureau de l’application. |
| Bureau de l’économiseur d’écran | Il s’agit du Bureau actuel lorsqu’un économiseur d’écran est en cours d’exécution. Si un utilisateur a ouvert une session, le système et la session interactive Logon ont accès au bureau. Dans le cas contraire, seul le système a accès au bureau.                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

En tant que propriétaire de ces postes de travail, Winlogon peut basculer le Bureau actuel ou visible sur l’un des trois postes de travail et autoriser GINA à accéder à cette fonctionnalité. En règle générale, les développeurs GINA ne changent pas le Bureau actuel, car Winlogon définit le bureau correctement avant de communiquer avec GINA. La description de chaque fonction GINA indique le Bureau à jour pour cet appel.



| Pour obtenir des informations sur                                    | Consultez                                                                                                      |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Les différents États dans lesquels Winlogon peut s’exécuter           | [États Winlogon](winlogon-states.md)                                                                   |
| Opérations de délai d’attente                                      | [Opérations de Temps de service de boîte de dialogue prises en charge](supported-dialog-box-service-time-out-operations.md) |
| Envoi de messages à GINA lors de l’affichage d’une boîte de dialogue | [Envoi de messages au GINA](sending-messages-to-the-gina.md)                                         |
| Fonctions de prise en charge                                        | [Fonctions de prise en charge de Winlogon](authentication-functions.md)                    |



 

 

 
