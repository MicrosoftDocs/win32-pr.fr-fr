---
title: ElementHasNoName
description: ElementHasNoName
ms.assetid: 893A758F-BD34-4ABE-A99E-8CABE33966E0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cde3597a0922159eb035e94e08691cf9d36a07f8a1c23ec0cb25280ab961faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829528"
---
# <a name="elementhasnoname"></a>ElementHasNoName

## <a name="text"></a>Texte

L’élément n’a pas de nom

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

Un élément n’a pas de nom. Par exemple, l’élément n’a pas d’accName implémenté et une chaîne vide est retournée lorsque la méthode [**\_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) est utilisée pour récupérer le nom MSAA de l’élément.

Ce problème entraîne des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car un élément peut être mal identifié à l’utilisateur.

## <a name="possible-causes"></a>Causes possibles

-   L’élément ou son parent n’a aucun nom ou étiquette.
-   Un [**accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) qui suggère que l’élément a un nom est assigné à l’élément.
-   L’élément qui a le focus ne doit pas recevoir le focus. Par exemple, une étiquette ou un contrôle désactivé.
-   Un contrôle invisible a reçu le focus.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IAccessible :: \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propriété Name](name-property.md)
</dt> </dl>

 

 




