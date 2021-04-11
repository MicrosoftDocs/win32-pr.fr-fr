---
title: À propos de SNMP
description: SNMP utilise une architecture distribuée composée de gestionnaires et d’agents.
ms.assetid: 55be55a8-1968-4373-a969-f7e03b75a824
keywords:
- SNMP, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1dab65173c96dce4bbd2f30edbca2a91f6153d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031684"
---
# <a name="about-snmp"></a>À propos de SNMP

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

SNMP utilise une architecture distribuée composée de gestionnaires et d’agents. Un agent est une application SNMP qui répond aux requêtes des applications du gestionnaire SNMP. L’agent SNMP est chargé de récupérer et de mettre à jour les informations de gestion locales en fonction des demandes du gestionnaire SNMP. L’agent notifie également les gestionnaires inscrits en cas d’événements ou d’interruptions importants. Un gestionnaire est une application SNMP qui génère des requêtes pour les applications de l’agent SNMP et reçoit des interruptions des applications de l’agent SNMP.

Sur les ordinateurs exécutant Microsoft Windows XP/Windows 2000/Windows NT, l’agent SNMP est implémenté par le service SNMP (SNMP.EXE). Le gestionnaire SNMP est généralement une application de console de gestion SNMP tierce. L’application console de gestion n’a pas besoin de s’exécuter sur le même hôte que l’agent SNMP. Pour utiliser les informations fournies par le service SNMP de Microsoft, vous avez besoin d’au moins une application de console de gestion SNMP. Le système inclut des bibliothèques qui prennent en charge les applications de console de gestion SNMP, mais il n’inclut pas d’application de console de gestion SNMP pour l’instant.

 

 