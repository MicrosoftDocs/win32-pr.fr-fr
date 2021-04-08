---
description: Décrit les paramètres de stratégie d’alimentation qui composent un mode de gestion de l’alimentation.
ms.assetid: cd515cd6-67f4-45d0-b769-3abc7a56faa8
title: Paramètres de stratégie d’alimentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f490c758a890faf314be1ddffe9ac7a503bd473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756573"
---
# <a name="power-policy-settings"></a>Paramètres de stratégie d’alimentation

Les modes de gestion de l’alimentation et les schémas sont des préférences et des paramètres de stratégie.

Un mode de gestion de l’alimentation se compose d’un groupe de préférences de paramètres d’alimentation. Ces préférences se composent à la fois d’une valeur AC et DC pour chacun des paramètres d’alimentation. Chaque mode de gestion de l’alimentation est identifié par un **GUID** unique, ainsi qu’un nom convivial. Windows Vista offre trois modes de gestion de l’alimentation par défaut : l’économiseur d’énergie, l’équilibre et les performances élevées. Ces plans peuvent être personnalisés et des plans supplémentaires peuvent être créés. Tous les modes de gestion de l’alimentation ont un attribut de personnalité qui indique le comportement d’économie d’énergie global du plan.

Le tableau suivant présente les trois personnalités du mode de gestion de l’alimentation. 

| Nom complet     | Description                                                                   | **GUID**                             |
|------------------|-------------------------------------------------------------------------------|--------------------------------------|
| Économiseur d’énergie      | Offre des performances réduites, ce qui peut augmenter les économies d’énergie.                | a1841308-3541-4fab-bc81-f71556f20b4a |
| Équilibrée         | Équilibre automatiquement les performances et la consommation d’énergie en fonction de la demande. | 381b4222-f694-41f0-9685-ff5bb260df2e |
| Hautes performances | Offre des performances maximales au détriment de la consommation d’énergie.      | 8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c |



 

> [!Note]  
> Les appareils qui prennent en charge le mode [veille moderne](/windows-hardware/design/device-experiences/modern-standby) autorisent uniquement le mode de gestion de l’alimentation **équilibré** . La **mise en veille moderne** est la solution la plus récente et rationalisée pour la gestion des paramètres d’alimentation.

 

Chaque ordinateur dispose d’un mode de gestion de l’alimentation unique et actif. Par défaut, les utilisateurs non privilégiés sont en mesure d’accéder aux paramètres d’alimentation du système. L’accès à tous les paramètres d’alimentation ou individuels peut être contrôlé via des ACL sur les paramètres d’alimentation ou par le biais de stratégie de groupe. Les applications doivent appeler [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) pour déterminer si l’utilisateur a accès au paramètre d’alimentation.

Chaque paramètre d’alimentation est identifié par un **GUID** unique et comprend un nom convivial, une description, des valeurs autorisées et des valeurs par défaut pour AC et DC. Les paramètres d’alimentation personnalisés peuvent être créés à l’aide de la fonction [**PowerCreateSetting**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modes de gestion de l’alimentation](power-schemes.md)
</dt> </dl>

 

 
