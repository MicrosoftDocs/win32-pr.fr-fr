---
description: Cette section contient des informations sur les interfaces utilisées pour contrôler l’apparence et le comportement du panneau de saisie Tablet PC.
ms.assetid: 58f49d5b-8b38-45e7-94e1-8a4434d6e13b
title: Interfaces du panneau de saisie de texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 798dc60f34171ce7254bca74c27a51fa12eaba65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210600"
---
# <a name="text-input-panel-interfaces"></a>Interfaces du panneau de saisie de texte

Cette section contient des informations sur les interfaces utilisées pour contrôler l’apparence et le comportement du panneau de saisie Tablet PC.

> [!Note]  
> Les interfaces du panneau de saisie de texte ne sont pas compatibles avec Automation.

 

## <a name="in-this-section"></a>Dans cette section



| Interface                                                                | Description                                                                                                                                  |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interface IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) | Utilisé par le code d’entrée de texte personnalisé de l’application pour insérer le texte dans le champ de texte et dans le magasin de stockage des services de texte.<br/> |
| [**Interface ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)                     | Permet de contrôler le panneau de saisie Tablet PC.<br/>                                                                                  |
| [**Interface ITextInputPanelEventSink**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpaneleventsink)   | Définit des méthodes qui gèrent les événements de l' [**interface ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) .<br/>                                      |
| [**Interface ITextInputPanelRunInfo**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanelruninfo)       | Fournit une méthode pour déterminer si le panneau de saisie de texte est en cours d’exécution.<br/>                                                      |
| [**Interface ITipAutocompleteClient**](itipautocompleteclient.md)       | Permet au client d’appeler l’objet fournisseur de saisie semi-automatique du panneau de saisie du texte de l’application.<br/>                                      |
| [**Interface ITipAutocompleteProvider**](itipautocompleteprovider.md)   | Gère le côté de l’application de l’intégration de la saisie semi-automatique du panneau de saisie de texte.<br/>                                                 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence du panneau de saisie de texte](text-input-panel-reference.md)
</dt> </dl>

 

 




