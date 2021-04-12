---
description: Que vous choisissiez de convertir vos packages MTS en applications COM+ manuellement ou que le processus d’installation de Microsoft Windows le fasse automatiquement, vous devez être conscient des résultats de la conversion, ainsi que des problèmes rencontrés.
ms.assetid: 5b85aa5c-0409-4802-9335-04217ef5ddb9
title: Résultats et problèmes de conversion COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ded68e8e81d2c59c90607747c5f343dac364424
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393235"
---
# <a name="com-conversion-results-and-issues"></a><span data-ttu-id="9ea43-103">Résultats et problèmes de conversion COM+</span><span class="sxs-lookup"><span data-stu-id="9ea43-103">COM+ Conversion Results and Issues</span></span>

<span data-ttu-id="9ea43-104">Que vous choisissiez de convertir vos packages MTS en applications COM+ manuellement ou que le processus d’installation de Microsoft Windows le fasse automatiquement, vous devez être conscient des résultats de la conversion, ainsi que des problèmes rencontrés.</span><span class="sxs-lookup"><span data-stu-id="9ea43-104">Whether you choose to convert your MTS packages to COM+ applications manually or let the Microsoft Windows setup process do it for you automatically, you should be aware of the results of conversion as well as the issues.</span></span>

## <a name="what-is-converted"></a><span data-ttu-id="9ea43-105">Ce qui est converti</span><span class="sxs-lookup"><span data-stu-id="9ea43-105">What Is Converted</span></span>

<span data-ttu-id="9ea43-106">Au cours de la conversion, l’utilitaire MTSTOCOM convertit les rôles, les attributions de rôles, les interfaces, les méthodes, les utilisateurs, la liste des ordinateurs et la plupart des paramètres de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9ea43-106">During conversion, the MTSTOCOM utility converts roles, role assignments, interfaces, methods, users, the computer list, and most computer settings.</span></span> <span data-ttu-id="9ea43-107">L’utilitaire MTSTOCOM convertit également l’identité et le mot de passe d’un package MTS.</span><span class="sxs-lookup"><span data-stu-id="9ea43-107">The MTSTOCOM utility also converts the identity and password for an MTS package.</span></span>

<span data-ttu-id="9ea43-108">Les nouveaux attributs COM+ qui n’étaient pas disponibles dans MTS sont automatiquement définis sur les valeurs par défaut suivantes pour tous les composants MTS convertis.</span><span class="sxs-lookup"><span data-stu-id="9ea43-108">The new COM+ attributes that were not available in MTS are automatically set to the following defaults for all converted MTS components.</span></span> <span data-ttu-id="9ea43-109">Ces valeurs par défaut peuvent être modifiées à l’aide de l’outil d’administration Services de composants ou des interfaces d’administration COM+.</span><span class="sxs-lookup"><span data-stu-id="9ea43-109">These defaults can be changed using either the Component Services administrative tool or the COM+ administrative interfaces.</span></span>

-   <span data-ttu-id="9ea43-110">Activation JIT activée.</span><span class="sxs-lookup"><span data-stu-id="9ea43-110">JIT activation enabled.</span></span>
-   <span data-ttu-id="9ea43-111">Mise en pool d’objets désactivée.</span><span class="sxs-lookup"><span data-stu-id="9ea43-111">Object pooling disabled.</span></span>
-   <span data-ttu-id="9ea43-112">Synchronisation identique au paramètre de transaction.</span><span class="sxs-lookup"><span data-stu-id="9ea43-112">Synchronization same as Transaction setting.</span></span>

## <a name="conversion-issues"></a><span data-ttu-id="9ea43-113">Problèmes de conversion</span><span class="sxs-lookup"><span data-stu-id="9ea43-113">Conversion Issues</span></span>

<span data-ttu-id="9ea43-114">COM+ est installé automatiquement lorsque vous installez Windows.</span><span class="sxs-lookup"><span data-stu-id="9ea43-114">COM+ is automatically installed when you install Windows.</span></span> <span data-ttu-id="9ea43-115">Il n’est pas possible de désinstaller COM+.</span><span class="sxs-lookup"><span data-stu-id="9ea43-115">It is not possible to uninstall COM+.</span></span> <span data-ttu-id="9ea43-116">Les problèmes liés aux mises à niveau des installations MTS et COM+ existantes sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="9ea43-116">Issues related to upgrades of existing MTS and COM+ installations include the following:</span></span>

-   <span data-ttu-id="9ea43-117">Si vous utilisez actuellement MTS 1,0, MTS est automatiquement mis à niveau vers COM+.</span><span class="sxs-lookup"><span data-stu-id="9ea43-117">If you are currently using MTS 1.0, MTS is automatically upgraded to COM+.</span></span> <span data-ttu-id="9ea43-118">Toutefois, les packages définis par l’utilisateur sont perdus et vous devez les recréer.</span><span class="sxs-lookup"><span data-stu-id="9ea43-118">However, user-defined packages will be lost and you must re-create them.</span></span>
-   <span data-ttu-id="9ea43-119">Si vous utilisez actuellement MTS 2,0, MTS est automatiquement mis à niveau vers COM+.</span><span class="sxs-lookup"><span data-stu-id="9ea43-119">If you are currently using MTS 2.0, MTS is automatically upgraded to COM+.</span></span> <span data-ttu-id="9ea43-120">Tous les packages définis par l’utilisateur seront mis à niveau vers les applications COM+.</span><span class="sxs-lookup"><span data-stu-id="9ea43-120">All user-defined packages will be upgraded to COM+ applications.</span></span> <span data-ttu-id="9ea43-121">Tous les composants doivent fonctionner comme dans MTS 2,0.</span><span class="sxs-lookup"><span data-stu-id="9ea43-121">All components should work as they did under MTS 2.0.</span></span>
-   <span data-ttu-id="9ea43-122">Si vous utilisez MTS 1,0 et MTS 2,0 et que vous avez installé l’option du kit de développement logiciel (SDK), les fichiers du SDK seront supprimés.</span><span class="sxs-lookup"><span data-stu-id="9ea43-122">If you are using MTS 1.0 and MTS 2.0 and have installed the SDK option, the SDK files will be removed.</span></span> <span data-ttu-id="9ea43-123">Vous pouvez installer la dernière version du kit de développement logiciel (SDK) COM+ via le Microsoft Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="9ea43-123">You can install the latest COM+ SDK through the Microsoft Windows SDK.</span></span>
-   <span data-ttu-id="9ea43-124">Vous ne pouvez pas gérer un ordinateur MTS distant à partir d’un ordinateur COM+.</span><span class="sxs-lookup"><span data-stu-id="9ea43-124">You cannot manage a remote MTS computer from a COM+ computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ea43-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9ea43-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ea43-126">Conversion automatique à partir de MTS</span><span class="sxs-lookup"><span data-stu-id="9ea43-126">Automatic Conversion from MTS</span></span>](automatic-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="9ea43-127">Conversion manuelle à partir de MTS</span><span class="sxs-lookup"><span data-stu-id="9ea43-127">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="9ea43-128">Bibliothèque d’administration MTS</span><span class="sxs-lookup"><span data-stu-id="9ea43-128">MTS Administration Library</span></span>](mts-administration-library.md)
</dt> </dl>

 

 



