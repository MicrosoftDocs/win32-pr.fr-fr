---
title: Windows Defender Celles
description: Structures utilisées par les applications lors de l’appel de pour demander des analyses, des mises à jour de signature ou des informations de Windows Defender.
ms.assetid: EF4116D3-DA50-4078-A024-2D624945D8C1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d690de552137ce267b9d1d7a9cec711b161528
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292283"
---
# <a name="windows-defender-structures"></a>Windows Defender Celles

Structures utilisées par les applications lors de l’appel de pour demander des analyses, des mises à jour de signature ou des informations de Windows Defender.



| Structure                                                      | Description                                                                             |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**\_données MPCALLBACK**](mpcallback-data.md)                    | Données passées à la fonction de rappel.<br/>                                        |
| [**\_données MPCLEAN**](mpclean-data.md)                          | Données de notification transmises à la fonction de rappel propre.<br/>                         |
| [**MPCLEAN les données de la \_ PRÉvérification \_**](mpclean-precheck-data.md)       | Données de notification transmises à la fonction de rappel de prévérification propre.<br/>                |
| [**État de MPCOMPONENT \_**](mpcomponent-status.md)              | Informations sur l’état du composant.<br/>                                                |
| [**VERSION de MPCOMPONENT \_**](mpcomponent-version.md)            | Version et heure de mise à jour pour un composant individuel.<br/>                         |
| [**\_données MPCONFIGURATION**](mpconfiguration-data.md)          | Contient des données sur les modifications de configuration, y compris les anciennes et nouvelles valeurs.<br/> |
| [**\_données MPENDOFLIFE**](mpendoflife-data.md)                  | Données de notification de « fin de vie ».<br/>                                             |
| [**\_données MPEXPIRATION**](mpexpiration-data.md)                | Notification d’état d’expiration du produit.<br/>                                      |
| [**\_données MPFASTPATH**](mpfastpath-data.md)                    | Notification de mise à jour FastPath.<br/>                                                |
| [**\_données MPHEALTH**](mphealth-data.md)                        | Données de notification d’intégrité.<br/>                                                    |
| [**\_données MPMALWARETOAST**](mpmalwaretoast-data.md)            | Données de notification de Toast de programme malveillant.<br/>                                             |
| [**\_données privées \_ MPNIS**](mpnis-private-data.md)             | Notifications NIS privées.<br/>                                                   |
| [**\_données MPRESERVED**](mpreserved-data.md)                    | Données de notification réservées.<br/>                                                  |
| [**\_informations MPRESOURCE**](mpresource-info.md)                    | Structure des informations sur les ressources.<br/>                                              |
| [**statistiques de MPRESOURCE \_**](mpresource-stats.md)                  | Statistiques relatives aux ressources.<br/>                                                 |
| [**\_données MPSAMPLE**](mpsample-data.md)                        | Données de notification transmises à l’exemple de fonction de rappel de soumission.<br/>         |
| [**\_données MPSCAN**](mpscan-data.md)                            | Analyser les données passées au rappel.<br/>                                            |
| [**\_ressources MPSCAN**](mpscan-resources.md)                  | Informations de ressource passées pendant une opération d’analyse.<br/>                         |
| [**résultat de MPSCAN \_**](mpscan-result.md)                        | Résultats d’une analyse.<br/>                                                       |
| [**\_données MPSIGUPDATE**](mpsigupdate-data.md)                  | Données de notification transmises à la fonction de rappel de mise à jour de signature.<br/>          |
| [**\_données MPSTATUS**](mpstatus-data.md)                        | Contient des données sur l’état actuel d’un composant du produit.<br/>        |
| [**MPSTATUS \_ DATAEX \_ inutilisé**](mpstatus-dataex-unused.md)     | Structure factice pour non-SRP.<br/>                                                 |
| [**\_informations MPSTATUS**](mpstatus-info.md)                        | Informations d’État pour le gestionnaire de protection contre les programmes malveillants.<br/>                       |
| [**\_données MPTHREAT**](mpthreat-data.md)                        | Données de notification transmises en raison de la détection ou de la modification des menaces.<br/>            |
| [**\_informations MPTHREAT**](mpthreat-info.md)                        | Contient des informations sur une menace.<br/>                                         |
| [**comportement de MPTHREAT \_ INFOEX \_**](mpthreat-infoex-behavior.md) | Contient des informations spécifiques à la modification du comportement.<br/>                         |
| [**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md)           | Contient des informations spécifiques à NIS.<br/>                                           |
| [**MPTHREAT \_ INFOEX \_ inutilisé**](mpthreat-infoex-unused.md)     | Structure factice pour les menaces de type modification de non-comportement.<br/>                  |
| [**\_informations localisées \_ MPTHREAT**](mpthreat-localized-info.md)   | Informations localisées pour une menace.<br/>                                          |
| [**statistiques de MPTHREAT \_**](mpthreat-stats.md)                      | Statistiques relatives aux menaces.<br/>                                                   |
| [**\_données statistiques \_ MPTHREAT**](mpthreat-stats-data.md)           | Données de statistiques sur les menaces supplémentaires.<br/>                                           |
| [**\_informations MPVERSION**](mpversion-info.md)                      | Informations de version pour les composants du gestionnaire de protection contre les programmes malveillants.<br/>         |



 

 

 





