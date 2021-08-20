---
description: les propriétés utilisées dans le système de propriétés de Windows Vista et versions ultérieures sont déclarées dans les schémas de propriété.
ms.assetid: 4e301210-df3a-41db-a58e-015ee8d41714
title: Création de propriétés personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33ebd18c799dca757c1cf7e5b2f16fd35edb6072a52f7d1f5d41749ec0b8341
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117685559"
---
# <a name="creating-custom-properties"></a>Création de propriétés personnalisées

les propriétés utilisées dans le système de propriétés de Windows Vista et versions ultérieures sont déclarées dans les schémas de propriété. ces schémas de propriété sont définis dans des fichiers XML et décrivent les différents aspects d’une propriété, y compris son type (y compris les informations sur son type primitif et s’il s’agit de plusieurs valeurs), la manière dont elle peut être affichée dans l’interface utilisateur Windows, le type d’étiquettes (chaînes d’édition conviviales) à utiliser et la façon dont elle est mise en cache dans le Les propriétés sont identifiées par leur nom canonique ou leur clé de propriété (nom de la clé).

Un nom canonique est le nom convivial du lecteur de la propriété et utilise une convention d’espace de noms similaire à celle utilisée dans Microsoft .NET. pour les propriétés définies par le système (celles incluses dans Windows), la convention est `System.GroupName.PropertyName` . Notez que le schéma de casse Pascal, qui met en majuscules les lettres au début de chaque mot, est utilisé dans ces noms. Les noms canoniques sont utilisés dans différents emplacements, notamment les listes de propriétés et les noms de colonnes dans le cache de propriétés. ils sont donc utilisés dans les requêtes langage SQL (SQL) pour récupérer une valeur de propriété.

Un mot-n est une paire de valeurs comprenant un GUID et une **valeur DWORD**, respectivement appelés *formatID* et *propID* . Elle est représentée par une structure [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) . La plupart des API du système de propriétés acceptent ces clés de propriété. le kit de développement logiciel (SDK) Windows comprend le fichier d’en-tête Propkey. h qui comprend une définition de macro de chacune des `System` clés de propriété avec la convention de `PKEY_GroupName_PropertyName` . Par exemple, `PKEY_Photo_DateTaken` est la clé de propriété de la propriété avec le nom canonique `System.Photo.DateTaken` . Les valeurs de propriété sont stockées sous la forme d’une structure [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) , qui est une extension des types OLE variant.

Cette section contient la rubrique suivante, qui fait partie intégrante de la création de propriétés personnalisées :

-   [Présentation du schéma de description de propriété](./propdesc-schema-entry.md)

> [!Note]  
> En raison des problèmes potentiels que l’indexeur peut avoir lors de l’utilisation du schéma du système de propriétés, il est essentiel de définir des attributs avec soin et de façon stratégique pour la première version du schéma. Toutes les modifications apportées aux attributs (type, largeur de colonne, qu’il s’agisse de indexible) ne seront pas reflétées dans la base de données après l’inscription d’un schéma. Pour que ces modifications soient reconnues après que le schéma a été inscrit une fois sur un système, il suffit de reconstruire l’index, puis d’inscrire le nouveau schéma, ou d’inscrire le schéma, puis de créer une nouvelle propriété pour chaque version ultérieure. par exemple `PKEY_GroupName_PropertyNameV2` , `PKEY_GroupName_PropertyNameV3` , et ainsi de suite). Nous vous déconseillons de créer de nouvelles propriétés de cette manière, car plusieurs colonnes superflues peuvent avoir un impact sur les performances du système.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Implémentation de gestionnaires de propriétés](./building-property-handlers.md)
</dt> <dt>

[Schéma de la description de propriété](./propdesc-schema-entry.md)
</dt> </dl>

 

 
