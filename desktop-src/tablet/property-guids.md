---
description: Les Microsoft Recognizers utilisent les GUID suivants.
ms.assetid: dcf6bc5a-1b61-48f7-bc7a-f74ae6e2e57e
title: GUID de propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2eb089a9b3b5c7863f2d57d9a635b9ab042ae6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196247"
---
# <a name="property-guids"></a>GUID de propriété

Les Microsoft Recognizers utilisent les GUID suivants. Chaque fois que cela est possible, les applications doivent utiliser ces GUID. Toutefois, il est prévu et encouragé par d’autres programmeurs à utiliser des GUID supplémentaires pour les propriétés qui ne sont pas prises en charge par les Microsoft Recognizers.

Toutes les fonctions de propriété ont été développées en sachant que la liste des GUID peut être étendue par d’autres module de reconnaissance. Ces fonctions de propriété sont les suivantes :

-   [**GetContextPropertyList fonction)**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)
-   [**GetContextPropertyValue fonction)**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)
-   [**GetResultPropertyList fonction)**](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)
-   [**SetContextPropertyValue fonction)**](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)

Le tableau suivant répertorie les GUID des propriétés des Tablet PC définis dans msinkaut. h (installés dans c : \\ Program Files \\ Microsoft Tablet PC Platform SDK \\ include par défaut).



| GUID                                                  | Définition                                                                                   |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------|
| INKRECOGNITIONPROPERTY \_ BOXNUMBER<br/>          | Index de la boîte alternative du module de reconnaissance en mode zone<br/>                                    |
| INKRECOGNITIONPROPERTY \_ LINENUMBER<br/>         | Numéro de ligne<br/>                                                                   |
| \_segmentation INKRECOGNITIONPROPERTY<br/>       | Comment le module de reconnaissance segmente les mots et les caractères<br/>                                  |
| INKRECOGNITIONPROPERTY \_ HOTPOINT<br/>           | Point réactif du geste<br/>                                                             |
| INKRECOGNITIONPROPERTY \_ MAXIMUMSTROKECOUNT<br/> | Nombre maximal de traits pour un segment<br/>                                           |
| INKRECOGNITIONPROPERTY \_ POINTSPERINCH<br/>      | Métrique point par pouce<br/>                                                        |
| INKRECOGNITIONPROPERTY \_ CONFIDENCELEVEL<br/>    | [**Confiance \_**](/windows/win32/api/rectypes/ne-rectypes-confidence_level) Énumération de niveau<br/>                         |
| INKRECOGNITIONPROPERTY \_ LINEMETRICS<br/>        | Informations pour le calcul de la ligne de base, de la ligne médiane ou des deux, utilisée dans le treillis<br/> |



 

 

 




