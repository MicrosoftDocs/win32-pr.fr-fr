---
description: La méthode CreateSourceImage de l’objet Merge permet au client d’extraire les fichiers d’un module vers une image source sur le disque après une fusion, en tenant compte des modifications apportées au module au cours de la configuration du module.
ms.assetid: c3e3465a-d5a7-4fcc-b26a-5a8c763c23d9
title: Merge. CreateSourceImage, méthode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CreateSourceImage
- IMsmMerge.CreateSourceImage
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: e8d9365a69ff6f33c2989e9102bac7c9c22166aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542569"
---
# <a name="mergecreatesourceimage-method"></a><span data-ttu-id="b1e0d-103">Merge. CreateSourceImage, méthode</span><span class="sxs-lookup"><span data-stu-id="b1e0d-103">Merge.CreateSourceImage method</span></span>

<span data-ttu-id="b1e0d-104">La méthode **CreateSourceImage** de l’objet [**Merge**](merge-object.md) permet au client d’extraire les fichiers d’un module vers une image source sur le disque après une fusion, en tenant compte des modifications apportées au module au cours de la configuration du module.</span><span class="sxs-lookup"><span data-stu-id="b1e0d-104">The **CreateSourceImage** method of the [**Merge**](merge-object.md) object allows the client to extract the files from a module to a source image on disk after a merge, taking into account changes to the module that might have been made during module configuration.</span></span> <span data-ttu-id="b1e0d-105">La liste des fichiers à extraire est extraite de la table de fichiers du module pendant le processus de fusion.</span><span class="sxs-lookup"><span data-stu-id="b1e0d-105">The list of files to be extracted is taken from the file table of the module during the merge process.</span></span> <span data-ttu-id="b1e0d-106">La liste des fichiers se compose de chaque fichier copié avec succès à partir de la table de fichiers du module dans la base de données cible.</span><span class="sxs-lookup"><span data-stu-id="b1e0d-106">The list of files consists of every file successfully copied from the file table of the module to the target database.</span></span> <span data-ttu-id="b1e0d-107">Les entrées de table de fichiers qui n’ont pas été copiées en raison de conflits de clé primaire avec les lignes existantes dans la base de données ne font pas partie de cette liste.</span><span class="sxs-lookup"><span data-stu-id="b1e0d-107">File table entries that were not copied due to primary key conflicts with existing rows in the database are not a part of this list.</span></span> <span data-ttu-id="b1e0d-108">Au moment de la création de l’image, le répertoire de chacun de ces fichiers provient de la base de données ouverte (après la fusion).</span><span class="sxs-lookup"><span data-stu-id="b1e0d-108">At image creation time, the directory for each of these files comes from the open (post-merge) database.</span></span> <span data-ttu-id="b1e0d-109">Le chemin d’accès spécifié dans le paramètre *path* est la racine de l’image source pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="b1e0d-109">The path specified in the *Path* parameter is the root of the source image for the install.</span></span> <span data-ttu-id="b1e0d-110">*fLongFileNames* détermine si des noms de fichiers longs sont utilisés pour les segments de chemin d’accès et les noms de fichiers finaux.</span><span class="sxs-lookup"><span data-stu-id="b1e0d-110">*fLongFileNames* determines whether or not long file names are used for both path segments and final file names.</span></span> <span data-ttu-id="b1e0d-111">La fonction échoue si aucune base de données n’est ouverte, si aucun module n’est ouvert ou si aucune fusion n’a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="b1e0d-111">The function fails if no database is open, no module is open, or no merge has been performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1e0d-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1e0d-112">Syntax</span></span>


```JScript
Merge.CreateSourceImage(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a><span data-ttu-id="b1e0d-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1e0d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1e0d-114">*Chemin d’accès*</span><span class="sxs-lookup"><span data-stu-id="b1e0d-114">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="b1e0d-115">Chemin d’accès de la racine de l’image source pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="b1e0d-115">The path of the root of the source image for the install.</span></span>

</dd> <dt>

<span data-ttu-id="b1e0d-116">*fLongFileNames*</span><span class="sxs-lookup"><span data-stu-id="b1e0d-116">*fLongFileNames*</span></span> 
</dt> <dd>

<span data-ttu-id="b1e0d-117">*fLongFileNames* détermine si des noms de fichiers longs sont utilisés pour les segments de chemin d’accès et les noms de fichiers finaux.</span><span class="sxs-lookup"><span data-stu-id="b1e0d-117">*fLongFileNames* determines whether or not long file names are used for both path segments and final file names.</span></span>

</dd> <dt>

<span data-ttu-id="b1e0d-118">*pFilePaths*</span><span class="sxs-lookup"><span data-stu-id="b1e0d-118">*pFilePaths*</span></span> 
</dt> <dd>

<span data-ttu-id="b1e0d-119">Il s’agit d’une liste de chemins d’accès complets pour les fichiers qui ont été extraits avec succès.</span><span class="sxs-lookup"><span data-stu-id="b1e0d-119">This is a list of fully qualified paths for the files that were successfully extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1e0d-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b1e0d-120">Return value</span></span>

<span data-ttu-id="b1e0d-121">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b1e0d-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1e0d-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b1e0d-122">Remarks</span></span>

<span data-ttu-id="b1e0d-123">Tous les fichiers du répertoire de destination portant le même nom sont remplacés.</span><span class="sxs-lookup"><span data-stu-id="b1e0d-123">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="b1e0d-124">Le chemin d’accès est créé s’il n’existe pas déjà.</span><span class="sxs-lookup"><span data-stu-id="b1e0d-124">The path is created if it does not already exist.</span></span>

### <a name="c"></a><span data-ttu-id="b1e0d-125">C++</span><span class="sxs-lookup"><span data-stu-id="b1e0d-125">C++</span></span>

<span data-ttu-id="b1e0d-126">Consultez fonction [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage) .</span><span class="sxs-lookup"><span data-stu-id="b1e0d-126">See [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1e0d-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1e0d-127">Requirements</span></span>



| <span data-ttu-id="b1e0d-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1e0d-128">Requirement</span></span> | <span data-ttu-id="b1e0d-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1e0d-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1e0d-130">Version</span><span class="sxs-lookup"><span data-stu-id="b1e0d-130">Version</span></span><br/> | <span data-ttu-id="b1e0d-131">Mergemod.dll 2,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b1e0d-131">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="b1e0d-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1e0d-132">Header</span></span><br/>  | <dl> <span data-ttu-id="b1e0d-133"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1e0d-133"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1e0d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b1e0d-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="b1e0d-135"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1e0d-135"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




