---
title: ControlShouldHaveValue
description: ControlShouldHaveValue
ms.assetid: 90C37CC5-21D2-4D26-B6D9-2C95C52127BF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b078712319ffcfde386df519837ba467ca2fcf4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196937"
---
# <a name="controlshouldhavevalue"></a>ControlShouldHaveValue

## <a name="text"></a>Texte

Un contrôle avec le rôle {0} doit avoir une valeur, mais obtenir \_ accValue n’est pas implémenté

## <a name="type"></a>Type

Error

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

 

 




