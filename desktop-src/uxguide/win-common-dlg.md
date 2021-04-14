---
title: Boîtes de dialogue courantes
description: Les boîtes de dialogue communes à Microsoft Windows se composent des boîtes de dialogue Ouvrir un fichier, enregistrer un fichier, ouvrir le dossier, Rechercher et remplacer, imprimer, mise en page, police et couleur.
ms.assetid: 3f9fb0c9-bc1a-48c4-b021-99f155f8ea9e
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 336cb368fa25bf68313e2bf336de68845a87e663
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104393840"
---
# <a name="common-dialogs"></a>Boîtes de dialogue courantes

> [!NOTE]
> Ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Les boîtes de dialogue communes à Microsoft Windows se composent des boîtes de dialogue Ouvrir un fichier, enregistrer un fichier, ouvrir le dossier, Rechercher et remplacer, imprimer, mise en page, police et couleur.

## <a name="open-file"></a>Ouvrir un fichier

![capture d’écran de la boîte de dialogue Ouvrir ](images/win-common-dlg-image1.png)

L’ouverture du fichier est optimisée pour la recherche rapide d’éléments à utiliser avec un programme.

## <a name="save-file"></a>Enregistrer le fichier

![capture d’écran de la boîte de dialogue Enregistrer sous ](images/win-common-dlg-image2.png)

Enregistrer le fichier ferme la boucle en enregistrant un fichier avec ses métadonnées.

## <a name="open-folder"></a>Ouvrir un dossier

![capture d’écran de la boîte de dialogue Rechercher des fichiers/dossiers ](images/win-common-dlg-image3.png)

Ouvrir le dossier est spécifiquement destiné à choisir des dossiers.

## <a name="find-and-replace"></a>Rechercher et remplacer

![capture d’écran des boîtes de dialogue Rechercher et remplacer ](images/win-common-dlg-image4.png)

Find permet aux utilisateurs de rechercher des chaînes de texte, tandis que la version de remplacement permet éventuellement aux utilisateurs de remplacer des correspondances par une autre chaîne.

## <a name="print"></a>Imprimer

![capture d’écran de la boîte de dialogue Imprimer ](images/win-common-dlg-image5.png)

Imprimer permet aux utilisateurs de sélectionner les éléments à imprimer, le nombre de copies à imprimer et la séquence de classement, ainsi que la possibilité de choisir et de configurer des imprimantes.

## <a name="page-setup"></a>Mise en page

![capture d’écran de la boîte de dialogue mise en page ](images/win-common-dlg-image6.png)

La mise en page permet aux utilisateurs de sélectionner le format du papier et la source, l’orientation de la page et les marges.

## <a name="font"></a>Police

![capture d’écran de la boîte de dialogue police ](images/win-common-dlg-image7.png)

Police affiche les polices et les tailles en points des polices installées disponibles.

## <a name="color"></a>Couleur

![capture d’écran de la boîte de dialogue Modifier les couleurs ](images/win-common-dlg-image8.png)

Couleur permet aux utilisateurs de sélectionner une couleur, soit via un ensemble prédéfini de couleurs, soit en choisissant une couleur « personnalisée ».

## <a name="design-concepts"></a>Principes de conception

Les boîtes de dialogue courantes vous aident à offrir aux utilisateurs une expérience cohérente dans différents programmes. En utilisant bien les boîtes de dialogue courantes, vous aidez également les utilisateurs à bénéficier d’une expérience efficace et agréable.

Vous pouvez améliorer considérablement l’expérience des utilisateurs avec ces boîtes de dialogue en choisissant les valeurs par défaut les plus appropriées pour :

-   Valeurs d’entrée (exemples : dossiers par défaut, noms de fichiers par défaut).
-   Options sélectionnées (exemples : imprimante sélectionnée, options d’impression).
-   Vues (exemples : affichage d’images en mode miniature, affichage d’images sans noms de fichiers, Tri par date, largeur de colonne).
-   Présentation (exemples : taille de la fenêtre, emplacement et contenu).

Vous devez déterminer les valeurs par défaut initiales et les valeurs par défaut suivantes. Les valeurs initiales par défaut sont déterminées par votre programme et basées sur l’utilisation prévue de l’utilisateur cible, tandis que les valeurs par défaut suivantes sont basées sur l’utilisation réelle. L’utilisation passée est le meilleur indicateur de l’utilisation future.

Les valeurs par défaut de votre programme sont-elles efficaces ? Surveillez le nombre d’étapes que les utilisateurs doivent effectuer pour effectuer les tâches les plus courantes. Si les utilisateurs doivent répéter les mêmes étapes, éventuellement inutiles chaque fois qu’ils exécutent une tâche, vos valeurs par défaut peuvent être améliorées.

**Si vous n’avez qu’une seule chose...**

Donnez aux utilisateurs une expérience efficace et agréable en sélectionnant les paramètres initiaux appropriés et les valeurs par défaut suivantes.

## <a name="is-this-the-right-user-interface"></a>S’agit-il de l’interface utilisateur appropriée ?

