---
description: Le système de propriétés contient une propriété appelée System. Kind, qui divise les éléments en types en fonction de l’extension de nom de fichier, et quels utilisateurs finaux peuvent facilement identifier avec.
ms.assetid: 1466b4c7-49ea-417a-ac94-7b45515ccb96
title: Utilisation des noms de genres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38d5f1432e7680cfed63c2c210375f3b7a300fae4563ca308a3b25b8751fb139
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971098"
---
# <a name="using-kind-names"></a>Utilisation des noms de genres

Le système de propriétés contient une propriété appelée `System.Kind` , qui divise les éléments en types en fonction de l’extension de nom de fichier, et quels utilisateurs finaux peuvent facilement identifier avec.

Cette rubrique est organisée comme suit :

-   [À propos de la propriété System. Kind](#about-the-systemkind-property)
-   [Hiérarchie des valeurs de type et inscription](#kind-value-hierarchy-and-registration)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="about-the-systemkind-property"></a>À propos de la propriété System. Kind

le genre a été introduit dans Windows Vista pour exprimer une notion plus conviviale de type de fichier. la `System.Kind` propriété divise les éléments en types et fournit un nom de type que les utilisateurs finaux peuvent identifier avec, tels que des Documents, des Musique, des images, etc. Par conséquent, les noms de types sont connus comme conviviaux. Étant donné que la `System.Kind` propriété est définie sur la même valeur pour les éléments du même type de fichier, et associe les éléments qui ont des caractéristiques similaires à une propriété commune, le système et l’utilisateur peuvent agir sur le groupe dans son ensemble. Par exemple, la `System.Kind` propriété peut être utilisée pour limiter une recherche aux éléments d’un type spécifique, afficher les propriétés les plus pertinentes pour un élément de l’affichage de contenu, ou regrouper des éléments similaires.

Comme Kind est une propriété de chaîne à valeurs multiples, vous pouvez avoir `audio;video` une `link;document` valeur de type ou. Une `System.Kind` valeur est une liste triée de valeurs de chaîne. Dans certains cas, il peut y avoir un seul élément dans cette liste. Dans d’autres cas, un élément peut appartenir à plusieurs types. Pour obtenir un exemple d’un élément appartenant à plusieurs genres, consultez l’exemple de clé de Registre dans cette rubrique. Les valeurs de chaîne proviennent d’un ensemble prédéfini de valeurs connues. Les valeurs sont comparées à l’aide de fonctions de comparaison de chaînes qui ne respectent pas la casse et qui ne respectent pas les paramètres régionaux. Ces chaînes ne sont pas localisées.

Certains noms de types sont déjà associés à des propriétés et des modèles de disposition. Par exemple, les éléments associés à `Kind.Picture` et les éléments associés à `Kind.Document` affichent des propriétés différentes, même lorsqu’ils sont dans la même vue, en raison des propriétés et des modèles de disposition qui sont déjà associés à ces deux noms de genres. Chaque genre d’élément peut être associé à l’un des quatre modèles de disposition uniques qui définit le nombre de propriétés affichées pour chaque élément et leur disposition. Pour plus d’informations, consultez [affichage du contenu basé sur l’Association type ou type de fichier](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).

## <a name="kind-value-hierarchy-and-registration"></a>Hiérarchie des valeurs de type et inscription

Une `Kind` valeur doit représenter l’une des valeurs de la liste suivante.

```
Item
   Folder
   Program
   Game
   WebHistory
   Feed
   Document
   Link
   Movie
   Music
   RecordedTV
   Video
   Picture
   Communications
      Calendar
      Contact
      E-Mail
      Task
      Journal
      Note
      InstantMessage
```

Les gestionnaires de propriétés peuvent déclarer leur `System.Kind` propriété de manière statique par le biais du Registre, ou ils peuvent fournir la valeur dynamiquement par le biais de leur code, comme c’est le cas avec une propriété standard.

Pour définir la propriété de manière statique `Kind` , une entrée de valeur **reg \_ SZ** est ajoutée sous la clé de Registre **KindMap** , comme indiqué dans l’exemple suivant.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     .recipe = Document
                     .ccc = Contact; Communications
```

Notez que `Kind` peut être une valeur unique ou plusieurs valeurs dans une chaîne délimitée par des points-virgules. Lorsque vous fournissez plusieurs valeurs, la valeur la plus spécifique `Kind` est indiquée en premier avec les éléments suivants les moins spécifiques. Dans l’exemple, contact est nommé en premier, car il est hiérarchiquement plus spécifique que les communications. L' **élément** de valeur est supposé et ne doit pas être explicitement fourni.

## <a name="additional-resources"></a>Ressources supplémentaires

-   Pour obtenir une documentation de référence sur les propriétés, consultez [System. Kind](./props-system-kind.md) et [System. KindText](./props-system-kindtext.md).
-   Pour plus d’informations sur la création de nouveaux ou l’utilisation des types de fichiers existants, consultez [types de fichiers](../shell/fa-file-types.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnement des gestionnaires de propriétés](./building-property-handlers-properties.md)
</dt> <dt>

[Utilisation des listes de propriétés](./building-property-handlers-property-lists.md)
</dt> <dt>

[Initialisation des gestionnaires de propriétés](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Inscription et distribution des gestionnaires de propriétés](./prophand-reg-dist.md)
</dt> <dt>

[Meilleures pratiques pour le gestionnaire de propriétés et FAQ](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
