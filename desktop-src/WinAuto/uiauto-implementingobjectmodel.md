---
title: ObjectModel (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de IObjectModelProvider, y compris des informations sur les méthodes. Le modèle de contrôle ObjectModel est utilisé pour exposer un pointeur vers le modèle objet sous-jacent d’un document.
ms.assetid: 90A6937E-0E98-41EF-8EEB-E23CB71510E4
keywords:
- UI Automation, implémentation du modèle de contrôle ObjectModel
- UI Automation, modèle de contrôle ObjectModel
- UI Automation, IObjectModelProvider
- IObjectModelProvider
- implémentation du modèle de contrôle ObjectModel d’UI Automation
- ObjectModel (modèle de contrôle)
- modèles de contrôle, IObjectModelProvider
- modèles de contrôle, implémenter UI Automation ObjectModel
- modèles de contrôle, ObjectModel
- interfaces, IObjectModelProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ff115233faf19f93963153a0b2a0a1ff52c3f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010489"
---
# <a name="objectmodel-control-pattern"></a>ObjectModel (modèle de contrôle)

Fournit des instructions et des conventions pour l’implémentation de [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider), y compris des informations sur les méthodes. Le modèle de contrôle **ObjectModel** est utilisé pour exposer un pointeur vers le modèle objet sous-jacent d’un document.

De nombreuses applications implémentent des modèles d’objets enrichis qui ajoutent une valeur au-delà de ce que fournit Microsoft UI Automation. Ce modèle de contrôle permet à un client de naviguer à partir d’un élément UI Automation dans le modèle objet sous-jacent.

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **IObjectModelProvider**](#required-members-for-iobjectmodelprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **ObjectModel** , notez les conventions et recommandations suivantes :

-   La méthode [**IObjectModelProvider :: GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) doit retourner un pointeur vers l’objet le plus proche possible de l’élément d’interface utilisateur source. Par exemple, dans un navigateur Web, un fournisseur UI Automation pour un élément unique doit retourner un pointeur de modèle objet pour l’élément. Le retour d’un pointeur de modèle objet pour la racine du document serait beaucoup moins utile.
-   Le client du modèle de contrôle **ObjectModel** est supposé avoir l’IID pour l’interface qu’il recherche, ce qui explique pourquoi il suffit de retourner un pointeur [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) simple.
-   Dans la mesure où UI Automation marshale le pointeur vers le processus client, le fournisseur doit s’attendre à ce que le client accède au modèle objet à l’aide des pratiques COM (Component Object Model) standard.

## <a name="required-members-for-iobjectmodelprovider"></a>Membres requis pour **IObjectModelProvider**

La méthode suivante est requise pour l’implémentation de l’interface [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) .



| Membres nécessaires                                                                             | Type de membre | Notes                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) | Méthode      | Retourne un pointeur COM vers le modèle objet sous-jacent. Le client est censé appeler la méthode [**IUnknown :: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour récupérer des pointeurs de modèle objet spécifiques. |



 

Ce modèle de contrôle n’est associé aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 