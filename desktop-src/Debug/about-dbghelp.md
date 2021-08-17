---
description: Les rubriques suivantes décrivent les fichiers de symboles et les fonctionnalités fournies par les fonctions DbgHelp.
ms.assetid: 1bae2f0a-94a4-4152-bccc-b4deb1291a09
title: À propos de DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 958a139a7dcbffb8ee1b3b3d030d170fc821e6022038cab6a704b3b04f820f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162697"
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

 

 



