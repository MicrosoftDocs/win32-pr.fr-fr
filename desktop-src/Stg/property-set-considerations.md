---
title: Considérations relatives aux jeux de propriétés
description: Il est fortement recommandé que les jeux de propriétés soient réduits, car le flux de jeu de propriétés est lu en mémoire avant qu’une seule propriété puisse être lue ou écrite.
ms.assetid: 520db05e-81cd-40ef-af89-471d7194c634
keywords:
- Considérations relatives aux jeux de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f1ce6ba761922619c2e52d8a311249bf72ddf7d31ea157c11468f472fd88367
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992389"
---
# <a name="property-set-considerations"></a>Considérations relatives aux jeux de propriétés

Il est fortement recommandé que les jeux de propriétés soient réduits, car le flux de jeu de propriétés est lu en mémoire avant qu’une seule propriété puisse être lue ou écrite. « Small » signifie moins de 32 kilo-octets de données. Cela présente rarement un problème, car en général, les propriétés « en ligne » sont des éléments de petite taille, tels que des chaînes descriptives, des mots clés, des horodatages, des nombres, des noms d’auteur, des identificateurs globaux uniques (GUID), des identificateurs de classe (CLSID), etc.

Pour stocker des segments de données plus volumineux, ou dans les cas où la taille totale d’un ensemble de propriétés associées dépasse bien la quantité recommandée, l’utilisation de types non simples, tels que **VT \_ Stream** et **VT \_ Storage** , est fortement recommandée. Celles-ci ne sont pas stockées dans le flux de jeu de propriétés, de sorte qu’elles n’affectent pas de manière significative la surcharge initiale de la première opération d’accès et d’écriture d’une propriété. Il y a une surcharge minimale, car le flux de jeu de propriétés contient le nom de la propriété de flux ou de valeur de stockage frères, ce qui réduit le temps de traitement.

Pour plus d'informations, consultez les pages suivantes :

-   [Considérations relatives à l’implémentation de IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)
-   [Stockage des jeux de propriétés](storing-property-sets.md)
-   [Caractéristiques de performances](performance-characteristics.md)
-   [Implémentation du jeu de propriétés d’informations de résumé](implementing-the-summary-information-property-set.md)

 

 




