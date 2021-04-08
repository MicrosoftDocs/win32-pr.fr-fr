---
title: Propriétés du contrôle
description: Propriétés du contrôle
ms.assetid: 29c2cca3-9460-45d1-9591-026e8c18f26f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4749a7a7e408f6cd58951a72207ed801e4104d65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840785"
---
# <a name="control-properties"></a>Propriétés du contrôle

En plus des propriétés définies et implémentées par le contrôle lui-même, la technologie des contrôles ActiveX implique également :

<dl> <dt>

<span id="Ambient_properties"></span><span id="ambient_properties"></span><span id="AMBIENT_PROPERTIES"></span>Propriétés ambiantes
</dt> <dd>

Celles-ci sont exposées par le conteneur via un site client de contrôle afin de fournir des valeurs environnementales qui s’appliquent à tous les contrôles incorporés dans le conteneur. Par exemple, un conteneur peut fournir une couleur d’arrière-plan par défaut ou une police par défaut que le contrôle peut utiliser. Les propriétés ambiantes sont exposées par le biais de **IDispatch** implémenté sur l’objet site d’un conteneur. Le conteneur appelle la méthode [**IOleControl :: OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) du contrôle quand l’une de ses propriétés ambiantes change la valeur. En réponse, un contrôle peut avoir besoin de mettre à jour son propre état interne ou visuel en réponse. Le conteneur indique la propriété ambiante qui a changé avec le paramètre DISPID ou peut passer DISPID \_ Unknown pour indiquer que plusieurs propriétés ambiantes ont changé.

</dd> <dt>

<span id="Extended_properties"></span><span id="extended_properties"></span><span id="EXTENDED_PROPERTIES"></span>Propriétés étendues
</dt> <dd>

Ils sont implémentés par un conteneur pour encapsuler les contrôles qu’il contient pour fournir des propriétés gérées par le conteneur qui s’affichent comme s’il s’agissait de propriétés de contrôle natif. Le conteneur peut agréger le contrôle, en ajoutant les propriétés étendues pour compléter ou substituer les propriétés du contrôle. L’objet agrégé est appelé un contrôle étendu. Pour le conteneur, le contrôle étendu apparaît comme le contrôle lui-même et les propriétés étendues semblent être exposées par le contrôle. Le conteneur prend en charge un contrôle étendu par le biais de sa méthode de site client [**IOleControlSite :: GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol). La méthode **GetExtendedControl** permet aux contrôles de naviguer dans le site jusqu’à l’objet de contrôle étendu fourni pour eux par le conteneur, si le conteneur prend en charge cette fonctionnalité. Un conteneur peut également choisir d’afficher les pages de propriétés de ses contrôles étendus, en plus des pages qu’un contrôle spécifie normalement par le biais de [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages). Pour cette raison, un contrôle doit demander à un conteneur d’afficher un frame de propriété avant que le contrôle ne tente de le faire. Le contrôle appelle [**IOleControlSite :: ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe) pour effectuer cette opération. Si le conteneur implémente cette fonction, il affiche le frame de propriété lui-même ; Si la méthode retourne une erreur, le contrôle peut afficher le frame de propriété.

</dd> </dl>

Pour plus d'informations, voir les rubriques suivantes :

-   [Propriétés standard](standard-properties.md)
-   [Objet de police standard](standard-font-object.md)
-   [Objet image standard](standard-picture-object.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Méthodes de contrôle](control-methods.md)
</dt> </dl>

 

 




