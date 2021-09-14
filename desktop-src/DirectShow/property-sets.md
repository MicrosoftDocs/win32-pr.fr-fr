---
description: Jeux de propriétés
ms.assetid: 4b8a917f-7a6c-4433-83f4-b83ef6d26115
title: Jeux de propriétés (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdc65efbc99eeed3a5f94ab33ce5ec982975852
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094673"
---
# <a name="property-sets-directshow"></a>Jeux de propriétés (DirectShow)

Microsoft DirectShow utilise des jeux de propriétés pour prendre en charge les services étendus proposés par le matériel et les pilotes et filtres associés. Les fournisseurs de matériel et de filtre peuvent définir de nouvelles fonctionnalités en tant que propriétés, les réorganiser dans les jeux de propriétés et publier la spécification pour ces jeux de propriétés. En tant que développeur d’applications, vous pouvez utiliser les méthodes de l’interface [**IKsPropertySet**](ikspropertyset.md) pour déterminer si un pilote ou un filtre prend en charge un ensemble de propriétés particulier, et récupérer ou définir ces propriétés.

Toutes les méthodes exposées par **IKsPropertySet** requièrent un **GUID** qui identifie le jeu de propriétés (le paramètre *GuidPropSet* ) et une valeur **DWORD** qui identifie la propriété dans le jeu de propriétés (le paramètre *dwPropID* ). Le paramètre *dwPropID* est généralement un membre d’un type de données énuméré.

Les propriétés individuelles peuvent avoir des données associées que vous spécifiez dans le paramètre *pPropData* dans les méthodes [**IKsPropertySet :: Set**](ikspropertyset-set.md) et [**IKsPropertySet :: obtenir**](ikspropertyset-get.md) . Dans ces méthodes, les données de propriété sont typées comme un pointeur vers `void` . Le type de données et la signification des données sont spécifiés dans la définition du jeu de propriétés.

Les sections suivantes fournissent des informations sur les jeux de propriétés pris en charge dans DirectShow :

-   [**Jeu de propriétés protection de copie de DVD**](dvd-copy-protection-property-set.md)
-   [**Jeu de propriétés Karaoké DVD**](dvd-karaoke-property-set.md)
-   [**Jeu de propriétés de sous-image de DVD**](dvd-subpicture-property-set.md)
-   [Ensemble de propriétés de transport d’appareil externe](external-device-transport-property-set.md)
-   [Jeu de propriétés du pas à pas de frame](frame-stepping-property-set.md)
-   [Épingler le jeu de propriétés](pin-property-set.md)
-   [**Définition de la propriété change rate**](rate-change-property-set.md)

 

 



