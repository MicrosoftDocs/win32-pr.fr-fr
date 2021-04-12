---
title: Contrôles (COM)
description: Commandes
ms.assetid: 73947c81-6727-4112-9da0-efa60360f458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f440fff8f855f70c1a5ab3df78a6f6f6ed365ea
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104316974"
---
# <a name="controls-com"></a>Contrôles (COM)

Un contrôle ActiveX n’est qu’un autre terme pour un objet OLE ou plus spécifiquement, un objet COM. En d’autres termes, un contrôle, au moins, est un objet COM qui prend en charge l’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) et est également auto-inscrit. Via [**IUnknown :: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) , un conteneur peut gérer la durée de vie du contrôle, ainsi que découvrir de manière dynamique l’étendue complète des fonctionnalités d’un contrôle en fonction des interfaces disponibles. Cela permet à un contrôle d’implémenter le moins de fonctionnalités qu’il le doit, au lieu de prendre en charge un grand nombre d’interfaces qui ne font rien. En résumé, cette exigence minimale pour ne pas dépasser **IUnknown** permet à un contrôle d’être aussi léger que possible.

En résumé, autre que [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) et auto-inscription, aucune autre exigence n’est requise pour un contrôle. Toutefois, il existe des conventions qui doivent être suivies en ce qui concerne la prise en charge d’une interface, en termes de fonctionnalités fournies au conteneur par le contrôle. Cette section décrit ensuite ce que cela signifie pour qu’un contrôle prenne en charge une interface, ainsi que les méthodes, propriétés et événements qu’un contrôle doit fournir comme ligne de base s’il a l’occasion de prendre en charge des méthodes, des propriétés et des événements.

Pour plus d'informations, voir les rubriques suivantes :

-   [Inscription automatique pour les contrôles](self-registration-for-controls.md)
-   [Prise en charge d’une interface](what-support-for-an-interface-means.md)
-   [Interfaces de persistance](persistence-interfaces.md)
-   [Méthodes facultatives dans les interfaces de contrôle](optional-methods-in-control-interfaces.md)
-   [Options de fabrique de classes](class-factory-options.md)
-   [Exposition des propriétés via IDispatch](properties.md)
-   [Exposer des méthodes par le biais de IDispatch](exposing-methods-through-idispatch.md)
-   [Événements dans les contrôles](events-in-controls.md)
-   [Pages de propriétés](property-pages.md)
-   [Propriétés ambiantes pour les contrôles](ambient-properties-for-controls.md)
-   [Utilisation des fonctionnalités du conteneur](using-the-container-s-functionality.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions relatives au contrôle ActiveX et au conteneur de contrôles](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




