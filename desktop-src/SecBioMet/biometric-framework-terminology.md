---
title: Terminologie de l’infrastructure biométrique
description: les termes suivants sont utilisés dans la documentation de l’API Windows Biometric Framework.
ms.assetid: D6F2BAF0-8ABB-4810-86B1-A46854FBC328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd88fe552d9a53d8bcf214280e5b15a9206532383afa87bfee6fe6dd95c9c8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127259"
---
# <a name="biometric-framework-terminology"></a>Terminologie de l’infrastructure biométrique

les termes suivants sont utilisés dans la documentation de l’API Windows Biometric Framework.



| Terme                                                 | Définition                                                                                                                                                                                                                                                        |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Infrastructure biométrique (WBF)<br/>         | architecture d’infrastructure dans Windows qui fournit une interface de gestion cohérente et une expérience utilisateur pour les périphériques biométriques.<br/>                                                                                                                         |
| Service de biométrie Windows<br/>                 | service privilégié qui gère tous les périphériques biométriques à l’aide de Windows pilotes de périphérique compatibles avec l’Interface de pilote biométrique (server).<br/>                                                                                                                   |
| Windows Interface du pilote biométrique<br/>        | Norme d’interface pour les pilotes qui gèrent les capteurs d’empreintes digitales.<br/>                                                                                                                                                                                     |
| Windows Fournisseur de services biométriques (WBSP)<br/> | composant du Service biométrique Windows qui gère une catégorie spécifique de technologie biométrique, telle qu’un lecteur d’empreintes digitales. les WBSPs sont intégrés au Service biométrique Windows. Ils ne sont pas des plug-ins et les BSP tiers ne sont pas pris en charge. <br/> |
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



 

 

 





