---
title: Windows Fournisseur de l’outil d’évaluation du système
description: l’outil Windows System Assessment Tool (winsat) expose un certain nombre de classes qui évaluent les caractéristiques de performances et les fonctionnalités d’un ordinateur.
ms.assetid: f0ce8b55-25b4-40fa-b17f-32a021b50395
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: effd1f475418eaf5b0dcadbbb64d9bb59c5ed5cfd08fd3a1debefc0ae997187c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323001"
---
# <a name="windows-system-assessment-tool-provider"></a>Windows Fournisseur de l’outil d’évaluation du système

\[WinSAT peut être modifié ou non disponible pour les mises en production après Windows 8.1.\]

## <a name="purpose"></a>Objectif

l’outil Windows System Assessment Tool (winsat) expose un certain nombre de classes qui évaluent les caractéristiques de performances et les fonctionnalités d’un ordinateur. Les développeurs peuvent utiliser cette API pour développer des logiciels qui peuvent accéder aux informations de performances et de capacité d’un ordinateur afin de déterminer les paramètres d’application optimaux en fonction des capacités de performances de l’ordinateur.

Les utilisateurs peuvent utiliser les résultats d’une évaluation formelle pour déterminer les scénarios et les applications qui s’exécutent correctement sur un ordinateur. Par exemple, si un package logiciel contient une évaluation de son Packaging, un utilisateur peut utiliser l’évaluation pour déterminer si le logiciel s’exécute correctement sur l’ordinateur.

## <a name="developer-audience"></a>Développeurs concernés

winsat est conçu pour les développeurs C, C++ et Visual Basic, ainsi que pour ceux qui écrivent des scripts.

## <a name="run-time-requirements"></a>Conditions d’exécution

winsat est disponible sur les ordinateurs clients qui démarrent avec le système d’exploitation Windows Vista.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                               | Description                                                                                                   |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [Utilisation de WinSAT](using-winsat.md)<br/>         | Guide procédural pour initier des évaluations, récupérer des scores et récupérer des détails d’évaluation.<br/> |
| [Référence WinSAT](winsat-reference.md)<br/> | Informations de référence sur l’API WinSAT, les exemples et le schéma. <br/>                                    |



 

 

 





