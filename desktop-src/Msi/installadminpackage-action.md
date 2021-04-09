---
description: L’action InstallAdminPackage copie la base de données du produit sur le point d’installation d’administration, qui est défini par la propriété TARGETDIR.
ms.assetid: 9781f14b-0264-4d00-9a83-bd5400c614ec
title: Action InstallAdminPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1eb2f86390fe3a47a6d100a887d34798e7f4d4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951744"
---
# <a name="installadminpackage-action"></a><span data-ttu-id="0c4e8-103">Action InstallAdminPackage</span><span class="sxs-lookup"><span data-stu-id="0c4e8-103">InstallAdminPackage Action</span></span>

<span data-ttu-id="0c4e8-104">L’action InstallAdminPackage copie la base de données du produit sur le point d’installation d’administration, qui est défini par la propriété [**targetDir**](targetdir.md) .</span><span class="sxs-lookup"><span data-stu-id="0c4e8-104">The InstallAdminPackage action copies the product database to the administrative installation point, which is defined by the [**TARGETDIR**](targetdir.md) property.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="0c4e8-105">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="0c4e8-105">Sequence Restrictions</span></span>

<span data-ttu-id="0c4e8-106">Il n’existe aucune restriction de séquence.</span><span class="sxs-lookup"><span data-stu-id="0c4e8-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="0c4e8-107">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="0c4e8-107">ActionData Messages</span></span>



| <span data-ttu-id="0c4e8-108">Champ</span><span class="sxs-lookup"><span data-stu-id="0c4e8-108">Field</span></span> | <span data-ttu-id="0c4e8-109">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="0c4e8-109">Description of action data</span></span>                                 |
|-------|------------------------------------------------------------|
| <span data-ttu-id="0c4e8-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="0c4e8-110">\[1\]</span></span> | <span data-ttu-id="0c4e8-111">Nom des fichiers d’installation.</span><span class="sxs-lookup"><span data-stu-id="0c4e8-111">Name of install files.</span></span>                                     |
| <span data-ttu-id="0c4e8-112">\[6\]</span><span class="sxs-lookup"><span data-stu-id="0c4e8-112">\[6\]</span></span> | <span data-ttu-id="0c4e8-113">Taille de la base de données.</span><span class="sxs-lookup"><span data-stu-id="0c4e8-113">Size of database.</span></span>                                          |
| <span data-ttu-id="0c4e8-114">\[9\]</span><span class="sxs-lookup"><span data-stu-id="0c4e8-114">\[9\]</span></span> | <span data-ttu-id="0c4e8-115">Identificateur de l’installation administrative – répertoire du point.</span><span class="sxs-lookup"><span data-stu-id="0c4e8-115">Identifier of administrative installation–point directory.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0c4e8-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0c4e8-116">Remarks</span></span>

<span data-ttu-id="0c4e8-117">L’action InstallAdminPackage met également à jour les informations récapitulatives de la base de données et supprime tous les fichiers CAB situés dans les flux de données une fois la base de données copiée.</span><span class="sxs-lookup"><span data-stu-id="0c4e8-117">The InstallAdminPackage action also updates the summary information of the database and removes any cabinet files located in streams after the database is copied.</span></span>

 

 



