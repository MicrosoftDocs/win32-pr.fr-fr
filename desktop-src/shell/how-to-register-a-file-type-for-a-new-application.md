---
description: Si vous envisagez d’associer un ou plusieurs types de fichiers à une nouvelle application, vous devez définir un ProgID pour chaque type de fichier que vous souhaitez associer à l’application.
ms.assetid: 997600C9-5264-44EC-BAEC-CB5CEEA0BD14
title: Comment inscrire un type de fichier pour une nouvelle application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728cc48075ab1c2631f0a950059da65ae326ae79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973135"
---
# <a name="how-to-register-a-file-type-for-a-new-application"></a><span data-ttu-id="8b92f-103">Comment inscrire un type de fichier pour une nouvelle application</span><span class="sxs-lookup"><span data-stu-id="8b92f-103">How to Register a File Type for a New Application</span></span>

<span data-ttu-id="8b92f-104">Si vous envisagez d’associer un ou plusieurs types de fichiers à une nouvelle application, vous devez définir un ProgID pour chaque type de fichier que vous souhaitez associer à l’application.</span><span class="sxs-lookup"><span data-stu-id="8b92f-104">If you plan to associate one or more file types with a new application, you must define a ProgID for each file type that you want to associate with the application.</span></span>

<span data-ttu-id="8b92f-105">Pour créer un ProgID pour chaque type de fichier unique géré par votre application, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="8b92f-105">To create a ProgID for each unique file type that your application handles, use these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="8b92f-106">Instructions</span><span class="sxs-lookup"><span data-stu-id="8b92f-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="8b92f-107">Étape 1 :</span><span class="sxs-lookup"><span data-stu-id="8b92f-107">Step 1:</span></span>

<span data-ttu-id="8b92f-108">Notez que certains types de fichiers ont plusieurs extensions qui pointent vers le même ProgID ; par exemple :</span><span class="sxs-lookup"><span data-stu-id="8b92f-108">Note that some file types have multiple extensions that point to the same ProgID; for example:</span></span>

-   <span data-ttu-id="8b92f-109">**HKEY \_ CLASSES \_ racine** \\ **app. jpeg** (votre ProgID)</span><span class="sxs-lookup"><span data-stu-id="8b92f-109">**HKEY\_CLASSES\_ROOT**\\**App.jpeg** (your ProgID)</span></span>
-   <span data-ttu-id="8b92f-110">**HKEY \_ CLASSES \_ root** \\ **. jpg** = App. jpeg (mappages de types de fichiers)</span><span class="sxs-lookup"><span data-stu-id="8b92f-110">**HKEY\_CLASSES\_ROOT**\\ **.jpg** = App.jpeg (the file type mappings)</span></span>
-   <span data-ttu-id="8b92f-111">**HKEY \_ CLASSES \_ racine** \\ **. jpeg** = App. jpeg</span><span class="sxs-lookup"><span data-stu-id="8b92f-111">**HKEY\_CLASSES\_ROOT**\\ **.jpeg** = App.jpeg</span></span>

### <a name="step-2"></a><span data-ttu-id="8b92f-112">Étape 2 :</span><span class="sxs-lookup"><span data-stu-id="8b92f-112">Step 2:</span></span>

<span data-ttu-id="8b92f-113">Supprimez les valeurs ProgID lors de l’installation et de la désinstallation de votre programme.</span><span class="sxs-lookup"><span data-stu-id="8b92f-113">Remove the ProgID values when you install and uninstall your program.</span></span>

### <a name="step-3"></a><span data-ttu-id="8b92f-114">Étape 3 :</span><span class="sxs-lookup"><span data-stu-id="8b92f-114">Step 3:</span></span>

<span data-ttu-id="8b92f-115">Laissez les mappages de type de fichier inchangés au moment de la désinstallation.</span><span class="sxs-lookup"><span data-stu-id="8b92f-115">Leave the file type mappings unchanged at uninstall time.</span></span> <span data-ttu-id="8b92f-116">Cela fonctionne, car les mappages de types de fichiers sont stockés par utilisateur dans les \_ classes HKEY \_ root \\ . ext, et le système identifie le cas où la valeur ProgID est manquante et l’ignore.</span><span class="sxs-lookup"><span data-stu-id="8b92f-116">Doing so works because file type mappings are stored per user in HKEY\_CLASSES\_ROOT\\.ext, and the system identifies the case where the ProgID value is missing and ignores it.</span></span> <span data-ttu-id="8b92f-117">Le fait de laisser les mappages de types de fichiers inchangés évite d’avoir à utiliser du code conditionnel qui supprime uniquement le mappage de type de fichier si la valeur pointe encore sur votre ProgID.</span><span class="sxs-lookup"><span data-stu-id="8b92f-117">Leaving file type mappings unchanged avoids the need to have conditional code that only removes the file type mapping if the value still points to your ProgID.</span></span> <span data-ttu-id="8b92f-118">Il est important de ne pas le faire dans les cas où il peut avoir été modifié par une autre application et vous ne pouvez donc pas supprimer la valeur facilement.</span><span class="sxs-lookup"><span data-stu-id="8b92f-118">It is important to avoid doing so in cases where it might have been changed by another application and you thus cannot easily remove the value.</span></span>

### <a name="step-4"></a><span data-ttu-id="8b92f-119">Étape 4 :</span><span class="sxs-lookup"><span data-stu-id="8b92f-119">Step 4:</span></span>

<span data-ttu-id="8b92f-120">Spécifiez une valeur unique pour la description du type de fichier de chaque ProgID de type de fichier en procédant de l’une des façons suivantes :</span><span class="sxs-lookup"><span data-stu-id="8b92f-120">Specify a unique value for the file type description of each file type ProgID by doing one of the following:</span></span>

-   <span data-ttu-id="8b92f-121">Laissez la valeur par défaut du ProgID vide, auquel cas le système utilise le fichier. ext.</span><span class="sxs-lookup"><span data-stu-id="8b92f-121">Leave the default value of the ProgID empty, in which case the system uses the .ext file.</span></span>
-   <span data-ttu-id="8b92f-122">Fournissez une valeur localisée via FriendlyTypeName et, pour la compatibilité avec les anciennes applications qui lisent directement le registre, veillez à fournir la valeur par défaut du ProgID en tant que Description du type de fichier (autrement dit, utilisez la même valeur que celle référencée par FriendlyTypeName dans la ressource anglaise).</span><span class="sxs-lookup"><span data-stu-id="8b92f-122">Provide a localized value via FriendlyTypeName and, for compatibility with old applications that read the registry directly, be sure to provide the default value of the ProgID as the file type description (that is, use the same value that is referred to by the FriendlyTypeName in the English resource).</span></span>

## <a name="remarks"></a><span data-ttu-id="8b92f-123">Notes</span><span class="sxs-lookup"><span data-stu-id="8b92f-123">Remarks</span></span>

<span data-ttu-id="8b92f-124">Si vous envisagez d’associer le fichier à une application existante, localisez un ProgID d’application dans le registre.</span><span class="sxs-lookup"><span data-stu-id="8b92f-124">If you plan to associate the file with an existing application, locate an application ProgID in the registry.</span></span> <span data-ttu-id="8b92f-125">Pour plus d’informations, consultez [types de fichiers](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="8b92f-125">For more information, see [File Types](fa-file-types.md).</span></span>

 

 



