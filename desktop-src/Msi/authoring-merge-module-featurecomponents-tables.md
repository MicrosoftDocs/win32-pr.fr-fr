---
description: Une table FeatureComponents vide est requise dans chaque module de fusion. Cette table vide fournit un schéma pour l’outil de fusion si le fichier .msi cible n’a pas sa propre table FeatureComponents.
ms.assetid: 19463fc7-8362-4943-8907-22c38f66fe25
title: Création de tables FeatureComponents du module de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52b2da3e25d84f4f10edad6566edeba5a10d43c5617340d40c733aa23d31f4b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650298"
---
# <a name="authoring-merge-module-featurecomponents-tables"></a>Création de tables FeatureComponents du module de fusion

Une [table FeatureComponents](featurecomponents-table.md) vide est requise dans chaque module de fusion. Cette table vide fournit un schéma pour l’outil de fusion si le fichier .msi cible n’a pas sa propre table FeatureComponents.

Si, et uniquement si, il n’y a aucune table FeatureComponents dans le fichier de .msi cible, l’outil de fusion utilise la table vide fournie dans le module. Dans ce cas, l’outil de fusion crée une table dupliquée dans le fichier .msi cible et ajoute des lignes qui associent les nouveaux composants dans le module de fusion aux fonctionnalités du package d’installation de l’application.

 

 



