---
description: Nouveaux binaires de Low-Level
ms.assetid: 8c883462-29d8-46c4-b1c6-3ae8b8d3b397
title: Nouveaux binaires de Low-Level
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b4640d31b115dc85ecde9f9423997468ddc8456
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088067"
---
# <a name="new-low-level-binaries"></a>Nouveaux binaires de Low-Level

## <a name="affected-platforms"></a>Plateformes affectées

**Clients** -Windows 7  
**Serveurs** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impact sur les fonctionnalités

**Gravité** -moyenne  
**Fréquence** -élevée  











## <a name="description"></a>Description

Pour améliorer l’efficacité de l’ingénierie interne et améliorer les fondations pour un travail futur, nous avons déplacé certaines fonctionnalités vers de nouveaux binaires de bas niveau. Cette refactorisation permettra aux futures installations de Windows de fournir des sous-ensembles de fonctionnalités pour réduire la surface d’exposition (exigences en termes de disque et de mémoire, de maintenance et de surface d’attaque).

## <a name="manifestation-of-impact"></a>Manifeste de l’impact

En guise d’exemple de fonctionnalité que nous avons déplacée vers des binaires de bas niveau, kernelbase.dll obtient les fonctionnalités de kernel32.dll et de advapi32.dll. Cela signifie que le fichier binaire existant transfère désormais les appels vers le nouveau fichier binaire plutôt que de les gérer directement. le transfert peut être statique (la table d’exportation indique la redirection) ou le runtime (la dll a une routine stub qui appelle le nouveau binaire). Cela aura un impact sur les applications de bas niveau, telles que la sécurité et les applications de sauvegarde, qui dépendent des API internes et des décalages.

## <a name="solution"></a>Solution

Le seul impact est le code qui émet des hypothèses lorsqu’il tente d’examiner la kernel32.dll ou la table d’exportation advapi32.dll en mémoire, par exemple une application antivirus. Utilisez les API publiées et non les détails de leur implémentation. Il ne s’agit là que d’un exemple de mise en œuvre d’un détail d’implémentation pour une API.

 

 



