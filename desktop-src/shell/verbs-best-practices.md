---
description: Découvrez les meilleures pratiques pour les gestionnaires de menus contextuels et plusieurs verbes quand vous implémentez un format de fichier personnalisé dans le shell Windows.
title: Meilleures pratiques pour les gestionnaires de menus contextuels et les verbes multiples
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4D352ECB-6214-4f6e-A3E5-F79E154D090A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 14ec2e8915aa1df47ca21c6436ec963be3f590f5
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396444"
---
# <a name="best-practices-for-shortcut-menu-handlers-and-multiple-verbs"></a>Meilleures pratiques pour les gestionnaires de menus contextuels et les verbes multiples

Cette rubrique est organisée comme suit :

-   [Bonnes pratiques](#best-practices-for-shortcut-menu-handlers-and-multiple-verbs)
    -   [Meilleures pratiques pour les implémentations de verbes](#best-practices-for-verb-implementations)
-   [Meilleures pratiques pour les verbes de sélection multiple](#best-practices-for-multiple-selection-verbs)
    -   [Sélections hétérogènes](#heterogenous-selections)
-   [Rubriques connexes](#related-topics)

## <a name="best-practices"></a>Bonnes pratiques

Les verbes statiques sont les verbes les plus simples à implémenter et offrent des fonctionnalités riches. Nous vous encourageons fortement à implémenter un verbe à l’aide de l’une des méthodes de verbe statiques.

### <a name="best-practices-for-verb-implementations"></a>Meilleures pratiques pour les implémentations de verbes

La liste suivante représente les meilleures pratiques pour les implémentations de verbe :

-   Choisissez toujours la méthode Verb la plus simple qui répond à vos besoins.
-   Utilisez une méthode Verb statique, si possible.
-   N’effectuez pas d’opérations gourmandes en ressources ou d’e/s sur le thread d’interface utilisateur. [**IShellExtInit :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) et [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) doivent être très prudents dans le travail qu’ils effectuent. [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) doit être exécuté dans un autre processus, ou vous devez créer un nouveau thread pour éviter de bloquer l’appelant.
-   Préfixez les verbes avec le nom de l’éditeur de logiciels indépendant (ISV) comme suit, `ISVName.verb` . L’utilisation de noms non qualifiés peut entraîner des collisions avec plusieurs éditeurs de logiciels indépendants qui choisissent le même nom de verbe.
-   Utilisez toujours un ProgID propre à l’application. Étant donné que certains types d’éléments n’utilisent pas ce mappage, il est nécessaire de nommer les noms uniques des fournisseurs.
-   Positionnez l’interface utilisateur par rapport à la méthode d’appel, mais ne l’exécutez pas sur un thread appelant.
-   N’acceptez pas la valeur de **retour \_ OK** pour les verbes canoniques passés à la méthode [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) . Cela entraîne l’échec de l’implémentation du verbe réel et retourne un code d’erreur pour les verbes canoniques. Si vous ne prenez pas en charge les verbes canoniques, retournez l’erreur lorsqu’une valeur HIWORD (lpVerb) différente de zéro est rencontrée.
-   Évitez l’utilisation de **rundll32.exe** comme hôte pour votre verbe.
-   Lors de l’implémentation de [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) , veillez à retourner le nombre de verbes qui ont été ajoutés au menu par le biais de la valeur **HRESULT** à l’aide de la macro ResultFromShort.
-   Si vous vous inscrivez sur l’une des entrées de clé de Registre suivantes, soyez prudent et veillez à inscrire votre gestionnaire sur le type le plus spécifique pour réduire les conséquences éventuellement inattendues :
    -   **\_racine des classes HKEY \_\\\***
    -   **\_ \_ AllFileSystemObjects racine des classes HKEY \\**
    -   **\_ \_ Dossier racine des classes HKEY \\**
    -   **\_ \_ Répertoire racine des classes HKEY \\**
-   Définissez la clé **MayChangeDefaultMenu** uniquement si vous pensez que vous devrez peut-être modifier le verbe par défaut dans le menu contextuel. Si votre gestionnaire ne modifie pas le verbe par défaut, vous ne devez pas définir cette clé, car cela amène le système à charger votre DLL inutilement.
-   Réduisez le travail que vous effectuez dans [**IShellExtInit :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize). Pour les gestionnaires de menus contextuels, capturez l’objet de données passé à **IShellExtInit :: Initialize**, puis traitez-le dans [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)ou [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

## <a name="best-practices-for-multiple-selection-verbs"></a>Meilleures pratiques pour les verbes de sélection multiple

Étant donné que le nombre d’éléments dans un scénario de verbe à sélection multiple peut être important, il est important de prendre en compte les implications en matière de performances de vos implémentations de verbe. Par exemple, lorsqu’un utilisateur recherche « \* » sur une étendue qui comprend un grand nombre d’éléments, puis clique sur **Sélectionner tout** et clique avec le bouton droit, une sélection pouvant contenir des milliers d’éléments est présentée au verbe. Par conséquent, les verbes doivent uniquement prendre en compte le premier élément de la sélection et le nombre total d’éléments. Le premier élément est défini comme l’élément en haut de la vue, ou l’élément sur lequel l’utilisateur a cliqué pour la première fois avec le bouton droit.

Dans Windows 7 et versions ultérieures, le nombre d’éléments passés à un verbe est limité à 16 quand un menu contextuel est interrogé. Le verbe est ensuite recréé et réinitialisé avec la sélection complète lorsque ce verbe est appelé.

Dans certains cas, il convient de prendre en compte un petit nombre d’éléments fixes. Par exemple, il est approprié pour un verbe « diff » de considérer uniquement les deux premiers éléments. En règle générale, vous n’avez pas besoin de tester chaque élément de la sélection pour voir s’il s’agit d’un certain type, ou d’interroger chaque élément de la sélection pour ses propriétés. Regardez plutôt le premier élément et déterminez s’il convient d’ajouter votre verbe.

### <a name="heterogenous-selections"></a>Sélections hétérogènes

Les verbes optimistes sont automatiquement ajoutés dans le cas de sélection multiple, en supposant que les éléments non inspectés peuvent être gérés par le verbe. En revanche, les verbes pessimistes ne sont pas ajoutés lorsque la sélection contient des éléments non inspectés et sont uniquement ajoutés dans les cas où le nombre d’éléments est petit.

Les verbes de style de joueur doivent être optimistes et ignorer silencieusement les éléments qui ne sont pas gérés. Si un échec d’action sur des éléments peut entraîner une perte de données ou une confusion, le verbe doit avertir les utilisateurs des éléments qui ne peuvent pas être traités. Par exemple, un verbe « Backup » doit indiquer que certains éléments n’ont pas pu être sauvegardés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Choix d’un verbe statique ou dynamique pour votre menu contextuel](shortcut-choose-method.md)
</dt> <dt>

[Création de gestionnaires de menu contextuel](context-menu-handlers.md)
</dt> <dt>

[Personnalisation d’un menu contextuel à l’aide de verbes dynamiques](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menus contextuels (menu contextuel) et gestionnaires de menus contextuels](context-menu.md)
</dt> <dt>

[Verbes et associations de fichiers](fa-verbs.md)
</dt> <dt>

[Référence du menu contextuel](context-menu-reference.md)
</dt> </dl>

 

 



