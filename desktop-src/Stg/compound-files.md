---
title: Fichiers composés
description: Bien que vous puissiez implémenter vos propres interfaces et objets de stockage structurés, COM fournit une implémentation standard appelée fichiers composés.
ms.assetid: 23b425e6-dfe5-403b-8f43-de6843a03dcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62be79f09afd23e53a569b76ad3e0af46cae2f9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190870"
---
# <a name="compound-files"></a><span data-ttu-id="ba05f-103">Fichiers composés</span><span class="sxs-lookup"><span data-stu-id="ba05f-103">Compound Files</span></span>

<span data-ttu-id="ba05f-104">Bien que vous puissiez implémenter vos propres interfaces et objets de stockage structurés, COM fournit une implémentation standard appelée fichiers composés.</span><span class="sxs-lookup"><span data-stu-id="ba05f-104">Although you can implement your own structured storage objects and interfaces, COM provides a standard implementation called Compound Files.</span></span> <span data-ttu-id="ba05f-105">L’utilisation de fichiers composés vous fait gagner du travail de codage de votre propre implémentation du stockage structuré et confère plusieurs avantages supplémentaires dérivés de l’adhésion à une norme définie.</span><span class="sxs-lookup"><span data-stu-id="ba05f-105">Using Compound Files saves you the work of coding your own implementation of structured storage and confers several additional benefits derived from adhering to a defined standard.</span></span> <span data-ttu-id="ba05f-106">Ces avantages incluent ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="ba05f-106">These benefits include the following:</span></span>

-   <span data-ttu-id="ba05f-107">**Indépendance du système de fichiers et de la plateforme**.</span><span class="sxs-lookup"><span data-stu-id="ba05f-107">**File-system and platform independence**.</span></span> <span data-ttu-id="ba05f-108">Étant donné que l’implémentation des fichiers composés de COM s’exécute sur les systèmes de fichiers plats existants, les fichiers composés stockés dans le système de fichiers FAT, le système de fichiers NTFS ou les systèmes de fichiers Macintosh peuvent être ouverts par les applications à l’aide de l’un des autres systèmes de fichiers.</span><span class="sxs-lookup"><span data-stu-id="ba05f-108">Because COM's Compound Files implementation runs on top of existing flat-file systems, compound files stored in the FAT file system, NTFS file system, or Macintosh file systems can be opened by applications using any one of the other file systems.</span></span>
-   <span data-ttu-id="ba05f-109">**Recherche**.</span><span class="sxs-lookup"><span data-stu-id="ba05f-109">**Searchable**.</span></span> <span data-ttu-id="ba05f-110">Étant donné que les objets distincts d’un fichier composé sont enregistrés dans un format standard et accessibles à l’aide d’interfaces et d’API COM standard, tout utilitaire de navigateur utilisant ces interfaces et ces API peut répertorier les objets dans le fichier, même si les données d’un objet donné peuvent être dans un format propriétaire.</span><span class="sxs-lookup"><span data-stu-id="ba05f-110">Because the separate objects in a compound file are saved in a standard format and can be accessed using standard COM interfaces and APIs, any browser utility using these interfaces and APIs can list the objects in the file, even though data within a given object may be in a proprietary format.</span></span>
-   <span data-ttu-id="ba05f-111">**Accès à certaines données internes**.</span><span class="sxs-lookup"><span data-stu-id="ba05f-111">**Access to certain internal data**.</span></span> <span data-ttu-id="ba05f-112">Étant donné que l’implémentation de fichiers composés fournit des méthodes standard d’écriture de certains types de données (informations de synthèse, par exemple), les applications peuvent lire ces données à l’aide des interfaces COM et des API.</span><span class="sxs-lookup"><span data-stu-id="ba05f-112">Because the Compound Files implementation provides standard ways of writing certain types of data—summary information, for example—applications can read this data using COM interfaces and APIs.</span></span>

 

 




