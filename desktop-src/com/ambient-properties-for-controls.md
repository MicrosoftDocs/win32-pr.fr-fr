---
title: Propriétés ambiantes pour les contrôles
description: Propriétés ambiantes pour les contrôles
ms.assetid: 19aa3bc2-1605-43e1-acf4-ab782d012539
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 421a643873e818d8f5c0e006b4bb9049c1230c5f4e18525cdf7ed2b4175797bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994059"
---
# <a name="ambient-properties-for-controls"></a>Propriétés ambiantes pour les contrôles

Si un contrôle prend en charge toutes les propriétés ambiantes, il doit au moins respecter les valeurs des propriétés ambiantes suivantes dans les conditions indiquées dans le tableau suivant en utilisant les DISPID standard.



| Propriété ambiante            | Égal          | Commentaire/conditions d’utilisation                                                                                                                                                                                                                                                                |
|-----------------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocaleID<br/>         | -705<br/> | Si les paramètres régionaux sont significatifs pour le contrôle, par exemple pour la sortie de texte<br/>                                                                                                                                                                                                                  |
| UserMode <br/>        | -709<br/> | Si le contrôle se comporte différemment en mode utilisateur (conception) et en mode exécution<br/>                                                                                                                                                                                                          |
| UIDead<br/>           | -710<br/> | Si le contrôle réagit aux événements d’interface utilisateur, il doit honorer cette propriété ambiante<br/>                                                                                                                                                                                                 |
| ShowGrabHandles<br/>  | -711<br/> | Si le contrôle prend en charge le redimensionnement sur place de lui-même<br/>                                                                                                                                                                                                                             |
| ShowHatching<br/>     | -712<br/> | Si le contrôle prend en charge l’activation sur place et l’activation de l’interface utilisateur<br/>                                                                                                                                                                                                                   |
| DisplayAsDefault<br/> | -713<br/> | Uniquement si le contrôle est marqué OLEMISC \_ ACTSLIKEBUTTON (ce qui signifie que la prise en charge des mnémoniques de clavier est fournie, [**IOleControl :: GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) et [**IOleControl :: OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) doivent être implémentés).<br/> |



 

Comme décrit précédemment, l’utilisation d’ambiances nécessite à la fois [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (pour [**OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) au minimum) et [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (pour [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) et [**GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)).

Le \_ bit OLEMISC SETCLIENTSITEFIRST peut ne pas nécessairement être pris en charge par un conteneur. Dans ces circonstances, un contrôle doit recourir à des valeurs par défaut pour les propriétés ambiantes dont il a besoin.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôles](controls.md)
</dt> </dl>

 

 





