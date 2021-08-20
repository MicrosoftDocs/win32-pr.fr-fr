---
description: Un nom de symbole décoré comprend des caractères qui différencient la manière dont un symbole public a été déclaré.
ms.assetid: f02fa21d-3fe9-4838-a938-3136c34bc0e8
title: Noms de symboles décorés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60432788b69f0c8779030f32a190ccfb55859434f714a13f769b328ee246a309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076413"
---
# <a name="decorated-symbol-names"></a>Noms de symboles décorés

Un nom de symbole décoré comprend des caractères qui différencient la manière dont un symbole public a été déclaré. Pour les \_ \_ fonctions stdcall, les noms incluent le caractère « @ » et un nombre décimal qui spécifie le nombre d’octets dans ses paramètres de fonction. Par exemple, le nom décoré de la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) est LoadLibrary@4 . Pour les fonctions C++, la décoration de noms est plus complexe et varie d’un compilateur à l’autre.

Pour récupérer le nom du symbole non décoré, utilisez la fonction [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) . Vous pouvez également appeler la fonction [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) pour demander que le gestionnaire de symboles présente toujours des symboles avec des noms non décorés. Vous devez définir cette option avant de charger les symboles, car le gestionnaire de symboles crée les tables de noms de symboles au moment du chargement.

 

 
