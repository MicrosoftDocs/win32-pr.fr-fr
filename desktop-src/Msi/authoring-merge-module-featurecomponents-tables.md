---
description: Une table FeatureComponents vide est requise dans chaque module de fusion. Cette table vide fournit un schéma pour l’outil de fusion si le fichier. msi cible n’a pas sa propre table FeatureComponents.
ms.assetid: 19463fc7-8362-4943-8907-22c38f66fe25
title: Création de tables FeatureComponents du module de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3522f32f91a66df93e9096bf9c528f8d00e11f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518652"
---
# <a name="authoring-merge-module-featurecomponents-tables"></a>Création de tables FeatureComponents du module de fusion

Une [table FeatureComponents](featurecomponents-table.md) vide est requise dans chaque module de fusion. Cette table vide fournit un schéma pour l’outil de fusion si le fichier. msi cible n’a pas sa propre table FeatureComponents.

Si, et seulement si, il n’existe aucune table FeatureComponents dans le fichier. msi cible, l’outil de fusion utilise la table vide fournie dans le module. Dans ce cas, l’outil de fusion crée une table dupliquée dans le fichier. msi cible et ajoute des lignes qui associent les nouveaux composants dans le module de fusion aux fonctionnalités du package d’installation de l’application.

 

 



