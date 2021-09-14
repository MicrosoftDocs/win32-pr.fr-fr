---
title: Définition des propriétés des objets animés ou mobiles
description: Pour les contrôles d’animation, tels que le contrôle d’animation affiché lors de la copie de fichiers, utilisez le \_ rôle objet d’animation de système de rôle \_ .
ms.assetid: 8c5ebbc3-4066-452b-8f37-2fb595adea53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1551899305968471bf1425b5cc043be8329c2bd4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010630"
---
# <a name="setting-properties-for-animated-or-moving-objects"></a>Définition des propriétés des objets animés ou mobiles

Pour les contrôles d’animation, tels que le contrôle d’animation affiché lors de la copie de fichiers, utilisez le rôle objet d' [**\_ \_ animation de système de rôle**](object-roles.md) . Pour les graphiques qui sont parfois animés, utilisez le rôle d’objet [**\_ \_ graphique de système de rôle**](object-roles.md) avec l' [**État**](state-property.md) défini sur [**système d’état \_ \_ animé**](object-state-constants.md).

Utilisez l’indicateur d' [**état \_ \_ animé du système d’État**](object-state-constants.md) pour marquer un objet dont l’apparence change rapidement. Les clients utilisent cet indicateur pour éviter de notifier les utilisateurs à plusieurs reprises pour ce qui est vraiment une seule série de modifications visuelles.

C’est le cas, par exemple, du texte défilant, qui est divulgué progressivement à mesure qu’il défile sur l’écran. Ces objets reçoivent l’attribut de [**système d' \_ état \_ animé**](object-state-constants.md). Dans la plupart des cas, la chaîne de [**valeur**](value-property.md) de l’objet reflète l’intégralité du texte, même la partie qui n’est pas actuellement visible. La modification fréquente de la chaîne de **valeur** pour qu’elle corresponde au texte actuellement visible n’est pas recommandée, car cela entraîne un trop grand nombre d’événements de [**VALUECHANGE d' \_ objets \_ d’événement**](event-constants.md) qui ne communiquent pas d’informations utiles.

Par exemple, dans une fenêtre qui contient une zone rectangulaire qui affiche le mot « oui ! » dans le cadre d’un modèle figure-huit, le [**rôle**](role-property.md) est [**graphique de \_ système \_ de rôle**](object-roles.md), la propriété [**valeur**](value-property.md) est la chaîne affichée, la propriété [**emplacement**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) est le rectangle englobant autour du texte, et l’indicateur d’attribut [**animé du \_ système \_ d’État**](object-state-constants.md) est défini. La [**Description**](description-property.md) est « le mot oui ! » se déplace à travers l’écran dans un modèle à huit chiffres.» Le serveur génère uniquement les événements d' [**\_ objet \_ STATECHANGE**](event-constants.md) lorsque l’objet démarre ou arrête l’animation.

 

 




