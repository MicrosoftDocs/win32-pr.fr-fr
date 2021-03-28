---
title: Interface ID3DX11ThreadPump (D3DX11core. h)
description: Une pompe de thread exécute des tâches de façon asynchrone.
ms.assetid: 1a99f728-149d-4800-a6e4-e3a00cf8cf4f
keywords:
- Interface ID3DX11ThreadPump Direct3D 11
- Interface ID3DX11ThreadPump Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60cedaa4ef84cb9f3ea31cd619d7335cc09324e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103069"
---
# <a name="id3dx11threadpump-interface"></a><span data-ttu-id="942f7-105">Interface ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="942f7-105">ID3DX11ThreadPump interface</span></span>

> [!Note]  
> <span data-ttu-id="942f7-106">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="942f7-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="942f7-107">Une pompe de thread exécute des tâches de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="942f7-107">A thread pump executes tasks asynchronously.</span></span> <span data-ttu-id="942f7-108">Elle est créée en appelant [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md).</span><span class="sxs-lookup"><span data-stu-id="942f7-108">It is created by calling [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md).</span></span> <span data-ttu-id="942f7-109">Il existe plusieurs API qui prennent une pompe de thread facultative comme paramètre, comme [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) et [**D3DX11CompileFromFile**](d3dx11compilefromfile.md); Si vous transmettez une interface de pompage de thread dans ces API, les fonctions s’exécutent de façon asynchrone sur un thread séparé.</span><span class="sxs-lookup"><span data-stu-id="942f7-109">There are several APIs that take an optional thread pump as a parameter, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CompileFromFile**](d3dx11compilefromfile.md); if you pass a thread pump interface into these APIs, the functions will execute asynchronously on a separate thread.</span></span> <span data-ttu-id="942f7-110">En particulier sur les ordinateurs multiprocesseurs, une pompe de threads peut charger des ressources et traiter des données sans une baisse notable des performances.</span><span class="sxs-lookup"><span data-stu-id="942f7-110">Particularly on multiprocessor machines, a thread pump can load resources and process data without a noticeable decrease in performance.</span></span>

## <a name="members"></a><span data-ttu-id="942f7-111">Membres</span><span class="sxs-lookup"><span data-stu-id="942f7-111">Members</span></span>

<span data-ttu-id="942f7-112">L’interface **ID3DX11ThreadPump** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="942f7-112">The **ID3DX11ThreadPump** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="942f7-113">**ID3DX11ThreadPump** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="942f7-113">**ID3DX11ThreadPump** also has these types of members:</span></span>

