---
description: Choisissez une méthode de menu contextuel statique ou dynamique quand vous implémentez un format de fichier personnalisé dans le shell Windows.
title: Choix d’une méthode de menu contextuel statique ou dynamique
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 44227BCF-D35E-4a9e-B4E6-D50E6AFBAEDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: dfd73ee052594e1136fe2885ce92b682f229096b
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394774"
---
# <a name="choosing-a-static-or-dynamic-shortcut-menu-method"></a>Choix d’une méthode de menu contextuel statique ou dynamique

Cette rubrique est organisée comme suit :

-   [Choisir une méthode de verbe](#choose-a-verb-method)
    -   [Méthodes Verb statiques](#static-verb-methods)
    -   [Méthodes de verbe dynamique préférées](#preferred-dynamic-verb-methods)
    -   [Méthodes de verbe dynamique déconseillées](#discouraged-dynamic-verb-methods)
-   [Étendre un menu contextuel](#extend-a-shortcut-menu)
-   [Prise en charge des méthodes de verbe par système d’exploitation](#support-for-verb-methods-by-operating-system)
-   [Rubriques connexes](#related-topics)

## <a name="choose-a-verb-method"></a>Choisir une méthode de verbe

Il est vivement recommandé d’implémenter un menu contextuel à l’aide de l’une des méthodes de verbe statique.

### <a name="static-verb-methods"></a>Méthodes Verb statiques

Les verbes statiques sont les verbes les plus simples à implémenter, mais ils fournissent toujours des fonctionnalités riches. Choisissez toujours la méthode de menu contextuel la plus simple qui répond à vos besoins.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Verbe statique</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> avec paramètres de ligne de commande</td>
<td>Il s’agit des méthodes les plus simples et les plus familières pour implémenter un verbe statique. Un processus est appelé via un appel à la fonction <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> avec les fichiers sélectionnés et tous les paramètres facultatifs passés comme ligne de commande. Cela ouvre le fichier ou le dossier.<br/> Cette méthode présente les limitations suivantes :
<ul>
<li>La longueur de la ligne de commande est limitée à 2000 caractères, ce qui limite le nombre d’éléments que le verbe peut gérer.</li>
<li>Peut uniquement être utilisé avec les éléments du système de fichiers.</li>
<li>N’active pas la réutilisation d’un processus déjà en cours d’exécution.</li>
<li>Requiert l’installation d’un exécutable pour gérer le verbe.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"> <strong>IDropTarget</strong></a></td>
<td>Une activation de verbe basée sur COM signifie que prend en charge l’activation en mode in-proc ou hors processus. <strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> prend également en charge la réutilisation d’un gestionnaire déjà en cours d’exécution lorsque l’interface <strong>IDropTarget</strong> est implémentée par un serveur local. Il exprime également parfaitement les éléments via l’objet de données marshalés et fournit une référence à l’appel de la chaîne de site afin que vous puissiez interagir avec le demandeur via le service <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>.</td>
</tr>
<tr class="odd">
<td>Windows 7 et versions ultérieures : <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"> <strong>IExecuteCommand</strong></a></td>
<td>La méthode d’implémentation la plus directe. Étant donné qu’il s’agit d’une méthode d’appel COM (par exemple, DropTarget), cette interface prend en charge l’activation in-proc et out-of-process. Le verbe implémente <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> et <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>, et éventuellement <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a>. Les éléments sont passés directement en tant que tableau d’éléments d’interpréteur de commandes et davantage de paramètres du demandeur sont disponibles pour l’implémentation du verbe, y compris le point d’appel, l’état du clavier, etc.</td>
</tr>
<tr class="even">
<td>Windows 7 et versions ultérieures :<strong>ExplorerCommand</strong> /  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></td>
<td>Active les sources de données qui fournissent leurs commandes de module de commande via <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> pour utiliser ces commandes comme verbes dans un menu contextuel. Étant donné que cette interface prend en charge uniquement l’activation in-process, il est recommandé d’utiliser des sources de données Shell qui doivent partager l’implémentation entre les commandes et les menus contextuels.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) est un hybride entre un verbe statique et dynamique. **IExplorerCommand** a été déclaré dans Windows Vista, mais sa capacité à implémenter un verbe dans un menu contextuel est une nouveauté de Windows 7.

 

Pour plus d’informations sur les requêtes [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) et Shell pour les attributs d’association de fichiers, consultez [types perçus et inscription d’application](fa-perceivedtypes.md).

### <a name="preferred-dynamic-verb-methods"></a>Méthodes de verbe dynamique préférées

Les méthodes de verbe dynamique suivantes sont préférées :



| Type de verbe                                                                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verbe statique (listé dans le tableau précédent) + syntaxe de requête avancée (AQS)                  | Ce choix obtient la visibilité des verbes dynamiques.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Windows 7 et versions ultérieures : [ **IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)                         | Ce choix permet une implémentation courante des verbes et des commandes de l’Explorateur qui s’affichent dans le module de commande dans l’Explorateur Windows.                                                                                                                                                                                                                                                                                                                                                                                               |
| Windows 7 et versions ultérieures : [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + verbe statique | Ce choix obtient également la visibilité des verbes dynamiques. Il s’agit d’un modèle hybride dans lequel un simple gestionnaire in-process est utilisé pour calculer si un verbe statique donné doit être affiche. Cela peut être appliqué à toutes les méthodes d’implémentation de verbe statique pour obtenir un comportement dynamique et réduire l’exposition de la logique in-process. [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) présente l’avantage de s’exécuter sur un thread d’arrière-plan, ce qui évite les blocages de l’interface utilisateur. Elle est beaucoup plus simple que [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). |



 

### <a name="discouraged-dynamic-verb-methods"></a>Méthodes de verbe dynamique déconseillées

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) est la méthode la plus simple, mais également la plus compliquée à implémenter. Il est basé sur des objets COM in-process qui s’exécutent sur le thread de l’appelant, qui est généralement l’Explorateur Windows, mais peut être n’importe quelle application hébergeant les éléments. **IContextMenu** prend en charge la visibilité des verbes, le classement et le dessin personnalisé. Certaines de ces fonctionnalités ont été ajoutées aux fonctionnalités de verbe statique, telles qu’une icône à associer à une commande, et [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) pour gérer la visibilité.

Si vous devez étendre le menu contextuel d’un type de fichier en inscrivant un verbe dynamique pour le type de fichier, suivez les instructions fournies dans [Personnalisation d’un menu contextuel à l’aide de verbes dynamiques](shortcut-menu-using-dynamic-verbs.md).

## <a name="extend-a-shortcut-menu"></a>Étendre un menu contextuel

Une fois que vous avez choisi une méthode de verbe, vous pouvez étendre un menu contextuel pour un type de fichier en inscrivant un verbe statique pour le type de fichier. Pour plus d’informations, consultez [création de gestionnaires de menus contextuels](context-menu-handlers.md).

## <a name="support-for-verb-methods-by-operating-system"></a>Prise en charge des méthodes de verbe par système d’exploitation

La prise en charge des méthodes d’appel de verbe par système d’exploitation est répertoriée dans le tableau suivant.



| Méthode Verb          | Windows XP | Windows Vista | Windows 7 et versions ultérieures |
|----------------------|------------|---------------|----------------------|
| CreateProcess        | X          | X             | X                    |
| DDE                  | X          | X             | X                    |
| DropTarget           | X          | X             | X                    |
| ExecuteCommand       |            | X             | X                    |
| ExplorerCommand      |            |               | X                    |
| ExplorerCommandState |            |               | X                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Meilleures pratiques pour les gestionnaires de menus contextuels et les verbes de sélection multiple](verbs-best-practices.md)
</dt> <dt>

[Création de gestionnaires de menu contextuel](context-menu-handlers.md)
</dt> <dt>

[Personnalisation d’un menu contextuel à l’aide de verbes dynamiques](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menus contextuels (menu contextuel) et gestionnaires de menus contextuels](context-menu.md)
</dt> <dt>

[Référence du menu contextuel](context-menu-reference.md)
</dt> <dt>

[Verbes et associations de fichiers](fa-verbs.md)
</dt> </dl>

 

 
