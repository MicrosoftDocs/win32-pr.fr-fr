---
title: Terminologie de l’infrastructure biométrique
description: Les termes suivants sont utilisés dans la documentation de l’API Windows Biometric Framework.
ms.assetid: D6F2BAF0-8ABB-4810-86B1-A46854FBC328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30f150a30915a44dbd59a5a703577e79dc48933f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675165"
---
# <a name="biometric-framework-terminology"></a>Terminologie de l’infrastructure biométrique

Les termes suivants sont utilisés dans la documentation de l’API Windows Biometric Framework.



| Terme                                                 | Définition                                                                                                                                                                                                                                                        |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Biometric Framework (WBF)<br/>         | Architecture de Framework dans Windows qui fournit une interface de gestion cohérente et une expérience utilisateur pour les périphériques biométriques.<br/>                                                                                                                         |
| Service de biométrie Windows<br/>                 | Service privilégié qui gère tous les périphériques biométriques à l’aide de pilotes de périphérique compatibles avec l’interface de pilote Server Windows.<br/>                                                                                                                   |
| Interface du pilote de biométrie Windows<br/>        | Norme d’interface pour les pilotes qui gèrent les capteurs d’empreintes digitales.<br/>                                                                                                                                                                                     |
| Fournisseur de services de biométrie Windows (WBSP)<br/> | Composant du service de biométrie Windows qui gère une catégorie spécifique de technologie biométrique, telle qu’un lecteur d’empreintes digitales. Les WBSPs sont intégrés au service de biométrie Windows. Ils ne sont pas des plug-ins et les BSP tiers ne sont pas pris en charge. <br/> |
| Facteur biométrique<br/>                          | Caractéristique personnelle pouvant être mesurée et utilisée pour l’identification. Les exemples incluent les empreintes digitales et la géométrie de la main.<br/>                                                                                                                           |
| Sous-facteur biométrique<br/>                      | Caractéristique qualifiante qui peut être utilisée pour définir plus précisément un facteur biométrique. Par exemple, pour identifier complètement une empreinte digitale (facteur biométrique), il est nécessaire de spécifier le doigt d’où provient l’impression (sous-facteur biométrique).<br/>             |
| Exemple biométrique<br/>                          | Données résultant de la mesure d’une caractéristique unique à partir d’une seule personne, par exemple l’image d’une empreinte digitale.<br/>                                                                                                              |
| Modèle biométrique<br/>                        | Moyenne statistique générée par la collecte de plusieurs échantillons biométriques d’une caractéristique unique pour une seule personne. En général, un modèle contient uniquement les fonctionnalités nécessaires pour déterminer s’il existe une correspondance avec un nouvel échantillon.<br/>             |
| Unité biométrique<br/>                            | Objet logiciel qui représente un périphérique biométrique et qui peut être utilisé pour capturer et traiter des exemples biométriques et créer, enregistrer et mettre en correspondance des modèles biométriques.<br/>                                                                                         |
| Adaptateur de capteur<br/>                            | Composant de plug-in d’unité biométrique qui fournit une interface standard pour configurer le capteur, capturer des échantillons et contrôler le workflow de données biométriques à l’adaptateur de moteur.<br/>                                                                 |
| Adaptateur de moteur<br/>                            | Composant de plug-in d’unité biométrique qui traite un exemple en normalisant des données, en extrayant des fonctionnalités et en faisant correspondre des exemples de données à des modèles existants.<br/>                                                                                                   |
| Adaptateur de stockage<br/>                           | Composant de plug-in d’unité biométrique qui stocke, gère et récupère des modèles.<br/>                                                                                                                                                                      |
| Enregistrement d’informations biométriques (BIR)<br/>        | Structure de données qui contient des informations biométriques brutes ou traitées.<br/>                                                                                                                                                                                 |
| Pool de capteurs<br/>                               | Collection d’unités biométriques qui partagent une stratégie de gestion commune.<br/>                                                                                                                                                                                 |
| Test d’activité<br/>                          | Processus qui vérifie qu’un échantillon biométrique n’est pas falsifié ou relu à partir d’un échantillon précédemment collecté.<br/>                                                                                                                          |



 

 

 





