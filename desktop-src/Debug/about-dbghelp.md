---
description: Les rubriques suivantes décrivent les fichiers de symboles et les fonctionnalités fournies par les fonctions DbgHelp.
ms.assetid: 1bae2f0a-94a4-4152-bccc-b4deb1291a09
title: À propos de DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 634633d44d0c9e8202d99fd16140dd0a506453ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110331"
---
# <a name="about-dbghelp"></a>À propos de DbgHelp

Les rubriques suivantes décrivent les fichiers de symboles et les fonctionnalités fournies par les [fonctions dbghelp](dbghelp-functions.md).

-   [Versions de DbgHelp](dbghelp-versions.md)
-   [Fichiers de symboles](symbol-files.md)
-   [Gestion des symboles](symbol-handling.md)
-   [Serveurs de symboles et magasins de symboles](symbol-servers-and-symbol-stores.md)
-   [Fichiers minidump](minidump-files.md)
-   [Serveur source](source-server-and-source-indexing.md)
-   [Plateforme d'appui améliorée](updated-platform-support.md)

Notez que toutes les [fonctions dbghelp](dbghelp-functions.md) sont à thread unique. Par conséquent, les appels à partir de plusieurs threads à cette fonction entraîneront probablement un comportement inattendu ou une altération de la mémoire. Pour éviter cela, vous devez synchroniser tous les appels simultanés à partir de plusieurs threads à cette fonction.

 

 



