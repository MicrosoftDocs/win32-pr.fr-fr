---
title: Menus contextuels à utiliser avec les spécificateurs d’affichage
description: Les composants logiciels enfichables MMC d’administration Active Directory et Windows 2000 Shell fournissent un mécanisme pour ajouter un élément au menu contextuel affiché pour les objets dans Active Directory Domain Services.
ms.assetid: 0b0691f5-321d-4f22-b39c-bc528db9e707
ms.tgt_platform: multiple
keywords:
- afficher les spécificateurs Active Directory, menus contextuels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f28fbf703f17ea5c0fa7938365d485998be77e8d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103940835"
---
# <a name="context-menus-for-use-with-display-specifiers"></a>Menus contextuels à utiliser avec les spécificateurs d’affichage

Les composants logiciels enfichables MMC d’administration Active Directory et Windows 2000 Shell fournissent un mécanisme pour ajouter un élément au menu contextuel affiché pour les objets dans Active Directory Domain Services. Un élément de menu contextuel peut être ajouté en implémentant un serveur COM in-proc appelé *extension de menu contextuel*. Vous pouvez également ajouter un élément de menu contextuel qui appelle n’importe quel fichier démarré avec l’API [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) , telle qu’une application ou une URL de page Web. C’est ce qu’on appelle un *élément de menu contextuel statique*.

## <a name="developer-audience"></a>Public de développeurs

Cette documentation suppose que le lecteur est familiarisé avec l’opération COM et le développement de composants à l’aide de C++. Il n’est actuellement pas possible de créer une extension de menu contextuel Active Directory Domain Services à l’aide de Microsoft Visual Basic.

## <a name="extending-the-context-menu-with-a-context-menu-extension"></a>Extension du menu contextuel à l’aide d’une extension de menu contextuel

Une extension de menu contextuel est un serveur COM in-proc qui implémente certaines interfaces et est inscrit avec Active Directory Domain Services.

**Pour créer et installer une extension de menu contextuel**

1.  Créez la DLL d’extension du menu contextuel. Une extension de menu contextuel est un serveur COM in-proc qui, au minimum, implémente les interfaces [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) et [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) . Pour plus d’informations, consultez [implémentation de l’objet com du menu contextuel](implementing-the-context-menu-com-object.md).
2.  Installez l’extension de la feuille de menus contextuel sur les ordinateurs où l’extension du menu contextuel est utilisée. Pour ce faire, vous devez créer un package Microsoft Windows Installer pour la DLL d’extension du menu contextuel et déployer le package de manière appropriée à l’aide de la stratégie de groupe. Pour plus d’informations, consultez distribution des composants de l' [interface utilisateur](distributing-user-interface-components.md).
3.  Enregistrez l’extension du menu contextuel dans le Registre Windows et avec Active Directory Domain Services. Pour plus d’informations, consultez [inscription de l’objet com du menu contextuel dans un spécificateur d’affichage](registering-the-context-menu-com-object-in-a-display-specifier.md).

## <a name="extending-the-context-menu-with-a-static-context-menu-item"></a>Extension du menu contextuel à l’aide d’un élément de menu contextuel statique

Un élément de menu contextuel statique peut être utilisé pour appeler n’importe quel fichier démarré avec l’API [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) , par exemple une URL d’application ou de page Web. Pour ce faire, l’élément de menu contextuel statique d’une classe d’objet particulière doit être inscrit pour que l’élément de menu contextuel statique soit ajouté au menu contextuel des objets de cette classe. Pour plus d’informations, consultez [inscription d’un élément de menu contextuel statique](registering-a-static-context-menu-item.md).

 

 