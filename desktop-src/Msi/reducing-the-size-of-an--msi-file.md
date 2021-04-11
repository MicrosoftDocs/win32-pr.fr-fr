---
description: Les développeurs de packages de Windows Installer peuvent remarquer que leurs fichiers. msi sont plus volumineux que prévu après des modifications et des enregistrements répétés.
ms.assetid: d5229ef5-0cb5-4daf-8468-0cb653029c1c
title: Réduction de la taille d’un fichier. msi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5a19c92f0567fc6081d772279ec2cc0b6cafef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951907"
---
# <a name="reducing-the-size-of-an-msi-file"></a><span data-ttu-id="acdfa-103">Réduction de la taille d’un fichier. msi</span><span class="sxs-lookup"><span data-stu-id="acdfa-103">Reducing the Size of an .msi File</span></span>

<span data-ttu-id="acdfa-104">Les développeurs de packages de Windows Installer peuvent remarquer que leurs fichiers. msi sont plus volumineux que prévu après des modifications et des enregistrements répétés.</span><span class="sxs-lookup"><span data-stu-id="acdfa-104">Developers of Windows Installer packages may notice their .msi files getting larger than expected after repeated edits and saves.</span></span> <span data-ttu-id="acdfa-105">Windows Installer fichiers. msi sont des fichiers composés qui contiennent des stockages et des flux, et qui présentent certaines des mêmes limites de stockage que les fichiers de documents OLE.</span><span class="sxs-lookup"><span data-stu-id="acdfa-105">Windows Installer .msi files are compound files that contain storages and streams, and have some of the same storage limitations as OLE document files.</span></span> <span data-ttu-id="acdfa-106">Si vous modifiez et enregistrez le même fichier. msi à chaque fois, cela crée un espace de stockage gaspillé dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="acdfa-106">If you edit and save the same .msi file over and over, it creates wasted storage space in the file.</span></span> <span data-ttu-id="acdfa-107">Cela affecte uniquement les auteurs des fichiers. msi et n’a aucun effet sur les utilisateurs de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="acdfa-107">This only affects authors of .msi files and has no effect on Windows Installer users.</span></span> <span data-ttu-id="acdfa-108">Les développeurs peuvent souhaiter supprimer cet espace de stockage gaspillé avant d’expédier leur fichier. msi final.</span><span class="sxs-lookup"><span data-stu-id="acdfa-108">Developers may want to remove this wasted storage space before shipping their final .msi file.</span></span>

<span data-ttu-id="acdfa-109">Pour supprimer l’espace de stockage gaspillé et réduire la taille finale des fichiers. msi, vous disposez des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="acdfa-109">To remove wasted storage space and reduce the final size of .msi files, you have the following options.</span></span>

-   <span data-ttu-id="acdfa-110">Exportez toutes les tables de la base de données vers des fichiers. IDT, puis importez-les dans une nouvelle base de données.</span><span class="sxs-lookup"><span data-stu-id="acdfa-110">Export all of the tables in the database to .idt files, and then import those into a new database.</span></span> <span data-ttu-id="acdfa-111">Cela produit le stockage le plus compact possible.</span><span class="sxs-lookup"><span data-stu-id="acdfa-111">This produces the most compact storage possible.</span></span>
-   <span data-ttu-id="acdfa-112">Utilisez un utilitaire logiciel pour compacter l’espace de stockage des fichiers de documents OLE.</span><span class="sxs-lookup"><span data-stu-id="acdfa-112">Use a software utility for compacting the storage space of OLE document files.</span></span>

 

 