**Oui! Utilisez les boîtes de dialogue courantes pour une expérience utilisateur cohérente. Ne créez pas les vôtres.** Il est particulièrement difficile de créer des interfaces utilisateur personnalisées qui parcourent l’espace de noms correctement et en toute sécurité. Notez que vous pouvez personnaliser les boîtes de dialogue courantes si nécessaire.

Pour Windows Vista, le fichier ouvert et le fichier d’enregistrement ont une nouvelle architecture extensible pour faciliter l’exposition de fonctionnalités supplémentaires. Ce mécanisme est suffisamment flexible pour répondre aux exigences minimales des principaux éditeurs de logiciels indépendants (ISV), mais ne peut pas être interrompu par les futures versions de Windows.

## <a name="guidelines"></a>Consignes

### <a name="general"></a>Général

-   Le cas échéant, fournissez des alternatives plus directes ou [non](glossary.md) . Autoriser les utilisateurs à :
    -   Ouvrez les fichiers en les déposant sur votre programme.
    -   Enregistrez les fichiers en utilisant leur nom et leur emplacement actuels à l’aide d’une commande Save.
    -   Rechercher l’occurrence suivante d’une chaîne à l’aide de la touche F3.
    -   Imprimez une copie d’un document entier sur l’imprimante par défaut à l’aide d’une commande Imprimer.
    -   Modifiez les polices et les attributs de police à l’aide d’une barre d’outils ou d’une fenêtre de palette.
    -   Modifiez les couleurs à l’aide d’une barre d’outils ou d’une fenêtre de palette.
-   Utilisez les commandes suivantes pour afficher des boîtes de dialogue communes (fournies avec leurs [clés d’accès](glossary.md)préférées) :



|                              |                                               |
|------------------------------|-----------------------------------------------|
| **Boîte de dialogue courante**<br/> | **Commande**<br/>                        |
| Ouvrir un fichier<br/>         | Ouvrir…<br/>                            |
| Enregistrer le fichier<br/>         | Enregistrer sous...<br/>                         |
| Ouvrir un dossier<br/>       | Ouvrir le dossier... ou choisissez un dossier...<br/> |
| Rechercher et remplacer<br/>  | Rechercher... ou remplacer...<br/>              |
| Imprimer<br/>             | Imprimer...<br/>                           |
| Mise en page<br/>        | Mise en page...<br/>                      |
| Police<br/>              | Police... ou choisir la police...<br/>          |
| Couleur<br/>             | Couleur... ou choisir une couleur...<br/>        |



 

-   Vous pouvez utiliser des commandes plus spécifiques, le cas échéant. Exemple : pour l’exportation d’un fichier, utilisez le fichier d’exportation de commande au lieu de enregistrer sous.
-   Définissez le titre de la boîte de dialogue en fonction de la commande qui l’a lancée. Exemple : si l’option Enregistrer le fichier est lancée à partir d’une commande exporter un fichier, renommez la boîte de dialogue en exporter le fichier.

### <a name="open-file"></a>Ouvrir un fichier

-   Pour le dossier par défaut initial, utilisez un dossier spécialisé (images, musique, vidéos), le cas échéant, utilisez des documents.
-   Pour les dossiers par défaut suivants, utilisez le dernier dossier ouvert par l’utilisateur à l’aide du programme.
-   Lors de l’ouverture de fichiers photo, supprimer les noms de fichiers par défaut. Les photos sont généralement identifiées par leurs miniatures et leurs noms ne sont généralement pas significatifs.

### <a name="save-file"></a>Enregistrer le fichier

-   Pour le dossier par défaut initial (si un nouveau fichier est enregistré pour la première fois), utilisez le dossier spécialisé (images, musique, vidéos), le cas échéant, utilisez des documents.
-   Pour les fichiers temporaires, utilisez le dossier temporaire de l’utilisateur actuel. Choisissez des noms de fichiers simples, mais uniques. Exemple : utilisez File0001. tmp au lieu de ~ DF1A92. tmp.
    -   **Développeurs :** Vous pouvez récupérer le dossier temporaire de l’utilisateur actuel à l’aide de la fonction d’API GetTempPath.
-   Pour le nom de fichier par défaut initial, utilisez un nom par défaut unique basé sur :
    -   Contenu du fichier, s’il est connu. Exemple : les premiers mots d’un document.
    -   Modèle choisi par l’utilisateur. Exemple : si le fichier précédent s’intitule « Hawaii 1.jpg », choisissez « Hawaii 2.jpg » comme fichier suivant.
    -   Modèle générique basé sur le type de fichier. Exemple : « Photo1.jpg ».
-   Pour les valeurs par défaut suivantes (si le fichier existe déjà), utilisez le dossier et le nom actuels du fichier.
-   Lorsque vous enregistrez un fichier, conservez sa date de création. Si votre programme enregistre des fichiers en créant un fichier temporaire, supprime l’original et renomme le fichier temporaire avec le nom de fichier d’origine, veillez à copier la date de création à partir du fichier d’origine.
-   Utilisez enregistrer le fichier si l’utilisateur sélectionne la commande enregistrer sans spécifier de nom de fichier.

