---
description: De nombreuses applications enregistrent des erreurs et des événements dans des journaux d’erreurs propriétaires, chacun avec leur propre format et leur propre interface utilisateur.
ms.assetid: 5ec95938-ac5d-4f63-9080-2de71454eb17
title: Journalisation des événements (journalisation des événements)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8894c7a6d038efdc317611ca6284f62d99c82ebc767b6f96f83931803a887185
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927839"
---
# <a name="event-logging-event-logging"></a>Journalisation des événements (journalisation des événements)

De nombreuses applications enregistrent des erreurs et des événements dans des journaux d’erreurs propriétaires, chacun avec leur propre format et leur propre interface utilisateur. Les données provenant de différentes applications ne peuvent pas être facilement fusionnées dans un rapport complet, ce qui oblige les administrateurs système ou les représentants du support à vérifier diverses sources pour diagnostiquer les problèmes.

La journalisation des événements offre une méthode standard et centralisée pour les applications (et le système d’exploitation) pour enregistrer des événements logiciels et matériels importants. Le service de journalisation des événements enregistre les événements provenant de différentes sources et les stocke dans une collection unique appelée *Journal des événements*. Le observateur d’événements vous permet d’afficher les journaux ; l’interface de programmation vous permet également d’examiner les journaux.

-   [À propos de la journalisation des événements](about-event-logging.md)
-   [Utilisation de la journalisation des événements](using-event-logging.md)
-   [Référence de journalisation des événements](event-logging-reference.md)

> [!Note]  
> l’API de journalisation des événements a été conçue pour les applications qui s’exécutent sur le système d’exploitation Windows Server 2003, Windows XP ou Windows 2000. dans Windows Vista, l’infrastructure de journalisation des événements a été repensée. les Applications conçues pour s’exécuter sur Windows Vista ou les systèmes d’exploitation ultérieurs doivent utiliser [Windows journal des événements](/windows/desktop/WES/windows-event-log) pour consigner les événements.
