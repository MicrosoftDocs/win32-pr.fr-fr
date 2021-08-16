---
title: Compréhension des problèmes de performances
description: Cette rubrique décrit les problèmes de performances associés à l’utilisation des modèles de contrôle Text et TextRange.
ms.assetid: D78BFFA8-E303-441D-9D32-AD22E1B1A249
keywords:
- clients, comprendre les problèmes de performances
- clients, contrôles textuels
- clients, plages de texte
- clients, modèle de contrôle de texte
- clients, modèle de contrôle TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24846fea2f35cd9d265ab4f898b60dba2fc4e959b9a0f8bd7baea4661855f0a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861219"
---
# <a name="understanding-performance-issues"></a>Compréhension des problèmes de performances

Cette rubrique décrit les problèmes de performances associés à l’utilisation des modèles de contrôle [Text et TextRange](uiauto-implementingtextandtextrange.md) .


Les interfaces [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) et [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) s’appuient sur des appels interprocessus ; elles ne fournissent pas de mécanisme de mise en cache pour améliorer les performances lors de la récupération ou du traitement de contenu textuel.

Une application cliente peut améliorer les performances à l’aide de la méthode [**IUIAutomationTextRange :: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) pour récupérer des blocs de texte de taille modérée. Par exemple, l’utilisation de **gettext** pour récupérer des caractères uniques entraînera un impact sur les performances inter-processus pour chaque caractère, alors que la non-spécification d’une longueur maximale lors de l’appel de **gettext** entraînera un accès inter-processus, mais peut présenter une latence élevée selon la taille de la plage de texte.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèles de contrôle Text et TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Prise en charge d’UI Automation pour le contenu textuel](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Utilisation de contrôles textuels](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




