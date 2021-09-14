---
title: À propos des icônes
description: Cette rubrique décrit les icônes.
ms.assetid: 67867460-07f6-460f-9263-05bbf3474744
keywords:
- ressources, icônes
- icônes, zones réactives
- icônes, standard
- icônes standard
- icônes, personnalisées
- icônes personnalisées
- icônes, tailles
- création d’icônes
- icônes, affichage
- icônes, destruction
- icônes, duplication
- icônes, création
- afficher les icônes
- détruire des icônes
- duplication d’icônes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bda00540d613b6d0efd4a080251ebd6407560ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293458"
---
# <a name="about-icons"></a>À propos des icônes

Le système utilise des icônes dans l’interface utilisateur pour représenter des objets tels que des fichiers, des dossiers, des raccourcis, des applications et des documents. L’icône fonctions permet aux applications de créer, charger, afficher, organiser, animer et détruire des icônes. Pour plus d’informations sur la spécification des icônes pour les types de fichiers, consultez [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona).

Cette vue d’ensemble fournit des informations sur les rubriques suivantes :

-   [Zone réactive de l’icône](#icon-hot-spot)
-   [Types d’icônes](#icon-types)
-   [Tailles d’icône](#icon-sizes)
    -   [Pour modifier la taille de la petite icône système](#to-change-the-size-of-the-system-small-icon)
    -   [Pour récupérer la taille de la petite icône système](#to-retrieve-the-size-of-the-system-small-icon)
    -   [Pour récupérer la taille de l’icône système grande](#to-retrieve-the-size-of-the-system-large-icon)
    -   [Pour récupérer la taille de la petite icône de Shell](#to-retrieve-the-size-of-the-shell-small-icon)
    -   [Pour modifier la taille de la grande icône](#to-change-the-size-of-the-large-icon)
    -   [Pour récupérer la taille de la grande icône de Shell](#to-retrieve-the-size-of-the-shell-large-icon)
-   [Création d’icône](#icon-creation)
-   [Affichage des icônes](#icon-display)
-   [Destruction d’icône](#icon-destruction)
-   [Duplication d’icône](#icon-duplication)

## <a name="icon-hot-spot"></a>Zone réactive de l’icône

L’un des pixels d’une icône est désigné comme [zone réactive](#icon-hot-spot), qui est le point suivi et reconnu par le système comme position de l’icône. La zone réactive d’une icône correspond généralement au pixel situé au centre de l’icône. Si vous utilisez la fonction [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) pour créer une icône, vous pouvez spécifier n’importe quel pixel comme zone réactive.

## <a name="icon-types"></a>Types d’icônes

Le système d’exploitation fournit un ensemble d' *icônes standard* disponibles pour n’importe quelle application à utiliser à tout moment. Les fichiers d’en-tête du kit de développement logiciel (SDK) contiennent des identificateurs pour les icônes standard : les identificateurs commencent par le préfixe **IDI \_** .

Une image par défaut correspondante est associée à chaque icône standard. L’utilisateur peut remplacer l’image par défaut associée à n’importe quel curseur standard à tout moment.

Les *icônes personnalisées* sont conçues pour être utilisées dans une application particulière et peuvent être n’importe quelle conception. Voici plusieurs icônes personnalisées.

![plusieurs icônes personnalisées](images/csicn-02.png)

## <a name="icon-sizes"></a>Tailles d’icône

Le système utilise quatre tailles d’icône :

-   Système petit
-   Grand système
-   Shell petit
-   Grand Shell

La *petite icône système* est affichée dans le titre de la fenêtre.

### <a name="to-change-the-size-of-the-system-small-icon"></a>Pour modifier la taille de la petite icône système

1.  Dans le panneau de configuration, cliquez sur **affichage**, puis sur l’onglet **apparence** .
2.  Sélectionnez les **boutons de légende** dans la liste des **éléments** , puis définissez le champ **taille** .

### <a name="to-retrieve-the-size-of-the-system-small-icon"></a>Pour récupérer la taille de la petite icône système

-   Appelez la fonction [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) avec **SM \_ CXSMICON** et **SM \_ CYSMICON**.

La *grande icône système* est principalement utilisée par les applications, mais elle est également affichée dans la boîte de dialogue Alt + Tab. Les fonctions [**CreateIconFromResource**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresource), [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon), [**ExtractAssociatedIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extractassociatedicona), [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona), [**ExtractIconEx**](/windows/desktop/api/Shellapi/nf-shellapi-extracticonexa)et [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) utilisent toutes des grandes icônes système. La taille de la grande icône système est définie par le pilote vidéo. par conséquent, elle ne peut pas être modifiée.

### <a name="to-retrieve-the-size-of-the-system-large-icon"></a>Pour récupérer la taille de l’icône système grande

-   Appelez [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) avec **SM \_ CXICON** et **SM \_ CYICON**.

Les fonctions [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon), [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex), [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect)et [**SHGetFileInfo**](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) peuvent être utilisées pour travailler avec des icônes dans des tailles autres que System large.

la *petite icône de shell* est utilisée dans l’explorateur de Windows et les boîtes de dialogue courantes. Actuellement, la taille minimale du système est définie par défaut.

### <a name="to-retrieve-the-size-of-the-shell-small-icon"></a>Pour récupérer la taille de la petite icône de Shell

1.  Utilisez la fonction [SHGetFileInfo](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) avec `SHGFI_SHELLICONSIZE | SHGFI_SMALLICON` pour récupérer un handle de la liste d’images système.
2.  Appelez ensuite la fonction [**ImageList \_ GetIconSize**](/windows/win32/api/commctrl/nf-commctrl-imagelist_geticonsize) pour connaître la taille de l’icône.

La grande icône de Shell est utilisée sur le bureau.

### <a name="to-change-the-size-of-the-large-icon"></a>Pour modifier la taille de la grande icône

1.  Dans le panneau de configuration, cliquez sur **affichage**, puis sur l’onglet **apparence** .
2.  Sélectionnez **icône** dans la liste **élément** , puis définissez le champ **taille** (cette taille est stockée dans le registre, sous **HKEY \_ Current \_ User \\ Control Panel, Desktop \\ WindowMetrics \\ Shell Icon Size**).
3.  Cliquez sur le plus **!** , puis activez la case à cocher **utiliser de grandes icônes** .

### <a name="to-retrieve-the-size-of-the-shell-large-icon"></a>Pour récupérer la taille de la grande icône de Shell

1.  Utilisez la fonction [**SHGetFileInfo**](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) avec **SHGFI \_ SHELLICONSIZE** pour récupérer un handle de la liste d’images système.
2.  Appelez ensuite la fonction [**ImageList \_ GetIconSize**](/windows/win32/api/commctrl/nf-commctrl-imagelist_geticonsize) pour connaître la taille de l’icône.

le menu Démarrer utilise des petites icônes de shell ou des grandes icônes de shell, selon que la case à cocher **utiliser de grandes icônes** est activée ou non.

Votre application doit fournir des groupes d’images d’icône dans les tailles suivantes :

-   48, couleur 256
-   32x32, 16 couleurs
-   16x16 pixels, 16 couleurs

Lors du remplissage de la structure [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) à utiliser lors de l’enregistrement de votre classe de fenêtre, définissez le membre **HICON** sur l’icône 32X32 et le membre **hIconSm** sur l’icône 16x16. Pour plus d’informations sur les icônes de classe, consultez les [icônes de classe](/windows/desktop/winmsg/about-window-classes).

## <a name="icon-creation"></a>Création d’icône

Les icônes standard sont prédéfinies. il n’est donc pas nécessaire de les créer. Pour utiliser une icône standard, une application peut obtenir son handle à l’aide de la fonction [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) . Un *descripteur d’icône* est une valeur unique du type **HICON** qui identifie une icône standard ou personnalisée.

Pour créer une icône personnalisée pour une application, vous devez généralement utiliser une application graphique et inclure la [ressource icône](./icon-resource.md) dans le fichier de définition de ressources de l’application. Au moment de l’exécution, vous pouvez appeler [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) ou [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) pour récupérer un handle de l’icône. Une ressource icône peut contenir un groupe d’images pour plusieurs périphériques d’affichage différents. **LoadIcon** et **LoadImage** sélectionnent automatiquement l’icône la plus appropriée dans le groupe pour le périphérique d’affichage actuel.

Une application peut également créer une icône personnalisée au moment de l’exécution à l’aide de la fonction [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) , qui crée une icône basée sur le contenu d’une structure [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) . La fonction [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) remplit la structure avec les coordonnées et les informations de la zone réactive du masque de bits et de la bitmap de couleur pour l’icône.

Les applications doivent implémenter des icônes personnalisées en tant que ressources et doivent utiliser [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) ou [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea), plutôt que de créer l’icône au moment de l’exécution. L’utilisation des ressources d’icône évite la dépendance des appareils, simplifie la localisation et permet aux applications de partager des formes d’icône.

La fonction [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) permet à une application de parcourir les ressources du système et de créer des icônes et des curseurs basés sur les données de ressources. **CreateIconFromResourceEx** crée une icône basée sur les données de ressources binaires à partir d’autres fichiers exécutables ou dll. Une application doit précéder cette fonction avec des appels à la fonction [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) et à plusieurs des fonctions de ressources. **LookupIconIdFromDirectoryEx** retourne l’identificateur des données d’icône les plus appropriées pour le périphérique d’affichage actuel.

## <a name="icon-display"></a>Affichage des icônes

Vous pouvez récupérer l’image d’une icône à l’aide de la fonction [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) et la dessiner à l’aide de la fonction [**DrawIconEx**](/windows/desktop/api/Winuser/nf-winuser-drawiconex) . Pour dessiner l’image par défaut pour une icône, spécifiez l’indicateur **di \_ compat** dans l’appel à **DrawIconEx**. Si vous ne spécifiez pas l’indicateur de **\_ compatibilité di** , **DrawIconEx** dessine l’icône à l’aide de l’image spécifiée par l’utilisateur.

Quand le système affiche une icône, il doit extraire l’image d’icône appropriée du fichier .exe ou .dll. Le système utilise les étapes suivantes pour sélectionner l’image d’icône :

1.  Sélectionnez la **ressource \_ \_ icône de groupe RT** . Si plusieurs ressources existent, le système utilise la première ressource indiquée dans la ressource script.
2.  Sélectionnez l’image **d' \_ icône RT** appropriée dans la ressource **\_ \_ icône de groupe RT** . Si plusieurs images existent, le système utilise les critères suivants pour choisir une image :
    -   -   L’image la plus proche de la taille demandée est choisie.
        -   Si au moins deux images de cette taille sont présentes, celle qui correspond à la profondeur de couleur de l’affichage est choisie.
        -   Si aucune image ne correspond exactement à la profondeur de couleur de l’affichage, l’image ayant la plus grande profondeur de couleur qui ne dépasse pas la profondeur de couleur de l’affichage est choisie. Si la profondeur de couleur est dépassée, la profondeur de couleur la plus faible est choisie.

> [!Note]  
> Le système traite toutes les profondeurs de couleur de 8 bpp ou plus comme égaux. Par conséquent, il n’existe aucun avantage à inclure une image de 16x16 256 et une image de 16 x 16 couleurs dans la même ressource : le système choisira simplement la première image qu’il rencontre. Lorsque l’affichage est en mode 8 BPP, le système choisit une icône de 16 couleurs sur une icône de couleur 256 et affiche toutes les icônes à l’aide de la palette système par défaut.

 

Pour afficher une icône animée, utilisez un contrôle statique comme indiqué dans le fragment de code suivant.


```
hIcon = LoadImage(NULL, "ico.ani", IMAGE_ICON, 0, 0, LR_LOADFROMFILE);
SendMessage( hStatic, STM_SETIMAGE, IMAGE_ICON, (LPARAM)(UINT)hIcon);
```



## <a name="icon-destruction"></a>Destruction d’icône

Quand une application n’a plus besoin d’une icône créée à l’aide de la fonction [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) , elle doit détruire l’icône. La fonction [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) détruit le handle d’icône et libère toute mémoire utilisée par l’icône. Les applications doivent utiliser cette fonction uniquement pour les icônes créées avec **CreateIconIndirect**; Il n’est pas nécessaire de supprimer d’autres icônes.

## <a name="icon-duplication"></a>Duplication d’icône

La fonction [**CopyIcon**](/windows/desktop/api/Winuser/nf-winuser-copyicon) copie un handle d’icône. Cela permet à une application ou une DLL d’avoir son propre handle à une icône appartenant à un autre module. Ensuite, si l’autre module est libéré, l’application qui a copié l’icône sera toujours en mesure d’utiliser l’icône.

La fonction [**CopyImage**](/windows/desktop/api/Winuser/nf-winuser-copyimage) crée une icône basée sur l’icône source spécifiée. La nouvelle icône peut être plus grande ou plus petite que l’icône source.

Pour plus d’informations sur l’ajout, la suppression ou le remplacement des ressources d’icône dans les fichiers exécutables (.exe), consultez [ressources](resources.md).

La fonction [**DuplicateIcon**](/windows/desktop/api/Shellapi/nf-shellapi-duplicateicon) effectue une copie réelle de l’icône.

 

 