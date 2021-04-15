---
description: Utilisez la procédure suivante dans les applications héritées pour charger un fichier. x.
ms.assetid: 2b975873-2e5d-4c64-a022-d2098c3d95b8
title: Chargement d’un fichier X (hérité) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716ed54afdc7d1aa18fdde992a0799a8990a49c6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521167"
---
# <a name="loading-an-x-file-legacy-direct3d-9"></a>Chargement d’un fichier X (hérité) (Direct3D 9)

Utilisez la procédure suivante dans les applications héritées pour charger un fichier. x.

1.  Utilisez la fonction [**DirectXFileCreate**](directxfilecreate.md) pour créer un objet [**IDirectXFile**](idirectxfile.md) .
2.  Si des modèles sont présents dans le fichier DirectX que vous allez charger, utilisez la méthode [**IDirectXFile :: RegisterTemplates**](idirectxfile--registertemplates.md) pour inscrire ces modèles.
3.  Utilisez la méthode [**IDirectXFile :: CreateEnumObject**](idirectxfile--createenumobject.md) pour créer un objet énumérateur [**IDirectXFileEnumObject**](idirectxfileenumobject.md) .
4.  Parcourez les objets dans le fichier. Pour chaque objet, procédez comme suit.
    1.  Utilisez la méthode [**IDirectXFileEnumObject :: GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md) pour récupérer chaque objet [**IDirectXFileData**](idirectxfiledata.md) .
    2.  Utilisez la méthode [**IDirectXFileData :: GetType**](idirectxfiledata--gettype.md) pour récupérer le type des données.
    3.  Chargez les données à l’aide de la méthode [**IDirectXFileData :: GetData**](idirectxfiledata--getdata.md) .
    4.  Si l’objet a des membres facultatifs, récupérez les membres facultatifs en appelant la méthode [**IDirectXFileData :: GetNextObject**](idirectxfiledata--getnextobject.md) .
    5.  Libérer l’objet [**IDirectXFileData**](idirectxfiledata.md) .
5.  Libérer l’objet [**IDirectXFileEnumObject**](idirectxfileenumobject.md) .
6.  Libérer l’objet [**IDirectXFile**](idirectxfile.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[X fichiers (hérités)](x-files--legacy-.md)
</dt> </dl>

 

 



