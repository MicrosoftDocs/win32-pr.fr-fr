---
title: DuplicateSiblingIDs
description: DuplicateSiblingIDs
ms.assetid: 942385A4-BD14-4046-9ABC-110B32D96BB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27ba2ccca45234bb49fc782c5522b4e446d77a2c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511648"
---
# <a name="duplicatesiblingids"></a>DuplicateSiblingIDs

## <a name="text"></a>Texte

L’ID Automation dupliqué \\ « {0} \\ » entraîne une ambiguïté entre les éléments.

## <a name="type"></a>Type

Error

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

 

 




