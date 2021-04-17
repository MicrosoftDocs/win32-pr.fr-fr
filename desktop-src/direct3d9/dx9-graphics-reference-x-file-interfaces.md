---
description: Cette section contient des informations de référence pour les interfaces COM utilisées pour lire et écrire à partir de fichiers DirectX. x. Action déconseillée.
ms.assetid: 66e3476a-4ee8-48ac-aab8-6653793e0ef3
title: X, interfaces de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6e47325a4912faeb919cb60571de3cccbbe265
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521935"
---
# <a name="x-file-interfaces"></a>X, interfaces de fichiers

Cette section contient des informations de référence pour les interfaces COM utilisées pour lire et écrire à partir de fichiers DirectX. x. Action déconseillée.

-   [**IDirectXFile**](idirectxfile.md)
-   [**IDirectXFileBinary**](idirectxfilebinary.md)
-   [**IDirectXFileData**](idirectxfiledata.md)
-   [**IDirectXFileDataReference**](idirectxfiledatareference.md)
-   [**IDirectXFileEnumObject**](idirectxfileenumobject.md)
-   [**IDirectXFileObject**](idirectxfileobject.md)
-   [**IDirectXFileSaveObject**](idirectxfilesaveobject.md)

Les tableaux suivants illustrent la relation entre les interfaces de fichier. x.



| Interface             | Dérive de           | Dérive de |
|-----------------------|------------------------|--------------|
|                       | IDirectXFile           | IUnknown     |
| IDirectXFileBinary    | IDirectXFileObject     | IUnknown     |
| IDirectXFileData      | IDirectXFileObject     | IUnknown     |
| IDirectXFileReference | IDirectXFileObject     | IUnknown     |
|                       | IDirectXFileSaveObject | IUnknown     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de fichier X (héritée)](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 



