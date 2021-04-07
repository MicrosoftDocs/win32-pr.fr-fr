---
description: La table SelfReg contient des informations sur les modules qui doivent être inscrits automatiquement.
ms.assetid: 7fe5c96e-16a4-49c9-9a93-616608aa55b2
title: Table SelfReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5895b1d23369a7c121547fed841731b5d3e76ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760144"
---
# <a name="selfreg-table"></a><span data-ttu-id="66afd-103">Table SelfReg</span><span class="sxs-lookup"><span data-stu-id="66afd-103">SelfReg Table</span></span>

<span data-ttu-id="66afd-104">La table SelfReg contient des informations sur les modules qui doivent être inscrits automatiquement.</span><span class="sxs-lookup"><span data-stu-id="66afd-104">The SelfReg table contains information about modules that need to be self registered.</span></span> <span data-ttu-id="66afd-105">Le programme d’installation appelle la fonction [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) lors de l’installation du module ; elle appelle [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) au cours de la désinstallation du module.</span><span class="sxs-lookup"><span data-stu-id="66afd-105">The installer calls the [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) function during installation of the module; it calls [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) during uninstallation of the module.</span></span> <span data-ttu-id="66afd-106">Le programme d’installation n’inscrit pas automatiquement les fichiers EXE.</span><span class="sxs-lookup"><span data-stu-id="66afd-106">The installer does not self register EXE files.</span></span>

<span data-ttu-id="66afd-107">La table SelfReg contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="66afd-107">The SelfReg table has the following columns.</span></span>



