---
title: Interface IMsTscAdvancedSettings
description: Comprend des méthodes pour récupérer et définir des propriétés qui activent la mise en cache, la compression et la redirection de l’imprimante et du presse-papiers.
ms.assetid: 3385e843-be05-4801-8d59-6395d95686b1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsTscAdvancedSettings
- Services Bureau à distance de l’interface IMsTscAdvancedSettings, Description
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4d55df30c940ecc5a5515f13c05a285507499e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511149"
---
# <a name="imstscadvancedsettings-interface"></a><span data-ttu-id="cc762-105">Interface IMsTscAdvancedSettings</span><span class="sxs-lookup"><span data-stu-id="cc762-105">IMsTscAdvancedSettings interface</span></span>

<span data-ttu-id="cc762-106">Comprend des méthodes pour récupérer et définir des propriétés qui activent la mise en cache, la compression et la redirection de l’imprimante et du presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="cc762-106">Includes methods to retrieve and set properties that enable bitmap caching, compression, and printer and clipboard redirection.</span></span> <span data-ttu-id="cc762-107">Vous pouvez également spécifier les noms des dll clientes du canal virtuel.</span><span class="sxs-lookup"><span data-stu-id="cc762-107">You can also specify names of virtual channel client DLLs.</span></span>

<span data-ttu-id="cc762-108">Vous obtenez une instance de cette interface à l’aide de la propriété [**IMsTscAx :: AdvancedSettings**](imstscax-advancedsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="cc762-108">You obtain an instance of this interface by using the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="cc762-109">Membres</span><span class="sxs-lookup"><span data-stu-id="cc762-109">Members</span></span>

<span data-ttu-id="cc762-110">L’interface **IMsTscAdvancedSettings** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="cc762-110">The **IMsTscAdvancedSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="cc762-111">**IMsTscAdvancedSettings** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cc762-111">**IMsTscAdvancedSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="cc762-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cc762-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cc762-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cc762-113">Properties</span></span>

<span data-ttu-id="cc762-114">L’interface **IMsTscAdvancedSettings** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="cc762-114">The **IMsTscAdvancedSettings** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="cc762-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="cc762-115">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="cc762-116">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="cc762-116">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="cc762-117">Description</span><span class="sxs-lookup"><span data-stu-id="cc762-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cc762-118"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowBackgroundInput</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc762-118"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowBackgroundInput</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="cc762-119">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cc762-119">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="cc762-120">Spécifie si le mode d’entrée d’arrière-plan est activé.</span><span class="sxs-lookup"><span data-stu-id="cc762-120">Specifies whether background input mode is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cc762-121"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>BitmapPeristence</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc762-121"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>BitmapPeristence</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="cc762-122">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cc762-122">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="cc762-123">Spécifie si la mise en cache bitmap est activée.</span><span class="sxs-lookup"><span data-stu-id="cc762-123">Specifies whether bitmap caching is enabled.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cc762-124">La faute d’orthographe dans le nom de la propriété se trouve dans la version finale du contrôle.</span><span class="sxs-lookup"><span data-stu-id="cc762-124">The spelling error in the name of the property is in the released version of the control.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cc762-125"><a href="imstscadvancedsettings-compress.md"><strong>Dens</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc762-125"><a href="imstscadvancedsettings-compress.md"><strong>Compress</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="cc762-126">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cc762-126">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="cc762-127">Spécifie si la compression est activée.</span><span class="sxs-lookup"><span data-stu-id="cc762-127">Specifies whether compression is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cc762-128"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>ContainerHandledFullScreen</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc762-128"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>ContainerHandledFullScreen</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="cc762-129">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cc762-129">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="cc762-130">Spécifie si le mode plein écran géré par le conteneur est activé.</span><span class="sxs-lookup"><span data-stu-id="cc762-130">Specifies whether the container-handled full-screen mode is enabled.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cc762-131"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>DisableRdpdr</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc762-131"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>DisableRdpdr</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="cc762-132">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="cc762-132">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="cc762-133">Spécifie si l’imprimante et la redirection du presse-papiers sont activées.</span><span class="sxs-lookup"><span data-stu-id="cc762-133">Specifies whether printer and clipboard redirection is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cc762-134"><a href="imstscadvancedsettings-iconfile.md"><strong>IconFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc762-134"><a href="imstscadvancedsettings-iconfile.md"><strong>IconFile</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="cc762-135">Écriture seule</span><span class="sxs-lookup"><span data-stu-id="cc762-135">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="cc762-136">Spécifie le nom du fichier contenant les données d’icône qui seront accessibles lors de l’affichage du client en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="cc762-136">Specifies the name of the file containing icon data that will be accessed when displaying the client in full-screen mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cc762-137"><a href="imstscadvancedsettings-iconindex.md"><strong>IndexIcône</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc762-137"><a href="imstscadvancedsettings-iconindex.md"><strong>IconIndex</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="cc762-138">Écriture seule</span><span class="sxs-lookup"><span data-stu-id="cc762-138">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="cc762-139">Spécifie l’index de l’icône dans le fichier icône actuel.</span><span class="sxs-lookup"><span data-stu-id="cc762-139">Specifies the index of the icon within the current icon file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="cc762-140"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>KeyBoardLayoutStr</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc762-140"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>KeyBoardLayoutStr</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="cc762-141">Écriture seule</span><span class="sxs-lookup"><span data-stu-id="cc762-141">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="cc762-142">Spécifie le nom de l’identificateur de paramètres régionaux d’entrée actif (anciennement appelé disposition de clavier) à utiliser pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="cc762-142">Specifies the name of the active input locale identifier (formerly called the keyboard layout) to use for the connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="cc762-143"><a href="imstscadvancedsettings-plugindlls.md"><strong>PluginDlls</strong></a></span><span class="sxs-lookup"><span data-stu-id="cc762-143"><a href="imstscadvancedsettings-plugindlls.md"><strong>PluginDlls</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="cc762-144">Écriture seule</span><span class="sxs-lookup"><span data-stu-id="cc762-144">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="cc762-145">Spécifie les noms des dll clientes du canal virtuel à charger.</span><span class="sxs-lookup"><span data-stu-id="cc762-145">Specifies the names of virtual channel client DLLs to be loaded.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="cc762-146">Notes</span><span class="sxs-lookup"><span data-stu-id="cc762-146">Remarks</span></span>

<span data-ttu-id="cc762-147">Cette interface a été étendue par les interfaces suivantes, chaque nouvelle interface héritant de toutes les méthodes et propriétés des interfaces précédentes :</span><span class="sxs-lookup"><span data-stu-id="cc762-147">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="cc762-148">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="cc762-148">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
-   [<span data-ttu-id="cc762-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="cc762-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
-   [<span data-ttu-id="cc762-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="cc762-150">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
-   [<span data-ttu-id="cc762-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="cc762-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="cc762-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="cc762-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="cc762-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="cc762-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="cc762-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="cc762-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="cc762-155">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="cc762-155">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc762-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc762-156">Requirements</span></span>



| <span data-ttu-id="cc762-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc762-157">Requirement</span></span> | <span data-ttu-id="cc762-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc762-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc762-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc762-159">Minimum supported client</span></span><br/> | <span data-ttu-id="cc762-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc762-160">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="cc762-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc762-161">Minimum supported server</span></span><br/> | <span data-ttu-id="cc762-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc762-162">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="cc762-163">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="cc762-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="cc762-164"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc762-164"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="cc762-165">DLL</span><span class="sxs-lookup"><span data-stu-id="cc762-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc762-166"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc762-166"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="cc762-167">IID</span><span class="sxs-lookup"><span data-stu-id="cc762-167">IID</span></span><br/>                      | <span data-ttu-id="cc762-168">IID \_ IMsTscAdvancedSettings est défini en tant que 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="cc762-168">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc762-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc762-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc762-170">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="cc762-170">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="cc762-171">Référence Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="cc762-171">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

