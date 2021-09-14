---
title: traçage réseau dans Windows 7
description: Windows 7 s’étend sur l’infrastructure de Diagnostic réseau (NDF) pour fournir une méthode rapide pour résoudre les problèmes de connectivité réseau en activant la collecte de toutes les informations nécessaires en une seule étape, et en tirant parti d’Suivi d’v nements pour Windows (ETW) pour consigner les paquets d’événements réseau dans un fichier unique.
ms.assetid: 7d331362-ff26-4ca0-aa45-07cc97304c7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e3abb4283262703123f8e7060a09af0b810477b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021159"
---
# <a name="network-tracing-in-windows-7"></a>traçage réseau dans Windows 7

À mesure que la complexité de la pile de mise en réseau augmente, il est souvent difficile de suivre et de diagnostiquer rapidement les problèmes au sein de la pile. Windows 7 s’étend sur l’infrastructure de Diagnostic réseau (NDF) pour fournir une méthode rapide pour résoudre les problèmes de connectivité réseau en activant la collecte de toutes les informations nécessaires en une seule étape et en tirant parti d' [Suivi d’v nements pour Windows (ETW)](../etw/event-tracing-portal.md) pour consigner les événements réseau & les paquets dans un fichier unique.

Les événements et les paquets associés sont regroupés pour une activité donnée, par exemple la navigation dans un site Web, sur les différents composants de la pile de mise en réseau. La sortie de ce processus est un fichier journal de suivi d’événements (ETL). En autorisant l’affichage à la fois de tous les événements liés à une activité spécifique dans ce fichier, le temps nécessaire pour isoler et diagnostiquer les problèmes réseau peut être très réduit.

## <a name="in-this-section"></a>Dans cette section



| Rubrique                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|
| [traçage réseau dans Windows 7 : Architecture](network-tracing-in-windows-7-architecture.md)                                |
| [outils de résolution des problèmes à l’aide du traçage réseau dans Windows 7](tools-for-troubleshooting-network-tracing-in-windows-7.md) |
| [traçage réseau dans Windows 7 : scénarios](network-tracing-in-windows-7-scenarios.md)                                      |



 

 

 