---
description: Quand un utilisateur clique avec le bouton droit sur un objet Shell, tel qu’un fichier, le shell affiche un menu contextuel (contexte).
ms.assetid: 4f46b8c3-1e12-447c-87f4-bbe2c305f77a
title: Verbes et associations de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a144051b04ef2d9a2c9877b53e1680d4274afc92d3fc87fbcb531b02a0f94946
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860786"
---
# <a name="verbs-and-file-associations"></a>Verbes et associations de fichiers

Quand un utilisateur clique avec le bouton droit sur un objet Shell, tel qu’un fichier, le shell affiche un menu contextuel (contexte). Ce menu contient une liste de commandes que l’utilisateur peut sélectionner pour effectuer diverses actions sur l’élément. Ces commandes sont également appelées éléments de menu contextuel ou verbes. Les menus contextuels peuvent être personnalisés.

Cette rubrique est organisée comme suit :

-   [Présentation des menus contextuels pour les objets de système de fichiers](#introduction-to-shortcut-menus-for-file-system-objects)
    -   [Ajouter des commandes à un menu contextuel](#add-commands-to-a-shortcut-menu)
-   [Verbes de menu contextuel](#shortcut-menu-verbs)
-   [diffuser en continu des éléments de système Non-fichier et des résultats de OpenSearch.](#stream-non-file-system-items-and-opensearch-results)
-   [Inscrire une application pour gérer des types de fichiers arbitraires](#register-an-application-to-handle-arbitrary-file-types)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="introduction-to-shortcut-menus-for-file-system-objects"></a>Présentation des menus contextuels pour les objets de système de fichiers

Comme les menus contextuels sont souvent utilisés pour la gestion des fichiers, l’interpréteur de commandes fournit un ensemble de commandes par défaut, telles que **couper** et **copier**, qui apparaissent dans le menu contextuel pour tout objet de système de fichiers, tel qu’un fichier ou un dossier.

L’exemple suivant illustre un menu contextuel par défaut qui s’affiche en cliquant avec le bouton droit sur **MyFile.xyz-MS**.

![capture d’écran du menu contextuel par défaut](images/context-menu/context-filesystemobjects.png)

La raison pour laquelle un menu contextuel par défaut s’affiche pour **MyFile.xyz-MS** est due au fait que **. xyz-MS** n’est pas membre d’un type de fichier inscrit. En revanche, **.txt** est un type de fichier inscrit. Si vous cliquez avec le bouton droit sur un fichier de **.txt** , un menu contextuel s’affiche avec trois commandes supplémentaires dans sa section supérieure : **Imprimer**, **modifier** et **Ouvrir avec**.

![capture d’écran du menu contextuel d’un fichier avec un type de fichier inscrit](images/context-menu/context-registeredfiletype.png)

Pour étendre le menu contextuel d’un type de fichier, vous devez créer une entrée de Registre pour chaque commande. Une approche plus sophistiquée consiste à implémenter un gestionnaire de menu contextuel (verbe), qui vous permet d’étendre le menu contextuel pour un type de fichier fichier par fichier. Pour plus d’informations, consultez [création de gestionnaires de menus contextuels](context-menu-handlers.md)et [Référence du menu contextuel](context-menu-reference.md).

### <a name="add-commands-to-a-shortcut-menu"></a>Ajouter des commandes à un menu contextuel

Un gestionnaire de menu contextuel est un gestionnaire de type de fichier qui ajoute des commandes à un menu contextuel existant. Les gestionnaires de menus contextuels sont associés à un type de fichier, et sont appelés chaque fois qu’un menu contextuel est affiché pour un membre de la classe. L’interpréteur de commandes vérifie le registre pour voir si le type de fichier est associé à n’importe quel gestionnaire de menu contextuel. Si c’est le cas, l’interpréteur de commandes interroge les gestionnaires pour obtenir d’autres éléments de menu contextuel.

## <a name="shortcut-menu-verbs"></a>Verbes de menu contextuel

Chaque commande du menu contextuel est identifiée dans le registre par son verbe. Ces verbes sont les mêmes que ceux utilisés par [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) lors du lancement d’applications par programme.

Un verbe est une chaîne de texte simple qui est utilisée par l’interpréteur de commandes pour identifier la commande associée. Chaque verbe correspond à la chaîne de commande utilisée pour lancer la commande dans une fenêtre de console ou un fichier de commandes (.bat).

Par exemple, le verbe Open lance normalement un programme pour ouvrir un fichier. La chaîne de commande se présente généralement comme suit :


```
"My Program.exe" "%1"
```



Si un élément de la chaîne de commande contient ou peut contenir des espaces, il doit être placé entre guillemets. Sinon, si l’élément contient un espace, il ne sera pas analysé correctement. Par exemple, **« My Program.exe »** démarre l’application correctement. Si vous utilisez la **Program.exe** sans guillemets, le système tente de lancer **My** avec **Program.exe** comme premier argument de ligne de commande. Vous devez toujours utiliser des guillemets avec des arguments tels que **« %1**» développés pour les chaînes par l’interpréteur de commandes, car vous ne pouvez pas être certain que la chaîne ne contiendra pas d’espace.

Les verbes peuvent également être associés à un nom d’affichage, qui est affiché dans le menu contextuel au lieu de la chaîne de verbe elle-même. Par exemple, la chaîne d’affichage pour openas est **ouverte avec**. Comme les chaînes de menu normales, y compris un caractère perluète dans la chaîne d’affichage, permet de sélectionner le clavier de la commande.

## <a name="stream-non-file-system-items-and-opensearch-results"></a>diffuser en continu des éléments de système Non-fichier et des résultats de OpenSearch.

dans Windows 7 et versions ultérieures, il existe une prise en charge de la connexion de sources externes au Client Windows via le protocole [OpenSearch](http://www.opensearch.org/) . cela permet aux utilisateurs de rechercher dans un magasin de données distant et d’afficher les résultats à partir de Windows Explorer. la norme OpenSearch v 1.1 définit des formats de fichiers simples qui peuvent être utilisés pour décrire comment un client doit interroger le service web pour le magasin de données et comment le service doit retourner les résultats à afficher par le client.

vous devrez peut-être diffuser en continu des éléments de système non-fichier pour éviter de devoir télécharger des éléments en cas de [OpenSearch](http://www.opensearch.org/) résultats. la fonctionnalité de recherche fédérée permet de rechercher des éléments à partir d’emplacements autres que les systèmes de fichiers qui prennent en charge OpenSearch, comme SharePoint et d’autres sites web, par exemple. Lors de l’appel de verbes sur ces éléments, le système télécharge une version temporaire de l’élément et le passe à l’implémentation du verbe. Les implémenteurs de verbes sont encouragés pour éviter de devoir télécharger le fichier en inscrivant l’ensemble de schémas d’URL que le verbe prend en charge pour diffuser les éléments. Les verbes le font à l’aide de la clé de Registre **SupportedProtocols** .

## <a name="register-an-application-to-handle-arbitrary-file-types"></a>Inscrire une application pour gérer des types de fichiers arbitraires

Définir des éléments de menu contextuel pour un type de fichier particulier vous permet de spécifier comment l’application associée ouvre un membre du type de fichier. Toutefois, les applications peuvent également inscrire une procédure par défaut distincte à utiliser lorsqu’un utilisateur tente d’utiliser l’application pour ouvrir un type de fichier qui n’est pas associé à l’application. Vous inscrivez la procédure par défaut à peu près de la même façon que vous enregistrez les éléments de menu contextuel. Pour plus d’informations sur la définition des éléments de menu contextuel, consultez [création de gestionnaires de menus contextuels](context-menu.md).

La procédure par défaut remplit deux fonctions de base. La première consiste à spécifier la manière dont votre application doit être appelée pour ouvrir un type de fichier arbitraire. Vous pouvez, par exemple, utiliser un indicateur de ligne de commande pour indiquer qu’un type de fichier inconnu est en cours d’ouverture. L’autre objectif est de définir les différentes caractéristiques d’un type de fichier, telles que les éléments de menu contextuel et l’icône. Si un utilisateur associe votre application à un type de fichier supplémentaire, cette classe aura ces caractéristiques. Si le type de fichier supplémentaire a été précédemment associé à une autre application, ces caractéristiques remplacent les originaux.

Pour inscrire la procédure par défaut, placez les mêmes clés de registre que celles que vous avez créées pour le ProgID de votre application sous la sous-clé de l’application des **\_ \_ \\ applications racines de la classe HKEY**. Vous pouvez également inclure une valeur **FriendlyAppName** pour fournir au système un nom convivial pour votre application. Le nom convivial de l’application peut également être extrait de son fichier exécutable, mais uniquement si la valeur FriendlyAppName est absente.

L’exemple d’entrée de Registre suivant illustre une procédure par défaut pour **MyProgram.exe** qui définit un nom convivial et plusieurs éléments de menu contextuel. Les chaînes de commande incluent l’indicateur **/a** pour notifier l’application qu’il ouvre un type de fichier arbitraire. Si vous incluez une sous-clé **DefaultIcon** , vous devez utiliser une icône générique.

```
HKEY_CLASSES_ROOT
   MyProgram.exe
      shell
         open
            command
               (Default) = C:\MyDir\MyProgram.exe /a "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /a /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /a /p "%1" "%2"
```

## <a name="additional-resources"></a>Ressources supplémentaires

-   Pour plus d’informations, consultez [Présentation des associations de fichiers](fa-intro.md).
-   Pour obtenir des informations conceptuelles sur l’extension de l’interpréteur de commandes avec des gestionnaires de types de fichiers, consultez [création de gestionnaires d’extension de Shell](handlers.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Meilleures pratiques pour les gestionnaires de menus contextuels et les verbes de sélection multiple](verbs-best-practices.md)
</dt> <dt>

[Choix d’un verbe statique ou dynamique pour votre menu contextuel](shortcut-choose-method.md)
</dt> <dt>

[Création de gestionnaires de menu contextuel](context-menu-handlers.md)
</dt> <dt>

[Personnalisation d’un menu contextuel à l’aide de verbes dynamiques](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menus contextuels (menu contextuel) et gestionnaires de menus contextuels](context-menu.md)
</dt> <dt>

[Référence du menu contextuel](context-menu-reference.md)
</dt> </dl>

 

 