| <span data-ttu-id="66afd-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="66afd-108">Column</span></span> | <span data-ttu-id="66afd-109">Type</span><span class="sxs-lookup"><span data-stu-id="66afd-109">Type</span></span>                         | <span data-ttu-id="66afd-110">Clé</span><span class="sxs-lookup"><span data-stu-id="66afd-110">Key</span></span> | <span data-ttu-id="66afd-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="66afd-111">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="66afd-112">fichier\_</span><span class="sxs-lookup"><span data-stu-id="66afd-112">File\_</span></span> | [<span data-ttu-id="66afd-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="66afd-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="66afd-114">O</span><span class="sxs-lookup"><span data-stu-id="66afd-114">Y</span></span>   | <span data-ttu-id="66afd-115">N</span><span class="sxs-lookup"><span data-stu-id="66afd-115">N</span></span>        |
| <span data-ttu-id="66afd-116">Coût</span><span class="sxs-lookup"><span data-stu-id="66afd-116">Cost</span></span>   | [<span data-ttu-id="66afd-117">Integer</span><span class="sxs-lookup"><span data-stu-id="66afd-117">Integer</span></span>](integer.md)       | <span data-ttu-id="66afd-118">N</span><span class="sxs-lookup"><span data-stu-id="66afd-118">N</span></span>   | <span data-ttu-id="66afd-119">O</span><span class="sxs-lookup"><span data-stu-id="66afd-119">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="66afd-120">Colonnes</span><span class="sxs-lookup"><span data-stu-id="66afd-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="66afd-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Txt\_</span><span class="sxs-lookup"><span data-stu-id="66afd-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="66afd-122">Clé externe dans la première colonne de la [table file](file-table.md) indiquant le module qui doit être enregistré.</span><span class="sxs-lookup"><span data-stu-id="66afd-122">External key into the first column of the [File table](file-table.md) indicating the module that needs to be registered.</span></span>

</dd> <dt>

<span data-ttu-id="66afd-123"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Coûts</span><span class="sxs-lookup"><span data-stu-id="66afd-123"><span id="Cost"></span><span id="cost"></span><span id="COST"></span>Cost</span></span>
</dt> <dd>

<span data-ttu-id="66afd-124">Coût de l’enregistrement du module en octets.</span><span class="sxs-lookup"><span data-stu-id="66afd-124">The cost of registering the module in bytes.</span></span> <span data-ttu-id="66afd-125">Il doit s’agir d’un nombre non négatif.</span><span class="sxs-lookup"><span data-stu-id="66afd-125">This must be a non-negative number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66afd-126">Notes</span><span class="sxs-lookup"><span data-stu-id="66afd-126">Remarks</span></span>

<span data-ttu-id="66afd-127">Les auteurs de packages d’installation sont fortement recommandés pour l’utilisation de l’inscription automatique.</span><span class="sxs-lookup"><span data-stu-id="66afd-127">Installation package authors are strongly advised against using self registration.</span></span> <span data-ttu-id="66afd-128">Au lieu de cela, ils doivent inscrire des modules en créant une ou plusieurs tables fournies par le programme d’installation à cet effet.</span><span class="sxs-lookup"><span data-stu-id="66afd-128">Instead they should register modules by authoring one or more tables provided by the installer for this purpose.</span></span> <span data-ttu-id="66afd-129">Pour plus d’informations, consultez [Registry tables Group](registry-tables-group.md).</span><span class="sxs-lookup"><span data-stu-id="66afd-129">For more information, see [Registry Tables Group](registry-tables-group.md).</span></span> <span data-ttu-id="66afd-130">La plupart des avantages offerts par un service d’installation central sont perdus avec l’inscription automatique, car les routines d’auto-inscription ont tendance à masquer les informations de configuration critiques.</span><span class="sxs-lookup"><span data-stu-id="66afd-130">Many of the benefits of having a central installer service are lost with self registration because self-registration routines tend to hide critical configuration information.</span></span> <span data-ttu-id="66afd-131">Voici quelques raisons pour lesquelles éviter l’inscription automatique :</span><span class="sxs-lookup"><span data-stu-id="66afd-131">Reasons for avoiding self registration include:</span></span>

-   <span data-ttu-id="66afd-132">La restauration d’une installation avec des modules auto-inscrits ne peut pas être effectuée en toute sécurité à l’aide de [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) , car il n’existe aucun moyen de savoir si les clés auto-inscrites sont utilisées par une autre fonctionnalité ou application.</span><span class="sxs-lookup"><span data-stu-id="66afd-132">Rollback of an installation with self-registered modules cannot be safely done using [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) because there is no way of telling if the self-registered keys are used by another feature or application.</span></span>
-   <span data-ttu-id="66afd-133">La possibilité d’utiliser la publication est réduite si l’inscription du serveur de classe ou d’extension est effectuée dans les routines d’auto-inscription.</span><span class="sxs-lookup"><span data-stu-id="66afd-133">The ability to use advertisement is reduced if Class or extension server registration is performed within self-registration routines.</span></span>
-   <span data-ttu-id="66afd-134">Le programme d’installation gère automatiquement les clés HKCR dans les tables du Registre pour les installations par utilisateur ou par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="66afd-134">The installer automatically handles HKCR keys in the registry tables for both per-user or per-machine installations.</span></span> <span data-ttu-id="66afd-135">Actuellement, les routines [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) ne prennent pas en charge la notion de clé HKCR par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="66afd-135">[**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) routines currently do not support the notion of a per-user HKCR key.</span></span>
-   <span data-ttu-id="66afd-136">Si plusieurs utilisateurs utilisent une application auto-inscrite sur le même ordinateur, chaque utilisateur doit installer l’application la première fois qu’il l’exécute.</span><span class="sxs-lookup"><span data-stu-id="66afd-136">If multiple users are using a self-registered application on the same computer, each user must install the application the first time they run it.</span></span> <span data-ttu-id="66afd-137">Dans le cas contraire, le programme d’installation ne peut pas déterminer facilement que les clés de Registre HKCU appropriées existent.</span><span class="sxs-lookup"><span data-stu-id="66afd-137">Otherwise the installer cannot easily determine that the proper HKCU registry keys exist.</span></span>
-   <span data-ttu-id="66afd-138">La fonction [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) peut se voir refuser l’accès aux ressources réseau telles que les bibliothèques de types si un composant est à la fois spécifié en tant que source d’exécution à partir de la source et est listé dans la table Selfreg.</span><span class="sxs-lookup"><span data-stu-id="66afd-138">The [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) can be denied access to network resources such as type libraries if a component is both specified as run-from-source and is listed in the SelfReg table.</span></span> <span data-ttu-id="66afd-139">Cela peut entraîner l’échec de l’installation du composant au cours d’une installation administrative.</span><span class="sxs-lookup"><span data-stu-id="66afd-139">This can cause the installation of the component to fail to during an administrative installation.</span></span>
-   <span data-ttu-id="66afd-140">L’inscription automatique des dll est plus sensible aux erreurs de codage, car le nouveau code requis pour [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) est généralement différent pour chaque dll.</span><span class="sxs-lookup"><span data-stu-id="66afd-140">Self-registering DLLs are more susceptible to coding errors because the new code required for [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) is commonly different for each DLL.</span></span> <span data-ttu-id="66afd-141">Utilisez plutôt les tables de Registre dans la base de données pour tirer parti du code existant fourni par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="66afd-141">Instead use the registry tables in the database to take advantage of existing code provided by the installer.</span></span>
-   <span data-ttu-id="66afd-142">L’inscription automatique des dll peut parfois être liée à des dll auxiliaires absentes ou dont la version est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="66afd-142">Self-registering DLLs can sometimes link to auxiliary DLLs that are not present or are the wrong version.</span></span> <span data-ttu-id="66afd-143">En revanche, le programme d’installation peut inscrire les dll à l’aide des tables de registre sans dépendance sur l’état actuel du système.</span><span class="sxs-lookup"><span data-stu-id="66afd-143">In contrast, the installer can register the DLLs using the registry tables with no dependency on the current state of the system.</span></span>

> [!Note]  
> <span data-ttu-id="66afd-144">Vous ne pouvez pas spécifier l’ordre dans lequel le programme d’installation enregistre ou annule l’enregistrement automatique des dll à l’aide des actions [SelfRegModules](selfregmodules-action.md) et [SelfUnRegModules](selfunregmodules-action.md) .</span><span class="sxs-lookup"><span data-stu-id="66afd-144">You cannot specify the order in which the installer registers or unregisters self-registering DLLs by using the [SelfRegModules](selfregmodules-action.md) and [SelfUnRegModules](selfunregmodules-action.md) actions.</span></span> <span data-ttu-id="66afd-145">Consultez [spécification de l’ordre d’inscription automatique](specifying-the-order-of-self-registration.md).</span><span class="sxs-lookup"><span data-stu-id="66afd-145">See [Specifying the Order of Self Registration](specifying-the-order-of-self-registration.md).</span></span>

 

## <a name="validation"></a><span data-ttu-id="66afd-146">Validation</span><span class="sxs-lookup"><span data-stu-id="66afd-146">Validation</span></span>

<dl>

[<span data-ttu-id="66afd-147">ICE03</span><span class="sxs-lookup"><span data-stu-id="66afd-147">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="66afd-148">ICE06</span><span class="sxs-lookup"><span data-stu-id="66afd-148">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="66afd-149">ICE32</span><span class="sxs-lookup"><span data-stu-id="66afd-149">ICE32</span></span>](ice32.md)  
</dl>

 

 
