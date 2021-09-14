---
description: Découvrez comment créer un gestionnaire de propriétés qui lit et écrit des propriétés vers et à partir d’un flux de fichier. Chaque gestionnaire est associé à un type de fichier donné.
ms.assetid: 9dacd399-2cf3-40dd-9501-f26f0281500d
title: Implémentation de gestionnaires de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aadfabf451d5a90ba88925d28f3f460aaeeb28f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231582"
---
# <a name="implementing-property-handlers"></a>Implémentation de gestionnaires de propriétés

dans Windows Vista et versions ultérieures, les métadonnées sont devenues centrales comme une méthode d’organisation d’éléments tels que des fichiers, des messages électroniques ou des contacts. pour activer un système où les éléments peuvent être recherchés en fonction de leurs métadonnées et où les utilisateurs peuvent lire ou écrire ces métadonnées, Windows Vista a introduit un nouveau système de propriétés. Les métadonnées de ce système sont représentées par un ensemble extensible de propriétés. Dans cet ensemble de rubriques, nous décrivons comment vous pouvez créer un gestionnaire qui lit et écrit des propriétés vers et à partir d’un flux de fichier. Ces gestionnaires sont appelés gestionnaires de propriétés et chacun d’eux est associé à un type de fichier donné, identifié par l’extension de nom de fichier.

Les rubriques suivantes décrivent les exigences et les stratégies impliquées dans la définition de vos propriétés et gestionnaires de propriétés.

-   [Fonctionnement des gestionnaires de propriétés](./building-property-handlers-properties.md)
-   [Utilisation des noms de genres](./building-property-handlers-user-friendly-kind-names.md)
-   [Utilisation des listes de propriétés](./building-property-handlers-property-lists.md)
-   [Initialisation des gestionnaires de propriétés](./building-property-handlers-property-handlers.md)
-   [Inscription et distribution des gestionnaires de propriétés](./prophand-reg-dist.md)
-   [Meilleures pratiques pour le gestionnaire de propriétés et FAQ](./prophand-bestprac-faq.yml)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de propriétés personnalisées](./building-property-handlers-property-schemas.md)
</dt> <dt>

[Schéma de la description de propriété](./propdesc-schema-entry.md)
</dt> </dl>

 

 