-   [<span data-ttu-id="942f7-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="942f7-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="942f7-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="942f7-115">Methods</span></span>

<span data-ttu-id="942f7-116">L’interface **ID3DX11ThreadPump** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="942f7-116">The **ID3DX11ThreadPump** interface has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="942f7-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="942f7-117">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="942f7-118">Description</span><span class="sxs-lookup"><span data-stu-id="942f7-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="942f7-119"><a href="id3dx11threadpump-addworkitem.md"><strong>AddWorkItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="942f7-119"><a href="id3dx11threadpump-addworkitem.md"><strong>AddWorkItem</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="942f7-120">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="942f7-120">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="942f7-121">Ajoute un élément de travail à la pompe de thread.</span><span class="sxs-lookup"><span data-stu-id="942f7-121">Adds a work item to the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="942f7-122"><a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a></span><span class="sxs-lookup"><span data-stu-id="942f7-122"><a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="942f7-123">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="942f7-123">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="942f7-124">Obtient le nombre d’éléments dans chacune des trois files d’attente à l’intérieur de la pompe de thread.</span><span class="sxs-lookup"><span data-stu-id="942f7-124">Gets the number of items in each of the three queues inside the thread pump.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="942f7-125"><a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="942f7-125"><a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="942f7-126">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="942f7-126">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="942f7-127">Obtient le nombre d’éléments de travail dans la pompe de thread.</span><span class="sxs-lookup"><span data-stu-id="942f7-127">Gets the number of work items in the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="942f7-128"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>ProcessDeviceWorkItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="942f7-128"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>ProcessDeviceWorkItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="942f7-129">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="942f7-129">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="942f7-130">Définit les éléments de travail sur l’appareil une fois qu’ils ont terminé le chargement et le traitement.</span><span class="sxs-lookup"><span data-stu-id="942f7-130">Sets work items to the device after they have finished loading and processing.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="942f7-131"><a href="id3dx11threadpump-purgeallitems.md"><strong>PurgeAllItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="942f7-131"><a href="id3dx11threadpump-purgeallitems.md"><strong>PurgeAllItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="942f7-132">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="942f7-132">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="942f7-133">Efface tous les éléments de travail de la pompe de thread.</span><span class="sxs-lookup"><span data-stu-id="942f7-133">Clears all work items from the thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="942f7-134"><a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="942f7-134"><a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a></span></span></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="942f7-135">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="942f7-135">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/> <span data-ttu-id="942f7-136">Attend la fin de l’exécution de tous les éléments de travail de la pompe de thread.</span><span class="sxs-lookup"><span data-stu-id="942f7-136">Waits for all work items in the thread pump to finish.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="942f7-137">Notes</span><span class="sxs-lookup"><span data-stu-id="942f7-137">Remarks</span></span>

### <a name="using-a-thread-pump"></a><span data-ttu-id="942f7-138">Utilisation d’une pompe de thread</span><span class="sxs-lookup"><span data-stu-id="942f7-138">Using a Thread Pump</span></span>

<span data-ttu-id="942f7-139">La pompe de thread charge et traite les données à l’aide du processus en trois étapes suivant :</span><span class="sxs-lookup"><span data-stu-id="942f7-139">The thread pump loads and processes data using the following three-step process:</span></span>

1.  <span data-ttu-id="942f7-140">Chargez et décompressez les données avec un [**chargeur de données**](id3dx11dataloader.md).</span><span class="sxs-lookup"><span data-stu-id="942f7-140">Load and decompress the data with a [**Data Loader**](id3dx11dataloader.md).</span></span> <span data-ttu-id="942f7-141">L’objet chargeur de données a trois méthodes que la pompe de thread appellera en interne lors du chargement et de la décompression des données : [**ID3DX11DataLoader :: Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader ::D eComPress**](id3dx11dataloader-decompress.md)et [**ID3DX11DataLoader ::D estroy**](id3dx11dataloader-destroy.md).</span><span class="sxs-lookup"><span data-stu-id="942f7-141">The data loader object has three methods that the thread pump will call internally as it is loading and decompressing the data: [**ID3DX11DataLoader::Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader::Decompress**](id3dx11dataloader-decompress.md), and [**ID3DX11DataLoader::Destroy**](id3dx11dataloader-destroy.md).</span></span> <span data-ttu-id="942f7-142">La fonctionnalité spécifique de ces trois API diffère selon le type de données chargées et décompressées.</span><span class="sxs-lookup"><span data-stu-id="942f7-142">The specific functionality of these three APIs differs depending on the type of data being loaded and decompressed.</span></span> <span data-ttu-id="942f7-143">L’interface de chargeur de données peut également être héritée et ses API peuvent être modifiées si l’une d’elles est en cours de chargement d’un fichier de données défini dans son propre format personnalisé.</span><span class="sxs-lookup"><span data-stu-id="942f7-143">The data loader interface can also be inherited and its APIs can be changed if one is loading a data file defined in one's own custom format.</span></span>
2.  <span data-ttu-id="942f7-144">Traitez les données avec un [**processeur de données**](id3dx11dataprocessor.md).</span><span class="sxs-lookup"><span data-stu-id="942f7-144">Process the data with a [**Data Processor**](id3dx11dataprocessor.md).</span></span> <span data-ttu-id="942f7-145">L’objet de traitement de données a trois méthodes que la pompe de thread appellera en interne lors du traitement des données : [**ID3DX11DataProcessor ::P tionnaire**](id3dx11dataprocessor-process.md), [**ID3DX11DataProcessor :: CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)et [**ID3DX11DataProcessor ::D estroy**](id3dx11dataprocessor-destroy.md).</span><span class="sxs-lookup"><span data-stu-id="942f7-145">The data processor object has three methods that the thread pump will call internally as it is processing the data: [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md), [**ID3DX11DataProcessor::CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md), and [**ID3DX11DataProcessor::Destroy**](id3dx11dataprocessor-destroy.md).</span></span> <span data-ttu-id="942f7-146">La façon dont il traite les données est différente selon le type de données.</span><span class="sxs-lookup"><span data-stu-id="942f7-146">The way it processes the data will be different depending on the type of data.</span></span> <span data-ttu-id="942f7-147">Par exemple, si les données sont une texture stockée en tant que JPEG, [**ID3DX11DataProcessor ::P tionnaire**](id3dx11dataprocessor-process.md) effectue la décompression JPEG pour obtenir les bits d’image RAW de l’image.</span><span class="sxs-lookup"><span data-stu-id="942f7-147">For example, if the data is a texture stored as a JPEG, then [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md) will do JPEG decompression to get the image's raw image bits.</span></span> <span data-ttu-id="942f7-148">Si les données sont un nuanceur, [**ID3DX11DataProcessor ::P tionnaire**](id3dx11dataprocessor-process.md) compile le langage HLSL en bytecode.</span><span class="sxs-lookup"><span data-stu-id="942f7-148">If the data is a shader, then [**ID3DX11DataProcessor::Process**](id3dx11dataprocessor-process.md) will compile the HLSL into bytecode.</span></span> <span data-ttu-id="942f7-149">Une fois les données traitées, un objet périphérique sera créé pour ces données (avec [**ID3DX11DataProcessor :: CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)) et l’objet sera ajouté à une file d’attente d’objets périphériques.</span><span class="sxs-lookup"><span data-stu-id="942f7-149">After the data has been processed a device object will be created for that data (with [**ID3DX11DataProcessor::CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)) and the object will be added to a queue of device objects.</span></span> <span data-ttu-id="942f7-150">L’interface du processeur de données peut également être héritée et ses API peuvent être modifiées si l’une d’elles est en cours de traitement d’un fichier de données défini dans son propre format personnalisé.</span><span class="sxs-lookup"><span data-stu-id="942f7-150">The data processor interface can also be inherited and its APIs can be changed if one is processing a data file defined in one's own custom format.</span></span>
3.  <span data-ttu-id="942f7-151">Liez l’objet appareil à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="942f7-151">Bind the device object to the device.</span></span> <span data-ttu-id="942f7-152">Cette opération est effectuée quand une application appelle [**ID3DX11ThreadPump ::P rocessdeviceworkitems**](id3dx11threadpump-processdeviceworkitems.md), qui lie un nombre spécifié d’objets dans la file d’attente d’objets d’appareil à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="942f7-152">This is done when one's application calls [**ID3DX11ThreadPump::ProcessDeviceWorkItems**](id3dx11threadpump-processdeviceworkitems.md), which will bind a specified number of objects in the queue of device objects to the device.</span></span>

<span data-ttu-id="942f7-153">La pompe de threads peut être utilisée pour charger des données de deux manières : en appelant une API qui prend une pompe de thread comme paramètre, tel que [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) et [**D3DX11CompileFromFile**](d3dx11compilefromfile.md), ou en appelant [**ID3DX11ThreadPump :: AddWorkItem**](id3dx11threadpump-addworkitem.md).</span><span class="sxs-lookup"><span data-stu-id="942f7-153">The thread pump can be used to load data in one of two ways: by calling an API that takes a thread pump as a parameter, such as [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) and [**D3DX11CompileFromFile**](d3dx11compilefromfile.md), or by calling [**ID3DX11ThreadPump::AddWorkItem**](id3dx11threadpump-addworkitem.md).</span></span> <span data-ttu-id="942f7-154">Dans le cas des API qui prennent une pompe de thread, le chargeur de données et le processeur de données sont créés en interne.</span><span class="sxs-lookup"><span data-stu-id="942f7-154">In the case of the APIs that take a thread pump, the data loader and data processor are created internally.</span></span> <span data-ttu-id="942f7-155">Dans le cas de AddWorkItem, le chargeur de données et le processeur de données doivent être créés au préalable et sont ensuite passés à AddWorkItem.</span><span class="sxs-lookup"><span data-stu-id="942f7-155">In the case of AddWorkItem, the data loader and data processor must be created beforehand and are then passed into AddWorkItem.</span></span> <span data-ttu-id="942f7-156">D3DX11 fournit un ensemble d’API permettant de créer des chargeurs de données et des processeurs de données qui disposent de fonctionnalités pour le chargement et le traitement des formats de données courants.</span><span class="sxs-lookup"><span data-stu-id="942f7-156">D3DX11 provides a set of APIs for creating data loaders and data processors that have functionality for loading and processing common data formats.</span></span> <span data-ttu-id="942f7-157">Pour les formats de données personnalisés, les interfaces du chargeur de données et du processeur de données doivent être héritées et leurs méthodes doivent être redéfinies.</span><span class="sxs-lookup"><span data-stu-id="942f7-157">For custom data formats, the data loader and data processor interfaces must be inherited and their methods must be redefined.</span></span>

<span data-ttu-id="942f7-158">L’objet thread Pump occupe une quantité importante de ressources. en général, un seul doit être créé par application.</span><span class="sxs-lookup"><span data-stu-id="942f7-158">The thread pump object takes up a substantial amount of resources, so generally only one should be created per application.</span></span>

## <a name="requirements"></a><span data-ttu-id="942f7-159">Spécifications</span><span class="sxs-lookup"><span data-stu-id="942f7-159">Requirements</span></span>



| <span data-ttu-id="942f7-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="942f7-160">Requirement</span></span> | <span data-ttu-id="942f7-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="942f7-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="942f7-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="942f7-162">Minimum supported client</span></span><br/> | <span data-ttu-id="942f7-163">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="942f7-163">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="942f7-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="942f7-164">Minimum supported server</span></span><br/> | <span data-ttu-id="942f7-165">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="942f7-165">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="942f7-166">En-tête</span><span class="sxs-lookup"><span data-stu-id="942f7-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="942f7-167"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="942f7-167"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="942f7-168">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="942f7-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="942f7-169"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="942f7-169"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="942f7-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="942f7-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="942f7-171">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="942f7-171">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

