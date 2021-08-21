---
title: Monikers de classe
description: Bien que les classes soient généralement identifiées directement avec des CLSID dans des fonctions telles que CoCreateInstance ou CoGetClassObject, les classes peuvent également être identifiées par un moniker appelé un moniker de classe.
ms.assetid: 63f5d256-cb61-4673-b5d6-da5c1d89dfa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499a117372cd7364fc52b3503b30175a4be11afb9e28e3dd32adbf1007185f85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048690"
---
# <a name="class-monikers"></a>Monikers de classe

Bien que les classes soient généralement identifiées directement avec des CLSID dans des fonctions telles que [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), les classes peuvent également être identifiées par un moniker appelé un *moniker de classe*. Les monikers de classe sont liés à l’objet de classe de la classe pour laquelle ils sont créés.

La possibilité d’identifier des classes avec un moniker prend en charge des opérations utiles qui, sinon, ne sont pas difficiles à manier. Par exemple, les monikers de fichiers traditionnellement prennent en charge la liaison riche uniquement à la classe associée à la classe de fichier à laquelle ils font appel ; le moniker d’un fichier Excel est lié à une instance d’un objet Excel et un moniker à une image gif est lié à une instance du gestionnaire GIF actuellement inscrit. Un moniker de classe vous permet d’indiquer la classe que vous souhaitez utiliser pour manipuler un fichier par le biais d’une composition avec un moniker de fichier. un moniker de classe pour une classe de graphique 3d composée d’un moniker à un fichier Excel produit un moniker qui se lie à une instance de l’objet de graphique 3d et initialise l’objet avec le contenu du fichier Excel.

Les monikers de classe sont donc particulièrement utiles dans la composition avec d’autres types de monikers, tels que des monikers de fichiers ou des monikers d’élément.

Les monikers de classes peuvent également être composés à droite des monikers qui prennent en charge la liaison à l’interface [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) . Lorsqu’il est composé de cette manière, **IClassActivator** donne simplement accès à l’objet de classe et aux instances de la classe par le biais de [**IClassActivator :: GetClassObject,**](/windows/desktop/api/ObjIdl/nf-objidl-iclassactivator-getclassobject). Les monikers de classe peuvent être identifiés via [**IMoniker :: IsSystemMoniker**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-issystemmoniker), qui retourne MKSYS \_ CLASSMONIKER dans *pdwMksys*.

Les programmeurs créent généralement des monikers de classe à l’aide de la fonction [**CreateClassMoniker**](/windows/desktop/api/Objbase/nf-objbase-createclassmoniker) ou via [**MkParseDisplayName**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname). (Pour plus d’informations, consultez [**IMoniker ::P arsedisplayname**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-parsedisplayname) .)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Anti-monikers](anti-monikers.md)
</dt> <dt>

[Monikers composites](composite-monikers.md)
</dt> <dt>

[Monikers de fichiers](file-monikers.md)
</dt> <dt>

[Monikers d’élément](item-monikers.md)
</dt> <dt>

[Monikers de pointeur](pointer-monikers.md)
</dt> </dl>

 

 




