---
description: à partir de Windows 7, les menus en cascade sont créés à l’aide de l’entrée de registre subcommandes, de l’entrée de registre ExtendedSubCommandsKey ou de l’interface IExplorerCommand.
title: Création de menus en cascade statiques
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E3A6F174-BE53-48EF-AE9B-A3F297E91B95
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 22fdc261012697affd99b5a1491ef5829fcc5329d5570ae4e3c37dcd111b457f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456329"
---
# <a name="creating-static-cascading-menus"></a>Création de menus en cascade statiques

dans Windows 7 et versions ultérieures, l’implémentation des menus en cascade est prise en charge via les paramètres du registre. avant le Windows 7, la création de menus en cascade était possible uniquement via l’implémentation de l’interface [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) . dans Windows 7 et versions ultérieures, vous devez recourir à des solutions basées sur le code COM (component Object Model) uniquement lorsque les méthodes statiques sont insuffisantes.

La capture d’écran suivante fournit un exemple de menu en cascade.

![capture d’écran montrant un exemple de menu en cascade](images/file-assoc/filecascademenu2ndex.png)

dans Windows 7 et versions ultérieures, il existe trois façons de créer des menus en cascade, qui sont décrits dans les sections suivantes.

-   [Comment créer des menus en cascade avec l’entrée de Registre subcommandes](how-to--create-cascading-menus-with-the-subcommands-registry-entry.md)
-   [Comment créer des menus en cascade avec l’entrée de Registre ExtendedSubCommandsKey](how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry.md)
-   [Comment créer des menus en cascade avec l’interface IExplorerCommand](how-to-create-cascading-menus-with-the-iexplorercommand-interface.md)

 

 
