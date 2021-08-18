---
description: Pour l’utilisateur, l’avantage du multitâche est la possibilité de permettre à plusieurs applications d’être ouvertes et opérationnelles en même temps. Par exemple, un utilisateur peut modifier un fichier avec une application alors qu’une autre application recalcule une feuille de calcul.
ms.assetid: 163291ce-78bd-43ee-98ca-564ce91c520c
title: Avantages de la multitâche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811bab71242022babc2a555225a9d02b248f42a03db28cfe1f636f4feb8fb962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143142"
---
# <a name="advantages-of-multitasking"></a>Avantages de la multitâche

Pour l’utilisateur, l’avantage du multitâche est la possibilité de permettre à plusieurs applications d’être ouvertes et opérationnelles en même temps. Par exemple, un utilisateur peut modifier un fichier avec une application alors qu’une autre application recalcule une feuille de calcul.

Pour le développeur d’applications, l’avantage du multitâche est la possibilité de créer des applications qui utilisent plusieurs processus et de créer des processus qui utilisent plusieurs threads d’exécution. Par exemple, un processus peut avoir un thread d’interface utilisateur qui gère les interactions avec l’utilisateur (entrée de clavier et de souris) et les threads de travail qui effectuent d’autres tâches pendant que le thread d’interface utilisateur attend des entrées utilisateur. Si vous attribuez une priorité plus élevée au thread d’interface utilisateur, l’application sera plus réactive pour l’utilisateur, tandis que les threads de travail utiliseront efficacement le processeur pendant les périodes où il n’y a aucune entrée d’utilisateur.

 

 



