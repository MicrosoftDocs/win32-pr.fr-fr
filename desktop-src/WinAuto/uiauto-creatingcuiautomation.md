---
title: Création de l’objet CUIAutomation
description: Cette section décrit comment prendre en main l’écriture d’une application cliente UI Automation Microsoft en instanciant un objet qui implémente IUIAutomation.
ms.assetid: 9b90da60-0204-48c1-bb16-ff4a843bac67
keywords:
- clients, création d’un objet CUIAutomation
- clients, objet CUIAutomation
- UI Automation, objet CUIAutomation
- UI Automation, création d’un objet CUIAutomation
- création de l’objet CUIAutomation
- Objet CUIAutomation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8162dac5276bbb22d00413276482cca34334fda5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941049"
---
# <a name="creating-the-cuiautomation-object"></a>Création de l’objet CUIAutomation

Cette section décrit comment prendre en main l’écriture d’une application cliente UI Automation Microsoft en instanciant un objet qui implémente [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).

Cette rubrique contient les sections suivantes.

-   [Objet CUIAutomation](#the-cuiautomation-object)
-   [Création de l’objet](#creating-the-object)
-   [Rubriques connexes](#related-topics)

## <a name="the-cuiautomation-object"></a>Objet CUIAutomation

La première étape de l’utilisation d’UI Automation consiste à créer un objet de la classe [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) . Cet objet expose l’interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) , qui est la passerelle vers tous les autres objets et interfaces utilisés par les applications clientes. Entre autres choses, **IUIAutomation** est utilisé pour les tâches suivantes :

-   Abonnement à des événements.
-   Création de conditions. Les conditions sont des objets utilisés pour limiter l’étendue des recherches d’éléments UI Automation.
-   Obtention d’éléments UI Automation directement à partir du Bureau (élément racine), ou à partir de coordonnées d’écran ou de handles de fenêtre.
-   Création d’objets de l’Explorateur d’arborescence qui peuvent être utilisés pour naviguer dans la hiérarchie des éléments UI Automation.
-   Conversion des types de données.

## <a name="creating-the-object"></a>Création de l’objet

Pour commencer à utiliser UI Automation dans votre application, procédez comme suit :

-   Incluez UIAutomation. h dans les en-têtes de votre projet. UIAutomation. h apporte les autres en-têtes qui définissent l’API.
-   Déclarez un pointeur vers [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).
-   Initialisez le modèle COM (Component Object Model).
-   Créez une instance de [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) et récupérez l’interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) dans votre pointeur.

L’exemple de fonction suivant initialise COM, puis crée l’objet [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) , en extrayant l’interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) dans le pointeur *ppAutomation* .


```C++
#include <uiautomation.h>

// CoInitialize must be called before calling this function, and the  
// caller must release the returned pointer when finished with it.
// 
HRESULT InitializeUIAutomation(IUIAutomation **ppAutomation)
{
    return CoCreateInstance(CLSID_CUIAutomation, NULL,
        CLSCTX_INPROC_SERVER, IID_IUIAutomation, 
        reinterpret_cast<void**>(ppAutomation));
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des événements UI Automation](uiauto-eventsoverview.md)
</dt> <dt>

[Obtention d'éléments UI Automation](uiauto-obtainingelements.md)
</dt> </dl>

 

 