---
title: Inscription du client du canal virtuel
description: Vous devez stocker le nom de la DLL cliente dans le registre.
ms.assetid: bf84b2f4-55c2-45fd-bba7-8ff3efe4b1fd
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ac019a2c32a1eed09eb11b45a73261f1510bfa409ebe8e049370023f9199ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868649"
---
# <a name="virtual-channel-client-registration"></a>Inscription du client du canal virtuel

Vous devez stocker le nom de la DLL cliente dans le registre.

Dans le registre, ajoutez une sous-clé à l’un des emplacements suivants :

**HKEY \_ \_** \\  \\  \\  \\  \\ **Compléments** par défaut du client Microsoft Terminal Server du logiciel utilisateur actuel

**HKEY \_ \_** \\  \\  \\  \\  \\ **Compléments** de connexion client Microsoft Terminal Server du logiciel utilisateur actuel

> [!Note]  
> Dans le chemin d’accès du Registre, la *connexion* représente le nom d’une connexion dans le gestionnaire de connexions.

 

Les entrées sous la clé de **\\ \\ compléments par défaut** s’appliquent à toutes les connexions. Les entrées sous la **\\** clé de *_\\ compléments_* de _connexion_ s’appliquent uniquement à la connexion identifiée par la *connexion*. Les connexions peuvent être créées et gérées à l’aide du gestionnaire de connexions.

Vous pouvez attribuer n’importe quel nom à la sous-clé. Il doit contenir une valeur SZ **reg \_** ou **reg \_ expand \_** et peut éventuellement contenir une valeur **reg \_ DWORD** . La syntaxe de la valeur de **reg \_ SZ** ou **reg \_ expand \_** est la suivante.

``` syntax
Name = DLLname
```

Si **Name** est une valeur de **reg \_ expand \_ SZ** , il peut contenir des variables d’environnement non développées qui sont développées au moment de l’exécution.

La valeur de *DLLname* peut être un chemin d’accès complet. Si *DLLname* ne contient pas de chemin d’accès, la stratégie de recherche de dll standard est utilisée. Pour plus d’informations, consultez la section Notes pour [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya).

 

 