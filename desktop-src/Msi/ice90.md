---
description: ICE90 publie un avertissement s’il détecte que le répertoire d’un raccourci a été spécifié en tant que propriété publique.
ms.assetid: 47565d9b-c3c2-4a5c-8f91-2b3912a63b47
title: ICE90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b4063d06aa5a0a8688e2a411040d4b64f58f75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864225"
---
# <a name="ice90"></a><span data-ttu-id="ad6c6-103">ICE90</span><span class="sxs-lookup"><span data-stu-id="ad6c6-103">ICE90</span></span>

<span data-ttu-id="ad6c6-104">ICE90 publie un avertissement s’il détecte que le répertoire d’un raccourci a été spécifié en tant que propriété publique.</span><span class="sxs-lookup"><span data-stu-id="ad6c6-104">ICE90 posts a warning if it finds that a shortcut's directory has been specified as a public property.</span></span> <span data-ttu-id="ad6c6-105">Les noms des [propriétés publiques](public-properties.md) sont écrits en lettres majuscules.</span><span class="sxs-lookup"><span data-stu-id="ad6c6-105">The names of [Public Properties](public-properties.md) are written in uppercase letters.</span></span> <span data-ttu-id="ad6c6-106">Un raccourci spécifié par une propriété publique peut ne pas fonctionner si la valeur de la propriété [**ALLUSERS**](allusers.md) change.</span><span class="sxs-lookup"><span data-stu-id="ad6c6-106">A shortcut specified by a public property may not work if the value of the [**ALLUSERS**](allusers.md) property changes.</span></span>

<span data-ttu-id="ad6c6-107">Cette action personnalisée ICE valide la table de raccourcis et utilise la table de répertoires.</span><span class="sxs-lookup"><span data-stu-id="ad6c6-107">This ICE custom action validates the Shortcut table and uses the Directory table.</span></span> <span data-ttu-id="ad6c6-108">Si la table de répertoires n’est pas présente, elle retourne sans valider la table de raccourcis et ne publie aucune erreur ou avertissement.</span><span class="sxs-lookup"><span data-stu-id="ad6c6-108">If the Directory table is not present, it returns without validating the Shortcut table and posts no errors or warnings.</span></span>

## <a name="result"></a><span data-ttu-id="ad6c6-109">Résultats</span><span class="sxs-lookup"><span data-stu-id="ad6c6-109">Result</span></span>

<span data-ttu-id="ad6c6-110">ICE90 publie l’avertissement suivant.</span><span class="sxs-lookup"><span data-stu-id="ad6c6-110">ICE90 posts the following warning.</span></span>



| <span data-ttu-id="ad6c6-111">Erreur ICE90</span><span class="sxs-lookup"><span data-stu-id="ad6c6-111">ICE90 error</span></span>                                                                                                                                                                                                                    | <span data-ttu-id="ad6c6-112">Description</span><span class="sxs-lookup"><span data-stu-id="ad6c6-112">Description</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="ad6c6-113">Le raccourci' \[ 1 \] 'a un répertoire qui est une propriété publique (tout en majuscules) et se trouve sous le répertoire du profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ad6c6-113">The shortcut '\[1\]' has a directory that is a public property (ALL CAPS) and is under user profile directory.</span></span> <span data-ttu-id="ad6c6-114">Cela entraîne un problème si la valeur de la propriété [**ALLUSERS**](allusers.md) change dans la séquence d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ad6c6-114">This results in a problem if the value of the [**ALLUSERS**](allusers.md) property changes in the UI sequence.</span></span> | <span data-ttu-id="ad6c6-115">Le répertoire d’un raccourci a été spécifié en tant que propriété publique.</span><span class="sxs-lookup"><span data-stu-id="ad6c6-115">A shortcut's directory has been specified as a public property.</span></span> |



 

## <a name="example"></a><span data-ttu-id="ad6c6-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="ad6c6-116">Example</span></span>

