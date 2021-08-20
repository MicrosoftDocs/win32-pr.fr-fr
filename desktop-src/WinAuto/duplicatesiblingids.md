---
title: DuplicateSiblingIDs
description: DuplicateSiblingIDs
ms.assetid: 942385A4-BD14-4046-9ABC-110B32D96BB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd9bb311d4aafdf1f509d3404cfe057f96f6bf378b822f6f77cab4943cea097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115356"
---
# <a name="duplicatesiblingids"></a>DuplicateSiblingIDs

## <a name="text"></a>Texte

L’ID Automation dupliqué \\ « {0} \\ » entraîne une ambiguïté entre les éléments.

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

Un élément a le même ID Automation qu’un autre élément.

Ce problème peut entraîner des problèmes d’automatisation qui empêchent le code de test de référencer l’élément correct.

## <a name="possible-causes"></a>Causes possibles

-   Les éléments frères ont le même ID Automation.
-   Implémentation incorrecte de la propriété UIA AutomationId.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement.CurrentAutomationId**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentautomationid)
</dt> </dl>

 

 




