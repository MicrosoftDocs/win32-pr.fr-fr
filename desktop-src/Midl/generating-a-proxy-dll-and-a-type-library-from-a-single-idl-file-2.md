---
title: Génération d’une DLL de proxy et d’une bibliothèque de types à partir d’un seul fichier IDL
description: Vous pouvez utiliser un seul fichier IDL pour générer des fichiers stub proxy et des fichiers d’en-tête pour le marshaling de code et une bibliothèque de types.
ms.assetid: faa647ac-765a-45bd-8193-b6ea90d064ff
keywords:
- Microsoft Interface Definition Language MIDL, tâches, génération d’une DLL de proxy et d’une bibliothèque de types
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e7bf2694b791007b0f1da303525217cf55d75d574e083c6d1756bc2784d0ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384235"
---
# <a name="generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file"></a>Génération d’une DLL de proxy et d’une bibliothèque de types à partir d’un seul fichier IDL

Vous pouvez utiliser un seul fichier IDL pour générer des fichiers stub proxy et des fichiers d’en-tête pour le marshaling de code et une bibliothèque de types. Pour ce faire, définissez une interface en dehors du bloc de bibliothèque, puis référencez cette interface à l’intérieur du bloc de bibliothèque, comme illustré dans cet exemple :

``` syntax
//file: AllKnown.idl

[
    object, uuid(. . .), <other interface attributes>
]
interface IKnown : IUnknown 
{
    import "unknwn.idl";
    <declarations, etc. for IKnown interface go here>
};

[
    <library attributes>
]
library KnownLibrary 
{

    //reference interface IKnown:
    interface IKnown;

    //or create a new class:
    [
        <coclass attributes>
    ] 
    coclass KnowMore 
    {
       interface IKnown;
    };
};
```

Pour plus d’informations, consultez [marshaling de types de données OLE](marshaling-ole-data-types.md) et [fichiers supplémentaires requis pour générer une bibliothèque de types](additional-files-required-to-generate-a-type-library-2.md).

 

 




