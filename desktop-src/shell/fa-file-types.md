---
description: Cette rubrique explique comment créer de nouveaux types de fichiers et comment associer votre application à votre type de fichier et à d’autres types de fichiers bien définis.
ms.assetid: 055648cd-46ce-4e61-80b2-bcf1d1823e20
title: Types de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d697c42626c6e1ab3e0b5cc0b88bd065523d53a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973243"
---
# <a name="file-types"></a>Types de fichiers

Cette rubrique explique comment créer de nouveaux types de fichiers et comment associer votre application à votre type de fichier et à d’autres types de fichiers bien définis. Les fichiers avec une extension de nom de fichier commun partagée (. doc,. html, etc.) sont du même *type*. Par exemple, si vous créez un éditeur de texte, vous pouvez utiliser le type de fichier. txt existant. Dans d’autres cas, vous devrez peut-être créer un nouveau type de fichier.

Cette rubrique est organisée comme suit :

-   [Types de fichiers publics et privés](#public-and-private-file-types)
-   [Enregistrement d’un type de fichier](#registering-a-file-type)
    -   [Définition des sous-clés facultatives et des attributs d’extension de type de fichier](#setting-optional-subkeys-and-file-type-extension-attributes)
    -   [Suppression des informations du registre lors de la désinstallation](#deleting-registry-information-during-uninstallation)
-   [Types de fichiers prenant en charge les métadonnées ouvertes](#file-types-that-support-open-metadata)
-   [Rubriques connexes](#related-topics)

Vous trouverez des informations supplémentaires dans les rubriques suivantes :

-   [Comment choisir une extension de type de fichier](how-to-choose-a-file-type-extension.md)
-   [Comment définir des attributs de type de fichier](./how-to-define-file-type-attributes.md)
-   [Comment inclure une application dans la boîte de dialogue Ouvrir avec](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [Comment exclure une application de la boîte de dialogue Ouvrir avec pour les types de fichiers non associés](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)

## <a name="public-and-private-file-types"></a>Types de fichiers publics et privés

Les types de fichiers publics sont également appelés types populaires ou contentieuses, car les applications concurrentes peuvent souhaiter être associées à ces types de fichiers. Les caractéristiques des types de fichiers publics sont les suivantes :

-   Elles sont généralement définies par des corps de normes et/ou sont promues par leurs organisations de définition en tant que formats d’échange.
-   Ils sont souvent échangés entre les ordinateurs et les utilisateurs à des fins diverses.
-   Ils doivent être pris en charge sur de nombreuses plateformes différentes.
-   Les applications de plusieurs fournisseurs sont susceptibles de les gérer.

Voici quelques exemples de types de fichiers considérés comme étant publics : types de fichiers image. png,. gif,. jpg et. bmp, et types audio. wav,. mp3 et. au.

Contrairement aux types de fichiers publics, les types de fichiers privés ou propriétaires ont généralement un format qui est implémenté et interprété par une seule application ou un seul fournisseur. Par conséquent, les types de fichiers privés ne sont généralement pas sujets aux conflits entre les applications. Certains types de fichiers peuvent démarrer en tant que types de fichiers privés, mais deviennent par la suite des types de fichiers publics.

> [!Note]  
> Windows ne fait pas la distinction entre les types de fichiers publics et privés. La distinction est pertinente uniquement pour prendre des décisions sur votre choix d’inscription de type de fichier.

 

## <a name="registering-a-file-type"></a>Enregistrement d’un type de fichier

Pour associer le type de fichier à une application existante, localisez le ProgID de l’application dans le registre. Pour associer le type de fichier à une nouvelle application, définissez un ProgID pour votre application. Pour plus d’informations sur la définition d’un nouveau ProgID, consultez [identificateurs par programmation](fa-progids.md).

Les sous-clés d’extension de nom de fichier se présentent sous la forme générale suivante : ProgID d' *extension* = . Les sous-clés d’extension de nom de fichier sont stockées dans la sous-arborescence **\_ \_ racine de classes HKEY** .

Il est important d’inclure le point de début (.) lors de la création de sous-clés de type de fichier dans le registre. Par exemple, si vous souhaitez qu’un type de fichier avec l’extension Short. MYP et l’extension long. MYP-file soit ouvert avec une application appelée MyProgram, utilisez la syntaxe suivante :

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = ApplicationVendor.MyProgram
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
```

Comme illustré dans l’exemple précédent, si vous inscrivez également une extension de nom de fichier Short (. MYP), vous devez créer une sous-clé pour l’extension longue (fichier. MYP). Pour plus d’informations, consultez [gestionnaires de types de fichiers](fa-file-extensions.md).

### <a name="setting-optional-subkeys-and-file-type-extension-attributes"></a>Définition des sous-clés facultatives et des attributs d’extension de type de fichier

Les entrées d’extension de type de fichier dans le registre ont plusieurs sous-clés et attributs facultatifs.

Les entrées d’extension de type de fichier utilisées par les associations de fichiers sont décrites dans le tableau suivant. Toutes les valeurs sont du type de **Registre \_ SZ** .



| Entrée de Registre  | Action                                                                                                                                                                                                                                                                                                                             |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Default         | Définissez la valeur par défaut de la sous-clé d’extension sur le ProgID auquel elle est liée.                                                                                                                                                                                                                                                 |
| Type de contenu    | Définissez la valeur type de contenu sur le type de contenu MIME du type de fichier.                                                                                                                                                                                                                                                                   |
| OpenWithList    | Ne pas utiliser. Cette sous-clé contient une ou plusieurs sous-clés d’application pour les applications qui s’affichent dans l’entrée de la boîte de dialogue **Ouvrir avec** pour le type de fichier et est destinée uniquement aux applications. exe sur les systèmes d’exploitation antérieurs à Windows XP. Utilisez OpenWithProgIds à la place.                                                            |
| OpenWithProgIds | Cette sous-clé contient une liste d’autres ProgID pour ce type de fichier. Les programmes pour ces ProgID s’affichent dans le menu **Ouvrir avec** et sont disponibles en tant qu’applications du Windows Store par défaut pour le type de fichier. Chaque fois qu’une application prend le contrôle de ce type de fichier en modifiant la valeur par défaut, elle doit également ajouter une entrée à cette liste. |
| PerceivedType   | Définissez la valeur PerceivedType sur le PerceivedType auquel le fichier appartient, le cas échéant. Cette chaîne n’est pas utilisée par les versions de Windows antérieures à Windows Vista. Pour plus d’informations, consultez [types perçus et inscription des applications](fa-perceivedtypes.md).                                                                           |



 

La forme générale d’une sous-clé d’extension de nom de fichier est la suivante. Tous les types d’entrée sont du type de **Registre \_ SZ** .

```
HKEY_CLASSES_ROOT
   .ext
      (Default) = ProgID.ext.1
      Content Type = MIME content type
      PerceivedType = PerceivedType
      OpenWithProgids
         ProgID2.ext.1
         ProgID3.ext.1
      ProgID.ext.1
         shellnew
```

Considérations importantes à propos des types de fichiers :

-   La sous-arborescence **\_ \_ racine de classes HKEY** est une vue formée en fusionnant les classes de logiciels de l' **\_ \_ utilisateur actuel HKEY** \\  \\  et les classes de logiciel **HKEY \_ local \_ machine** \\  \\ 
-   En général, **la \_ \_ racine de classes HKEY** est destinée à être lue à partir de, mais n’est pas écrite dans. Pour plus d’informations, consultez l’article [ \_ \_ racine des classes HKEY](../sysinfo/hkey-classes-root-key.md) .
-   Pour inscrire globalement un type de fichier sur un ordinateur particulier, créez une entrée pour le type de fichier dans la sous-clé de classes de logiciels de l' **\_ \_ ordinateur local HKEY** \\  \\  .
-   Pour que l’inscription d’un type de fichier soit visible pour l’utilisateur actuel uniquement, créez une entrée pour le type de fichier dans la sous-clé de classes de logiciels de la clé **HKEY \_ Current \_ User** \\  \\  .
-   Une application peut fournir sa propre implémentation d’un verbe, tel que Open ou Play, comme indiqué dans l’exemple de Registre suivant.

    ```
    HKEY_CLASSES_ROOT
       Applications
          ApplicationName.exe
             shell
                verb
    ```

    Les sous-clés de la sous-clé de verbe incluent la ligne de commande et la méthode cible de déplacement : **Command** et **dropTarget**.

-   Lorsque vous créez ou modifiez une association de fichiers, il est important d’informer le système que vous avez apporté une modification. Pour ce faire, appelez [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) et spécifiez l’événement **\_ ASSOCCHANGED SHCNE** . Si vous n’appelez pas **SHChangeNotify**, la modification peut ne pas être reconnue tant que le système n’a pas été redémarré.
-   Pour récupérer les informations de Registre relatives à une association de fichiers, utilisez l’interface [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) . Pour un scénario qui illustre cette procédure, consultez [exemple de scénario d’association de fichiers](fa-sample-scenarios.md).

> [!Note]  
> Les sous-clés de registre des **applications** et des **chemins d’application** sont utilisées pour enregistrer et contrôler le comportement du système pour le compte des applications. Pour plus d’informations sur cette fonctionnalité, consultez [inscription de l’application](app-registration.md).

 

### <a name="deleting-registry-information-during-uninstallation"></a>Suppression des informations du registre lors de la désinstallation

Lors de la désinstallation d’une application, les ProgID et la plupart des autres informations de Registre associées à cette application doivent être supprimés dans le cadre de la désinstallation. Toutefois, les applications qui ont pris possession d’un type de fichier (en définissant la valeur par défaut de la sous-clé HKEY. extension **\_ \_ racine** du type de fichier \\  sur le ProgID de l’application) ne doivent pas tenter de supprimer cette valeur lors de la désinstallation de. Le fait de laisser les données en place pour la valeur par défaut évite de déterminer si une autre application a pris possession du type de fichier et a remplacé la valeur par défaut après l’installation de l’application d’origine. Windows respecte la valeur par défaut uniquement si le ProgID a trouvé un ProgID enregistré. Si le ProgID n’est pas inscrit, il est ignoré.

Notez que d’autres informations sur la propriété du type de fichier sont stockées dans la sous-arborescence de l' **\_ \_ utilisateur actuel HKEY** et sont également utilisées uniquement lorsque l’application à laquelle elle fait référence est inscrite. Par conséquent, il n’est pas nécessaire de supprimer ces données lors de la désinstallation d’une application.

À titre d’exemple, le code suivant montre l’état du Registre avant la désinstallation d’une application :

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID
      shell
         open
            command
               (Default) = yourapp.exe %1
```

L’exemple suivant montre l’état de ces mêmes entrées de registre après la désinstallation de l’application.

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID subkey removed
```

## <a name="file-types-that-support-open-metadata"></a>Types de fichiers prenant en charge les métadonnées ouvertes

Dans Windows 7 et versions ultérieures, les types de fichiers suivants prennent en charge les métadonnées ouvertes.



| Type de fichier                                                               | Extensions de nom de fichier                                          |
|-------------------------------------------------------------------------|---------------------------------------------------------------|
| Documents Office 2007                                                   | . docx,. xlsx,. pptx                                           |
| Documents Office 97-2003                                                | . doc,. xls,. ppt                                              |
| Recherche enregistrée                                                            | . search-ms                                                    |
| Formats basés sur Windows Media (conteneur ASF) | . wmv,. WMA                                                    |
| MP4 (gestionnaire de propriétés)                                                  | . MP4,. M4A,. m4v,. mp4v,. M4P,. M4B,. 3gp,. 3GPP,. 3GP2,. mov |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription de l’application](app-registration.md)
</dt> <dt>

[Fonctionnement des associations de fichiers](fa-how-work.md)
</dt> <dt>

[Affichage du contenu par type de fichier ou par type](prophand-content-view.md)
</dt> <dt>

[Vérificateur de type de fichier](file-type-verifier.md)
</dt> <dt>

[Gestionnaires de types de fichiers](fa-file-extensions.md)
</dt> <dt>

[Identificateurs programmatiques](fa-progids.md)
</dt> <dt>

[Types perçus](fa-perceivedtypes.md)
</dt> <dt>

[Tableaux d’association](fa-associationarray.md)
</dt> </dl>

 

 
