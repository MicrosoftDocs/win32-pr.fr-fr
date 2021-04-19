---
description: Windows Installer implémente un certain nombre de contrôles standard que les auteurs de packages peuvent placer dans des boîtes de dialogue. Toutefois, tous les contrôles Microsoft Windows standard ne sont pas disponibles et les contrôles personnalisés ne peuvent pas être créés pour être utilisés avec l’interface utilisateur du programme d’installation.
ms.assetid: 28416905-ce9a-4bb7-97b7-646c01f370ab
title: Vue d’ensemble des contrôles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85fbd8477416eb5a126eca56cb1050112309b0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521190"
---
# <a name="controls-overview"></a>Vue d’ensemble des contrôles

Windows Installer implémente un certain nombre de contrôles standard que les auteurs de packages peuvent placer dans des boîtes de dialogue. Toutefois, tous les contrôles Microsoft Windows standard ne sont pas disponibles et les contrôles personnalisés ne peuvent pas être créés pour être utilisés avec l’interface utilisateur du programme d’installation.

Les contrôles sont créés sur les boîtes de dialogue dans le programme d’installation d’une manière similaire à la façon dont les boîtes de dialogue sont créées par programme à l’aide de l’API de l’interface utilisateur Microsoft Windows. Un contrôle est créé à partir d’un modèle enregistré dans la table de contrôle. Ce modèle est légèrement différent en ce qu’il contient le nom unique de la boîte de dialogue dans laquelle le contrôle apparaît.

Dans l’API de l’interface utilisateur de Microsoft Windows, l’interaction de l’utilisateur s’effectue en créant une fonction de rappel pour gérer les messages publiés par le contrôle. En outre, la plupart des contrôles Microsoft Windows reçoivent des messages, tels que ceux envoyés par la fonction [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) .

La communication entre l’utilisateur et les contrôles s’effectue dans le programme d’installation à l’aide de [ControlEvents](controlevent-overview.md). Toutefois, il existe un ensemble limité de ControlEvents qui sont spécifiques à chaque contrôle dans l’ensemble limité de contrôles dans Windows Installer. Les contrôles peuvent poster plus d’un ControlEvent, et peuvent recevoir plusieurs ControlEvent,.

Les contrôles peuvent publier des ControlEvents spécifiques à l’aide de la table ControlEvent,. Les contrôles peuvent recevoir ControlEvents via l’utilisation de la [table EventMapping](eventmapping-table.md).

Windows Installer publie ControlEvents lors de l’exécution de certaines actions également, et les contrôles souscrits à ces ControlEvents dans la table EventMapping les reçoivent.

 

 
