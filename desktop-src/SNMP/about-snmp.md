---
title: À propos de SNMP
description: SNMP utilise une architecture distribuée composée de gestionnaires et d’agents.
ms.assetid: 55be55a8-1968-4373-a969-f7e03b75a824
keywords:
- SNMP, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9b43fe4c6b297f0a6973be425239453bb2f03f551f217f4baf7ed0c55099b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009907"
---
# <a name="about-snmp"></a>À propos de SNMP

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

SNMP utilise une architecture distribuée composée de gestionnaires et d’agents. Un agent est une application SNMP qui répond aux requêtes des applications du gestionnaire SNMP. L’agent SNMP est chargé de récupérer et de mettre à jour les informations de gestion locales en fonction des demandes du gestionnaire SNMP. L’agent notifie également les gestionnaires inscrits en cas d’événements ou d’interruptions importants. Un gestionnaire est une application SNMP qui génère des requêtes pour les applications de l’agent SNMP et reçoit des interruptions des applications de l’agent SNMP.

sur les ordinateurs exécutant Microsoft Windows XP/Windows 2000/Windows NT, l’agent snmp est implémenté par le service snmp (SNMP.EXE). Le gestionnaire SNMP est généralement une application de console de gestion SNMP tierce. L’application console de gestion n’a pas besoin de s’exécuter sur le même hôte que l’agent SNMP. Pour utiliser les informations fournies par le service SNMP de Microsoft, vous avez besoin d’au moins une application de console de gestion SNMP. Le système inclut des bibliothèques qui prennent en charge les applications de console de gestion SNMP, mais il n’inclut pas d’application de console de gestion SNMP pour l’instant.

 

 