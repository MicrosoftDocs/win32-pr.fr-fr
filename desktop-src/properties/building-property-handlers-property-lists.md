---
description: après avoir évalué votre stratégie de propriété, vous devez déterminer les propriétés à afficher dans l’interface utilisateur de l’explorateur de Windows, et où.
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: Utilisation des listes de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72289612d61ebfb198ec0f2ee3d4a7d206209e91
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477395"
---
# <a name="using-property-lists"></a>Utilisation des listes de propriétés

après avoir évalué votre stratégie de propriété, vous devez déterminer les propriétés à afficher dans l’interface utilisateur de l’explorateur de Windows, et où. Il existe différents emplacements où les propriétés sont affichées en lecture seule. La modification de propriété, en revanche, est uniquement activée dans la boîte de dialogue **Propriétés** . Cette boîte de dialogue peut être appelée via le lien **modifier les propriétés** dans le **volet de visualisation** ou le menu contextuel d’un élément.

Les listes de propriétés sont des chaînes délimitées par des points-virgules qui se présentent sous la forme suivante.


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



Le seul indicateur actuellement disponible est indiqué dans le tableau suivant.



| Indicateur | Description                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | N’affichez pas la propriété dans le **volet de visualisation** comme indiqué dans la valeur de clé de Registre **PreviewDetails** . Consultez l’exemple qui suit le tableau suivant si la valeur de cette propriété n’est pas définie. |



 

Une fois que vous avez défini une liste de propriétés, vous pouvez stocker cette chaîne dans le registre par le biais du système d' [Association de fichiers Shell](../shell/fa-file-types.md) standard sous **HKEY \_ classes \_ root.** Le tableau suivant récapitule les valeurs des listes de propriétés qui peuvent être assignées sous la clé de Registre pour une extension de nom de fichier particulière.




| Valeur | Description | 
|-------|-------------|
| FullDetails | Les propriétés s’affichent sous l’onglet <strong>Détails</strong> de la boîte de dialogue <strong>Propriétés</strong> . Il s’agit de la liste complète des propriétés prises en charge par le type de fichier. | 
| PreviewDetails | Les propriétés s’affichent dans le <strong>volet de visualisation</strong>. | 
| PreviewTitle | Les propriétés s’affichent dans la zone de titre du <strong>volet de visualisation</strong> en regard de la miniature de l’élément. Le nombre maximal d’entrées est de 3. Si la liste de propriétés contient plus que le nombre maximal autorisé, les autres entrées sont ignorées. | 
| TileInfo | Les propriétés sont affichées lorsque l’affichage de liste est en mode <strong>mosaïques</strong> . Le nombre maximal d’entrées est de 3. Si la liste de propriétés contient plus que le nombre maximal autorisé, les autres entrées sont ignorées.<blockquote>[!Note]<br />cette valeur était présente dans Windows XP.</blockquote><br /> | 
| ExtendedTileInfo | Les propriétés sont affichées pour un élément lorsque l’affichage de la liste est en mode <strong>mosaïque étendue</strong> . | 
| InfoTip | Les propriétés sont affichées dans une info-bulle quand un utilisateur pointe sur un élément.<blockquote>[!Note]<br />cette valeur était présente dans Windows XP.</blockquote><br /> | 
| QuickTip | Les propriétés s’affichent lorsqu’il est difficile de récupérer des propriétés directement à partir d’un élément, par exemple lorsque l’élément doit être accessible via une connexion réseau lente. Il est recommandé que les propriétés nommées ici, telles que le type ou la taille, ne requièrent pas l’ouverture du flux de fichier pour déterminer leur valeur.<blockquote>[!Note]<br />cette valeur était présente dans Windows XP.</blockquote><br /> | 




 

L’exemple ci-dessous définit la valeur PreviewDetails pour un type de fichier. Recipe, à l’aide d’un ProgID de **RecipeKey**.

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

Comme expliqué dans la rubrique [Association de fichiers Shell](../shell/fa-file-types.md) , les associations de fichiers peuvent être décrites pour le formulaire le plus spécifique au plus général. Le formulaire le plus spécifique est l’extension de nom de fichier unique et le formulaire le plus générique est une clé qui s’applique à tous les fichiers et dossiers de fichiers. Entre ces deux extrêmes, vous pouvez également définir un [ProgID](../shell/fa-progids.md) qui regroupe un ensemble d’extensions de nom de fichier (par exemple, les types .jpg et. jpeg regroupés en tant que **jpegfile**). Quand vous définissez des listes de propriétés, vous devez les définir pour les ProgID ou, dans certains cas, des extensions de nom de fichier spécifiques. Évitez d’utiliser des entrées étendues, telles que la clé **AllFileSystemObjects** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnement des gestionnaires de propriétés](./building-property-handlers-properties.md)
</dt> <dt>

[Utilisation des noms de genres](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Initialisation des gestionnaires de propriétés](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Inscription et distribution des gestionnaires de propriétés](./prophand-reg-dist.md)
</dt> <dt>

[Meilleures pratiques pour le gestionnaire de propriétés et FAQ](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
