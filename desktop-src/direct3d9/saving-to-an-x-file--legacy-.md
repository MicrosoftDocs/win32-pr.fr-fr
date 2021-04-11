---
description: Utilisez la procédure suivante dans les applications héritées pour enregistrer les modèles de fichier. x et les données dans un fichier. x.
ms.assetid: 5401b381-3599-465a-b41b-e63b7372fc0e
title: Enregistrement dans un fichier X (hérité) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 467f824c8e3ab9cd360a93d3f69fd1a2352548ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317654"
---
# <a name="saving-to-an-x-file-legacy-direct3d-9"></a>Enregistrement dans un fichier X (hérité) (Direct3D 9)

Utilisez la procédure suivante dans les applications héritées pour enregistrer les modèles de fichier. x et les données dans un fichier. x.

1.  Utilisez la fonction [**DirectXFileCreate**](directxfilecreate.md) pour créer un objet [**IDirectXFile**](idirectxfile.md) .
2.  Utilisez la méthode [**IDirectXFile :: RegisterTemplates**](idirectxfile--registertemplates.md) pour informer le système de fichiers DirectX des modèles que vous allez utiliser.
3.  Utilisez la méthode [**IDirectXFile :: CreateSaveObject**](idirectxfile--createsaveobject.md) pour créer un objet [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) .
4.  Utilisez la méthode [**IDirectXFileSaveObject :: SaveTemplates**](idirectxfilesaveobject--savetemplates.md) pour enregistrer les modèles, si vous le souhaitez.
5.  Parcourez les objets à enregistrer. Pour chaque objet de niveau supérieur, procédez comme suit.
    -   Utilisez la méthode [**IDirectXFileSaveObject :: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) pour créer un objet [**IDirectXFileData**](idirectxfiledata.md) en tant qu’objet de niveau supérieur dans le fichier. Si l’objet de données de niveau supérieur a des objets enfants facultatifs, ajoutez-les à l’objet à l’aide de la méthode appropriée de l’étape suivante.
    -   Chaque objet [**IDirectXFileData**](idirectxfiledata.md) peut avoir des objets enfants facultatifs si son modèle l’autorise. Les objets enfants peuvent être l’un des trois types d’objets suivants : **IDirectXFileData**, [**IDirectXFileDataReference**](idirectxfiledatareference.md)ou [**IDirectXFileBinary**](idirectxfilebinary.md). Parcourez les objets que vous devez enregistrer, en ajoutant chaque membre enfant facultatif à la liste d’objets de la manière appropriée à son type, comme illustré dans les étapes suivantes. Ensuite, si le type d’objet est données, appelez la méthode [**IDirectXFileSaveObject :: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) pour créer un objet **IDirectXFileData** , puis appelez la méthode [**IDirectXFileData :: AddDataObject**](idirectxfiledata--adddataobject.md) pour l’ajouter en tant qu’enfant de l’objet. Si le type d’objet est une référence de données, appelez la méthode [**IDirectXFileData :: AddDataReference**](idirectxfiledata--adddatareference.md) pour créer et ajouter l’objet de référence de données en tant qu’enfant de l’objet. Ou, si le type d’objet est binaire, appelez la méthode [**IDirectXFileData :: AddBinaryObject**](idirectxfiledata--addbinaryobject.md) pour créer et ajouter l’objet binaire en tant qu’enfant de l’objet.
    -   Appelez la méthode [**IDirectXFileSaveObject :: SaveData**](idirectxfilesaveobject--savedata.md) pour enregistrer l’objet de données et ses enfants.
    -   Libérer l’objet [**IDirectXFileData**](idirectxfiledata.md) .
6.  Libérer l’objet [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) .
7.  Libérer l’objet [**IDirectXFile**](idirectxfile.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[X fichiers (hérités)](x-files--legacy-.md)
</dt> </dl>

 

 



