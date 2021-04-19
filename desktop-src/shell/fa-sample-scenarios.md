---
description: Dans l’exemple suivant, une société de développement de logiciels hypothétique appelée Litware, Inc.
ms.assetid: e4392907-a84f-40ea-aa88-2ad0510bca3c
title: Exemple d’association de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23b92922bb907c4dd90b3e2bdc3d16c8e8b52e6a
ms.sourcegitcommit: b0d03febac36ff77cba034615b94ea103311398d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/19/2021
ms.locfileid: "107715787"
---
# <a name="file-association-example"></a>Exemple d’association de fichiers

Dans l’exemple suivant, une société de développement de logiciels hypothétique, appelée Litware, Inc., crée un nouveau lecteur audio appelé LitwarePlayer. Litware souhaite concevoir une association de fichiers entre LitwarePlayer et son type de fichier primaire, qui utilise un format audio nouvellement développé qui permet à un CD audio entier d’être stocké en moins de 10 kilo-octets de mémoire sans perte de qualité.

> [!IMPORTANT]
> Cette rubrique ne s’applique pas à Windows 10. Le mode de fonctionnement des associations de fichiers par défaut dans Windows 10. Pour plus d’informations, consultez la section sur les **modifications apportées à la façon dont Windows 10 gère les applications par défaut** dans [cette publication](https://blogs.windows.com/windows-insider/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

## <a name="designing-a-new-file-association"></a>Conception d’une nouvelle association de fichiers

La société doit effectuer les étapes suivantes.

1.  **Déterminez si le nouveau type de fichier doit être considéré comme public ou privé.** Ce nouveau type de fichier est un type de média. Étant donné que les utilisateurs échangent des fichiers multimédias sur différentes plateformes et qu’il peut y avoir d’autres applications qui doivent lire le format LitwarePlayer, un type de fichier [public](fa-file-types.md) est le plus approprié.
2.  **Déterminez si ce type de fichier est déjà défini.** Vérifiez la base de données MIME IANA (Internet Assigned Numbers Authority) et d’autres bases de données de type de fichier public sur Internet pour déterminer qu’aucun type de fichier comparable n’a été défini. Étant donné qu’il s’agit d’un nouveau format de fichier, vous devez définir un nouveau type de fichier.
3.  **Définissez une extension de nom de fichier pour le nouveau type de fichier.** Les développeurs choisissent le `.opa-ltw-audio` , qui intègre leur abréviation de fournisseur et une indication sur le contenu du fichier. La recherche détermine que l’extension n’est pas utilisée par un autre utilisateur. Conformément aux recommandations actuelles, aucune extension brève n’est définie.
4.  **Définissez un type MIME pour le type de fichier et inscrivez-le auprès de l’IANA.** Litware définit le nouveau type MIME comme *audio/LitwarePlayer. 1* et prépare une application de type MIME, conformément aux directives énoncées dans les numéros RFC 2045, 2046, 2047 et 2048. Ils envoient ensuite l’application à l’IANA, qui ajoute le nouveau type de fichier à la base de données des types MIME inscrits.
5.  **Déterminez si un ProgID existe pour le type de fichier.** Étant donné qu’il s’agit d’un nouveau type de fichier, aucun [ProgID](fa-progids.md) n’existe pour celui-ci. Litware définit la conception d’un nouveau ProgID pour LitwarePlayer. Ils décident du nom convivial « LitwarePlayer Audio Player » (qui est stocké en tant que ressource dans le fichier LitwarePlayer.exe), et ils conçoivent une icône par défaut à utiliser pour les fichiers associés à LitwarePlayer (également stockés dans LitwarePlayer.exe). Étant donné que LitwarePlayer est une nouvelle application, il s’agit d’un ProgID version 1.
6.  **Enregistrez le ProgID.** Lorsque LitwarePlayer est installé, le programme d’installation crée l’entrée [ProgID](fa-progids.md) suivante dans le registre.

    ```
    HKEY_CLASSES_ROOT
       Litware.LitwarePlayer.1
          (Default) = LitwarePlayer Audio Player
          FriendlyTypeName = @LitwarePlayer, -120
          CurVer
             (Default) = Litware.LitwarePlayer.1
          DefaultIcon
             (Default) = LitwarePlayer, -142
          shell
             play
                command
                   (Default) = "%ProgramFiles%\LitwarePlayer\LitwarePlayer.exe" "%1"
    ```

    Dans la clé de commande, %1 est passé en tant que chemin d’accès au fichier à lire.

7.  **Enregistrez l’extension de nom de fichier pour le type de fichier.** Lorsque LitwarePlayer est installé, le programme d’installation crée les entrées suivantes dans le registre pour son extension de type de fichier personnalisé.

    ```
    HKEY_CLASSES_ROOT
       .opa-vwi-audio
          (Default) = Litware.LitwarePlayer.1
          PerceivedType = Audio
          Content Type = audio/LitwarePlayer
    ```

> [!Note]  
> Chaque fois qu’une association de fichier est créée ou modifiée, avertissez le système qu’une modification a été apportée en appelant [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), en spécifiant l' \_ événement ASSOCCHANGED SHCNE. Si ce n’est pas le cas, l’interpréteur de commandes peut ne pas reconnaître les modifications apportées tant que le système n’a pas redémarré.

 

## <a name="additional-resources"></a>Ressources supplémentaires

-   [Présentation des associations de fichiers](fa-intro.md)
-   [Inscription d’un navigateur Internet ou d’un client de messagerie à l’aide du menu Démarrer de Windows](start-menu-reg.md)
-   [Inscription d’une application dans un schéma d’URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Meilleures pratiques pour les associations de fichiers](fa-best-practices.md)
</dt> <dt>

[Instructions pour la gestion des applications par défaut dans Windows Vista et versions ultérieures](vista-managing-defaults.md)
</dt> <dt>

[Programmes par défaut](default-programs.md)
</dt> <dt>

[Définir l’accès aux programmes et les paramètres par défaut de l’ordinateur (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
