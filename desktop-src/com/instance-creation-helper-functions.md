---
title: Fonctions d’assistance pour la création d’instances
description: Fonctions d’assistance pour la création d’instances
ms.assetid: 0b9b7bcf-f0f0-42c4-945e-63a532640d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84956f6040aaba13b46dea92bea611a49d5d8de3
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363372"
---
# <a name="instance-creation-helper-functions"></a>Fonctions d’assistance pour la création d’instances

Dans les versions précédentes de COM, le mécanisme principal utilisé pour créer une instance d’objet était la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) . Cette fonction encapsule le processus de création d’un objet de classe, à l’aide de cette fonction pour créer une nouvelle instance et libérer l’objet de classe. Une autre fonction de ce type est le [**OleCreate**](/windows/desktop/api/ole/nf-ole-olecreate)plus spécifique, le programme d’assistance de document composite OLE qui crée un objet de classe et récupère un pointeur vers un objet demandé.

Pour faciliter le processus de création d’instance sur des systèmes distribués, COM a introduit quatre nouveaux mécanismes de création d’instance importants :

-   Monikers de classe et [ **IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator)
-   [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)

Un moniker de classe vous permet d’identifier la classe d’un objet et est généralement utilisé avec un autre moniker, comme un moniker de fichier, pour indiquer l’emplacement de l’objet. Cela vous permet d’effectuer une liaison à un objet et de spécifier le serveur qui doit être lancé pour cet objet. Les monikers de classes peuvent également être composés à droite des monikers qui prennent en charge la liaison à l’interface [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) . Pour plus d’informations, consultez [monikers de classes](class-monikers.md).

[**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) étend [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour permettre de créer un objet unique non initialisé associé au CLSID donné sur une machine distante spécifiée. En outre, au lieu de demander une seule interface et d’obtenir un seul pointeur vers cette interface, **CoCreateInstanceEx** permet d’interroger plusieurs interfaces et (si disponibles) de recevoir des pointeurs vers ces interfaces en un seul aller-retour, ce qui permet de réduire le nombre d’allers-retours entre les machines. Cela peut rendre l’interaction des objets à distance bien plus efficace. Pour ce faire, la fonction utilise un tableau de [**structures \_ Qi multiples**](/windows/win32/api/objidlbase/ns-objidlbase-multi_qi) .

La création d’un objet via [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) requiert toujours que l’objet soit initialisé via un appel à l’une des interfaces d’initialisation (telle que [**IPersistStorage :: Load**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-load)). Les fonctions d’assistance [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) et [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) encapsulent à la fois la puissance de création d’instance de **CoCreateInstanceEx** et l’initialisation, la première d’un fichier et la dernière à partir d’un stockage.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’un objet à l’aide d’un objet de classe](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 