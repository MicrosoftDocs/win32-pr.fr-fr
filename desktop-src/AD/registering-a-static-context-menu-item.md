---
title: Inscription d’un élément de menu contextuel statique
description: Cette rubrique décrit l’inscription d’un élément de menu contextuel statique affiché pour des objets Active Directory.
ms.assetid: ed945812-3adb-4058-bdb6-8d9d34468265
ms.tgt_platform: multiple
keywords:
- Inscription d’un élément de menu contextuel statique AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26e34d2ed02a4f30702ca91551b5b7f5c9dc3e2d1294faae043054be047031b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184508"
---
# <a name="registering-a-static-context-menu-item"></a>Inscription d’un élément de menu contextuel statique

les composants logiciels enfichables MMC d’administration de Active Directory Domain Services et le shell Windows fournissent un mécanisme pour ajouter un élément au menu contextuel affiché pour les objets dans Active Directory Domain Services. Le menu contextuel peut appeler n’importe quel fichier pouvant être démarré avec l’API [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) , par exemple une URL d’application ou de page Web.

## <a name="registering-with-active-directory-domain-services"></a>Inscription avec Active Directory Domain Services

L’inscription de l’extension du menu contextuel est spécifique à un paramètre régional. Si l’extension du menu contextuel s’applique à tous les paramètres régionaux, elle doit être inscrite dans l’objet [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) de la classe d’objet dans tous les sous-conteneurs de paramètres régionaux dans le conteneur de spécificateurs d’affichage. Si l’extension de menu contextuel est localisée pour certains paramètres régionaux, elle doit être inscrite dans l’objet **displaySpecifier** de ce sous-conteneur de paramètres régionaux. Pour plus d’informations sur le conteneur et les paramètres régionaux des spécificateurs d’affichage, consultez [spécificateurs d’affichage](display-specifiers.md) et [conteneur DisplaySpecifiers](displayspecifiers-container.md).

Il existe deux attributs de spécificateur d’affichage dans lesquels un élément de menu contextuel statique peut être inscrit, [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) et [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu).

L’attribut [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) identifie les menus contextuels d’administration à afficher dans les composants logiciels enfichables d’administration de Active Directory Domain Services. Le menu contextuel s’affiche lorsque l’utilisateur affiche le menu contextuel des objets de la classe appropriée dans l’un des composants logiciels enfichables MMC d’administration.

l’attribut [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) identifie les menus contextuels de l’utilisateur final à afficher dans le shell Windows. le menu contextuel s’affiche lorsque l’utilisateur consulte le menu contextuel des objets de la classe appropriée dans l’explorateur de Windows. à partir de Windows Server 2003, le shell Windows n’affiche plus les objets qui proviennent de Active Directory Domain Services.

Tous ces attributs sont à valeurs multiples.

Lors de l’inscription d’un élément de menu contextuel statique, les valeurs des attributs [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) et [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) requièrent le format suivant.


```C++
<order number>,<menu text>,<command>
```



« &lt; Order Number &gt; » est un nombre non signé qui représente la position de l’élément dans le menu contextuel. Lorsqu’un menu contextuel s’affiche, les valeurs sont triées à l’aide d’une comparaison de la valeur « &lt; Order Number » de chaque valeur &gt; . Si plusieurs valeurs ont le même « numéro de &lt; commande &gt; », ces extensions de menu contextuel sont chargées dans l’ordre dans lequel elles sont lues à partir du serveur de Active Directory. Si possible, utilisez un « numéro d’ordre » non existant &lt; &gt; , autrement dit un « numéro d’ordre » qui n’a pas été utilisé par d’autres valeurs de la propriété. Il n’y a pas de position de départ prescrite, et les espaces sont autorisés dans la &lt; séquence « Order Number &gt; ».

Le « &lt; texte &gt; de menu » est la chaîne affichée dans le menu contextuel. Le « &lt; texte &gt; de menu » peut inclure un caractère « & » qui précède le caractère de raccourci clavier pour l’élément de menu. Le caractère précédée est alors souligné. Par exemple, si le « &lt; texte du menu &gt; » est « &fichier », le texte du menu s’affiche sous la forme « fichier », « f » est souligné et « f » est le raccourci clavier de l’élément de menu.

« &lt; Command &gt; » est le programme ou le fichier exécuté par le composant logiciel enfichable. Soit le chemin d’accès complet doit être spécifié, soit le fichier doit exister dans la variable d’environnement du chemin d’accès de l’ordinateur. Le fichier est appelé à l’aide de la fonction [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) . La « &lt; commande &gt; » ne peut pas contenir de paramètres supplémentaires, par exemple, Notepad.exe Myfile.txt. Comme **ShellExecute** est utilisé, tout fichier ou adresse qui peut être passé à **ShellExecute** peut être utilisé pour « &lt; Command &gt; ». Par exemple, si « &lt; Command &gt; » contient « d : \\file.txt », d : \\file.txt sera ouvert avec l’application associée à l’extension .txt. De même, si « &lt; Command &gt; » contient « https://www.fabrikam.com », le navigateur Web par défaut s’ouvre et affiche la page Web spécifiée. Les chemins d’accès et les noms d’application avec des espaces sont autorisés. Si « &lt; Command &gt; » est une application, l’ADsPath et la classe de l’objet sélectionné sont passés en tant qu’arguments de ligne de commande, séparés par un espace.

dans l’interpréteur de commandes Windows, les éléments de menu contextuel à sélection multiple sont pris en charge. Dans ce cas, la « &lt; commande &gt; » est appelée pour chaque objet sélectionné. Dans Active Directory Domain Services composants logiciels enfichables d’administration, les éléments de menu contextuel statiques à sélection multiple ne sont pas pris en charge.

> [!IMPORTANT]
> pour le shell Windows, les données du spécificateur d’affichage sont récupérées à l’ouverture de session de l’utilisateur et mises en cache pour la session de l’utilisateur. Pour les composants logiciels enfichables d’administration, les données du spécificateur d’affichage sont récupérées lorsque le composant logiciel enfichable est chargé et mis en cache pour la durée du processus. pour le shell Windows, cela signifie que les modifications apportées aux spécificateurs d’affichage prennent effet après qu’un utilisateur se déconnecte puis de nouveau. Pour les composants logiciels enfichables d’administration, les modifications prennent effet lors du rechargement du composant logiciel enfichable ou de la console. autrement dit, si vous démarrez une nouvelle instance du fichier de console ou d’une nouvelle instance de Mmc.exe et que vous ajoutez le composant logiciel enfichable, les données du spécificateur d’affichage les plus récentes sont récupérées.

 

Pour plus d’informations et pour obtenir un exemple de code, consultez [exemple de code pour l’installation d’un élément de menu contextuel statique](example-code-for-installing-a-static-context-menu-item.md).

 

 