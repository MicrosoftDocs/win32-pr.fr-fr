---
description: Combinaison de zéro ou plusieurs options de verrouillage qui décrivent le type de verrou à effectuer.
ms.assetid: 46a611bd-a1ec-4967-b68d-72661d1b5cad
title: D3DLOCK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e4fcf8db9e60a30aee060dcc483b8d01e59b1c
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343194"
---
# <a name="d3dlock"></a><span data-ttu-id="fb79d-103">D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="fb79d-103">D3DLOCK</span></span>

<span data-ttu-id="fb79d-104">Combinaison de zéro ou plusieurs options de verrouillage qui décrivent le type de verrou à effectuer.</span><span class="sxs-lookup"><span data-stu-id="fb79d-104">A combination of zero or more locking options that describe the type of lock to perform.</span></span>



| <span data-ttu-id="fb79d-105">\#définition</span><span class="sxs-lookup"><span data-stu-id="fb79d-105">\#define</span></span>                   | <span data-ttu-id="fb79d-106">Description</span><span class="sxs-lookup"><span data-stu-id="fb79d-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb79d-107">D3DLOCK \_ Ignorer</span><span class="sxs-lookup"><span data-stu-id="fb79d-107">D3DLOCK\_DISCARD</span></span>           | <span data-ttu-id="fb79d-108">L’application ignore toute la mémoire dans la région verrouillée.</span><span class="sxs-lookup"><span data-stu-id="fb79d-108">The application discards all memory within the locked region.</span></span> <span data-ttu-id="fb79d-109">Pour les mémoires tampons de vertex et d’index, la mémoire tampon entière est ignorée.</span><span class="sxs-lookup"><span data-stu-id="fb79d-109">For vertex and index buffers, the entire buffer will be discarded.</span></span> <span data-ttu-id="fb79d-110">Cette option est valide uniquement lorsque la ressource est créée avec une utilisation dynamique (voir [D3DUSAGE](d3dusage.md)).</span><span class="sxs-lookup"><span data-stu-id="fb79d-110">This option is only valid when the resource is created with dynamic usage (see [D3DUSAGE](d3dusage.md)).</span></span>                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="fb79d-111">D3DLOCK \_ DONOTWAIT</span><span class="sxs-lookup"><span data-stu-id="fb79d-111">D3DLOCK\_DONOTWAIT</span></span>         | <span data-ttu-id="fb79d-112">Permet à une application de récupérer les cycles de processeur si le pilote ne peut pas verrouiller immédiatement la surface.</span><span class="sxs-lookup"><span data-stu-id="fb79d-112">Allows an application to gain back CPU cycles if the driver cannot lock the surface immediately.</span></span> <span data-ttu-id="fb79d-113">Si cet indicateur est défini et que le pilote ne peut pas verrouiller la surface immédiatement, l’appel de verrou retourne D3DERR \_ WASSTILLDRAWING.</span><span class="sxs-lookup"><span data-stu-id="fb79d-113">If this flag is set and the driver cannot lock the surface immediately, the lock call will return D3DERR\_WASSTILLDRAWING.</span></span> <span data-ttu-id="fb79d-114">Cet indicateur ne peut être utilisé que lors du verrouillage d’une surface créée à l’aide de [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateRenderTarget**](/windows/desktop/api)ou [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface).</span><span class="sxs-lookup"><span data-stu-id="fb79d-114">This flag can only be used when locking a surface created using [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateRenderTarget**](/windows/desktop/api), or [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface).</span></span> <span data-ttu-id="fb79d-115">Cet indicateur peut également être utilisé avec une mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="fb79d-115">This flag can also be used with a back buffer.</span></span>            |
| <span data-ttu-id="fb79d-116">D3DLOCK \_ aucune \_ \_ mise à jour incorrecte</span><span class="sxs-lookup"><span data-stu-id="fb79d-116">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span> | <span data-ttu-id="fb79d-117">Par défaut, un verrou sur une ressource ajoute une région modifiée à cette ressource.</span><span class="sxs-lookup"><span data-stu-id="fb79d-117">By default, a lock on a resource adds a dirty region to that resource.</span></span> <span data-ttu-id="fb79d-118">Cette option empêche toute modification de l’état de modification de la ressource.</span><span class="sxs-lookup"><span data-stu-id="fb79d-118">This option prevents any changes to the dirty state of the resource.</span></span> <span data-ttu-id="fb79d-119">Les applications doivent utiliser cette option quand elles ont des informations supplémentaires sur l’ensemble des régions modifiées pendant l’opération de verrouillage.</span><span class="sxs-lookup"><span data-stu-id="fb79d-119">Applications should use this option when they have additional information about the set of regions changed during the lock operation.</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="fb79d-120">D3DLOCK \_ NOOVERWRITE</span><span class="sxs-lookup"><span data-stu-id="fb79d-120">D3DLOCK\_NOOVERWRITE</span></span>       | <span data-ttu-id="fb79d-121">Indique que la mémoire qui a été référencée dans un appel de dessin depuis le dernier verrou sans cet indicateur ne sera pas modifiée pendant le verrouillage.</span><span class="sxs-lookup"><span data-stu-id="fb79d-121">Indicates that memory that was referred to in a drawing call since the last lock without this flag will not be modified during the lock.</span></span> <span data-ttu-id="fb79d-122">Cela peut permettre des optimisations lorsque l’application ajoute des données à une ressource.</span><span class="sxs-lookup"><span data-stu-id="fb79d-122">This can enable optimizations when the application is appending data to a resource.</span></span> <span data-ttu-id="fb79d-123">Si vous spécifiez cet indicateur, le pilote est immédiatement retourné si la ressource est en cours d’utilisation. dans le cas contraire, le pilote doit terminer l’utilisation de la ressource avant de revenir au verrouillage.</span><span class="sxs-lookup"><span data-stu-id="fb79d-123">Specifying this flag enables the driver to return immediately if the resource is in use, otherwise, the driver must finish using the resource before returning from locking.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="fb79d-124">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="fb79d-124">D3DLOCK\_NOSYSLOCK</span></span>         | <span data-ttu-id="fb79d-125">Le comportement par défaut d’un verrou de mémoire vidéo est de réserver une section critique au niveau du système, ce qui garantit qu’aucune modification du mode d’affichage ne se produit pendant la durée du verrouillage.</span><span class="sxs-lookup"><span data-stu-id="fb79d-125">The default behavior of a video memory lock is to reserve a system-wide critical section, guaranteeing that no display mode changes will occur for the duration of the lock.</span></span> <span data-ttu-id="fb79d-126">Cette option entraîne la non-conservation de la section critique au niveau du système pendant la durée du verrouillage.</span><span class="sxs-lookup"><span data-stu-id="fb79d-126">This option causes the system-wide critical section not to be held for the duration of the lock.</span></span><br/> <span data-ttu-id="fb79d-127">L’opération de verrouillage prend beaucoup de temps, mais peut permettre au système d’exécuter d’autres tâches, telles que le déplacement du curseur de la souris.</span><span class="sxs-lookup"><span data-stu-id="fb79d-127">The lock operation is time consuming, but can enable the system to perform other duties, such as moving the mouse cursor.</span></span> <span data-ttu-id="fb79d-128">Cette option est utile pour les verrous de longue durée, tels que le verrouillage de la mémoire tampon d’arrière-plan pour le rendu logiciel qui, autrement, aurait un impact négatif sur la réactivité du système.</span><span class="sxs-lookup"><span data-stu-id="fb79d-128">This option is useful for long-duration locks, such as the lock of the back buffer for software rendering that would otherwise adversely affect system responsiveness.</span></span><br/> |
| <span data-ttu-id="fb79d-129">D3DLOCK en \_ lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb79d-129">D3DLOCK\_READONLY</span></span>          | <span data-ttu-id="fb79d-130">L’application n’écrira pas dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="fb79d-130">The application will not write to the buffer.</span></span> <span data-ttu-id="fb79d-131">Cela permet aux ressources stockées dans des formats non natifs d’enregistrer l’étape de recompression lors du déverrouillage.</span><span class="sxs-lookup"><span data-stu-id="fb79d-131">This enables resources stored in non-native formats to save the recompression step when unlocking.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="fb79d-132">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="fb79d-132">Constant Information</span></span>



