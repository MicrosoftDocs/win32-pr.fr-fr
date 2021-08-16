---
description: Une analyse est une bibliothèque de liens dynamiques (DLL) qui examine les captures en temps réel du trafic réseau.
ms.assetid: 96d04352-5f1c-4964-94d2-692c6b642cb8
title: Analyses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29adc2e3abaa165903b78ac10683f76ce07719b7513cd25b8b4a7ca4377bb6c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364632"
---
# <a name="monitors"></a>Analyses

Une analyse est une bibliothèque de liens dynamiques (DLL) qui examine les captures en temps réel du trafic réseau. Il recherche des conditions prédéfinies, puis génère des événements lorsque ces conditions sont détectées. Par exemple, un événement peut être déclenché en cas de tentative d’interruption du réseau, lorsqu’un poste de travail non autorisé est en charge d’adresses IP ou en cas de défaillance d’un routeur.

> [!Note]  
> Si vous devez effectuer des analyses détaillées sur les données réseau qui nécessitent une analyse après capture, vous devez utiliser des applications d' [*analyse*](p.md) et d' [*experts*](e.md) .

 

Le [*service de contrôle d’analyse*](m.md) (MCSVC) fournit l’infrastructure permettant de gérer vos analyses. Il fournit des fonctions pour charger les dll du moniteur et une interface de communication à l’outil de contrôle de l’analyse afin que vous puissiez créer, configurer, démarrer, arrêter et désactiver plusieurs instances de vos moniteurs.

Les analyses s’exécutent dans deux threads d’exécution. Le MCSVC fournit le premier thread, qui fournit le contrôle direct de l’analyse. Le deuxième thread est fourni par le [*fournisseur de paquets réseau*](n.md) (NPP), qui permet de transmettre les données réseau capturées, les statistiques et l’état de la capture du NPP à l’analyse.

Plusieurs instances du même moniteur peuvent exister pour chaque interface NPP au moment de l’exécution utilisée pour capturer des données.

 

 



