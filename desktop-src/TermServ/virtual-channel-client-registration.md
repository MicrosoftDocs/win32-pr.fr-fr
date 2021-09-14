---
title: Inscription du client du canal virtuel
description: Vous devez stocker le nom de la DLL cliente dans le registre.
ms.assetid: bf84b2f4-55c2-45fd-bba7-8ff3efe4b1fd
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd7ecf128f125f6f25202bf683f8aa55ae4f257
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217348"
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

 

 