---
description: À propos de l’architecture ACM
ms.assetid: 4a5c0085-0e7b-424d-9205-5ec39518a088
title: À propos de l’architecture ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d75b6b365970c34174facd035ddf38c625e3e4fac72f011e612998c46e9bee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065174"
---
# <a name="about-the-acm-architecture"></a>À propos de l’architecture ACM

le Module d’Auto-configuration (ACM) est le nouveau composant de configuration sans fil pour Windows Vista. Windows xp avec service pack 3 (SP3) et l’API de réseau local sans fil pour Windows XP avec service pack 2 (SP2) utilisent le service de Configuration automatique sans fil à la place.

L’ACM balaie régulièrement les réseaux et utilise un processus itératif pour sélectionner le réseau le plus favori de la plage et s’y connecter, si une interface est activée pour la connexion automatique sur ce réseau. L’ACM enregistre et récupère également les profils réseau, qui contiennent des paramètres d’ACM, de module spécifique aux médias (MSM), de sécurité et de fabricants de matériel indépendant. Ces profils réseau sont destinés à la configuration automatique.

La configuration automatique prend en charge les paramètres globaux et par interface et les profils réseau. Les paramètres globaux et les profils réseau sont configurés si l’ordinateur a rejoint un domaine avec un objet de stratégie de groupe (GPO) au niveau du domaine ou de l’unité d’organisation (UO) dans la hiérarchie Active Directory (AD). Ces paramètres et profils de stratégie de groupe sont en lecture seule, appliqués à chaque interface 802,11 dans le système, et sont toujours prioritaires sur les paramètres par interface et par utilisateur et les profils réseau. Les profils de stratégie de groupe sont placés en haut de la liste des profils réseau préférés sur chaque interface réseau 802,11.

L’architecture ACM est extensible. Les IHV peuvent implémenter une fonctionnalité sans fil propriétaire sans altérer l’infrastructure 802,11 native fournie. Les structures et fonctions de contrôle IHV exposées activent cette extensibilité.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la WiFi Native](about-native-wifi.md)
</dt> </dl>

 

 



