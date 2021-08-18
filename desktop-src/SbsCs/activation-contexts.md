---
description: Les contextes d’activation sont des structures de données en mémoire qui contiennent des informations que le système peut utiliser pour rediriger une application afin de charger une version de DLL particulière, une instance d’objet COM ou une version de fenêtre personnalisée.
ms.assetid: 5416f8c0-d99b-4a5d-a689-a47bd0cf1a88
title: Contextes d’activation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21aaf2c4d2e4fc0f3ef691406e663dc5efac44a9d0b34880596d21cac8a5f621
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142542"
---
# <a name="activation-contexts"></a>Contextes d’activation

Les [*contextes d’activation*](a-sbscs-gly.md) sont des structures de données en mémoire qui contiennent des informations que le système peut utiliser pour rediriger une application afin de charger une version de dll particulière, une instance d’objet com ou une version de fenêtre personnalisée. Une section du contexte d’activation peut contenir des informations de redirection de DLL qui sont utilisées par le chargeur de DLL. une autre section peut contenir des informations sur le serveur COM. Les fonctions de contexte d’activation utilisent, créent, activent et désactivent des contextes d’activation. Les fonctions d’activation peuvent rediriger la liaison d’une application vers des objets de version nommée qui spécifient des versions de DLL, des classes de fenêtre, des serveurs COM, des bibliothèques de types et des interfaces spécifiques. Pour plus d’informations sur les structures et les fonctions de contexte d’activation, consultez la [Référence du contexte d’activation](activation-context-reference.md).

à partir de Windows XP, les fonctions de contexte d’activation permettent à Windows d’utiliser des informations dans les [manifestes](manifests.md) pour créer des objets de nom de version. si une application crée un processus en appelant [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa), Windows vérifie l’existence d’un [manifeste d’application](application-manifests.md). si un manifeste existe, Windows utilise les informations du manifeste pour remplir le contexte d’activation. Étant donné que les manifestes décrivent la dépendance d’une application vis-à-vis des versions d' [assembly côte à côte](about-side-by-side-assemblies-.md) , les objets spécifiés sans versions dans le manifeste sont mappés aux objets de version nommée. Par exemple, le manifeste peut décrire des dll, des fichiers, des classes de fenêtre, des serveurs COM, des bibliothèques de types et des interfaces.

Lorsqu’un objet global est créé dans le contexte d’activation, le système attribue automatiquement à l’objet un nom spécifique à la version en consultant le manifeste. Lorsque l’application s’exécute et demande un objet nommé, elle obtient l’objet de nom de version. Cela permet à plusieurs versions d’un module de code de s’exécuter sur le système en même temps sans interférer entre eux. par exemple, [Windows Shell](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)) utilise un manifeste pour décrire une dépendance à la version 6,0 de COMCTL32 et pour créer des versions de classes de fenêtres.

Si une application crée une ressource en appelant [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa), le processus spécifie un nom de classe pour cette fonction. L’appel à [**GetCurrentActCtx**](/windows/desktop/api/Winbase/nf-winbase-getcurrentactctx) obtient le contexte d’activation actuel et vérifie s’il existe un mappage pour le nom de classe donné. Si un mappage existe, il utilise cette version du processus appelant pour résoudre le mappage et fournir le nom de classe spécifique à la version. Windows crée une fenêtre avec la procédure de fenêtre, les styles et d’autres attributs associés à ce nom de classe et à cette version.

Le contexte d’activation est géré par le système dans la plupart des cas. Les développeurs d’applications et les fournisseurs d’assemblys n’ont généralement pas besoin d’effectuer des appels à la pile. Les applications peuvent gérer un contexte d’activation en appelant directement le contexte d’activation. Pour plus d’informations, consultez [utilisation de l’API de contexte d’activation](using-the-activation-context-api.md).

 

 
