---
description: L’illustration suivante montre la relation entre les analyses et les autres composants de l’architecture Moniteur réseau.
ms.assetid: cbd6116c-1a95-4ac4-bc79-632ebe198197
title: Analyser l’architecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c1a36ef19933d888f27079d8d94ddba16bde79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550911"
---
# <a name="monitor-architecture"></a>Analyser l’architecture

L’illustration suivante montre la relation entre les [*analyses*](m.md) et les autres composants de l’architecture Moniteur réseau.

![relation entre les moniteurs et d’autres composants du moniteur réseau](images/nmarch2.png)

Le trafic réseau est collecté (sous forme de trames individuelles) à partir du pilote NDIS. Le pilote de Moniteur réseau (Nmnt.sys) achemine ensuite les trames vers un fournisseur de paquets réseau (NPP), qui à son tour capture les données en temps réel. Le NPP est une collection d’interfaces COM utilisées pour capturer des données. Dans ce cas, l’interface [**IRTC**](irtc.md) est utilisée pour effectuer une capture en temps réel.

> [!Note]  
> Le NPP est utilisé pour les captures retardées et en temps réel. Pour les captures différées utilisées par les experts et les analyseurs, l’interface [**IDelaydC**](idelaydc.md) est utilisée.

 

Le moniteur examine ensuite les données capturées en temps réel, en détectant les conditions réseau spécifiques et en générant les événements nécessaires.

Trois autres composants sont utilisés par les applications de surveillance : l’outil de contrôle de l’analyse, le service de contrôle d’analyse (MCSVC) et le observateur d’événements :

-   L’outil de contrôle de l’analyse est utilisé pour gérer vos applications de surveillance. Cela comprend la configuration et l’exécution de toutes les applications du moniteur.
-   Le service de contrôle de l’analyse (MCSVC) déclenche des événements, fournit un lien de communication vers WMI pour l’affichage des événements et coordonne le traitement des opérations du moniteur.
-   Le observateur d’événements affiche les événements déclenchés par le service de contrôle de l’analyse.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IMonitor**](imonitor.md)
</dt> <dt>

[**IMonitorEventer**](imonitoreventer.md)
</dt> <dt>

[**IRTC**](irtc.md)
</dt> </dl>

 

 