|  <span data-ttu-id="fb79d-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb79d-133">Requirement</span></span>                        | <span data-ttu-id="fb79d-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb79d-134">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="fb79d-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb79d-135">Header</span></span>                   | <span data-ttu-id="fb79d-136">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="fb79d-136">d3d9types.h</span></span> |
| <span data-ttu-id="fb79d-137">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="fb79d-137">Minimum operating system</span></span> | <span data-ttu-id="fb79d-138">Windows 98</span><span class="sxs-lookup"><span data-stu-id="fb79d-138">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="fb79d-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fb79d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb79d-140">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="fb79d-140">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="fb79d-141">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="fb79d-141">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="fb79d-142">**Verrouillage**</span><span class="sxs-lookup"><span data-stu-id="fb79d-142">**Lock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[<span data-ttu-id="fb79d-143">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="fb79d-143">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="fb79d-144">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="fb79d-144">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="fb79d-145">**Verrouillage**</span><span class="sxs-lookup"><span data-stu-id="fb79d-145">**Lock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[<span data-ttu-id="fb79d-146">**Scellé**</span><span class="sxs-lookup"><span data-stu-id="fb79d-146">**LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="fb79d-147">**Scellé**</span><span class="sxs-lookup"><span data-stu-id="fb79d-147">**LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="fb79d-148">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="fb79d-148">**LockIndexBuffer**</span></span>](id3dxbasemesh--lockindexbuffer.md)
</dt> <dt>

[<span data-ttu-id="fb79d-149">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="fb79d-149">**LockVertexBuffer**</span></span>](id3dxbasemesh--lockvertexbuffer.md)
</dt> <dt>

<span data-ttu-id="fb79d-150">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="fb79d-150">**LockVertexBuffer**</span></span>
</dt> <dt>

[<span data-ttu-id="fb79d-151">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="fb79d-151">**LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="fb79d-152">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="fb79d-152">**LockAttributeBuffer**</span></span>](id3dxpatchmesh--lockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="fb79d-153">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="fb79d-153">**LockIndexBuffer**</span></span>](id3dxpatchmesh--lockindexbuffer.md)
</dt> <dt>

[<span data-ttu-id="fb79d-154">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="fb79d-154">**LockVertexBuffer**</span></span>](id3dxpatchmesh--lockvertexbuffer.md)
</dt> </dl>

 

 