<span data-ttu-id="ad6c6-117">ICE90 signale l’avertissement suivant pour l’exemple :</span><span class="sxs-lookup"><span data-stu-id="ad6c6-117">ICE90 reports the following warning for the example:</span></span>

``` syntax
The shortcut 'Shortcut1' has a directory that is a public property (ALL CAPS) 
and is under user profile directory. This results in a problem if the value 
of the ALLUSERS property changes in the UI sequence.
```

<span data-ttu-id="ad6c6-118">Dans cet exemple, MYDIR se trouve sous un profil Users.</span><span class="sxs-lookup"><span data-stu-id="ad6c6-118">In this example, MYDIR is under a users profile.</span></span> <span data-ttu-id="ad6c6-119">ICE90 publie un avertissement, car l’emplacement du répertoire cible est spécifié par une propriété publique, MYDIR.</span><span class="sxs-lookup"><span data-stu-id="ad6c6-119">ICE90 posts a warning because the location of the target directory is specified by a public property, MYDIR.</span></span> <span data-ttu-id="ad6c6-120">Un utilisateur peut modifier la propriété MYDIR ou [**ALLUSERS**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="ad6c6-120">A user may change MYDIR or [**ALLUSERS**](allusers.md) property.</span></span> <span data-ttu-id="ad6c6-121">Si **ALLUSERS** est défini pour le [contexte d’installation](installation-context.md)par ordinateur et que MYDIR se trouve sous un profil utilisateurs, le fichier de raccourci dans MYDIR est copié sous le profil « tous les utilisateurs », et non un profil utilisateur particulier.</span><span class="sxs-lookup"><span data-stu-id="ad6c6-121">If **ALLUSERS** is set for the per-machine [installation context](installation-context.md), and MYDIR is under a users profile, the shortcut file in MYDIR are copied under the "All Users" profile and not a particular user's profile.</span></span> <span data-ttu-id="ad6c6-122">Si **ALLUSERS** est défini pour le contexte d’installation par utilisateur, le fichier de raccourci dans MYDIR est copié dans le profil d’un utilisateur particulier et n’est pas disponible pour les autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ad6c6-122">If **ALLUSERS** is set for the per-user installation context, the shortcut file in MYDIR is copied into a particular user's profile and is not available to other users.</span></span>

<span data-ttu-id="ad6c6-123">[Table de raccourcis](shortcut-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="ad6c6-123">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="ad6c6-124">Raccourci</span><span class="sxs-lookup"><span data-stu-id="ad6c6-124">Shortcut</span></span>  | <span data-ttu-id="ad6c6-125">Répertoire\_</span><span class="sxs-lookup"><span data-stu-id="ad6c6-125">Directory\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="ad6c6-126">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="ad6c6-126">Shortcut1</span></span> | <span data-ttu-id="ad6c6-127">MYDIR</span><span class="sxs-lookup"><span data-stu-id="ad6c6-127">MYDIR</span></span>       |



 

<span data-ttu-id="ad6c6-128">[Table de répertoires](directory-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="ad6c6-128">[Directory Table](directory-table.md) (partial)</span></span>



| <span data-ttu-id="ad6c6-129">Répertoire</span><span class="sxs-lookup"><span data-stu-id="ad6c6-129">Directory</span></span> | <span data-ttu-id="ad6c6-130">Répertoire \_ parent</span><span class="sxs-lookup"><span data-stu-id="ad6c6-130">Directory\_Parent</span></span> |
|-----------|-------------------|
| <span data-ttu-id="ad6c6-131">MYDIR</span><span class="sxs-lookup"><span data-stu-id="ad6c6-131">MYDIR</span></span>     | <span data-ttu-id="ad6c6-132">ProgramMenuFolder</span><span class="sxs-lookup"><span data-stu-id="ad6c6-132">ProgramMenuFolder</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ad6c6-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ad6c6-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad6c6-134">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="ad6c6-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



