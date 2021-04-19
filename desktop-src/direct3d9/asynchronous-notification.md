---
description: Il existe un certain nombre de requêtes intéressantes sur un pilote qu’une application peut prendre en cas de baisse des performances.
ms.assetid: 81e1c5c5-03bc-4598-814e-14e56513e221
title: Notification asynchrone (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aee8acb791e2e1e2de7eb305cc19df4e7711e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514114"
---
# <a name="asynchronous-notification-direct3d-9"></a><span data-ttu-id="fbca1-103">Notification asynchrone (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fbca1-103">Asynchronous Notification (Direct3D 9)</span></span>

<span data-ttu-id="fbca1-104">Il existe un certain nombre de requêtes intéressantes sur un pilote qu’une application peut prendre en cas de baisse des performances.</span><span class="sxs-lookup"><span data-stu-id="fbca1-104">There are number of interesting queries on a driver that an application can make if there is no performance cost.</span></span> <span data-ttu-id="fbca1-105">Dans Direct3D 7 et Direct3D 8, un mécanisme de requête synchrone, GetInfo, fonctionnait bien pour des statistiques, mais aucune requête critique pour les performances n’a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="fbca1-105">In Direct3D 7 and Direct3D 8, a synchronous query mechanism, GetInfo, worked well for things like statistics, but no performance-critical queries were added.</span></span> <span data-ttu-id="fbca1-106">Il existe d’autres éléments (tels que des délimiteurs) qui sont intrinsèquement asynchrones.</span><span class="sxs-lookup"><span data-stu-id="fbca1-106">There are other things (like fences) that are inherently asynchronous.</span></span> <span data-ttu-id="fbca1-107">Il s’agit d’une API simple pour effectuer des requêtes synchrones et asynchrones.</span><span class="sxs-lookup"><span data-stu-id="fbca1-107">This is a simple API to make both synchronous and asynchronous queries.</span></span> <span data-ttu-id="fbca1-108">GetInfo sera mis hors service dans Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="fbca1-108">GetInfo will be retired in Direct3D 9.</span></span>

<span data-ttu-id="fbca1-109">Créez une requête à l’aide de [**IDirect3DDevice9 :: CreateQuery**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="fbca1-109">Create a query using [**IDirect3DDevice9::CreateQuery**](/windows/desktop/api).</span></span> <span data-ttu-id="fbca1-110">Cette méthode prend un D3DQUERYTYPE, qui définit le type de requête à créer et retourne un pointeur vers un objet [**IDirect3DQuery9**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="fbca1-110">This method takes a D3DQUERYTYPE, which defines what kind of query to make and returns a pointer to an [**IDirect3DQuery9**](/windows/desktop/api) object.</span></span> <span data-ttu-id="fbca1-111">Si le type de requête n’est pas pris en charge, l’appel retourne une erreur D3DERR \_ NOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="fbca1-111">If the query type is not supported, the call returns an error D3DERR\_NOTAVAILABLE.</span></span> <span data-ttu-id="fbca1-112">À l’aide de l’objet de requête, l’application soumet la requête au runtime à l’aide de [**IDirect3DQuery9 :: issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue), et interroge l’état de la requête à l’aide de [**IDirect3DQuery9 :: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="fbca1-112">Using the query object, the application submits the query to the runtime using [**IDirect3DQuery9::Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue), and polls the query status using [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span> <span data-ttu-id="fbca1-113">Si le résultat de la requête est disponible, S \_ OK est retourné ; sinon, s \_ false est retourné.</span><span class="sxs-lookup"><span data-stu-id="fbca1-113">If the query result is available, S\_OK is returned; otherwise, S\_FALSE is returned.</span></span> <span data-ttu-id="fbca1-114">L’application est censée passer une mémoire tampon de taille appropriée pour les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="fbca1-114">The application is expected to pass an appropriately sized buffer for the query results.</span></span>

<span data-ttu-id="fbca1-115">L’application a la possibilité de forcer le runtime à vider la requête au pilote à l’aide de D3DGETDATA \_ flush avec [**IDirect3DQuery9 :: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="fbca1-115">The application has an option to force the runtime to flush the query down to the driver by using D3DGETDATA\_FLUSH with [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span> <span data-ttu-id="fbca1-116">Elle provoque un vidage, forçant le pilote à voir la requête.</span><span class="sxs-lookup"><span data-stu-id="fbca1-116">It causes a flush, forcing the driver to see the query.</span></span> <span data-ttu-id="fbca1-117">Dans ce cas, D3DERR \_ DEVICELOST est retourné si l’appareil est perdu.</span><span class="sxs-lookup"><span data-stu-id="fbca1-117">In this case, D3DERR\_DEVICELOST is returned if the device becomes lost.</span></span>

<span data-ttu-id="fbca1-118">Toutes les requêtes sont perdues lorsque l’appareil est perdu, l’application doit les recréer.</span><span class="sxs-lookup"><span data-stu-id="fbca1-118">All queries are lost when the device is lost, the application has to re-create them.</span></span> <span data-ttu-id="fbca1-119">Si l’appareil ne prend pas en charge la requête et que pQueryID a la **valeur null**, la création de la requête échoue avec D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fbca1-119">If the device does not support the query and the pQueryID is **NULL**, the query creation will fail with D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="fbca1-120">Le tableau suivant récapitule les informations importantes sur chaque type de requête.</span><span class="sxs-lookup"><span data-stu-id="fbca1-120">The following table summaries important information about each query type.</span></span>



| <span data-ttu-id="fbca1-121">QuertyType</span><span class="sxs-lookup"><span data-stu-id="fbca1-121">QuertyType</span></span>                    | <span data-ttu-id="fbca1-122">Indicateur de problème valide</span><span class="sxs-lookup"><span data-stu-id="fbca1-122">Valid issue flag</span></span>              | <span data-ttu-id="fbca1-123">Mémoire tampon GetData</span><span class="sxs-lookup"><span data-stu-id="fbca1-123">GetData buffer</span></span>              | <span data-ttu-id="fbca1-124">Runtime</span><span class="sxs-lookup"><span data-stu-id="fbca1-124">Runtime</span></span>      | <span data-ttu-id="fbca1-125">Début de requête implicite</span><span class="sxs-lookup"><span data-stu-id="fbca1-125">Implicit beginning of query</span></span> |
|-------------------------------|-------------------------------|-----------------------------|--------------|-----------------------------|
| <span data-ttu-id="fbca1-126">D3DQUERYTYPE \_ Vcache</span><span class="sxs-lookup"><span data-stu-id="fbca1-126">D3DQUERYTYPE\_VCACHE</span></span>          | <span data-ttu-id="fbca1-127">Fin de D3DISSUE \_</span><span class="sxs-lookup"><span data-stu-id="fbca1-127">D3DISSUE\_END</span></span>                 | <span data-ttu-id="fbca1-128">D3DDEVINFO \_ Vcache</span><span class="sxs-lookup"><span data-stu-id="fbca1-128">D3DDEVINFO\_VCACHE</span></span>          | <span data-ttu-id="fbca1-129">Vente au détail/débogage</span><span class="sxs-lookup"><span data-stu-id="fbca1-129">Retail/Debug</span></span> | <span data-ttu-id="fbca1-130">CreateDevice</span><span class="sxs-lookup"><span data-stu-id="fbca1-130">CreateDevice</span></span>                |
| <span data-ttu-id="fbca1-131">D3DQUERYTYPE \_ ResourceManager</span><span class="sxs-lookup"><span data-stu-id="fbca1-131">D3DQUERYTYPE\_ResourceManager</span></span> | <span data-ttu-id="fbca1-132">Fin de D3DISSUE \_</span><span class="sxs-lookup"><span data-stu-id="fbca1-132">D3DISSUE\_END</span></span>                 | <span data-ttu-id="fbca1-133">D3DDEVINFO \_ ResourceManager</span><span class="sxs-lookup"><span data-stu-id="fbca1-133">D3DDEVINFO\_ResourceManager</span></span> | <span data-ttu-id="fbca1-134">Déboguer uniquement</span><span class="sxs-lookup"><span data-stu-id="fbca1-134">Debug only</span></span>   | <span data-ttu-id="fbca1-135">Présent</span><span class="sxs-lookup"><span data-stu-id="fbca1-135">Present</span></span>                     |
| <span data-ttu-id="fbca1-136">D3DQUERYTYPE \_ VERTEXSTATS</span><span class="sxs-lookup"><span data-stu-id="fbca1-136">D3DQUERYTYPE\_VERTEXSTATS</span></span>     | <span data-ttu-id="fbca1-137">Fin de D3DISSUE \_</span><span class="sxs-lookup"><span data-stu-id="fbca1-137">D3DISSUE\_END</span></span>                 | <span data-ttu-id="fbca1-138">D3DDEVINFO \_ D3DVERTEXSTATS</span><span class="sxs-lookup"><span data-stu-id="fbca1-138">D3DDEVINFO\_D3DVERTEXSTATS</span></span>  | <span data-ttu-id="fbca1-139">Déboguer uniquement</span><span class="sxs-lookup"><span data-stu-id="fbca1-139">Debug only</span></span>   | <span data-ttu-id="fbca1-140">Présent</span><span class="sxs-lookup"><span data-stu-id="fbca1-140">Present</span></span>                     |
| <span data-ttu-id="fbca1-141">\_Événement D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="fbca1-141">D3DQUERYTYPE\_EVENT</span></span>           | <span data-ttu-id="fbca1-142">Fin de D3DISSUE \_</span><span class="sxs-lookup"><span data-stu-id="fbca1-142">D3DISSUE\_END</span></span>                 | <span data-ttu-id="fbca1-143">BOOL</span><span class="sxs-lookup"><span data-stu-id="fbca1-143">BOOL</span></span>                        | <span data-ttu-id="fbca1-144">Vente au détail/débogage</span><span class="sxs-lookup"><span data-stu-id="fbca1-144">Retail/Debug</span></span> | <span data-ttu-id="fbca1-145">CreateDevice</span><span class="sxs-lookup"><span data-stu-id="fbca1-145">CreateDevice</span></span>                |
| <span data-ttu-id="fbca1-146">\_Occlusion D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="fbca1-146">D3DQUERYTYPE\_OCCLUSION</span></span>       | <span data-ttu-id="fbca1-147">D3DISSUE \_ Begin, D3DISSUE \_ end</span><span class="sxs-lookup"><span data-stu-id="fbca1-147">D3DISSUE\_BEGIN,D3DISSUE\_END</span></span> | <span data-ttu-id="fbca1-148">DWORD</span><span class="sxs-lookup"><span data-stu-id="fbca1-148">DWORD</span></span>                       | <span data-ttu-id="fbca1-149">Vente au détail/débogage</span><span class="sxs-lookup"><span data-stu-id="fbca1-149">Retail/Debug</span></span> | <span data-ttu-id="fbca1-150">N/A</span><span class="sxs-lookup"><span data-stu-id="fbca1-150">N/A</span></span>                         |



 

<span data-ttu-id="fbca1-151">Champ Flags pour [**IDirect3DQuery9 :: issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):</span><span class="sxs-lookup"><span data-stu-id="fbca1-151">Flags field for [**IDirect3DQuery9::Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):</span></span>


```
#define D3DISSUE_END (1 << 0) 
// Tells the runtime to issue the end of a query, changing its state to 
//   "non-signaled" 
```




```
 
#define D3DISSUE_BEGIN (1 << 1) // Tells the runtime to issue the 
// beginning of a query. 
```



<span data-ttu-id="fbca1-152">Champ Flags pour [**IDirect3DQuery9 :: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):</span><span class="sxs-lookup"><span data-stu-id="fbca1-152">Flags field for [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):</span></span>


```
 
#define D3DGETDATA_FLUSH (1 << 0) // Tells the runtime to flush 
// if the query is outstanding.
```



## <a name="related-topics"></a><span data-ttu-id="fbca1-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fbca1-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbca1-154">Conseils de programmation</span><span class="sxs-lookup"><span data-stu-id="fbca1-154">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
