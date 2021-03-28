---
description: Les éditeurs de logiciels indépendants (ISV) peuvent étendre l’ensemble des dossiers connus sur un système en inscrivant leurs propres dossiers connus.
ms.assetid: bb2c63e6-7525-4d20-ac50-591b3e53dea2
title: Comment étendre des dossiers connus avec des dossiers personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3556b2e28664c63e7bc3b5fa28cf8696f679bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202780"
---
# <a name="how-to-extend-known-folders-with-custom-folders"></a><span data-ttu-id="18f72-103">Comment étendre des dossiers connus avec des dossiers personnalisés</span><span class="sxs-lookup"><span data-stu-id="18f72-103">How to Extend Known Folders with Custom Folders</span></span>

<span data-ttu-id="18f72-104">Les éditeurs de logiciels indépendants (ISV) peuvent étendre l’ensemble des dossiers connus sur un système en inscrivant leurs propres dossiers connus.</span><span class="sxs-lookup"><span data-stu-id="18f72-104">Independent software vendors (ISVs) can extend the set of known folders on a system by registering known folders of their own.</span></span> <span data-ttu-id="18f72-105">Une fois inscrits, ces dossiers tiers sont connus du système.</span><span class="sxs-lookup"><span data-stu-id="18f72-105">Once registered, those third-party folders are known to the system.</span></span> <span data-ttu-id="18f72-106">Ils sont trouvés par un appel à [**IKnownFolderManager :: GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids).</span><span class="sxs-lookup"><span data-stu-id="18f72-106">They are found by any call to [**IKnownFolderManager::GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids).</span></span> <span data-ttu-id="18f72-107">Notez qu’un dossier connu doit être un dossier par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="18f72-107">Note that a known folder must be a per-machine folder.</span></span> <span data-ttu-id="18f72-108">Vous ne pouvez pas créer un dossier connu par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="18f72-108">You cannot create a per-user known folder.</span></span>

## <a name="instructions"></a><span data-ttu-id="18f72-109">Instructions</span><span class="sxs-lookup"><span data-stu-id="18f72-109">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="18f72-110">Étape 1 :</span><span class="sxs-lookup"><span data-stu-id="18f72-110">Step 1:</span></span>

<span data-ttu-id="18f72-111">Définissez votre dossier connu via une structure de [**\_ définition KNOWNFOLDER**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) .</span><span class="sxs-lookup"><span data-stu-id="18f72-111">Define your known folder through a [**KNOWNFOLDER\_DEFINITION**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) structure.</span></span>

### <a name="step-2"></a><span data-ttu-id="18f72-112">Étape 2 :</span><span class="sxs-lookup"><span data-stu-id="18f72-112">Step 2:</span></span>

<span data-ttu-id="18f72-113">Inscrivez le dossier connu via un appel à [**IKnownFolderManager :: RegisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder).</span><span class="sxs-lookup"><span data-stu-id="18f72-113">Register the known folder through a call to [**IKnownFolderManager::RegisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder).</span></span>

## <a name="remarks"></a><span data-ttu-id="18f72-114">Notes</span><span class="sxs-lookup"><span data-stu-id="18f72-114">Remarks</span></span>

<span data-ttu-id="18f72-115">Si vous créez un dossier connu pour votre application dans le cadre de votre procédure d’installation, vous devez également inclure [**IKnownFolderManager :: UnregisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) dans le cadre de votre code de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="18f72-115">If you create a known folder for your application as part of your installation procedure, you must also include [**IKnownFolderManager::UnregisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) as part of your uninstallation code.</span></span>

<span data-ttu-id="18f72-116">Prenez en compte la raison pour laquelle vous souhaitez que votre dossier soit inclus dans le système de dossiers connu avant de l’inscrire.</span><span class="sxs-lookup"><span data-stu-id="18f72-116">Give consideration to why you want your folder to be included in the known folder system before you register it.</span></span> <span data-ttu-id="18f72-117">Vous devez avoir une raison valable d’élever votre dossier à ce niveau de visibilité du système.</span><span class="sxs-lookup"><span data-stu-id="18f72-117">You should have a valid reason for elevating your folder to that level of system visibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18f72-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="18f72-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="18f72-119">[Dossiers connus, exemple](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="18f72-119">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
