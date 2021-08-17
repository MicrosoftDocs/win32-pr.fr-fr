---
description: Disponibilité des références SKU des contrôles parentaux
ms.assetid: 5fbf6c4a-3897-4a12-bef6-19478fdb48aa
title: Disponibilité des références SKU des contrôles parentaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21184a383a28e3ae06198f203475c1c03334e5d678278bbb3b4988b52971e79e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461199"
---
# <a name="parental-controls-sku-availability"></a>Disponibilité des références SKU des contrôles parentaux

Les interfaces utilisateur, les fonctionnalités et les API des contrôles parentaux décrits dans cette section sont actuellement planifiées pour être disponibles uniquement sur les références (SKU) axées sur le consommateur, telles que :

-   Windows Vista Starter
-   Windows Vista Édition Familiale Basique
-   Windows Vista Édition Familiale Premium
-   Windows Vista Édition Intégrale

Le contrôle parental s’installe uniquement sur ces références (SKU). Les solutions qui doivent être déployées sur les références SKU de l’entreprise devront :

-   Détectez et ne fournissez pas de fonctionnalités de contrôle parental sur les références métier.
-   Détectez et fournissez un autre moyen de configuration, de journalisation et de restrictions.

Il est recommandé que les solutions détectent la disponibilité de l’infrastructure de contrôle parental en vérifiant la réussite de COM CoCreateInstance sur l’API de conformité.

les applications prenant en charge les contrôles parentaux en fonction de l’infrastructure Windows Vista peuvent également vouloir supprimer une de leurs propres paramètres ou d’autres fonctionnalités lorsque l’interface utilisateur des contrôles parentaux est supprimée sur une référence SKU prise en charge. Une fonction est fournie pour une détermination de visibilité qui couvre des cas tels que la suppression jointe à un domaine.

 

 



