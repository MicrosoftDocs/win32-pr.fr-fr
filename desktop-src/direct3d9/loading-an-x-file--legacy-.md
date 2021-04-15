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
# <a name="loading-an-x-file-legacy-direct3d-9"></a><span data-ttu-id="bbca6-103">Chargement d’un fichier X (hérité) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bbca6-103">Loading an X File (Legacy) (Direct3D 9)</span></span>

<span data-ttu-id="bbca6-104">Utilisez la procédure suivante dans les applications héritées pour charger un fichier. x.</span><span class="sxs-lookup"><span data-stu-id="bbca6-104">Use the following procedure in legacy applications to load a .x file.</span></span>

1.  <span data-ttu-id="bbca6-105">Utilisez la fonction [**DirectXFileCreate**](directxfilecreate.md) pour créer un objet [**IDirectXFile**](idirectxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="bbca6-105">Use the [**DirectXFileCreate**](directxfilecreate.md) function to create an [**IDirectXFile**](idirectxfile.md) object.</span></span>
2.  <span data-ttu-id="bbca6-106">Si des modèles sont présents dans le fichier DirectX que vous allez charger, utilisez la méthode [**IDirectXFile :: RegisterTemplates**](idirectxfile--registertemplates.md) pour inscrire ces modèles.</span><span class="sxs-lookup"><span data-stu-id="bbca6-106">If templates are present in the DirectX file that you will load, use the [**IDirectXFile::RegisterTemplates**](idirectxfile--registertemplates.md) method to register those templates.</span></span>
3.  <span data-ttu-id="bbca6-107">Utilisez la méthode [**IDirectXFile :: CreateEnumObject**](idirectxfile--createenumobject.md) pour créer un objet énumérateur [**IDirectXFileEnumObject**](idirectxfileenumobject.md) .</span><span class="sxs-lookup"><span data-stu-id="bbca6-107">Use the [**IDirectXFile::CreateEnumObject**](idirectxfile--createenumobject.md) method to create an [**IDirectXFileEnumObject**](idirectxfileenumobject.md) enumerator object.</span></span>
4.  <span data-ttu-id="bbca6-108">Parcourez les objets dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="bbca6-108">Loop through the objects in the file.</span></span> <span data-ttu-id="bbca6-109">Pour chaque objet, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="bbca6-109">For each object, perform the following steps.</span></span>
    1.  <span data-ttu-id="bbca6-110">Utilisez la méthode [**IDirectXFileEnumObject :: GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md) pour récupérer chaque objet [**IDirectXFileData**](idirectxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="bbca6-110">Use the [**IDirectXFileEnumObject::GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md) method to retrieve each [**IDirectXFileData**](idirectxfiledata.md) object.</span></span>
    2.  <span data-ttu-id="bbca6-111">Utilisez la méthode [**IDirectXFileData :: GetType**](idirectxfiledata--gettype.md) pour récupérer le type des données.</span><span class="sxs-lookup"><span data-stu-id="bbca6-111">Use the [**IDirectXFileData::GetType**](idirectxfiledata--gettype.md) method to retrieve the data's type.</span></span>
    3.  <span data-ttu-id="bbca6-112">Chargez les données à l’aide de la méthode [**IDirectXFileData :: GetData**](idirectxfiledata--getdata.md) .</span><span class="sxs-lookup"><span data-stu-id="bbca6-112">Load the data using the [**IDirectXFileData::GetData**](idirectxfiledata--getdata.md) method.</span></span>
    4.  <span data-ttu-id="bbca6-113">Si l’objet a des membres facultatifs, récupérez les membres facultatifs en appelant la méthode [**IDirectXFileData :: GetNextObject**](idirectxfiledata--getnextobject.md) .</span><span class="sxs-lookup"><span data-stu-id="bbca6-113">If the object has optional members, retrieve the optional members by calling the [**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md) method.</span></span>
    5.  <span data-ttu-id="bbca6-114">Libérer l’objet [**IDirectXFileData**](idirectxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="bbca6-114">Release the [**IDirectXFileData**](idirectxfiledata.md) object.</span></span>
5.  <span data-ttu-id="bbca6-115">Libérer l’objet [**IDirectXFileEnumObject**](idirectxfileenumobject.md) .</span><span class="sxs-lookup"><span data-stu-id="bbca6-115">Release the [**IDirectXFileEnumObject**](idirectxfileenumobject.md) object.</span></span>
6.  <span data-ttu-id="bbca6-116">Libérer l’objet [**IDirectXFile**](idirectxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="bbca6-116">Release the [**IDirectXFile**](idirectxfile.md) object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbca6-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bbca6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbca6-118">X fichiers (hérités)</span><span class="sxs-lookup"><span data-stu-id="bbca6-118">X Files (Legacy)</span></span>](x-files--legacy-.md)
</dt> </dl>

 

 



