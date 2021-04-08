---
title: AccNameShouldNotContainRole
description: AccNameShouldNotContainRole
ms.assetid: 271461FF-5123-482F-B66D-A323CB3361DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fb91eeeb34d484c1f51cd0b7cd2d2947e86abda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675662"
---
# <a name="accnameshouldnotcontainrole"></a>AccNameShouldNotContainRole

## <a name="text"></a>Texte

Le nom de l’élément ( {0} ) ne doit pas contenir le texte du rôle de l’élément ( {1} )

## <a name="type"></a>Type

Avertissement

## <a name="description"></a>Description

Le nom d’un élément intègre son rôle MSAA ou le type de contrôle UIA. Par exemple, cet avertissement peut se produire si la méthode [**\_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) , qui est utilisée pour récupérer le nom MSAA d’un élément, retourne la valeur \_ « \_ ScrollBar système Role \_ \* ».

Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car le rôle est lu deux fois, ou il peut être non significatif ou non intuitif pour les utilisateurs.

## <a name="possible-causes"></a>Causes possibles

-   Un nom ou une étiquette n’est pas assigné à l’élément ou à son parent.
-   L’élément ou son parent a un nom par défaut qui n’a pas été révisé à un nom convivial. Par exemple, bouton 1.
-   Un développeur ne sait pas que les lecteurs d’écran lisent les noms.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IAccessible :: \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propriété Name](name-property.md)
</dt> </dl>

 

 