### <a name="file-types-lists"></a>Listes de types de fichiers

**Remarque :** Les listes de types de fichiers sont utilisées par Open file et Save file pour déterminer les types de fichiers affichés et l’extension de fichier par défaut.

-   Si la liste types de fichiers est abrégée (au maximum, il s’agit de cinq), classez la liste selon la probabilité d’utilisation. Si la liste est longue (six ou plus), utilisez un ordre alphabétique pour faciliter la recherche des types.
-   Pour enregistrer le fichier, incluez toutes les variantes des extensions de fichier prises en charge, même si elles sont rares, et placez d’abord l’extension la plus courante. La logique de gestion des fichiers examine cette liste pour déterminer si l’utilisateur a fourni une extension de fichier prise en charge. Exemple : si une liste de types de fichiers JPEG comprend uniquement des fichiers. jpg et. jpeg, le fichier test. jpe peut être enregistré en tant que test.jpe.jpg.
-   Pour le fichier d’enregistrement, le type de fichier par défaut initial est le plus probablement choisi par l’utilisateur cible. La valeur par défaut suivante est le type actuel du fichier.
-   Pour Open file, le type de fichier par défaut initial est le plus probablement choisi par l’utilisateur cible. La valeur par défaut suivante doit être le dernier type de fichier utilisé.
-   Pour ouvrir un fichier, incluez une entrée « tous les fichiers » comme premier élément si les utilisateurs peuvent ouvrir n’importe quel type de fichier, ou peuvent avoir besoin de voir tous les fichiers dans un dossier en même temps. Envisagez de fournir d’autres filtres de métadonnées, tels que « toutes les images », « tout la musique » et « toutes les vidéos ». Placez-les immédiatement après « tous les fichiers ».
-   Utilisez le format «nom du type de fichier ( \* . EXT1 ; \* . ext2).» Le nom du type de fichier doit être le nom du type de fichier inscrit, que vous pouvez afficher dans l’élément options du dossier du panneau de configuration. Exemple : «document HTML ( \* . htm ; \* . html).»
    -   **Exception :** Pour les filtres de métadonnées, supprimez la liste d’extensions de fichier pour éliminer tout encombrement. Exemples : « tous les fichiers », « toutes les images », « tout le contenu » et « toutes les vidéos ».
-   Utilisez la mise [en majuscules de style phrase](glossary.md) pour les noms de types de fichier et les extensions de type de fichier en minuscules.

### <a name="open-folder"></a>Ouvrir un dossier

-   **Pour les nouveaux programmes, utilisez la boîte de dialogue Ouvrir des fichiers dans le mode « choisir des dossiers ».** Si vous avez besoin de Windows Vista ou d’une version ultérieure, utilisez la boîte de dialogue Ouvrir un dossier pour les programmes qui s’exécutent dans les versions antérieures de Windows.
    -   **Développeurs :** Vous pouvez utiliser la boîte de dialogue Ouvrir des fichiers dans le mode « sélectionner des dossiers » à l’aide de l' \_ indicateur Fos PICKFOLDERS.

### <a name="font"></a>Police

-   Si nécessaire, vous pouvez filtrer la liste des polices pour afficher uniquement les polices disponibles pour votre programme.

### <a name="persistence"></a>Persistance

-   Envisagez de rendre les valeurs suivantes persistantes pour les utiliser comme valeurs par défaut suivantes :
    -   Valeurs d’entrée (exemples : dossiers par défaut, noms de fichiers par défaut).
    -   Options sélectionnées (exemples : imprimante sélectionnée, options d’impression).
    -   Vues (exemples : affichage d’images en mode miniature, affichage d’images sans noms de fichiers, Tri par date, largeur de colonne).
    -   Présentation (exemples : taille de la fenêtre, emplacement et contenu).

**Exception :** Ne rendez pas ces valeurs persistantes pour les boîtes de dialogue courantes lorsque leur utilisation est telle que les utilisateurs sont beaucoup plus susceptibles de démarrer complètement.

-   Lorsque vous déterminez les valeurs par défaut, réfléchissez aux utilisateurs cibles les plus susceptibles de le faire en fonction des scénarios importants. Tenez également compte des scénarios au sein d’une instance de programme, sur plusieurs instances (à la fois consécutives ou simultanées) et sur plusieurs documents. Ne rendez pas les valeurs persistantes dans des circonstances qui ne sont pas susceptibles d’être utiles.
    -   **Exemple :** Pour une application basée sur les documents standard, il est utile d’utiliser les paramètres Open file et Save file persistants dans une instance de programme et sur des instances consécutives, tout en conservant les instances simultanées indépendantes. De cette façon, les utilisateurs peuvent travailler efficacement avec plusieurs documents à la fois.
-   Rendez les paramètres persistants en fonction du programme, par utilisateur.

 

