---
description: Windows Le programme d’installation implémente un certain nombre de contrôles standard que les auteurs de packages peuvent placer dans des boîtes de dialogue. toutefois, tous les contrôles Microsoft Windows standard ne sont pas disponibles et les contrôles personnalisés ne peuvent pas être créés pour être utilisés avec l’interface utilisateur du programme d’installation.
ms.assetid: 28416905-ce9a-4bb7-97b7-646c01f370ab
title: Vue d’ensemble des contrôles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee9d03f0f21f9cc0611a1fae4831b6ccbbda9f40eda873cdf4c26b259ec43f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638521"
---
# <a name="controls-overview"></a>Vue d’ensemble des contrôles

Windows Le programme d’installation implémente un certain nombre de contrôles standard que les auteurs de packages peuvent placer dans des boîtes de dialogue. toutefois, tous les contrôles Microsoft Windows standard ne sont pas disponibles et les contrôles personnalisés ne peuvent pas être créés pour être utilisés avec l’interface utilisateur du programme d’installation.

les contrôles sont créés sur les boîtes de dialogue dans le programme d’installation d’une manière similaire à la façon dont les boîtes de dialogue sont créées par programme à l’aide de l’API de l’interface utilisateur Microsoft Windows. Un contrôle est créé à partir d’un modèle enregistré dans la table de contrôle. Ce modèle est légèrement différent en ce qu’il contient le nom unique de la boîte de dialogue dans laquelle le contrôle apparaît.

dans l’API de l’interface utilisateur de Microsoft Windows, l’interaction de l’utilisateur s’effectue en créant une fonction de rappel pour gérer les messages publiés par le contrôle. en outre, la plupart des contrôles Microsoft Windows reçoivent des messages, tels que ceux envoyés par la fonction [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) .

La communication entre l’utilisateur et les contrôles s’effectue dans le programme d’installation à l’aide de [ControlEvents](controlevent-overview.md). toutefois, il existe un ensemble limité de ControlEvents qui sont spécifiques à chaque contrôle dans l’ensemble limité de contrôles dans Windows Installer. Les contrôles peuvent poster plus d’un ControlEvent, et peuvent recevoir plusieurs ControlEvent,.

Les contrôles peuvent publier des ControlEvents spécifiques à l’aide de la table ControlEvent,. Les contrôles peuvent recevoir ControlEvents via l’utilisation de la [table EventMapping](eventmapping-table.md).

Windows Le programme d’installation publie ControlEvents au cours de l’exécution de certaines actions, et les contrôles souscrits à ces ControlEvents dans la table EventMapping les reçoivent.

 

 
