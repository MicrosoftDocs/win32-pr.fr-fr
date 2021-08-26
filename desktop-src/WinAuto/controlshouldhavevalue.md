---
title: ControlShouldHaveValue
description: ControlShouldHaveValue
ms.assetid: 90C37CC5-21D2-4D26-B6D9-2C95C52127BF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6ced460fac38552e0b82396e6bbbcf92e90c341e40b289e332a3f188c7e4ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998739"
---
# <a name="controlshouldhavevalue"></a>ControlShouldHaveValue

## <a name="text"></a>Texte

Un contrôle avec le rôle {0} doit avoir une valeur, mais obtenir \_ accValue n’est pas implémenté

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

Un élément ne fournit pas de valeur comme prévu en fonction du rôle MSAA attribué, ce qui implique que l’élément n’a pas la méthode [**\_ accValue obtenue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) . Par exemple, les rôles MSAA suivants doivent tous fournir une valeur.

-   \_ComboBox système de rôle \_
-   \_adresse IP du système de rôle \_
-   \_lien système de rôle \_
-   système de rôle \_ \_ OUTLINEITEM
-   \_PROGRESSBAR du système de rôle \_
-   \_curseur système de rôle \_
-   \_SPINBUTTON du système de rôle \_
-   \_ScrollBar système de rôle \_
-   \_texte du système de rôle \_

Ce problème est un problème pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car un élément ayant une valeur intrinsèque doit pouvoir signaler cette valeur à un utilisateur.

## <a name="possible-causes"></a>Causes possibles

Un rôle MSAA est défini de manière inappropriée pour l’élément ou son parent.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IAccessible :: \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Rôles d’objet**](object-roles.md)
</dt> </dl>

 

 




