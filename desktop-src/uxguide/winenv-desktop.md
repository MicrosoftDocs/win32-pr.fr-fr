---
title: Bureau
description: Le bureau est la zone de travail de l’utilisateur pour ses programmes. Ce n’est pas un moyen de promouvoir votre programme ou sa personnalisation. N’abusez pas.
ms.assetid: 99cb218d-9b1f-4e43-94d2-4ea74b0e10d3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: f72230d5177ed9f0714282a8eec7168994ba9bdfd60cdeff0b0409d714d216f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594060"
---
# <a name="desktop"></a>Bureau

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Le bureau est la zone de travail de l’utilisateur pour ses programmes. Ce n’est pas un moyen de promouvoir votre programme ou sa personnalisation. Ne vous inquiétez pas !

le bureau est la zone de travail à l’écran fournie par Microsoft Windows, analogue à un bureau physique. Il se compose d’une [zone de travail](glossary.md) et d’une [barre des tâches](winenv-taskbar.md). La zone de travail peut s’étendre sur plusieurs moniteurs.

![capture d’écran d’un bureau Windows classique ](images/winenv-desktop-image1.png)

un bureau Windows classique.

Le moniteur actif est le moniteur sur lequel le programme actif est en cours d’exécution. l’analyse par défaut est celle avec le menu Démarrer, la barre des tâches et la zone de notification.

## <a name="design-concepts"></a>Principes de conception

le bureau Windows dispose des points d’accès aux programmes suivants :

-   **Zone de travail.** Zone à l’écran où les utilisateurs peuvent effectuer leur travail, ainsi que pour stocker des programmes, des documents et leurs raccourcis. Techniquement, le bureau comprend la barre des tâches. dans la plupart des contextes, il fait uniquement référence à la zone de travail.
-   **Bouton Démarrer.** point d’accès pour tous les programmes et emplacements de Windows spéciaux (Documents, images, Musique, jeux, ordinateur, panneau de configuration), avec les listes de fichiers les plus récemment utilisées pour accéder rapidement aux programmes et Documents récemment utilisés.
-   **Lancement rapide. supprimé de Windows 7.** Point d’accès direct pour les programmes sélectionnés par l’utilisateur.
-   **Tâches.** Point d’accès pour l’exécution des programmes qui ont une présence sur le bureau. Bien que techniquement, la barre des tâches couvre l’ensemble de la barre du bouton Démarrer vers la zone de notification. dans la plupart des contextes, la barre des tâches fait référence à la zone comprise entre, contenant les boutons de la barre des tâches. Cette zone est parfois appelée TaskBand.
-   **Deskbands. Non recommandé.** Des programmes fonctionnels et de longue durée réduits, tels que la barre de langue. Les programmes qui réduisent à deskbands n’affichent pas les boutons de la barre des tâches lorsqu’ils sont réduits.
-   **Zone de notification.** Source à bref terme des notifications et de l’État, ainsi qu’un point d’accès pour les fonctionnalités système et de programme qui n’ont aucune présence sur le bureau.

![capture d’écran du bouton Démarrer, barre des tâches, miniature ](images/winenv-desktop-image2.png)

les points d’accès au bureau Windows incluent le bouton démarrer, la barre des tâches et la zone de notification. Notez la fonctionnalité miniature du bouton de la barre des tâches.

**le bureau Windows est une ressource partagée limitée qui est le point d’entrée de l’utilisateur pour Windows. Laissez les utilisateurs dans le contrôle.** Vous devez utiliser ses zones comme prévu ; toute autre utilisation doit être considérée comme un abus. Ne les affichez jamais comme des moyens de sensibiliser votre programme ou sa [personnalisation](exper-branding.md).

par Windows 7, les fabricants d’ordinateurs oem et les fabricants de matériel indépendants (ihv) peuvent utiliser Device Stage pour concevoir une interface utilisateur personnalisée et personnalisée pour l’ordinateur et les périphériques, sans encombrer les bureaux des utilisateurs. En particulier, les OEM peuvent utiliser Device Stage PC pour proposer des programmes personnalisés, des offres de service et un support technique. Pour plus d’informations, consultez le [Kit de développement Microsoft Device Experience](https://www.microsoft.com/whdc/device/DeviceExperience/Dev-Kit.mspx).

**Si vous n’avez qu’une seule chose...**

-   N’abusez pas du bureau, et gardez le contrôle des utilisateurs. Si vos utilisateurs cibles sont susceptibles d’utiliser votre programme fréquemment, fournissez une option lors de l’installation pour placer un raccourci sur le bureau, non sélectionné par défaut.

## <a name="guidelines"></a>Consignes

-   **Si vos utilisateurs sont très susceptibles d’utiliser votre programme fréquemment, fournissez une option lors de l’installation pour placer un raccourci de programme sur le bureau.** La plupart des programmes ne sont pas utilisés suffisamment souvent pour garantir l’offre de cette option.
-   **Présente l’option désélectionnée par défaut.** Demander aux utilisateurs de sélectionner l’option est important car une fois que les icônes indésirables se trouvent sur le bureau, de nombreux utilisateurs hésitent à les supprimer. Cela peut entraîner un encombrement inutile du bureau.
-   **Si les utilisateurs sélectionnent l’option, fournissez un seul raccourci de programme.** Si votre produit est constitué de plusieurs programmes, fournissez un raccourci uniquement au programme principal.
-   **Placez uniquement les raccourcis de programme sur le bureau.** Ne placez pas le programme réel ou d’autres types de fichiers.

    **Correct :**

    ![capture d’écran de l’icône de raccourci avec superposition de flèche ](images/winenv-desktop-image3.png)

    **Incorrect :**

    ![capture d’écran de l’icône de programme ](images/winenv-desktop-image4.png)

    Dans l’exemple incorrect, le programme, et non un raccourci, est copié sur le bureau.

-   **Choisissez une étiquette qui peut être affichée sans troncation.** Les utilisateurs ne doivent pas voir de points de suspension.

    **Correct :**

    ![capture d’écran de l’icône de raccourci avec le nom complet ](images/winenv-desktop-image3.png)

    **Incorrect :**

    ![capture d’écran de l’icône de raccourci avec nom tronqué ](images/winenv-desktop-image5.png)

    Dans l’exemple incorrect, l’étiquette du raccourci du programme est tellement longue qu’elle est tronquée.

## <a name="documentation"></a>Documentation

-   Lorsque vous faites référence au bureau, utilisez le bureau, en majuscules.
-   Quand vous faites référence à des raccourcis de bureau, utilisez le raccourci, en majuscules.

 

 