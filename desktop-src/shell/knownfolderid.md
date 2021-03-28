---
Description: Les constantes KNOWNFOLDERID représentent des GUID qui identifient les dossiers standard enregistrés avec le système comme dossiers connus.
ms.assetid: f2c08ade-3083-44e4-82b0-dde45f0e3094
title: KNOWNFOLDERID (fichier KnownFolders. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 97748d074d6b0982708f51ea679f0629e8abfad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982858"
---
# <a name="knownfolderid"></a><span data-ttu-id="a3428-103">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="a3428-103">KNOWNFOLDERID</span></span>

<span data-ttu-id="a3428-104">Les constantes **KNOWNFOLDERID** représentent des GUID qui identifient les dossiers standard enregistrés avec le système comme [dossiers connus](known-folders.md).</span><span class="sxs-lookup"><span data-stu-id="a3428-104">The **KNOWNFOLDERID** constants represent GUIDs that identify standard folders registered with the system as [Known Folders](known-folders.md).</span></span> <span data-ttu-id="a3428-105">Ces dossiers sont installés avec Windows Vista et les systèmes d’exploitation ultérieurs, et un ordinateur ne dispose que de dossiers appropriés.</span><span class="sxs-lookup"><span data-stu-id="a3428-105">These folders are installed with Windows Vista and later operating systems, and a computer will have only folders appropriate to it installed.</span></span> <span data-ttu-id="a3428-106">Pour obtenir une description de ces dossiers, consultez [**CSIDL**](csidl.md).</span><span class="sxs-lookup"><span data-stu-id="a3428-106">For descriptions of these folders, see [**CSIDL**](csidl.md).</span></span>

## <a name="example"></a><span data-ttu-id="a3428-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="a3428-107">Example</span></span>

```c
HRESULT CExplorerBrowserHostDialog::_FillViewWithKnownFolders(IResultsFolder *prf)
{
    IKnownFolderManager *pManager;
    HRESULT hr = CoCreateInstance(CLSID_KnownFolderManager, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pManager));
    if (SUCCEEDED(hr))
    {
        UINT cCount;
        KNOWNFOLDERID *pkfid;

        hr = pManager->GetFolderIds(&pkfid, &cCount);
        if (SUCCEEDED(hr))
        {
            for (UINT i = 0; i < cCount; i++)
            {
                IKnownFolder *pKnownFolder;
                hr = pManager->GetFolder(pkfid[i], &pKnownFolder);
                if (SUCCEEDED(hr))
                {
                    IShellItem *psi;
                    hr = pKnownFolder->GetShellItem(0, IID_PPV_ARGS(&psi));
                    if (SUCCEEDED(hr))
                    {
                        hr = prf->AddItem(psi);
                        psi->Release();
                    }
                    pKnownFolder->Release();
                }
            }
            CoTaskMemFree(pkfid);
        }
        pManager->Release();
    }
    return hr;
}

```

<span data-ttu-id="a3428-108">Exemple tiré d' [exemples classiques Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winui/shell/appplatform/ExplorerBrowserCustomContents/ExplorerBrowserCustomContents.cpp) sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="a3428-108">Example from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winui/shell/appplatform/ExplorerBrowserCustomContents/ExplorerBrowserCustomContents.cpp) on GitHub.</span></span>

## <a name="constants"></a><span data-ttu-id="a3428-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="a3428-109">Constants</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="a3428-110">Constante</span><span class="sxs-lookup"><span data-stu-id="a3428-110">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="a3428-111">Description</span><span class="sxs-lookup"><span data-stu-id="a3428-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AccountPictures"></span><span id="folderid_accountpictures"></span><span id="FOLDERID_ACCOUNTPICTURES"></span><dl> <span data-ttu-id="a3428-112"><dt><strong>FOLDERID_AccountPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-112"><dt><strong>FOLDERID_AccountPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-113">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-113">GUID</span></span></td>
<td><span data-ttu-id="a3428-114">{008ca0b1-55b4-4c56-b8a8-4de4b299d3be}</span><span class="sxs-lookup"><span data-stu-id="a3428-114">{008ca0b1-55b4-4c56-b8a8-4de4b299d3be}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-115">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-115">Display Name</span></span></td>
<td><span data-ttu-id="a3428-116">Images de compte</span><span class="sxs-lookup"><span data-stu-id="a3428-116">Account Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-117">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-117">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-118">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-118">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-119">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-119">Default Path</span></span></td>
<td><span data-ttu-id="a3428-120">%APPDATA%\Microsoft\Windows\AccountPictures</span><span class="sxs-lookup"><span data-stu-id="a3428-120">%APPDATA%\Microsoft\Windows\AccountPictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-121">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-121">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-122">Aucun, valeur introduite dans Windows 8</span><span class="sxs-lookup"><span data-stu-id="a3428-122">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-123">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-123">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-124">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-124">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-125">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-125">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-126">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-126">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AddNewPrograms"></span><span id="folderid_addnewprograms"></span><span id="FOLDERID_ADDNEWPROGRAMS"></span><dl> <span data-ttu-id="a3428-127"><dt><strong>FOLDERID_AddNewPrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-127"><dt><strong>FOLDERID_AddNewPrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-128">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-128">GUID</span></span></td>
<td><span data-ttu-id="a3428-129">{de61d971-5ebc-4f02-a3a9-6c82895e5c04}</span><span class="sxs-lookup"><span data-stu-id="a3428-129">{de61d971-5ebc-4f02-a3a9-6c82895e5c04}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-130">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-130">Display Name</span></span></td>
<td><span data-ttu-id="a3428-131">Télécharger des programmes</span><span class="sxs-lookup"><span data-stu-id="a3428-131">Get Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-132">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-132">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-133">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-133">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-134">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-134">Default Path</span></span></td>
<td><span data-ttu-id="a3428-135">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-135">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-136">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-136">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-137">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-137">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-138">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-138">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-139">Ajouter de nouveaux programmes (situés dans l’élément <strong>Ajout/suppression de programmes</strong> du panneau de configuration)</span><span class="sxs-lookup"><span data-stu-id="a3428-139">Add New Programs (found in the <strong>Add or Remove Programs</strong> item in the Control Panel)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-140">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-140">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-141">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-141">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AdminTools"></span><span id="folderid_admintools"></span><span id="FOLDERID_ADMINTOOLS"></span><dl> <span data-ttu-id="a3428-142"><dt><strong>FOLDERID_AdminTools</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-142"><dt><strong>FOLDERID_AdminTools</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-143">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-143">GUID</span></span></td>
<td><span data-ttu-id="a3428-144">{724EF170-A42D-4FEF-9F26-B60E846FBA4F}</span><span class="sxs-lookup"><span data-stu-id="a3428-144">{724EF170-A42D-4FEF-9F26-B60E846FBA4F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-145">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-145">Display Name</span></span></td>
<td><span data-ttu-id="a3428-146">Outils d'administration</span><span class="sxs-lookup"><span data-stu-id="a3428-146">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-147">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-147">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-148">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-148">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-149">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-149">Default Path</span></span></td>
<td><span data-ttu-id="a3428-150">Outils \ outils d'%APPDATA%\Microsoft\Windows\Start</span><span class="sxs-lookup"><span data-stu-id="a3428-150">%APPDATA%\Microsoft\Windows\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-151">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-151">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-152">CSIDL_ADMINTOOLS</span><span class="sxs-lookup"><span data-stu-id="a3428-152">CSIDL_ADMINTOOLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-153">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-153">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-154">Outils d'administration</span><span class="sxs-lookup"><span data-stu-id="a3428-154">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-155">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-155">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-156">Outils \ outils d'%USERPROFILE%\Start</span><span class="sxs-lookup"><span data-stu-id="a3428-156">%USERPROFILE%\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppDataDesktop"></span><span id="folderid_appdatadesktop"></span><span id="FOLDERID_APPDATADESKTOP"></span><dl> <span data-ttu-id="a3428-157"><dt><strong>FOLDERID_AppDataDesktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-157"><dt><strong>FOLDERID_AppDataDesktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-158">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-158">GUID</span></span></td>
<td><span data-ttu-id="a3428-159">{B2C5E279-7ADD-439F-B28C-C41FE1BBF672}</span><span class="sxs-lookup"><span data-stu-id="a3428-159">{B2C5E279-7ADD-439F-B28C-C41FE1BBF672}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-160">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-160">Display Name</span></span></td>
<td><span data-ttu-id="a3428-161">AppDataDesktop</span><span class="sxs-lookup"><span data-stu-id="a3428-161">AppDataDesktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-162">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-162">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-163">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-163">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-164">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-164">Default Path</span></span></td>
<td><span data-ttu-id="a3428-165">%LOCALAPPDATA%\Desktop</span><span class="sxs-lookup"><span data-stu-id="a3428-165">%LOCALAPPDATA%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-166">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-166">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-167">Aucun, valeur introduite dans Windows 10, version 1709</span><span class="sxs-lookup"><span data-stu-id="a3428-167">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-168">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-168">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-169">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-169">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-170">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-170">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-171">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-171">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="a3428-172">Ce FOLDERID est utilisé en interne par les applications .NET pour activer les fonctionnalités d’application multiplateforme.</span><span class="sxs-lookup"><span data-stu-id="a3428-172">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="a3428-173">Elle n’est pas destinée à être utilisée directement à partir d’une application.</span><span class="sxs-lookup"><span data-stu-id="a3428-173">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppDataDocuments"></span><span id="folderid_appdatadocuments"></span><span id="FOLDERID_APPDATADOCUMENTS"></span><dl> <span data-ttu-id="a3428-174"><dt><strong>FOLDERID_AppDataDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-174"><dt><strong>FOLDERID_AppDataDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-175">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-175">GUID</span></span></td>
<td><span data-ttu-id="a3428-176">{7BE16610-1F7F-44AC-BFF0-83E15F2FFCA1}</span><span class="sxs-lookup"><span data-stu-id="a3428-176">{7BE16610-1F7F-44AC-BFF0-83E15F2FFCA1}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-177">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-177">Display Name</span></span></td>
<td><span data-ttu-id="a3428-178">AppDataDocuments</span><span class="sxs-lookup"><span data-stu-id="a3428-178">AppDataDocuments</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-179">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-179">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-180">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-180">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-181">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-181">Default Path</span></span></td>
<td><span data-ttu-id="a3428-182">%LOCALAPPDATA%\Documents</span><span class="sxs-lookup"><span data-stu-id="a3428-182">%LOCALAPPDATA%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-183">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-183">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-184">Aucun, valeur introduite dans Windows 10, version 1709</span><span class="sxs-lookup"><span data-stu-id="a3428-184">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-185">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-185">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-186">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-186">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-187">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-187">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-188">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-188">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="a3428-189">Ce FOLDERID est utilisé en interne par les applications .NET pour activer les fonctionnalités d’application multiplateforme.</span><span class="sxs-lookup"><span data-stu-id="a3428-189">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="a3428-190">Elle n’est pas destinée à être utilisée directement à partir d’une application.</span><span class="sxs-lookup"><span data-stu-id="a3428-190">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppDataFavorites"></span><span id="folderid_appdatafavorites"></span><span id="FOLDERID_APPDATAFAVORITES"></span><dl> <span data-ttu-id="a3428-191"><dt><strong>FOLDERID_AppDataFavorites</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-191"><dt><strong>FOLDERID_AppDataFavorites</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-192">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-192">GUID</span></span></td>
<td><span data-ttu-id="a3428-193">{7CFBEFBC-DE1F-45AA-B843-A542AC536CC9}</span><span class="sxs-lookup"><span data-stu-id="a3428-193">{7CFBEFBC-DE1F-45AA-B843-A542AC536CC9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-194">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-194">Display Name</span></span></td>
<td><span data-ttu-id="a3428-195">AppDataFavorites</span><span class="sxs-lookup"><span data-stu-id="a3428-195">AppDataFavorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-196">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-196">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-197">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-197">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-198">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-198">Default Path</span></span></td>
<td><span data-ttu-id="a3428-199">%LOCALAPPDATA%\Favorites</span><span class="sxs-lookup"><span data-stu-id="a3428-199">%LOCALAPPDATA%\Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-200">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-200">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-201">Aucun, valeur introduite dans Windows 10, version 1709</span><span class="sxs-lookup"><span data-stu-id="a3428-201">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-202">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-202">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-203">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-203">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-204">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-204">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-205">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-205">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="a3428-206">Ce FOLDERID est utilisé en interne par les applications .NET pour activer les fonctionnalités d’application multiplateforme.</span><span class="sxs-lookup"><span data-stu-id="a3428-206">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="a3428-207">Elle n’est pas destinée à être utilisée directement à partir d’une application.</span><span class="sxs-lookup"><span data-stu-id="a3428-207">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppDataProgramData"></span><span id="folderid_appdataprogramdata"></span><span id="FOLDERID_APPDATAPROGRAMDATA"></span><dl> <span data-ttu-id="a3428-208"><dt><strong>FOLDERID_AppDataProgramData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-208"><dt><strong>FOLDERID_AppDataProgramData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-209">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-209">GUID</span></span></td>
<td><span data-ttu-id="a3428-210">{559D40A3-A036-40FA-AF61-84CB430A4D34}</span><span class="sxs-lookup"><span data-stu-id="a3428-210">{559D40A3-A036-40FA-AF61-84CB430A4D34}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-211">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-211">Display Name</span></span></td>
<td><span data-ttu-id="a3428-212">AppDataProgramData</span><span class="sxs-lookup"><span data-stu-id="a3428-212">AppDataProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-213">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-213">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-214">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-214">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-215">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-215">Default Path</span></span></td>
<td><span data-ttu-id="a3428-216">%LOCALAPPDATA%\ProgramData</span><span class="sxs-lookup"><span data-stu-id="a3428-216">%LOCALAPPDATA%\ProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-217">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-217">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-218">Aucun, valeur introduite dans Windows 10, version 1709</span><span class="sxs-lookup"><span data-stu-id="a3428-218">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-219">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-219">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-220">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-220">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-221">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-221">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-222">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-222">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="a3428-223">Ce FOLDERID est utilisé en interne par les applications .NET pour activer les fonctionnalités d’application multiplateforme.</span><span class="sxs-lookup"><span data-stu-id="a3428-223">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="a3428-224">Elle n’est pas destinée à être utilisée directement à partir d’une application.</span><span class="sxs-lookup"><span data-stu-id="a3428-224">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ApplicationShortcuts"></span><span id="folderid_applicationshortcuts"></span><span id="FOLDERID_APPLICATIONSHORTCUTS"></span><dl> <span data-ttu-id="a3428-225"><dt><strong>FOLDERID_ApplicationShortcuts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-225"><dt><strong>FOLDERID_ApplicationShortcuts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-226">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-226">GUID</span></span></td>
<td><span data-ttu-id="a3428-227">{A3918781-E5F2-4890-B3D9-A7E54332328C}</span><span class="sxs-lookup"><span data-stu-id="a3428-227">{A3918781-E5F2-4890-B3D9-A7E54332328C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-228">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-228">Display Name</span></span></td>
<td><span data-ttu-id="a3428-229">Raccourcis d’application</span><span class="sxs-lookup"><span data-stu-id="a3428-229">Application Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-230">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-230">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-231">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-231">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-232">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-232">Default Path</span></span></td>
<td><span data-ttu-id="a3428-233">%LOCALAPPDATA%\Microsoft\Windows\Application les raccourcis</span><span class="sxs-lookup"><span data-stu-id="a3428-233">%LOCALAPPDATA%\Microsoft\Windows\Application Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-234">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-234">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-235">Aucun, valeur introduite dans Windows 8</span><span class="sxs-lookup"><span data-stu-id="a3428-235">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-236">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-236">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-237">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-237">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-238">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-238">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-239">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-239">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppsFolder"></span><span id="folderid_appsfolder"></span><span id="FOLDERID_APPSFOLDER"></span><dl> <span data-ttu-id="a3428-240"><dt><strong>FOLDERID_AppsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-240"><dt><strong>FOLDERID_AppsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-241">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-241">GUID</span></span></td>
<td><span data-ttu-id="a3428-242">{1e87508d-89c2-42f0-8a7e-645a0f50ca58}</span><span class="sxs-lookup"><span data-stu-id="a3428-242">{1e87508d-89c2-42f0-8a7e-645a0f50ca58}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-243">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-243">Display Name</span></span></td>
<td><span data-ttu-id="a3428-244">Applications</span><span class="sxs-lookup"><span data-stu-id="a3428-244">Applications</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-245">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-245">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-246">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-246">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-247">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-247">Default Path</span></span></td>
<td><span data-ttu-id="a3428-248">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-248">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-249">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-249">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-250">Aucun, valeur introduite dans Windows 8</span><span class="sxs-lookup"><span data-stu-id="a3428-250">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-251">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-251">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-252">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-252">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-253">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-253">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-254">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-254">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppUpdates"></span><span id="folderid_appupdates"></span><span id="FOLDERID_APPUPDATES"></span><dl> <span data-ttu-id="a3428-255"><dt><strong>FOLDERID_AppUpdates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-255"><dt><strong>FOLDERID_AppUpdates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-256">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-256">GUID</span></span></td>
<td><span data-ttu-id="a3428-257">{a305ce99-f527-492b-8b1a-7e76fa98d6e4}</span><span class="sxs-lookup"><span data-stu-id="a3428-257">{a305ce99-f527-492b-8b1a-7e76fa98d6e4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-258">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-258">Display Name</span></span></td>
<td><span data-ttu-id="a3428-259">Mises à jour installées</span><span class="sxs-lookup"><span data-stu-id="a3428-259">Installed Updates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-260">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-260">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-261">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-261">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-262">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-262">Default Path</span></span></td>
<td><span data-ttu-id="a3428-263">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-263">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-264">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-264">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-265">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-265">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-266">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-266">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-267">Aucune, la valeur introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a3428-267">None, value introduced in Windows Vista.</span></span> <span data-ttu-id="a3428-268">Dans les versions antérieures de Windows, les informations de cette page étaient incluses dans <strong>Ajout/suppression de programmes</strong> si la case à cocher <strong>afficher les mises à jour</strong> a été activée.</span><span class="sxs-lookup"><span data-stu-id="a3428-268">In earlier versions of Windows, the information on this page was included in <strong>Add or Remove Programs</strong> if the <strong>Show updates</strong> box was checked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-269">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-269">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-270">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-270">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CameraRoll"></span><span id="folderid_cameraroll"></span><span id="FOLDERID_CAMERAROLL"></span><dl> <span data-ttu-id="a3428-271"><dt><strong>FOLDERID_CameraRoll</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-271"><dt><strong>FOLDERID_CameraRoll</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-272">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-272">GUID</span></span></td>
<td><span data-ttu-id="a3428-273">{AB5FB87B-7CE2-4F83-915D-550846C9537B}</span><span class="sxs-lookup"><span data-stu-id="a3428-273">{AB5FB87B-7CE2-4F83-915D-550846C9537B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-274">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-274">Display Name</span></span></td>
<td><span data-ttu-id="a3428-275">Pellicule</span><span class="sxs-lookup"><span data-stu-id="a3428-275">Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-276">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-276">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-277">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-277">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-278">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-278">Default Path</span></span></td>
<td><span data-ttu-id="a3428-279">%USERPROFILE%\Pictures\Camera Roll</span><span class="sxs-lookup"><span data-stu-id="a3428-279">%USERPROFILE%\Pictures\Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-280">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-280">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-281">Aucun, valeur introduite dans Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a3428-281">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-282">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-282">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-283">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-283">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-284">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-284">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-285">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-285">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CDBurning"></span><span id="folderid_cdburning"></span><span id="FOLDERID_CDBURNING"></span><dl> <span data-ttu-id="a3428-286"><dt><strong>FOLDERID_CDBurning</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-286"><dt><strong>FOLDERID_CDBurning</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-287">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-287">GUID</span></span></td>
<td><span data-ttu-id="a3428-288">{9E52AB10-F80D-49DF-ACB8-4330F5687855}</span><span class="sxs-lookup"><span data-stu-id="a3428-288">{9E52AB10-F80D-49DF-ACB8-4330F5687855}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-289">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-289">Display Name</span></span></td>
<td><span data-ttu-id="a3428-290">Dossier de gravure temporaire</span><span class="sxs-lookup"><span data-stu-id="a3428-290">Temporary Burn Folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-291">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-291">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-292">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-292">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-293">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-293">Default Path</span></span></td>
<td><span data-ttu-id="a3428-294">%LOCALAPPDATA%\Microsoft\Windows\Burn\Burn</span><span class="sxs-lookup"><span data-stu-id="a3428-294">%LOCALAPPDATA%\Microsoft\Windows\Burn\Burn</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-295">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-295">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-296">CSIDL_CDBURN_AREA</span><span class="sxs-lookup"><span data-stu-id="a3428-296">CSIDL_CDBURN_AREA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-297">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-297">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-298">Gravage de CD</span><span class="sxs-lookup"><span data-stu-id="a3428-298">CD Burning</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-299">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-299">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-300">%USERPROFILE%\Local Settings\Application Data\Microsoft\CD, gravure</span><span class="sxs-lookup"><span data-stu-id="a3428-300">%USERPROFILE%\Local Settings\Application Data\Microsoft\CD Burning</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ChangeRemovePrograms"></span><span id="folderid_changeremoveprograms"></span><span id="FOLDERID_CHANGEREMOVEPROGRAMS"></span><dl> <span data-ttu-id="a3428-301"><dt><strong>FOLDERID_ChangeRemovePrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-301"><dt><strong>FOLDERID_ChangeRemovePrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-302">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-302">GUID</span></span></td>
<td><span data-ttu-id="a3428-303">{df7266ac-9274-4867-8d55-3bd661de872d}</span><span class="sxs-lookup"><span data-stu-id="a3428-303">{df7266ac-9274-4867-8d55-3bd661de872d}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-304">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-304">Display Name</span></span></td>
<td><span data-ttu-id="a3428-305">Programmes et fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="a3428-305">Programs and Features</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-306">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-306">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-307">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-307">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-308">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-308">Default Path</span></span></td>
<td><span data-ttu-id="a3428-309">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-309">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-310">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-310">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-311">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-311">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-312">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-312">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-313">Ajouter ou supprimer des programmes</span><span class="sxs-lookup"><span data-stu-id="a3428-313">Add or Remove Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-314">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-314">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-315">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-315">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonAdminTools"></span><span id="folderid_commonadmintools"></span><span id="FOLDERID_COMMONADMINTOOLS"></span><dl> <span data-ttu-id="a3428-316"><dt><strong>FOLDERID_CommonAdminTools</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-316"><dt><strong>FOLDERID_CommonAdminTools</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-317">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-317">GUID</span></span></td>
<td><span data-ttu-id="a3428-318">{D0384E7D-BAC3-4797-8F14-CBA229B392B5}</span><span class="sxs-lookup"><span data-stu-id="a3428-318">{D0384E7D-BAC3-4797-8F14-CBA229B392B5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-319">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-319">Display Name</span></span></td>
<td><span data-ttu-id="a3428-320">Outils d'administration</span><span class="sxs-lookup"><span data-stu-id="a3428-320">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-321">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-321">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-322">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-322">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-323">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-323">Default Path</span></span></td>
<td><span data-ttu-id="a3428-324">Outils \ outils d'%ALLUSERSPROFILE%\Microsoft\Windows\Start</span><span class="sxs-lookup"><span data-stu-id="a3428-324">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-325">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-325">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-326">CSIDL_COMMON_ADMINTOOLS</span><span class="sxs-lookup"><span data-stu-id="a3428-326">CSIDL_COMMON_ADMINTOOLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-327">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-327">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-328">Outils d'administration</span><span class="sxs-lookup"><span data-stu-id="a3428-328">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-329">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-329">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-330">Outils \ outils d'%ALLUSERSPROFILE%\Start</span><span class="sxs-lookup"><span data-stu-id="a3428-330">%ALLUSERSPROFILE%\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonOEMLinks"></span><span id="folderid_commonoemlinks"></span><span id="FOLDERID_COMMONOEMLINKS"></span><dl> <span data-ttu-id="a3428-331"><dt><strong>FOLDERID_CommonOEMLinks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-331"><dt><strong>FOLDERID_CommonOEMLinks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-332">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-332">GUID</span></span></td>
<td><span data-ttu-id="a3428-333">{C1BAE2D0-10DF-4334-LITIÈRE-7AA20B227A9D}</span><span class="sxs-lookup"><span data-stu-id="a3428-333">{C1BAE2D0-10DF-4334-BEDD-7AA20B227A9D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-334">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-334">Display Name</span></span></td>
<td><span data-ttu-id="a3428-335">Liens OEM</span><span class="sxs-lookup"><span data-stu-id="a3428-335">OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-336">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-336">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-337">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-337">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-338">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-338">Default Path</span></span></td>
<td><span data-ttu-id="a3428-339">Liens%ALLUSERSPROFILE%\OEM</span><span class="sxs-lookup"><span data-stu-id="a3428-339">%ALLUSERSPROFILE%\OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-340">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-340">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-341">CSIDL_COMMON_OEM_LINKS</span><span class="sxs-lookup"><span data-stu-id="a3428-341">CSIDL_COMMON_OEM_LINKS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-342">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-342">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-343">Liens OEM</span><span class="sxs-lookup"><span data-stu-id="a3428-343">OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-344">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-344">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-345">Liens%ALLUSERSPROFILE%\OEM</span><span class="sxs-lookup"><span data-stu-id="a3428-345">%ALLUSERSPROFILE%\OEM Links</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonPrograms"></span><span id="folderid_commonprograms"></span><span id="FOLDERID_COMMONPROGRAMS"></span><dl> <span data-ttu-id="a3428-346"><dt><strong>FOLDERID_CommonPrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-346"><dt><strong>FOLDERID_CommonPrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-347">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-347">GUID</span></span></td>
<td><span data-ttu-id="a3428-348">{0139D44E-6AFE-49F2-8690-3DAFCAE6FFB8}</span><span class="sxs-lookup"><span data-stu-id="a3428-348">{0139D44E-6AFE-49F2-8690-3DAFCAE6FFB8}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-349">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-349">Display Name</span></span></td>
<td><span data-ttu-id="a3428-350">Programmes</span><span class="sxs-lookup"><span data-stu-id="a3428-350">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-351">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-351">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-352">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-352">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-353">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-353">Default Path</span></span></td>
<td><span data-ttu-id="a3428-354">%ALLUSERSPROFILE%\Microsoft\Windows\Start \</span><span class="sxs-lookup"><span data-stu-id="a3428-354">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-355">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-355">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-356">CSIDL_COMMON_PROGRAMS</span><span class="sxs-lookup"><span data-stu-id="a3428-356">CSIDL_COMMON_PROGRAMS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-357">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-357">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-358">Programmes</span><span class="sxs-lookup"><span data-stu-id="a3428-358">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-359">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-359">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-360">%ALLUSERSPROFILE%\Start \</span><span class="sxs-lookup"><span data-stu-id="a3428-360">%ALLUSERSPROFILE%\Start Menu\Programs</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonStartMenu"></span><span id="folderid_commonstartmenu"></span><span id="FOLDERID_COMMONSTARTMENU"></span><dl> <span data-ttu-id="a3428-361"><dt><strong>FOLDERID_CommonStartMenu</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-361"><dt><strong>FOLDERID_CommonStartMenu</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-362">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-362">GUID</span></span></td>
<td><span data-ttu-id="a3428-363">{A4115719-D62E-491D-AA7C-E74B8BE3B067}</span><span class="sxs-lookup"><span data-stu-id="a3428-363">{A4115719-D62E-491D-AA7C-E74B8BE3B067}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-364">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-364">Display Name</span></span></td>
<td><span data-ttu-id="a3428-365">Menu Démarrer</span><span class="sxs-lookup"><span data-stu-id="a3428-365">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-366">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-366">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-367">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-367">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-368">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-368">Default Path</span></span></td>
<td><span data-ttu-id="a3428-369">Menu%ALLUSERSPROFILE%\Microsoft\Windows\Start</span><span class="sxs-lookup"><span data-stu-id="a3428-369">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-370">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-370">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-371">CSIDL_COMMON_STARTMENU</span><span class="sxs-lookup"><span data-stu-id="a3428-371">CSIDL_COMMON_STARTMENU</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-372">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-372">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-373">Menu Démarrer</span><span class="sxs-lookup"><span data-stu-id="a3428-373">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-374">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-374">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-375">Menu%ALLUSERSPROFILE%\Start</span><span class="sxs-lookup"><span data-stu-id="a3428-375">%ALLUSERSPROFILE%\Start Menu</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonStartup"></span><span id="folderid_commonstartup"></span><span id="FOLDERID_COMMONSTARTUP"></span><dl> <span data-ttu-id="a3428-376"><dt><strong>FOLDERID_CommonStartup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-376"><dt><strong>FOLDERID_CommonStartup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-377">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-377">GUID</span></span></td>
<td><span data-ttu-id="a3428-378">{82A5EA35-D9CD-47C5-9629-E15D2F714E6E}</span><span class="sxs-lookup"><span data-stu-id="a3428-378">{82A5EA35-D9CD-47C5-9629-E15D2F714E6E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-379">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-379">Display Name</span></span></td>
<td><span data-ttu-id="a3428-380">Démarrage</span><span class="sxs-lookup"><span data-stu-id="a3428-380">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-381">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-381">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-382">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-382">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-383">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-383">Default Path</span></span></td>
<td><span data-ttu-id="a3428-384">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\StartUp</span><span class="sxs-lookup"><span data-stu-id="a3428-384">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\StartUp</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-385">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-385">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-386">CSIDL_COMMON_STARTUP, CSIDL_COMMON_ALTSTARTUP</span><span class="sxs-lookup"><span data-stu-id="a3428-386">CSIDL_COMMON_STARTUP, CSIDL_COMMON_ALTSTARTUP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-387">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-387">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-388">Démarrage</span><span class="sxs-lookup"><span data-stu-id="a3428-388">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-389">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-389">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-390">%ALLUSERSPROFILE%\Start Menu\Programs\StartUp</span><span class="sxs-lookup"><span data-stu-id="a3428-390">%ALLUSERSPROFILE%\Start Menu\Programs\StartUp</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonTemplates"></span><span id="folderid_commontemplates"></span><span id="FOLDERID_COMMONTEMPLATES"></span><dl> <span data-ttu-id="a3428-391"><dt><strong>FOLDERID_CommonTemplates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-391"><dt><strong>FOLDERID_CommonTemplates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-392">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-392">GUID</span></span></td>
<td><span data-ttu-id="a3428-393">{B94237E7-57AC-4347-9151-B08C6C32D1F7}</span><span class="sxs-lookup"><span data-stu-id="a3428-393">{B94237E7-57AC-4347-9151-B08C6C32D1F7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-394">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-394">Display Name</span></span></td>
<td><span data-ttu-id="a3428-395">Modèles</span><span class="sxs-lookup"><span data-stu-id="a3428-395">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-396">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-396">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-397">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-397">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-398">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-398">Default Path</span></span></td>
<td><span data-ttu-id="a3428-399">%ALLUSERSPROFILE%\Microsoft\Windows\Templates</span><span class="sxs-lookup"><span data-stu-id="a3428-399">%ALLUSERSPROFILE%\Microsoft\Windows\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-400">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-400">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-401">CSIDL_COMMON_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="a3428-401">CSIDL_COMMON_TEMPLATES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-402">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-402">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-403">Modèles</span><span class="sxs-lookup"><span data-stu-id="a3428-403">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-404">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-404">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-405">%ALLUSERSPROFILE%\Templates</span><span class="sxs-lookup"><span data-stu-id="a3428-405">%ALLUSERSPROFILE%\Templates</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ComputerFolder"></span><span id="folderid_computerfolder"></span><span id="FOLDERID_COMPUTERFOLDER"></span><dl> <span data-ttu-id="a3428-406"><dt><strong>FOLDERID_ComputerFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-406"><dt><strong>FOLDERID_ComputerFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-407">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-407">GUID</span></span></td>
<td><span data-ttu-id="a3428-408">{0AC0837C-BBF8-452A-850D-79D08E667CA7}</span><span class="sxs-lookup"><span data-stu-id="a3428-408">{0AC0837C-BBF8-452A-850D-79D08E667CA7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-409">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-409">Display Name</span></span></td>
<td><span data-ttu-id="a3428-410">Computer</span><span class="sxs-lookup"><span data-stu-id="a3428-410">Computer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-411">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-411">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-412">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-412">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-413">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-413">Default Path</span></span></td>
<td><span data-ttu-id="a3428-414">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-414">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-415">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-415">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-416">CSIDL_DRIVES</span><span class="sxs-lookup"><span data-stu-id="a3428-416">CSIDL_DRIVES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-417">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-417">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-418">Poste de travail</span><span class="sxs-lookup"><span data-stu-id="a3428-418">My Computer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-419">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-419">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-420">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-420">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ConflictFolder"></span><span id="folderid_conflictfolder"></span><span id="FOLDERID_CONFLICTFOLDER"></span><dl> <span data-ttu-id="a3428-421"><dt><strong>FOLDERID_ConflictFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-421"><dt><strong>FOLDERID_ConflictFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-422">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-422">GUID</span></span></td>
<td><span data-ttu-id="a3428-423">{4bfefb45-347d-4006-A5be-ac0cb0567192}</span><span class="sxs-lookup"><span data-stu-id="a3428-423">{4bfefb45-347d-4006-a5be-ac0cb0567192}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-424">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-424">Display Name</span></span></td>
<td><span data-ttu-id="a3428-425">Conflits</span><span class="sxs-lookup"><span data-stu-id="a3428-425">Conflicts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-426">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-426">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-427">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-427">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-428">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-428">Default Path</span></span></td>
<td><span data-ttu-id="a3428-429">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-429">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-430">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-430">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-431">Aucun, valeur introduite dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3428-431">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-432">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-432">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-433">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="a3428-433">Not applicable.</span></span> <span data-ttu-id="a3428-434">Ce <strong>KNOWNFOLDERID</strong> fait référence au gestionnaire de synchronisation de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a3428-434">This <strong>KNOWNFOLDERID</strong> refers to the Windows Vista Synchronization Manager.</span></span> <span data-ttu-id="a3428-435">Ce n’est pas le dossier référencé par l’ancien <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>ISyncMgrConflictFolder</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a3428-435">It is not the folder referenced by the older <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>ISyncMgrConflictFolder</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-436">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-436">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-437">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-437">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ConnectionsFolder"></span><span id="folderid_connectionsfolder"></span><span id="FOLDERID_CONNECTIONSFOLDER"></span><dl> <span data-ttu-id="a3428-438"><dt><strong>FOLDERID_ConnectionsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-438"><dt><strong>FOLDERID_ConnectionsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-439">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-439">GUID</span></span></td>
<td><span data-ttu-id="a3428-440">{6F0CD92B-2E97-45D1-88FF-B0D186B8DEDD}</span><span class="sxs-lookup"><span data-stu-id="a3428-440">{6F0CD92B-2E97-45D1-88FF-B0D186B8DEDD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-441">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-441">Display Name</span></span></td>
<td><span data-ttu-id="a3428-442">Connexions réseau</span><span class="sxs-lookup"><span data-stu-id="a3428-442">Network Connections</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-443">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-443">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-444">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-444">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-445">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-445">Default Path</span></span></td>
<td><span data-ttu-id="a3428-446">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-446">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-447">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-447">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-448">CSIDL_CONNECTIONS</span><span class="sxs-lookup"><span data-stu-id="a3428-448">CSIDL_CONNECTIONS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-449">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-449">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-450">Connexions réseau</span><span class="sxs-lookup"><span data-stu-id="a3428-450">Network Connections</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-451">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-451">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-452">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-452">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Contacts"></span><span id="folderid_contacts"></span><span id="FOLDERID_CONTACTS"></span><dl> <span data-ttu-id="a3428-453"><dt><strong>FOLDERID_Contacts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-453"><dt><strong>FOLDERID_Contacts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-454">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-454">GUID</span></span></td>
<td><span data-ttu-id="a3428-455">{56784854-C6CB-462b-8169-88E350ACB882}</span><span class="sxs-lookup"><span data-stu-id="a3428-455">{56784854-C6CB-462b-8169-88E350ACB882}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-456">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-456">Display Name</span></span></td>
<td><span data-ttu-id="a3428-457">Contacts</span><span class="sxs-lookup"><span data-stu-id="a3428-457">Contacts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-458">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-458">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-459">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-459">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-460">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-460">Default Path</span></span></td>
<td><span data-ttu-id="a3428-461">%USERPROFILE%\Contacts</span><span class="sxs-lookup"><span data-stu-id="a3428-461">%USERPROFILE%\Contacts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-462">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-462">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-463">Aucun, valeur introduite dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3428-463">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-464">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-464">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-465">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-465">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-466">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-466">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-467">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-467">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ControlPanelFolder"></span><span id="folderid_controlpanelfolder"></span><span id="FOLDERID_CONTROLPANELFOLDER"></span><dl> <span data-ttu-id="a3428-468"><dt><strong>FOLDERID_ControlPanelFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-468"><dt><strong>FOLDERID_ControlPanelFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-469">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-469">GUID</span></span></td>
<td><span data-ttu-id="a3428-470">{82A74AEB-AEB4-465C-A014-D097EE346D63}</span><span class="sxs-lookup"><span data-stu-id="a3428-470">{82A74AEB-AEB4-465C-A014-D097EE346D63}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-471">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-471">Display Name</span></span></td>
<td><span data-ttu-id="a3428-472">Control panel</span><span class="sxs-lookup"><span data-stu-id="a3428-472">Control Panel</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-473">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-473">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-474">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-474">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-475">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-475">Default Path</span></span></td>
<td><span data-ttu-id="a3428-476">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-476">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-477">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-477">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-478">CSIDL_CONTROLS</span><span class="sxs-lookup"><span data-stu-id="a3428-478">CSIDL_CONTROLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-479">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-479">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-480">Control panel</span><span class="sxs-lookup"><span data-stu-id="a3428-480">Control Panel</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-481">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-481">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-482">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-482">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Cookies"></span><span id="folderid_cookies"></span><span id="FOLDERID_COOKIES"></span><dl> <span data-ttu-id="a3428-483"><dt><strong>FOLDERID_Cookies</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-483"><dt><strong>FOLDERID_Cookies</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-484">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-484">GUID</span></span></td>
<td><span data-ttu-id="a3428-485">{2B0F765D-C0E9-4171-908E-08A611B84FF6}</span><span class="sxs-lookup"><span data-stu-id="a3428-485">{2B0F765D-C0E9-4171-908E-08A611B84FF6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-486">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-486">Display Name</span></span></td>
<td><span data-ttu-id="a3428-487">Cookies</span><span class="sxs-lookup"><span data-stu-id="a3428-487">Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-488">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-488">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-489">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-489">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-490">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-490">Default Path</span></span></td>
<td><span data-ttu-id="a3428-491">%APPDATA%\Microsoft\Windows\Cookies</span><span class="sxs-lookup"><span data-stu-id="a3428-491">%APPDATA%\Microsoft\Windows\Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-492">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-492">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-493">CSIDL_COOKIES</span><span class="sxs-lookup"><span data-stu-id="a3428-493">CSIDL_COOKIES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-494">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-494">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-495">Cookies</span><span class="sxs-lookup"><span data-stu-id="a3428-495">Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-496">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-496">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-497">%USERPROFILE%\Cookies</span><span class="sxs-lookup"><span data-stu-id="a3428-497">%USERPROFILE%\Cookies</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Desktop"></span><span id="folderid_desktop"></span><span id="FOLDERID_DESKTOP"></span><dl> <span data-ttu-id="a3428-498"><dt><strong>FOLDERID_Desktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-498"><dt><strong>FOLDERID_Desktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-499">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-499">GUID</span></span></td>
<td><span data-ttu-id="a3428-500">{B4BFCC3A-DB2C-424C-B029-7FE99A87C641}</span><span class="sxs-lookup"><span data-stu-id="a3428-500">{B4BFCC3A-DB2C-424C-B029-7FE99A87C641}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-501">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-501">Display Name</span></span></td>
<td><span data-ttu-id="a3428-502">Bureau</span><span class="sxs-lookup"><span data-stu-id="a3428-502">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-503">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-503">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-504">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-504">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-505">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-505">Default Path</span></span></td>
<td><span data-ttu-id="a3428-506">%USERPROFILE%\Desktop</span><span class="sxs-lookup"><span data-stu-id="a3428-506">%USERPROFILE%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-507">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-507">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-508">CSIDL_DESKTOP, CSIDL_DESKTOPDIRECTORY</span><span class="sxs-lookup"><span data-stu-id="a3428-508">CSIDL_DESKTOP, CSIDL_DESKTOPDIRECTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-509">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-509">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-510">Bureau</span><span class="sxs-lookup"><span data-stu-id="a3428-510">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-511">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-511">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-512">%USERPROFILE%\Desktop</span><span class="sxs-lookup"><span data-stu-id="a3428-512">%USERPROFILE%\Desktop</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_DeviceMetadataStore"></span><span id="folderid_devicemetadatastore"></span><span id="FOLDERID_DEVICEMETADATASTORE"></span><dl> <span data-ttu-id="a3428-513"><dt><strong>FOLDERID_DeviceMetadataStore</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-513"><dt><strong>FOLDERID_DeviceMetadataStore</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-514">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-514">GUID</span></span></td>
<td><span data-ttu-id="a3428-515">{5CE4A5E9-E4EB-479D-B89F-130C02886155}</span><span class="sxs-lookup"><span data-stu-id="a3428-515">{5CE4A5E9-E4EB-479D-B89F-130C02886155}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-516">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-516">Display Name</span></span></td>
<td><span data-ttu-id="a3428-517">DeviceMetadataStore</span><span class="sxs-lookup"><span data-stu-id="a3428-517">DeviceMetadataStore</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-518">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-518">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-519">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-519">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-520">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-520">Default Path</span></span></td>
<td><span data-ttu-id="a3428-521">%ALLUSERSPROFILE%\Microsoft\Windows\DeviceMetadataStore</span><span class="sxs-lookup"><span data-stu-id="a3428-521">%ALLUSERSPROFILE%\Microsoft\Windows\DeviceMetadataStore</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-522">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-522">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-523">Aucun, valeur introduite dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3428-523">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-524">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-524">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-525">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-525">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-526">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-526">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-527">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-527">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Documents"></span><span id="folderid_documents"></span><span id="FOLDERID_DOCUMENTS"></span><dl> <span data-ttu-id="a3428-528"><dt><strong>FOLDERID_Documents</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-528"><dt><strong>FOLDERID_Documents</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-529">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-529">GUID</span></span></td>
<td><span data-ttu-id="a3428-530">{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</span><span class="sxs-lookup"><span data-stu-id="a3428-530">{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-531">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-531">Display Name</span></span></td>
<td><span data-ttu-id="a3428-532">Documents</span><span class="sxs-lookup"><span data-stu-id="a3428-532">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-533">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-533">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-534">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-534">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-535">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-535">Default Path</span></span></td>
<td><span data-ttu-id="a3428-536">%USERPROFILE%\Documents</span><span class="sxs-lookup"><span data-stu-id="a3428-536">%USERPROFILE%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-537">Équivalents CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-537">CSIDL Equivalents</span></span></td>
<td><span data-ttu-id="a3428-538">CSIDL_MYDOCUMENTS, CSIDL_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="a3428-538">CSIDL_MYDOCUMENTS, CSIDL_PERSONAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-539">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-539">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-540">Mes documents</span><span class="sxs-lookup"><span data-stu-id="a3428-540">My Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-541">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-541">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-542">Documents%USERPROFILE%\My</span><span class="sxs-lookup"><span data-stu-id="a3428-542">%USERPROFILE%\My Documents</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_DocumentsLibrary"></span><span id="folderid_documentslibrary"></span><span id="FOLDERID_DOCUMENTSLIBRARY"></span><dl> <span data-ttu-id="a3428-543"><dt><strong>FOLDERID_DocumentsLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-543"><dt><strong>FOLDERID_DocumentsLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-544">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-544">GUID</span></span></td>
<td><span data-ttu-id="a3428-545">{7B0DB17D-9CD2-4A93-9733-46CC89022E7C}</span><span class="sxs-lookup"><span data-stu-id="a3428-545">{7B0DB17D-9CD2-4A93-9733-46CC89022E7C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-546">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-546">Display Name</span></span></td>
<td><span data-ttu-id="a3428-547">Documents</span><span class="sxs-lookup"><span data-stu-id="a3428-547">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-548">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-548">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-549">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-549">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-550">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-550">Default Path</span></span></td>
<td><span data-ttu-id="a3428-551">%APPDATA%\Microsoft\Windows\Libraries\Documents.library-ms</span><span class="sxs-lookup"><span data-stu-id="a3428-551">%APPDATA%\Microsoft\Windows\Libraries\Documents.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-552">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-552">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-553">Aucun, valeur introduite dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3428-553">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-554">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-554">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-555">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-555">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-556">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-556">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-557">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-557">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Downloads"></span><span id="folderid_downloads"></span><span id="FOLDERID_DOWNLOADS"></span><dl> <span data-ttu-id="a3428-558"><dt><strong>FOLDERID_Downloads</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-558"><dt><strong>FOLDERID_Downloads</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-559">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-559">GUID</span></span></td>
<td><span data-ttu-id="a3428-560">{374DE290-123F-4565-9164-39C4925E467B}</span><span class="sxs-lookup"><span data-stu-id="a3428-560">{374DE290-123F-4565-9164-39C4925E467B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-561">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-561">Display Name</span></span></td>
<td><span data-ttu-id="a3428-562">Téléchargements</span><span class="sxs-lookup"><span data-stu-id="a3428-562">Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-563">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-563">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-564">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-564">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-565">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-565">Default Path</span></span></td>
<td><span data-ttu-id="a3428-566">%USERPROFILE%\Downloads</span><span class="sxs-lookup"><span data-stu-id="a3428-566">%USERPROFILE%\Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-567">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-567">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-568">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-568">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-569">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-569">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-570">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-570">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-571">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-571">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-572">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-572">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Favorites"></span><span id="folderid_favorites"></span><span id="FOLDERID_FAVORITES"></span><dl> <span data-ttu-id="a3428-573"><dt><strong>FOLDERID_Favorites</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-573"><dt><strong>FOLDERID_Favorites</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-574">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-574">GUID</span></span></td>
<td><span data-ttu-id="a3428-575">{1777F761-68AD-4D8A-87BD-30B759FA33DD}</span><span class="sxs-lookup"><span data-stu-id="a3428-575">{1777F761-68AD-4D8A-87BD-30B759FA33DD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-576">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-576">Display Name</span></span></td>
<td><span data-ttu-id="a3428-577">Favoris</span><span class="sxs-lookup"><span data-stu-id="a3428-577">Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-578">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-578">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-579">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-579">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-580">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-580">Default Path</span></span></td>
<td><span data-ttu-id="a3428-581">%USERPROFILE%\Favorites</span><span class="sxs-lookup"><span data-stu-id="a3428-581">%USERPROFILE%\Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-582">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-582">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-583">CSIDL_FAVORITES, CSIDL_COMMON_FAVORITES</span><span class="sxs-lookup"><span data-stu-id="a3428-583">CSIDL_FAVORITES, CSIDL_COMMON_FAVORITES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-584">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-584">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-585">Favoris</span><span class="sxs-lookup"><span data-stu-id="a3428-585">Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-586">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-586">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-587">%USERPROFILE%\Favorites</span><span class="sxs-lookup"><span data-stu-id="a3428-587">%USERPROFILE%\Favorites</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Fonts"></span><span id="folderid_fonts"></span><span id="FOLDERID_FONTS"></span><dl> <span data-ttu-id="a3428-588"><dt><strong>FOLDERID_Fonts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-588"><dt><strong>FOLDERID_Fonts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-589">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-589">GUID</span></span></td>
<td><span data-ttu-id="a3428-590">{FD228CB7-AE11-4AE3-864C-16F3910AB8FE}</span><span class="sxs-lookup"><span data-stu-id="a3428-590">{FD228CB7-AE11-4AE3-864C-16F3910AB8FE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-591">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-591">Display Name</span></span></td>
<td><span data-ttu-id="a3428-592">Polices</span><span class="sxs-lookup"><span data-stu-id="a3428-592">Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-593">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-593">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-594">FIXED</span><span class="sxs-lookup"><span data-stu-id="a3428-594">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-595">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-595">Default Path</span></span></td>
<td><span data-ttu-id="a3428-596">%windir%\Fonts</span><span class="sxs-lookup"><span data-stu-id="a3428-596">%windir%\Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-597">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-597">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-598">CSIDL_FONTS</span><span class="sxs-lookup"><span data-stu-id="a3428-598">CSIDL_FONTS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-599">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-599">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-600">Polices</span><span class="sxs-lookup"><span data-stu-id="a3428-600">Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-601">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-601">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-602">%windir%\Fonts</span><span class="sxs-lookup"><span data-stu-id="a3428-602">%windir%\Fonts</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Games"></span><span id="folderid_games"></span><span id="FOLDERID_GAMES"></span><dl> <span data-ttu-id="a3428-603"><dt><strong>FOLDERID_Games</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-603"><dt><strong>FOLDERID_Games</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="a3428-604">Ce FOLDERID est déconseillé dans Windows 10, version 1803 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a3428-604">This FOLDERID is deprecated in Windows 10, version 1803 and later versions.</span></span> <span data-ttu-id="a3428-605">Dans ces versions, elle retourne <strong>0x80070057-E_INVALIDARG</strong>
</span><span class="sxs-lookup"><span data-stu-id="a3428-605">In these versions, it returns <strong>0x80070057 - E_INVALIDARG</strong>
</span></span></blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-606">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-606">GUID</span></span></td>
<td><span data-ttu-id="a3428-607">{CAC52C1A-B53D-4edc-92D7-6B2E8AC19434}</span><span class="sxs-lookup"><span data-stu-id="a3428-607">{CAC52C1A-B53D-4edc-92D7-6B2E8AC19434}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-608">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-608">Display Name</span></span></td>
<td><span data-ttu-id="a3428-609">Jeux</span><span class="sxs-lookup"><span data-stu-id="a3428-609">Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-610">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-610">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-611">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-611">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-612">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-612">Default Path</span></span></td>
<td><span data-ttu-id="a3428-613">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-613">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-614">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-614">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-615">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-615">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-616">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-616">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-617">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-617">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-618">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-618">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-619">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-619">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_GameTasks"></span><span id="folderid_gametasks"></span><span id="FOLDERID_GAMETASKS"></span><dl> <span data-ttu-id="a3428-620"><dt><strong>FOLDERID_GameTasks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-620"><dt><strong>FOLDERID_GameTasks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-621">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-621">GUID</span></span></td>
<td><span data-ttu-id="a3428-622">{054FAE61-4DD8-4787-80B6-090220C4B700}</span><span class="sxs-lookup"><span data-stu-id="a3428-622">{054FAE61-4DD8-4787-80B6-090220C4B700}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-623">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-623">Display Name</span></span></td>
<td><span data-ttu-id="a3428-624">GameExplorer</span><span class="sxs-lookup"><span data-stu-id="a3428-624">GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-625">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-625">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-626">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-626">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-627">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-627">Default Path</span></span></td>
<td><span data-ttu-id="a3428-628">%LOCALAPPDATA%\Microsoft\Windows\GameExplorer</span><span class="sxs-lookup"><span data-stu-id="a3428-628">%LOCALAPPDATA%\Microsoft\Windows\GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-629">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-629">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-630">Aucun, valeur introduite dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3428-630">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-631">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-631">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-632">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-632">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-633">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-633">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-634">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-634">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_History"></span><span id="folderid_history"></span><span id="FOLDERID_HISTORY"></span><dl> <span data-ttu-id="a3428-635"><dt><strong>FOLDERID_History</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-635"><dt><strong>FOLDERID_History</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-636">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-636">GUID</span></span></td>
<td><span data-ttu-id="a3428-637">{D9DC8A3B-B784-432E-A781-5A1130A75963}</span><span class="sxs-lookup"><span data-stu-id="a3428-637">{D9DC8A3B-B784-432E-A781-5A1130A75963}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-638">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-638">Display Name</span></span></td>
<td><span data-ttu-id="a3428-639">Historique</span><span class="sxs-lookup"><span data-stu-id="a3428-639">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-640">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-640">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-641">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-641">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-642">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-642">Default Path</span></span></td>
<td><span data-ttu-id="a3428-643">%LOCALAPPDATA%\Microsoft\Windows\History</span><span class="sxs-lookup"><span data-stu-id="a3428-643">%LOCALAPPDATA%\Microsoft\Windows\History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-644">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-644">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-645">CSIDL_HISTORY</span><span class="sxs-lookup"><span data-stu-id="a3428-645">CSIDL_HISTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-646">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-646">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-647">Historique</span><span class="sxs-lookup"><span data-stu-id="a3428-647">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-648">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-648">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-649">%USERPROFILE%\Local Settings\History</span><span class="sxs-lookup"><span data-stu-id="a3428-649">%USERPROFILE%\Local Settings\History</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_HomeGroup"></span><span id="folderid_homegroup"></span><span id="FOLDERID_HOMEGROUP"></span><dl> <span data-ttu-id="a3428-650"><dt><strong>FOLDERID_HomeGroup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-650"><dt><strong>FOLDERID_HomeGroup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-651">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-651">GUID</span></span></td>
<td><span data-ttu-id="a3428-652">{52528A6B-B9E3-4ADD-B60D-588C2DBA842D}</span><span class="sxs-lookup"><span data-stu-id="a3428-652">{52528A6B-B9E3-4ADD-B60D-588C2DBA842D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-653">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-653">Display Name</span></span></td>
<td><span data-ttu-id="a3428-654">Groupement résidentiel</span><span class="sxs-lookup"><span data-stu-id="a3428-654">Homegroup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-655">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-655">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-656">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-656">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-657">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-657">Default Path</span></span></td>
<td><span data-ttu-id="a3428-658">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-658">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-659">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-659">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-660">Aucun, valeur introduite dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3428-660">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-661">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-661">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-662">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-662">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-663">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-663">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-664">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-664">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_HomeGroupCurrentUser"></span><span id="folderid_homegroupcurrentuser"></span><span id="FOLDERID_HOMEGROUPCURRENTUSER"></span><dl> <span data-ttu-id="a3428-665"><dt><strong>FOLDERID_HomeGroupCurrentUser</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-665"><dt><strong>FOLDERID_HomeGroupCurrentUser</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-666">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-666">GUID</span></span></td>
<td><span data-ttu-id="a3428-667">{9B74B6A3-0DFD-4f11-9E78-5F7800F2E772}</span><span class="sxs-lookup"><span data-stu-id="a3428-667">{9B74B6A3-0DFD-4f11-9E78-5F7800F2E772}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-668">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-668">Display Name</span></span></td>
<td><span data-ttu-id="a3428-669">Nom d’utilisateur de l’utilisateur (% USERNAME%)</span><span class="sxs-lookup"><span data-stu-id="a3428-669">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-670">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-670">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-671">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-671">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-672">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-672">Default Path</span></span></td>
<td><span data-ttu-id="a3428-673">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-673">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-674">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-674">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-675">Aucun, valeur introduite dans Windows 8</span><span class="sxs-lookup"><span data-stu-id="a3428-675">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-676">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-676">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-677">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-677">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-678">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-678">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-679">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-679">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ImplicitAppShortcuts"></span><span id="folderid_implicitappshortcuts"></span><span id="FOLDERID_IMPLICITAPPSHORTCUTS"></span><dl> <span data-ttu-id="a3428-680"><dt><strong>FOLDERID_ImplicitAppShortcuts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-680"><dt><strong>FOLDERID_ImplicitAppShortcuts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-681">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-681">GUID</span></span></td>
<td><span data-ttu-id="a3428-682">{BCB5256F-79F6-4CEE-B725-DC34E402FD46}</span><span class="sxs-lookup"><span data-stu-id="a3428-682">{BCB5256F-79F6-4CEE-B725-DC34E402FD46}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-683">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-683">Display Name</span></span></td>
<td><span data-ttu-id="a3428-684">ImplicitAppShortcuts</span><span class="sxs-lookup"><span data-stu-id="a3428-684">ImplicitAppShortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-685">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-685">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-686">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-686">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-687">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-687">Default Path</span></span></td>
<td><span data-ttu-id="a3428-688">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User Pinned\ImplicitAppShortcuts</span><span class="sxs-lookup"><span data-stu-id="a3428-688">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User Pinned\ImplicitAppShortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-689">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-689">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-690">Aucun, valeur introduite dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3428-690">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-691">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-691">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-692">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-692">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-693">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-693">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-694">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-694">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_InternetCache"></span><span id="folderid_internetcache"></span><span id="FOLDERID_INTERNETCACHE"></span><dl> <span data-ttu-id="a3428-695"><dt><strong>FOLDERID_InternetCache</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-695"><dt><strong>FOLDERID_InternetCache</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-696">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-696">GUID</span></span></td>
<td><span data-ttu-id="a3428-697">{352481E8-33BE-4251-BA85-6007CAEDCF9D}</span><span class="sxs-lookup"><span data-stu-id="a3428-697">{352481E8-33BE-4251-BA85-6007CAEDCF9D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-698">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-698">Display Name</span></span></td>
<td><span data-ttu-id="a3428-699">Fichiers Internet temporaires</span><span class="sxs-lookup"><span data-stu-id="a3428-699">Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-700">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-700">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-701">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-701">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-702">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-702">Default Path</span></span></td>
<td><span data-ttu-id="a3428-703">Fichiers Internet%LOCALAPPDATA%\Microsoft\Windows\Temporary</span><span class="sxs-lookup"><span data-stu-id="a3428-703">%LOCALAPPDATA%\Microsoft\Windows\Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-704">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-704">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-705">CSIDL_INTERNET_CACHE</span><span class="sxs-lookup"><span data-stu-id="a3428-705">CSIDL_INTERNET_CACHE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-706">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-706">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-707">Fichiers Internet temporaires</span><span class="sxs-lookup"><span data-stu-id="a3428-707">Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-708">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-708">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-709">%USERPROFILE%\Local Settings\Temporary Internet Files</span><span class="sxs-lookup"><span data-stu-id="a3428-709">%USERPROFILE%\Local Settings\Temporary Internet Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_InternetFolder"></span><span id="folderid_internetfolder"></span><span id="FOLDERID_INTERNETFOLDER"></span><dl> <span data-ttu-id="a3428-710"><dt><strong>FOLDERID_InternetFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-710"><dt><strong>FOLDERID_InternetFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-711">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-711">GUID</span></span></td>
<td><span data-ttu-id="a3428-712">{4D9F7874-4E0C-4904-967B-40B0D20C3E4B}</span><span class="sxs-lookup"><span data-stu-id="a3428-712">{4D9F7874-4E0C-4904-967B-40B0D20C3E4B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-713">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-713">Display Name</span></span></td>
<td><span data-ttu-id="a3428-714">Internet</span><span class="sxs-lookup"><span data-stu-id="a3428-714">The Internet</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-715">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-715">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-716">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-716">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-717">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-717">Default Path</span></span></td>
<td><span data-ttu-id="a3428-718">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-718">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-719">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-719">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-720">CSIDL_INTERNET</span><span class="sxs-lookup"><span data-stu-id="a3428-720">CSIDL_INTERNET</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-721">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-721">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-722">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="a3428-722">Internet Explorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-723">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-723">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-724">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-724">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Libraries"></span><span id="folderid_libraries"></span><span id="FOLDERID_LIBRARIES"></span><dl> <span data-ttu-id="a3428-725"><dt><strong>FOLDERID_Libraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-725"><dt><strong>FOLDERID_Libraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-726">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-726">GUID</span></span></td>
<td><span data-ttu-id="a3428-727">{1B3EA5DC-B587-4786-B4EF-BD1DC332AEAE}</span><span class="sxs-lookup"><span data-stu-id="a3428-727">{1B3EA5DC-B587-4786-B4EF-BD1DC332AEAE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-728">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-728">Display Name</span></span></td>
<td><span data-ttu-id="a3428-729">Bibliothèques</span><span class="sxs-lookup"><span data-stu-id="a3428-729">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-730">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-730">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-731">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-731">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-732">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-732">Default Path</span></span></td>
<td><span data-ttu-id="a3428-733">%APPDATA%\Microsoft\Windows\Libraries</span><span class="sxs-lookup"><span data-stu-id="a3428-733">%APPDATA%\Microsoft\Windows\Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-734">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-734">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-735">Aucun, valeur introduite dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3428-735">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-736">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-736">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-737">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-737">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-738">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-738">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-739">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-739">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Links"></span><span id="folderid_links"></span><span id="FOLDERID_LINKS"></span><dl> <span data-ttu-id="a3428-740"><dt><strong>FOLDERID_Links</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-740"><dt><strong>FOLDERID_Links</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-741">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-741">GUID</span></span></td>
<td><span data-ttu-id="a3428-742">{bfb9d5e0-c6a9-404c-b2b2-ae6db6af4968}</span><span class="sxs-lookup"><span data-stu-id="a3428-742">{bfb9d5e0-c6a9-404c-b2b2-ae6db6af4968}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-743">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-743">Display Name</span></span></td>
<td><span data-ttu-id="a3428-744">Liens</span><span class="sxs-lookup"><span data-stu-id="a3428-744">Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-745">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-745">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-746">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-746">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-747">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-747">Default Path</span></span></td>
<td><span data-ttu-id="a3428-748">%USERPROFILE%\Links</span><span class="sxs-lookup"><span data-stu-id="a3428-748">%USERPROFILE%\Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-749">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-749">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-750">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-750">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-751">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-751">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-752">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-752">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-753">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-753">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-754">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-754">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_LocalAppData"></span><span id="folderid_localappdata"></span><span id="FOLDERID_LOCALAPPDATA"></span><dl> <span data-ttu-id="a3428-755"><dt><strong>FOLDERID_LocalAppData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-755"><dt><strong>FOLDERID_LocalAppData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-756">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-756">GUID</span></span></td>
<td><span data-ttu-id="a3428-757">{F1B32785-6FBA-4FCF-9D55-7B8E7F157091}</span><span class="sxs-lookup"><span data-stu-id="a3428-757">{F1B32785-6FBA-4FCF-9D55-7B8E7F157091}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-758">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-758">Display Name</span></span></td>
<td><span data-ttu-id="a3428-759">Local</span><span class="sxs-lookup"><span data-stu-id="a3428-759">Local</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-760">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-760">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-761">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-761">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-762">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-762">Default Path</span></span></td>
<td><span data-ttu-id="a3428-763">% LOCALAPPDATA% (%USERPROFILE%\AppData\Local)</span><span class="sxs-lookup"><span data-stu-id="a3428-763">%LOCALAPPDATA% (%USERPROFILE%\AppData\Local)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-764">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-764">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-765">CSIDL_LOCAL_APPDATA</span><span class="sxs-lookup"><span data-stu-id="a3428-765">CSIDL_LOCAL_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-766">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-766">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-767">Données d'application</span><span class="sxs-lookup"><span data-stu-id="a3428-767">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-768">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-768">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-769">%USERPROFILE%\Local Settings\Application Data</span><span class="sxs-lookup"><span data-stu-id="a3428-769">%USERPROFILE%\Local Settings\Application Data</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_LocalAppDataLow"></span><span id="folderid_localappdatalow"></span><span id="FOLDERID_LOCALAPPDATALOW"></span><dl> <span data-ttu-id="a3428-770"><dt><strong>FOLDERID_LocalAppDataLow</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-770"><dt><strong>FOLDERID_LocalAppDataLow</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-771">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-771">GUID</span></span></td>
<td><span data-ttu-id="a3428-772">{A520A1A4-1780-4FF6-BD18-167343C5AF16}</span><span class="sxs-lookup"><span data-stu-id="a3428-772">{A520A1A4-1780-4FF6-BD18-167343C5AF16}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-773">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-773">Display Name</span></span></td>
<td><span data-ttu-id="a3428-774">LocalLow</span><span class="sxs-lookup"><span data-stu-id="a3428-774">LocalLow</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-775">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-775">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-776">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-776">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-777">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-777">Default Path</span></span></td>
<td><span data-ttu-id="a3428-778">%USERPROFILE%\AppData\LocalLow</span><span class="sxs-lookup"><span data-stu-id="a3428-778">%USERPROFILE%\AppData\LocalLow</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-779">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-779">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-780">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-780">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-781">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-781">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-782">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-782">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-783">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-783">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-784">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-784">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_LocalizedResourcesDir"></span><span id="folderid_localizedresourcesdir"></span><span id="FOLDERID_LOCALIZEDRESOURCESDIR"></span><dl> <span data-ttu-id="a3428-785"><dt><strong>FOLDERID_LocalizedResourcesDir</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-785"><dt><strong>FOLDERID_LocalizedResourcesDir</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-786">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-786">GUID</span></span></td>
<td><span data-ttu-id="a3428-787">{2A00375E-224C-49DE-B8D1-440DF7EF3DDC}</span><span class="sxs-lookup"><span data-stu-id="a3428-787">{2A00375E-224C-49DE-B8D1-440DF7EF3DDC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-788">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-788">Display Name</span></span></td>
<td><span data-ttu-id="a3428-789">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-789">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-790">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-790">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-791">FIXED</span><span class="sxs-lookup"><span data-stu-id="a3428-791">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-792">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-792">Default Path</span></span></td>
<td><span data-ttu-id="a3428-793">%windir%\resources\0409 (page de codes)</span><span class="sxs-lookup"><span data-stu-id="a3428-793">%windir%\resources\0409 (code page)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-794">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-794">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-795">CSIDL_RESOURCES_LOCALIZED</span><span class="sxs-lookup"><span data-stu-id="a3428-795">CSIDL_RESOURCES_LOCALIZED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-796">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-796">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-797">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-797">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-798">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-798">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-799">%windir%\resources\0409 (page de codes)</span><span class="sxs-lookup"><span data-stu-id="a3428-799">%windir%\resources\0409 (code page)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Music"></span><span id="folderid_music"></span><span id="FOLDERID_MUSIC"></span><dl> <span data-ttu-id="a3428-800"><dt><strong>FOLDERID_Music</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-800"><dt><strong>FOLDERID_Music</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-801">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-801">GUID</span></span></td>
<td><span data-ttu-id="a3428-802">{4BD8D571-6D19-48D3-BE97-422220080E43}</span><span class="sxs-lookup"><span data-stu-id="a3428-802">{4BD8D571-6D19-48D3-BE97-422220080E43}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-803">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-803">Display Name</span></span></td>
<td><span data-ttu-id="a3428-804">Musique</span><span class="sxs-lookup"><span data-stu-id="a3428-804">Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-805">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-805">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-806">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-806">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-807">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-807">Default Path</span></span></td>
<td><span data-ttu-id="a3428-808">%USERPROFILE%\Music</span><span class="sxs-lookup"><span data-stu-id="a3428-808">%USERPROFILE%\Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-809">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-809">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-810">CSIDL_MYMUSIC</span><span class="sxs-lookup"><span data-stu-id="a3428-810">CSIDL_MYMUSIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-811">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-811">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-812">Ma musique</span><span class="sxs-lookup"><span data-stu-id="a3428-812">My Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-813">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-813">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-814">%USERPROFILE%\My Documents\mes musique</span><span class="sxs-lookup"><span data-stu-id="a3428-814">%USERPROFILE%\My Documents\My Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_MusicLibrary"></span><span id="folderid_musiclibrary"></span><span id="FOLDERID_MUSICLIBRARY"></span><dl> <span data-ttu-id="a3428-815"><dt><strong>FOLDERID_MusicLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-815"><dt><strong>FOLDERID_MusicLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-816">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-816">GUID</span></span></td>
<td><span data-ttu-id="a3428-817">{2112AB0A-C86A-4FFE-A368-0DE96E47012E}</span><span class="sxs-lookup"><span data-stu-id="a3428-817">{2112AB0A-C86A-4FFE-A368-0DE96E47012E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-818">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-818">Display Name</span></span></td>
<td><span data-ttu-id="a3428-819">Musique</span><span class="sxs-lookup"><span data-stu-id="a3428-819">Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-820">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-820">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-821">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-821">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-822">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-822">Default Path</span></span></td>
<td><span data-ttu-id="a3428-823">%APPDATA%\Microsoft\Windows\Libraries\Music.library-ms</span><span class="sxs-lookup"><span data-stu-id="a3428-823">%APPDATA%\Microsoft\Windows\Libraries\Music.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-824">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-824">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-825">Aucun, valeur introduite dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3428-825">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-826">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-826">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-827">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-827">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-828">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-828">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-829">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-829">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_NetHood"></span><span id="folderid_nethood"></span><span id="FOLDERID_NETHOOD"></span><dl> <span data-ttu-id="a3428-830"><dt><strong>FOLDERID_NetHood</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-830"><dt><strong>FOLDERID_NetHood</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-831">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-831">GUID</span></span></td>
<td><span data-ttu-id="a3428-832">{C5ABBF53-E17F-4121-8900-86626FC2C973}</span><span class="sxs-lookup"><span data-stu-id="a3428-832">{C5ABBF53-E17F-4121-8900-86626FC2C973}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-833">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-833">Display Name</span></span></td>
<td><span data-ttu-id="a3428-834">Raccourcis réseau</span><span class="sxs-lookup"><span data-stu-id="a3428-834">Network Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-835">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-835">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-836">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-836">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-837">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-837">Default Path</span></span></td>
<td><span data-ttu-id="a3428-838">%APPDATA%\Microsoft\Windows\Network les raccourcis</span><span class="sxs-lookup"><span data-stu-id="a3428-838">%APPDATA%\Microsoft\Windows\Network Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-839">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-839">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-840">CSIDL_NETHOOD</span><span class="sxs-lookup"><span data-stu-id="a3428-840">CSIDL_NETHOOD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-841">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-841">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-842">Nethotte</span><span class="sxs-lookup"><span data-stu-id="a3428-842">NetHood</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-843">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-843">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-844">%USERPROFILE%\NetHood</span><span class="sxs-lookup"><span data-stu-id="a3428-844">%USERPROFILE%\NetHood</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_NetworkFolder"></span><span id="folderid_networkfolder"></span><span id="FOLDERID_NETWORKFOLDER"></span><dl> <span data-ttu-id="a3428-845"><dt><strong>FOLDERID_NetworkFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-845"><dt><strong>FOLDERID_NetworkFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-846">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-846">GUID</span></span></td>
<td><span data-ttu-id="a3428-847">{D20BEEC4-5CA8-4905-AE3B-BF251EA09B53}</span><span class="sxs-lookup"><span data-stu-id="a3428-847">{D20BEEC4-5CA8-4905-AE3B-BF251EA09B53}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-848">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-848">Display Name</span></span></td>
<td><span data-ttu-id="a3428-849">Réseau</span><span class="sxs-lookup"><span data-stu-id="a3428-849">Network</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-850">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-850">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-851">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-851">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-852">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-852">Default Path</span></span></td>
<td><span data-ttu-id="a3428-853">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-853">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-854">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-854">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-855">CSIDL_NETWORK, CSIDL_COMPUTERSNEARME</span><span class="sxs-lookup"><span data-stu-id="a3428-855">CSIDL_NETWORK, CSIDL_COMPUTERSNEARME</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-856">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-856">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-857">Favoris réseau</span><span class="sxs-lookup"><span data-stu-id="a3428-857">My Network Places</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-858">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-858">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-859">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-859">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Objects3D"></span><span id="folderid_objects3d"></span><span id="FOLDERID_OBJECTS3D"></span><dl> <span data-ttu-id="a3428-860"><dt><strong>FOLDERID_Objects3D</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-860"><dt><strong>FOLDERID_Objects3D</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-861">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-861">GUID</span></span></td>
<td><span data-ttu-id="a3428-862">{31C0DD25-9439-4F12-BF41-7FF4EDA38722}</span><span class="sxs-lookup"><span data-stu-id="a3428-862">{31C0DD25-9439-4F12-BF41-7FF4EDA38722}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-863">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-863">Display Name</span></span></td>
<td><span data-ttu-id="a3428-864">Objets 3D</span><span class="sxs-lookup"><span data-stu-id="a3428-864">3D Objects</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-865">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-865">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-866">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-866">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-867">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-867">Default Path</span></span></td>
<td><span data-ttu-id="a3428-868">Objets%USERPROFILE%\3D</span><span class="sxs-lookup"><span data-stu-id="a3428-868">%USERPROFILE%\3D Objects</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-869">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-869">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-870">Aucun, valeur introduite dans Windows 10, version 1703</span><span class="sxs-lookup"><span data-stu-id="a3428-870">None, value introduced in Windows 10, version 1703</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-871">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-871">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-872">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-872">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-873">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-873">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-874">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-874">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_OriginalImages"></span><span id="folderid_originalimages"></span><span id="FOLDERID_ORIGINALIMAGES"></span><dl> <span data-ttu-id="a3428-875"><dt><strong>FOLDERID_OriginalImages</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-875"><dt><strong>FOLDERID_OriginalImages</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-876">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-876">GUID</span></span></td>
<td><span data-ttu-id="a3428-877">{2C36C0AA-5812-4b87-BFD0-4CD0DFB19B39}</span><span class="sxs-lookup"><span data-stu-id="a3428-877">{2C36C0AA-5812-4b87-BFD0-4CD0DFB19B39}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-878">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-878">Display Name</span></span></td>
<td><span data-ttu-id="a3428-879">Images d’origine</span><span class="sxs-lookup"><span data-stu-id="a3428-879">Original Images</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-880">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-880">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-881">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-881">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-882">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-882">Default Path</span></span></td>
<td><span data-ttu-id="a3428-883">Images%LOCALAPPDATA%\Microsoft\Windows photo Gallery\Original</span><span class="sxs-lookup"><span data-stu-id="a3428-883">%LOCALAPPDATA%\Microsoft\Windows Photo Gallery\Original Images</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-884">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-884">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-885">Aucun, valeur introduite dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3428-885">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-886">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-886">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-887">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-887">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-888">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-888">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-889">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-889">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PhotoAlbums"></span><span id="folderid_photoalbums"></span><span id="FOLDERID_PHOTOALBUMS"></span><dl> <span data-ttu-id="a3428-890"><dt><strong>FOLDERID_PhotoAlbums</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-890"><dt><strong>FOLDERID_PhotoAlbums</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-891">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-891">GUID</span></span></td>
<td><span data-ttu-id="a3428-892">{69D2CF90-FC33-4FB7-9A0C-EBB0F0FCB43C}</span><span class="sxs-lookup"><span data-stu-id="a3428-892">{69D2CF90-FC33-4FB7-9A0C-EBB0F0FCB43C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-893">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-893">Display Name</span></span></td>
<td><span data-ttu-id="a3428-894">Diaporamas</span><span class="sxs-lookup"><span data-stu-id="a3428-894">Slide Shows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-895">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-895">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-896">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-896">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-897">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-897">Default Path</span></span></td>
<td><span data-ttu-id="a3428-898">%USERPROFILE%\Pictures\Slide affiche</span><span class="sxs-lookup"><span data-stu-id="a3428-898">%USERPROFILE%\Pictures\Slide Shows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-899">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-899">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-900">Aucun, valeur introduite dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3428-900">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-901">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-901">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-902">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-902">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-903">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-903">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-904">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-904">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PicturesLibrary"></span><span id="folderid_pictureslibrary"></span><span id="FOLDERID_PICTURESLIBRARY"></span><dl> <span data-ttu-id="a3428-905"><dt><strong>FOLDERID_PicturesLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-905"><dt><strong>FOLDERID_PicturesLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-906">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-906">GUID</span></span></td>
<td><span data-ttu-id="a3428-907">{A990AE9F-A03B-4E80-94BC-9912D7504104}</span><span class="sxs-lookup"><span data-stu-id="a3428-907">{A990AE9F-A03B-4E80-94BC-9912D7504104}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-908">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-908">Display Name</span></span></td>
<td><span data-ttu-id="a3428-909">Images</span><span class="sxs-lookup"><span data-stu-id="a3428-909">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-910">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-910">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-911">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-911">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-912">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-912">Default Path</span></span></td>
<td><span data-ttu-id="a3428-913">%APPDATA%\Microsoft\Windows\Libraries\Pictures.library-ms</span><span class="sxs-lookup"><span data-stu-id="a3428-913">%APPDATA%\Microsoft\Windows\Libraries\Pictures.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-914">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-914">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-915">Aucun, valeur introduite dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3428-915">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-916">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-916">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-917">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-917">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-918">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-918">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-919">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-919">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Pictures"></span><span id="folderid_pictures"></span><span id="FOLDERID_PICTURES"></span><dl> <span data-ttu-id="a3428-920"><dt><strong>FOLDERID_Pictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-920"><dt><strong>FOLDERID_Pictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-921">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-921">GUID</span></span></td>
<td><span data-ttu-id="a3428-922">{33E28130-4E1E-4676-835A-98395C3BC3BB}</span><span class="sxs-lookup"><span data-stu-id="a3428-922">{33E28130-4E1E-4676-835A-98395C3BC3BB}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-923">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-923">Display Name</span></span></td>
<td><span data-ttu-id="a3428-924">Images</span><span class="sxs-lookup"><span data-stu-id="a3428-924">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-925">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-925">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-926">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-926">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-927">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-927">Default Path</span></span></td>
<td><span data-ttu-id="a3428-928">%USERPROFILE%\Pictures</span><span class="sxs-lookup"><span data-stu-id="a3428-928">%USERPROFILE%\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-929">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-929">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-930">CSIDL_MYPICTURES</span><span class="sxs-lookup"><span data-stu-id="a3428-930">CSIDL_MYPICTURES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-931">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-931">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-932">Mes images</span><span class="sxs-lookup"><span data-stu-id="a3428-932">My Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-933">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-933">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-934">%USERPROFILE%\My Documents\mes images</span><span class="sxs-lookup"><span data-stu-id="a3428-934">%USERPROFILE%\My Documents\My Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Playlists"></span><span id="folderid_playlists"></span><span id="FOLDERID_PLAYLISTS"></span><dl> <span data-ttu-id="a3428-935"><dt><strong>FOLDERID_Playlists</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-935"><dt><strong>FOLDERID_Playlists</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-936">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-936">GUID</span></span></td>
<td><span data-ttu-id="a3428-937">{DE92C1C7-837F-4F69-A3BB-86E631204A23}</span><span class="sxs-lookup"><span data-stu-id="a3428-937">{DE92C1C7-837F-4F69-A3BB-86E631204A23}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-938">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-938">Display Name</span></span></td>
<td><span data-ttu-id="a3428-939">Sélections</span><span class="sxs-lookup"><span data-stu-id="a3428-939">Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-940">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-940">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-941">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-941">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-942">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-942">Default Path</span></span></td>
<td><span data-ttu-id="a3428-943">%USERPROFILE%\Music\Playlists</span><span class="sxs-lookup"><span data-stu-id="a3428-943">%USERPROFILE%\Music\Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-944">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-944">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-945">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-945">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-946">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-946">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-947">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-947">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-948">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-948">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-949">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-949">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PrintersFolder"></span><span id="folderid_printersfolder"></span><span id="FOLDERID_PRINTERSFOLDER"></span><dl> <span data-ttu-id="a3428-950"><dt><strong>FOLDERID_PrintersFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-950"><dt><strong>FOLDERID_PrintersFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-951">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-951">GUID</span></span></td>
<td><span data-ttu-id="a3428-952">{76FC4E2D-D6AD-4519-A663-37BD56068185}</span><span class="sxs-lookup"><span data-stu-id="a3428-952">{76FC4E2D-D6AD-4519-A663-37BD56068185}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-953">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-953">Display Name</span></span></td>
<td><span data-ttu-id="a3428-954">Imprimantes</span><span class="sxs-lookup"><span data-stu-id="a3428-954">Printers</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-955">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-955">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-956">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-956">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-957">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-957">Default Path</span></span></td>
<td><span data-ttu-id="a3428-958">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-958">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-959">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-959">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-960">CSIDL_PRINTERS</span><span class="sxs-lookup"><span data-stu-id="a3428-960">CSIDL_PRINTERS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-961">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-961">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-962">Imprimantes et télécopieurs</span><span class="sxs-lookup"><span data-stu-id="a3428-962">Printers and Faxes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-963">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-963">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-964">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-964">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PrintHood"></span><span id="folderid_printhood"></span><span id="FOLDERID_PRINTHOOD"></span><dl> <span data-ttu-id="a3428-965"><dt><strong>FOLDERID_PrintHood</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-965"><dt><strong>FOLDERID_PrintHood</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-966">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-966">GUID</span></span></td>
<td><span data-ttu-id="a3428-967">{9274BD8D-CFD1-41C3-B35E-B13F55A758F4}</span><span class="sxs-lookup"><span data-stu-id="a3428-967">{9274BD8D-CFD1-41C3-B35E-B13F55A758F4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-968">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-968">Display Name</span></span></td>
<td><span data-ttu-id="a3428-969">Raccourcis de l’imprimante</span><span class="sxs-lookup"><span data-stu-id="a3428-969">Printer Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-970">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-970">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-971">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-971">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-972">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-972">Default Path</span></span></td>
<td><span data-ttu-id="a3428-973">%APPDATA%\Microsoft\Windows\Printer les raccourcis</span><span class="sxs-lookup"><span data-stu-id="a3428-973">%APPDATA%\Microsoft\Windows\Printer Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-974">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-974">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-975">CSIDL_PRINTHOOD</span><span class="sxs-lookup"><span data-stu-id="a3428-975">CSIDL_PRINTHOOD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-976">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-976">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-977">PrintHood</span><span class="sxs-lookup"><span data-stu-id="a3428-977">PrintHood</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-978">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-978">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-979">%USERPROFILE%\PrintHood</span><span class="sxs-lookup"><span data-stu-id="a3428-979">%USERPROFILE%\PrintHood</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Profile"></span><span id="folderid_profile"></span><span id="FOLDERID_PROFILE"></span><dl> <span data-ttu-id="a3428-980"><dt><strong>FOLDERID_Profile</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-980"><dt><strong>FOLDERID_Profile</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-981">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-981">GUID</span></span></td>
<td><span data-ttu-id="a3428-982">{5E6C858F-0E22-4760-9AFE-EA3317B67173}</span><span class="sxs-lookup"><span data-stu-id="a3428-982">{5E6C858F-0E22-4760-9AFE-EA3317B67173}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-983">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-983">Display Name</span></span></td>
<td><span data-ttu-id="a3428-984">Nom d’utilisateur de l’utilisateur (% USERNAME%)</span><span class="sxs-lookup"><span data-stu-id="a3428-984">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-985">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-985">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-986">FIXED</span><span class="sxs-lookup"><span data-stu-id="a3428-986">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-987">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-987">Default Path</span></span></td>
<td><span data-ttu-id="a3428-988">% USERPROFILE% (%SystemDrive%\Users \% nom_utilisateur%)</span><span class="sxs-lookup"><span data-stu-id="a3428-988">%USERPROFILE% (%SystemDrive%\Users\%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-989">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-989">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-990">CSIDL_PROFILE</span><span class="sxs-lookup"><span data-stu-id="a3428-990">CSIDL_PROFILE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-991">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-991">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-992">Nom d’utilisateur de l’utilisateur (% USERNAME%)</span><span class="sxs-lookup"><span data-stu-id="a3428-992">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-993">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-993">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-994">% USERPROFILE% (%SystemDrive%\Documents and Settings \% nom_utilisateur%)</span><span class="sxs-lookup"><span data-stu-id="a3428-994">%USERPROFILE% (%SystemDrive%\Documents and Settings\%USERNAME%)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramData"></span><span id="folderid_programdata"></span><span id="FOLDERID_PROGRAMDATA"></span><dl> <span data-ttu-id="a3428-995"><dt><strong>FOLDERID_ProgramData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-995"><dt><strong>FOLDERID_ProgramData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-996">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-996">GUID</span></span></td>
<td><span data-ttu-id="a3428-997">{62AB5D82-FDC1-4DC3-A9DD-070D1D495D97}</span><span class="sxs-lookup"><span data-stu-id="a3428-997">{62AB5D82-FDC1-4DC3-A9DD-070D1D495D97}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-998">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-998">Display Name</span></span></td>
<td><span data-ttu-id="a3428-999">ProgramData</span><span class="sxs-lookup"><span data-stu-id="a3428-999">ProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1000">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1000">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1001">FIXED</span><span class="sxs-lookup"><span data-stu-id="a3428-1001">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1002">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1002">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1003">% ALLUSERSPROFILE% (% ProgramData%,%SystemDrive%\ProgramData)</span><span class="sxs-lookup"><span data-stu-id="a3428-1003">%ALLUSERSPROFILE% (%ProgramData%, %SystemDrive%\ProgramData)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1004">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1004">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1005">CSIDL_COMMON_APPDATA</span><span class="sxs-lookup"><span data-stu-id="a3428-1005">CSIDL_COMMON_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1006">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1006">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1007">Données d'application</span><span class="sxs-lookup"><span data-stu-id="a3428-1007">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1008">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1008">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1009">Données%ALLUSERSPROFILE%\Application</span><span class="sxs-lookup"><span data-stu-id="a3428-1009">%ALLUSERSPROFILE%\Application Data</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFiles"></span><span id="folderid_programfiles"></span><span id="FOLDERID_PROGRAMFILES"></span><dl> <span data-ttu-id="a3428-1010"><dt><strong>FOLDERID_ProgramFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1010"><dt><strong>FOLDERID_ProgramFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="a3428-1011">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="a3428-1011">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1012">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1012">GUID</span></span></td>
<td><span data-ttu-id="a3428-1013">{905e63b6-c1bf-494e-b29c-65b732d3d21a}</span><span class="sxs-lookup"><span data-stu-id="a3428-1013">{905e63b6-c1bf-494e-b29c-65b732d3d21a}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1014">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1014">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1015">Program Files</span><span class="sxs-lookup"><span data-stu-id="a3428-1015">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1016">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1016">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1017">FIXED</span><span class="sxs-lookup"><span data-stu-id="a3428-1017">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1018">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1018">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1019">% ProgramFiles% (%SystemDrive%\Program Files)</span><span class="sxs-lookup"><span data-stu-id="a3428-1019">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1020">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1020">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1021">CSIDL_PROGRAM_FILES</span><span class="sxs-lookup"><span data-stu-id="a3428-1021">CSIDL_PROGRAM_FILES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1022">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1022">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1023">Program Files</span><span class="sxs-lookup"><span data-stu-id="a3428-1023">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1024">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1024">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1025">% ProgramFiles% (%SystemDrive%\Program Files)</span><span class="sxs-lookup"><span data-stu-id="a3428-1025">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesX64"></span><span id="folderid_programfilesx64"></span><span id="FOLDERID_PROGRAMFILESX64"></span><dl> <span data-ttu-id="a3428-1026"><dt><strong>FOLDERID_ProgramFilesX64</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1026"><dt><strong>FOLDERID_ProgramFilesX64</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="a3428-1027">Cette valeur n’est pas prise en charge sur les systèmes d’exploitation 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a3428-1027">This value is not supported on 32-bit operating systems.</span></span> <span data-ttu-id="a3428-1028">Il n’est pas non plus pris en charge pour les applications 32 bits s’exécutant sur des systèmes d’exploitation 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a3428-1028">It also is not supported for 32-bit applications running on 64-bit operating systems.</span></span> <span data-ttu-id="a3428-1029">Toute tentative d’utilisation d’FOLDERID_ProgramFilesX64 dans les deux cas génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="a3428-1029">Attempting to use FOLDERID_ProgramFilesX64 in either situation results in an error.</span></span> <span data-ttu-id="a3428-1030">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="a3428-1030">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1031">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1031">GUID</span></span></td>
<td><span data-ttu-id="a3428-1032">{6D809377-6AF0-444b-8957-A3773F02200E}</span><span class="sxs-lookup"><span data-stu-id="a3428-1032">{6D809377-6AF0-444b-8957-A3773F02200E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1033">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1033">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1034">Program Files</span><span class="sxs-lookup"><span data-stu-id="a3428-1034">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1035">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1035">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1036">FIXED</span><span class="sxs-lookup"><span data-stu-id="a3428-1036">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1037">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1037">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1038">% ProgramFiles% (%SystemDrive%\Program Files)</span><span class="sxs-lookup"><span data-stu-id="a3428-1038">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1039">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1039">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1040">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-1040">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1041">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1041">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1042">Program Files</span><span class="sxs-lookup"><span data-stu-id="a3428-1042">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1043">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1043">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1044">% ProgramFiles% (%SystemDrive%\Program Files)</span><span class="sxs-lookup"><span data-stu-id="a3428-1044">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesX86"></span><span id="folderid_programfilesx86"></span><span id="FOLDERID_PROGRAMFILESX86"></span><dl> <span data-ttu-id="a3428-1045"><dt><strong>FOLDERID_ProgramFilesX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1045"><dt><strong>FOLDERID_ProgramFilesX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="a3428-1046">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="a3428-1046">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1047">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1047">GUID</span></span></td>
<td><span data-ttu-id="a3428-1048">{7C5A40EF-A0FB-4BFC-874A-C0F2E0B9FA8E}</span><span class="sxs-lookup"><span data-stu-id="a3428-1048">{7C5A40EF-A0FB-4BFC-874A-C0F2E0B9FA8E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1049">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1049">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1050">Program Files</span><span class="sxs-lookup"><span data-stu-id="a3428-1050">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1051">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1051">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1052">FIXED</span><span class="sxs-lookup"><span data-stu-id="a3428-1052">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1053">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1053">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1054">% ProgramFiles% (%SystemDrive%\Program Files)</span><span class="sxs-lookup"><span data-stu-id="a3428-1054">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1055">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1055">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1056">CSIDL_PROGRAM_FILESX86</span><span class="sxs-lookup"><span data-stu-id="a3428-1056">CSIDL_PROGRAM_FILESX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1057">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1057">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1058">Program Files</span><span class="sxs-lookup"><span data-stu-id="a3428-1058">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1059">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1059">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1060">% ProgramFiles% (%SystemDrive%\Program Files)</span><span class="sxs-lookup"><span data-stu-id="a3428-1060">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommon"></span><span id="folderid_programfilescommon"></span><span id="FOLDERID_PROGRAMFILESCOMMON"></span><dl> <span data-ttu-id="a3428-1061"><dt><strong>FOLDERID_ProgramFilesCommon</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1061"><dt><strong>FOLDERID_ProgramFilesCommon</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="a3428-1062">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="a3428-1062">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1063">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1063">GUID</span></span></td>
<td><span data-ttu-id="a3428-1064">{F7F1ED05-9F6D-47A2-AAAE-29D317C6F066}</span><span class="sxs-lookup"><span data-stu-id="a3428-1064">{F7F1ED05-9F6D-47A2-AAAE-29D317C6F066}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1065">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1065">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1066">Fichiers communs</span><span class="sxs-lookup"><span data-stu-id="a3428-1066">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1067">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1067">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1068">FIXED</span><span class="sxs-lookup"><span data-stu-id="a3428-1068">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1069">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1069">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1070">Fichiers%ProgramFiles%\Common</span><span class="sxs-lookup"><span data-stu-id="a3428-1070">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1071">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1071">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1072">CSIDL_PROGRAM_FILES_COMMON</span><span class="sxs-lookup"><span data-stu-id="a3428-1072">CSIDL_PROGRAM_FILES_COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1073">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1073">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1074">Fichiers communs</span><span class="sxs-lookup"><span data-stu-id="a3428-1074">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1075">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1075">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1076">Fichiers%ProgramFiles%\Common</span><span class="sxs-lookup"><span data-stu-id="a3428-1076">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommonX64"></span><span id="folderid_programfilescommonx64"></span><span id="FOLDERID_PROGRAMFILESCOMMONX64"></span><dl> <span data-ttu-id="a3428-1077"><dt><strong>FOLDERID_ProgramFilesCommonX64</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1077"><dt><strong>FOLDERID_ProgramFilesCommonX64</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="a3428-1078">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="a3428-1078">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1079">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1079">GUID</span></span></td>
<td><span data-ttu-id="a3428-1080">{6365D5A7-0F0D-45E5-87F6-0DA56B6A4F7D}</span><span class="sxs-lookup"><span data-stu-id="a3428-1080">{6365D5A7-0F0D-45E5-87F6-0DA56B6A4F7D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1081">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1081">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1082">Fichiers communs</span><span class="sxs-lookup"><span data-stu-id="a3428-1082">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1083">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1083">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1084">FIXED</span><span class="sxs-lookup"><span data-stu-id="a3428-1084">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1085">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1085">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1086">Fichiers%ProgramFiles%\Common</span><span class="sxs-lookup"><span data-stu-id="a3428-1086">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1087">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1087">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1088">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-1088">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1089">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1089">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1090">Fichiers communs</span><span class="sxs-lookup"><span data-stu-id="a3428-1090">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1091">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1091">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1092">Fichiers%ProgramFiles%\Common</span><span class="sxs-lookup"><span data-stu-id="a3428-1092">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommonX86"></span><span id="folderid_programfilescommonx86"></span><span id="FOLDERID_PROGRAMFILESCOMMONX86"></span><dl> <span data-ttu-id="a3428-1093"><dt><strong>FOLDERID_ProgramFilesCommonX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1093"><dt><strong>FOLDERID_ProgramFilesCommonX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="a3428-1094">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="a3428-1094">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1095">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1095">GUID</span></span></td>
<td><span data-ttu-id="a3428-1096">{DE974D24-D9C6-4D3E-BF91-F4455120B917}</span><span class="sxs-lookup"><span data-stu-id="a3428-1096">{DE974D24-D9C6-4D3E-BF91-F4455120B917}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1097">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1097">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1098">Fichiers communs</span><span class="sxs-lookup"><span data-stu-id="a3428-1098">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1099">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1099">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1100">FIXED</span><span class="sxs-lookup"><span data-stu-id="a3428-1100">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1101">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1101">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1102">Fichiers%ProgramFiles%\Common</span><span class="sxs-lookup"><span data-stu-id="a3428-1102">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1103">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1103">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1104">CSIDL_PROGRAM_FILES_COMMONX86</span><span class="sxs-lookup"><span data-stu-id="a3428-1104">CSIDL_PROGRAM_FILES_COMMONX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1105">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1105">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1106">Fichiers communs</span><span class="sxs-lookup"><span data-stu-id="a3428-1106">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1107">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1107">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1108">Fichiers%ProgramFiles%\Common</span><span class="sxs-lookup"><span data-stu-id="a3428-1108">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Programs"></span><span id="folderid_programs"></span><span id="FOLDERID_PROGRAMS"></span><dl> <span data-ttu-id="a3428-1109"><dt><strong>FOLDERID_Programs</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1109"><dt><strong>FOLDERID_Programs</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1110">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1110">GUID</span></span></td>
<td><span data-ttu-id="a3428-1111">{A77F5D77-2E2B-44C3-A6A2-ABA601054A51}</span><span class="sxs-lookup"><span data-stu-id="a3428-1111">{A77F5D77-2E2B-44C3-A6A2-ABA601054A51}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1112">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1112">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1113">Programmes</span><span class="sxs-lookup"><span data-stu-id="a3428-1113">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1114">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1114">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1115">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1115">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1116">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1116">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1117">%APPDATA%\Microsoft\Windows\Start \</span><span class="sxs-lookup"><span data-stu-id="a3428-1117">%APPDATA%\Microsoft\Windows\Start Menu\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1118">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1118">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1119">CSIDL_PROGRAMS</span><span class="sxs-lookup"><span data-stu-id="a3428-1119">CSIDL_PROGRAMS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1120">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1120">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1121">Programmes</span><span class="sxs-lookup"><span data-stu-id="a3428-1121">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1122">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1122">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1123">%USERPROFILE%\Start \</span><span class="sxs-lookup"><span data-stu-id="a3428-1123">%USERPROFILE%\Start Menu\Programs</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Public"></span><span id="folderid_public"></span><span id="FOLDERID_PUBLIC"></span><dl> <span data-ttu-id="a3428-1124"><dt><strong>FOLDERID_Public</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1124"><dt><strong>FOLDERID_Public</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1125">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1125">GUID</span></span></td>
<td><span data-ttu-id="a3428-1126">{DFDF76A2-C82A-4D63-906A-5644AC457385}</span><span class="sxs-lookup"><span data-stu-id="a3428-1126">{DFDF76A2-C82A-4D63-906A-5644AC457385}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1127">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1127">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1128">Public</span><span class="sxs-lookup"><span data-stu-id="a3428-1128">Public</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1129">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1129">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1130">FIXED</span><span class="sxs-lookup"><span data-stu-id="a3428-1130">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1131">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1131">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1132">% PUBLIC% (%SystemDrive%\Users\Public)</span><span class="sxs-lookup"><span data-stu-id="a3428-1132">%PUBLIC% (%SystemDrive%\Users\Public)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1133">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1133">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1134">Aucun, nouveau pour Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3428-1134">None, new for Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1135">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1135">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1136">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1136">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1137">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1137">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1138">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1138">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicDesktop"></span><span id="folderid_publicdesktop"></span><span id="FOLDERID_PUBLICDESKTOP"></span><dl> <span data-ttu-id="a3428-1139"><dt><strong>FOLDERID_PublicDesktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1139"><dt><strong>FOLDERID_PublicDesktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1140">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1140">GUID</span></span></td>
<td><span data-ttu-id="a3428-1141">{C4AA340D-F20F-4863-AFEF-F87EF2E6BA25}</span><span class="sxs-lookup"><span data-stu-id="a3428-1141">{C4AA340D-F20F-4863-AFEF-F87EF2E6BA25}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1142">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1142">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1143">Bureau public</span><span class="sxs-lookup"><span data-stu-id="a3428-1143">Public Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1144">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1144">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1145">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-1145">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1146">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1146">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1147">%PUBLIC%\Desktop</span><span class="sxs-lookup"><span data-stu-id="a3428-1147">%PUBLIC%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1148">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1148">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1149">CSIDL_COMMON_DESKTOPDIRECTORY</span><span class="sxs-lookup"><span data-stu-id="a3428-1149">CSIDL_COMMON_DESKTOPDIRECTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1150">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1150">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1151">Bureau</span><span class="sxs-lookup"><span data-stu-id="a3428-1151">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1152">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1152">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1153">%ALLUSERSPROFILE%\Desktop</span><span class="sxs-lookup"><span data-stu-id="a3428-1153">%ALLUSERSPROFILE%\Desktop</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicDocuments"></span><span id="folderid_publicdocuments"></span><span id="FOLDERID_PUBLICDOCUMENTS"></span><dl> <span data-ttu-id="a3428-1154"><dt><strong>FOLDERID_PublicDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1154"><dt><strong>FOLDERID_PublicDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1155">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1155">GUID</span></span></td>
<td><span data-ttu-id="a3428-1156">{ED4824AF-DCE4-45A8-81E2-FC7965083634}</span><span class="sxs-lookup"><span data-stu-id="a3428-1156">{ED4824AF-DCE4-45A8-81E2-FC7965083634}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1157">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1157">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1158">Documents publics</span><span class="sxs-lookup"><span data-stu-id="a3428-1158">Public Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1159">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1159">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1160">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-1160">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1161">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1161">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1162">%PUBLIC%\Documents</span><span class="sxs-lookup"><span data-stu-id="a3428-1162">%PUBLIC%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1163">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1163">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1164">CSIDL_COMMON_DOCUMENTS</span><span class="sxs-lookup"><span data-stu-id="a3428-1164">CSIDL_COMMON_DOCUMENTS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1165">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1165">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1166">Documents partagés</span><span class="sxs-lookup"><span data-stu-id="a3428-1166">Shared Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1167">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1167">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1168">%ALLUSERSPROFILE%\Documents</span><span class="sxs-lookup"><span data-stu-id="a3428-1168">%ALLUSERSPROFILE%\Documents</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicDownloads"></span><span id="folderid_publicdownloads"></span><span id="FOLDERID_PUBLICDOWNLOADS"></span><dl> <span data-ttu-id="a3428-1169"><dt><strong>FOLDERID_PublicDownloads</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1169"><dt><strong>FOLDERID_PublicDownloads</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1170">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1170">GUID</span></span></td>
<td><span data-ttu-id="a3428-1171">{3D644C9B-1FB8-4f30-9B45-F670235F79C0}</span><span class="sxs-lookup"><span data-stu-id="a3428-1171">{3D644C9B-1FB8-4f30-9B45-F670235F79C0}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1172">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1172">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1173">Téléchargements publics</span><span class="sxs-lookup"><span data-stu-id="a3428-1173">Public Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1174">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1174">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1175">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-1175">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1176">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1176">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1177">%PUBLIC%\Downloads</span><span class="sxs-lookup"><span data-stu-id="a3428-1177">%PUBLIC%\Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1178">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1178">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1179">Aucun, valeur introduite dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3428-1179">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1180">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1180">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1181">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1181">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1182">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1182">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1183">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1183">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicGameTasks"></span><span id="folderid_publicgametasks"></span><span id="FOLDERID_PUBLICGAMETASKS"></span><dl> <span data-ttu-id="a3428-1184"><dt><strong>FOLDERID_PublicGameTasks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1184"><dt><strong>FOLDERID_PublicGameTasks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1185">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1185">GUID</span></span></td>
<td><span data-ttu-id="a3428-1186">{DEBF2536-E1A8-4c59-B6A2-414586476AEA}</span><span class="sxs-lookup"><span data-stu-id="a3428-1186">{DEBF2536-E1A8-4c59-B6A2-414586476AEA}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1187">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1187">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1188">GameExplorer</span><span class="sxs-lookup"><span data-stu-id="a3428-1188">GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1189">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1189">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1190">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-1190">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1191">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1191">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1192">%ALLUSERSPROFILE%\Microsoft\Windows\GameExplorer</span><span class="sxs-lookup"><span data-stu-id="a3428-1192">%ALLUSERSPROFILE%\Microsoft\Windows\GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1193">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1193">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1194">Aucun, valeur introduite dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3428-1194">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1195">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1195">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1196">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1196">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1197">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1197">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1198">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1198">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicLibraries"></span><span id="folderid_publiclibraries"></span><span id="FOLDERID_PUBLICLIBRARIES"></span><dl> <span data-ttu-id="a3428-1199"><dt><strong>FOLDERID_PublicLibraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1199"><dt><strong>FOLDERID_PublicLibraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1200">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1200">GUID</span></span></td>
<td><span data-ttu-id="a3428-1201">{48DAF80B-E6CF-4F4E-B800-0E69D84EE384}</span><span class="sxs-lookup"><span data-stu-id="a3428-1201">{48DAF80B-E6CF-4F4E-B800-0E69D84EE384}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1202">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1202">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1203">Bibliothèques</span><span class="sxs-lookup"><span data-stu-id="a3428-1203">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1204">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1204">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1205">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-1205">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1206">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1206">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1207">%ALLUSERSPROFILE%\Microsoft\Windows\Libraries</span><span class="sxs-lookup"><span data-stu-id="a3428-1207">%ALLUSERSPROFILE%\Microsoft\Windows\Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1208">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1208">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1209">Aucun, valeur introduite dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3428-1209">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1210">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1210">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1211">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1211">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1212">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1212">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1213">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1213">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicMusic"></span><span id="folderid_publicmusic"></span><span id="FOLDERID_PUBLICMUSIC"></span><dl> <span data-ttu-id="a3428-1214"><dt><strong>FOLDERID_PublicMusic</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1214"><dt><strong>FOLDERID_PublicMusic</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1215">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1215">GUID</span></span></td>
<td><span data-ttu-id="a3428-1216">{3214FAB5-9757-4298-BB61-92A9DEAA44FF}</span><span class="sxs-lookup"><span data-stu-id="a3428-1216">{3214FAB5-9757-4298-BB61-92A9DEAA44FF}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1217">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1217">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1218">Musique publique</span><span class="sxs-lookup"><span data-stu-id="a3428-1218">Public Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1219">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1219">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1220">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-1220">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1221">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1221">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1222">%PUBLIC%\Music</span><span class="sxs-lookup"><span data-stu-id="a3428-1222">%PUBLIC%\Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1223">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1223">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1224">CSIDL_COMMON_MUSIC</span><span class="sxs-lookup"><span data-stu-id="a3428-1224">CSIDL_COMMON_MUSIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1225">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1225">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1226">Musique partagée</span><span class="sxs-lookup"><span data-stu-id="a3428-1226">Shared Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1227">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1227">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1228">Musique%ALLUSERSPROFILE%\Documents\My</span><span class="sxs-lookup"><span data-stu-id="a3428-1228">%ALLUSERSPROFILE%\Documents\My Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicPictures"></span><span id="folderid_publicpictures"></span><span id="FOLDERID_PUBLICPICTURES"></span><dl> <span data-ttu-id="a3428-1229"><dt><strong>FOLDERID_PublicPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1229"><dt><strong>FOLDERID_PublicPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1230">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1230">GUID</span></span></td>
<td><span data-ttu-id="a3428-1231">{B6EBFB86-6907-413C-9AF7-4FC2ABF07CC5}</span><span class="sxs-lookup"><span data-stu-id="a3428-1231">{B6EBFB86-6907-413C-9AF7-4FC2ABF07CC5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1232">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1232">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1233">Images publiques</span><span class="sxs-lookup"><span data-stu-id="a3428-1233">Public Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1234">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1234">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1235">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-1235">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1236">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1236">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1237">%PUBLIC%\Pictures</span><span class="sxs-lookup"><span data-stu-id="a3428-1237">%PUBLIC%\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1238">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1238">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1239">CSIDL_COMMON_PICTURES</span><span class="sxs-lookup"><span data-stu-id="a3428-1239">CSIDL_COMMON_PICTURES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1240">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1240">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1241">Images partagées</span><span class="sxs-lookup"><span data-stu-id="a3428-1241">Shared Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1242">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1242">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1243">Images%ALLUSERSPROFILE%\Documents\My</span><span class="sxs-lookup"><span data-stu-id="a3428-1243">%ALLUSERSPROFILE%\Documents\My Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicRingtones"></span><span id="folderid_publicringtones"></span><span id="FOLDERID_PUBLICRINGTONES"></span><dl> <span data-ttu-id="a3428-1244"><dt><strong>FOLDERID_PublicRingtones</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1244"><dt><strong>FOLDERID_PublicRingtones</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1245">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1245">GUID</span></span></td>
<td><span data-ttu-id="a3428-1246">{E555AB60-153B-4D17-9F04-A5FE99FC15EC}</span><span class="sxs-lookup"><span data-stu-id="a3428-1246">{E555AB60-153B-4D17-9F04-A5FE99FC15EC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1247">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1247">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1248">Sonneries</span><span class="sxs-lookup"><span data-stu-id="a3428-1248">Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1249">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1249">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1250">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-1250">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1251">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1251">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1252">%ALLUSERSPROFILE%\Microsoft\Windows\Ringtones</span><span class="sxs-lookup"><span data-stu-id="a3428-1252">%ALLUSERSPROFILE%\Microsoft\Windows\Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1253">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1253">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1254">Aucun, valeur introduite dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3428-1254">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1255">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1255">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1256">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1256">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1257">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1257">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1258">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1258">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicUserTiles"></span><span id="folderid_publicusertiles"></span><span id="FOLDERID_PUBLICUSERTILES"></span><dl> <span data-ttu-id="a3428-1259"><dt><strong>FOLDERID_PublicUserTiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1259"><dt><strong>FOLDERID_PublicUserTiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1260">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1260">GUID</span></span></td>
<td><span data-ttu-id="a3428-1261">{0482af6c-08f1-4c34-8c90-e17ec98b1e17}</span><span class="sxs-lookup"><span data-stu-id="a3428-1261">{0482af6c-08f1-4c34-8c90-e17ec98b1e17}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1262">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1262">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1263">Images de compte public</span><span class="sxs-lookup"><span data-stu-id="a3428-1263">Public Account Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1264">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1264">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1265">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-1265">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1266">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1266">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1267">%PUBLIC%\AccountPictures</span><span class="sxs-lookup"><span data-stu-id="a3428-1267">%PUBLIC%\AccountPictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1268">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1268">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1269">Aucun, valeur introduite dans Windows 8</span><span class="sxs-lookup"><span data-stu-id="a3428-1269">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1270">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1270">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1271">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1271">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1272">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1272">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1273">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1273">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicVideos"></span><span id="folderid_publicvideos"></span><span id="FOLDERID_PUBLICVIDEOS"></span><dl> <span data-ttu-id="a3428-1274"><dt><strong>FOLDERID_PublicVideos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1274"><dt><strong>FOLDERID_PublicVideos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1275">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1275">GUID</span></span></td>
<td><span data-ttu-id="a3428-1276">{2400183A-6185-49FB-A2D8-4A392A602BA3}</span><span class="sxs-lookup"><span data-stu-id="a3428-1276">{2400183A-6185-49FB-A2D8-4A392A602BA3}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1277">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1277">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1278">Vidéos publiques</span><span class="sxs-lookup"><span data-stu-id="a3428-1278">Public Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1279">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1279">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1280">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-1280">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1281">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1281">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1282">%PUBLIC%\Videos</span><span class="sxs-lookup"><span data-stu-id="a3428-1282">%PUBLIC%\Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1283">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1283">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1284">CSIDL_COMMON_VIDEO</span><span class="sxs-lookup"><span data-stu-id="a3428-1284">CSIDL_COMMON_VIDEO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1285">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1285">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1286">Vidéo partagée</span><span class="sxs-lookup"><span data-stu-id="a3428-1286">Shared Video</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1287">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1287">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1288">Vidéos%ALLUSERSPROFILE%\Documents\My</span><span class="sxs-lookup"><span data-stu-id="a3428-1288">%ALLUSERSPROFILE%\Documents\My Videos</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_QuickLaunch"></span><span id="folderid_quicklaunch"></span><span id="FOLDERID_QUICKLAUNCH"></span><dl> <span data-ttu-id="a3428-1289"><dt><strong>FOLDERID_QuickLaunch</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1289"><dt><strong>FOLDERID_QuickLaunch</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1290">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1290">GUID</span></span></td>
<td><span data-ttu-id="a3428-1291">{52a4f021-7b75-48a9-9f6b-4b87a210bc8f}</span><span class="sxs-lookup"><span data-stu-id="a3428-1291">{52a4f021-7b75-48a9-9f6b-4b87a210bc8f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1292">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1292">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1293">Lancement rapide</span><span class="sxs-lookup"><span data-stu-id="a3428-1293">Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1294">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1294">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1295">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1295">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1296">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1296">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1297">Lancement de%APPDATA%\Microsoft\Internet Explorer\Quick</span><span class="sxs-lookup"><span data-stu-id="a3428-1297">%APPDATA%\Microsoft\Internet Explorer\Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1298">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1298">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1299">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-1299">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1300">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1300">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1301">Lancement rapide</span><span class="sxs-lookup"><span data-stu-id="a3428-1301">Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1302">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1302">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1303">Lancement de%APPDATA%\Microsoft\Internet Explorer\Quick</span><span class="sxs-lookup"><span data-stu-id="a3428-1303">%APPDATA%\Microsoft\Internet Explorer\Quick Launch</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Recent"></span><span id="folderid_recent"></span><span id="FOLDERID_RECENT"></span><dl> <span data-ttu-id="a3428-1304"><dt><strong>FOLDERID_Recent</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1304"><dt><strong>FOLDERID_Recent</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1305">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1305">GUID</span></span></td>
<td><span data-ttu-id="a3428-1306">{AE50C081-EBD2-438A-8655-8A092E34987A}</span><span class="sxs-lookup"><span data-stu-id="a3428-1306">{AE50C081-EBD2-438A-8655-8A092E34987A}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1307">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1307">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1308">Éléments récents</span><span class="sxs-lookup"><span data-stu-id="a3428-1308">Recent Items</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1309">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1309">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1310">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1310">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1311">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1311">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1312">%APPDATA%\Microsoft\Windows\Recent</span><span class="sxs-lookup"><span data-stu-id="a3428-1312">%APPDATA%\Microsoft\Windows\Recent</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1313">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1313">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1314">CSIDL_RECENT</span><span class="sxs-lookup"><span data-stu-id="a3428-1314">CSIDL_RECENT</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1315">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1315">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1316">Mes documents récents</span><span class="sxs-lookup"><span data-stu-id="a3428-1316">My Recent Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1317">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1317">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1318">%USERPROFILE%\Recent</span><span class="sxs-lookup"><span data-stu-id="a3428-1318">%USERPROFILE%\Recent</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RecordedTV"></span><span id="folderid_recordedtv"></span><span id="FOLDERID_RECORDEDTV"></span><dl> <span data-ttu-id="a3428-1319"><dt><strong>FOLDERID_RecordedTV</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1319"><dt><strong>FOLDERID_RecordedTV</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="a3428-1320">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="a3428-1320">Not used.</span></span> <span data-ttu-id="a3428-1321">Cette valeur n’est pas définie à partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a3428-1321">This value is undefined as of Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RecordedTVLibrary"></span><span id="folderid_recordedtvlibrary"></span><span id="FOLDERID_RECORDEDTVLIBRARY"></span><dl> <span data-ttu-id="a3428-1322"><dt><strong>FOLDERID_RecordedTVLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1322"><dt><strong>FOLDERID_RecordedTVLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1323">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1323">GUID</span></span></td>
<td><span data-ttu-id="a3428-1324">{1A6FDBA2-F42D-4358-A798-B74D745926C5}</span><span class="sxs-lookup"><span data-stu-id="a3428-1324">{1A6FDBA2-F42D-4358-A798-B74D745926C5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1325">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1325">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1326">TV enregistrée</span><span class="sxs-lookup"><span data-stu-id="a3428-1326">Recorded TV</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1327">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1327">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1328">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-1328">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1329">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1329">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1330">%PUBLIC%\RecordedTV.library-ms</span><span class="sxs-lookup"><span data-stu-id="a3428-1330">%PUBLIC%\RecordedTV.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1331">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1331">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1332">Aucun, valeur introduite dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3428-1332">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1333">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1333">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1334">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1334">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1335">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1335">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1336">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RecycleBinFolder"></span><span id="folderid_recyclebinfolder"></span><span id="FOLDERID_RECYCLEBINFOLDER"></span><dl> <span data-ttu-id="a3428-1337"><dt><strong>FOLDERID_RecycleBinFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1337"><dt><strong>FOLDERID_RecycleBinFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1338">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1338">GUID</span></span></td>
<td><span data-ttu-id="a3428-1339">{B7534046-3ECB-4C18-BE4E-64CD4CB7D6AC}</span><span class="sxs-lookup"><span data-stu-id="a3428-1339">{B7534046-3ECB-4C18-BE4E-64CD4CB7D6AC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1340">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1340">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1341">Corbeille</span><span class="sxs-lookup"><span data-stu-id="a3428-1341">Recycle Bin</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1342">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1342">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1343">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-1343">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1344">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1344">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1345">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-1345">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1346">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1346">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1347">CSIDL_BITBUCKET</span><span class="sxs-lookup"><span data-stu-id="a3428-1347">CSIDL_BITBUCKET</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1348">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1348">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1349">Corbeille</span><span class="sxs-lookup"><span data-stu-id="a3428-1349">Recycle Bin</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1350">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1350">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1351">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-1351">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ResourceDir"></span><span id="folderid_resourcedir"></span><span id="FOLDERID_RESOURCEDIR"></span><dl> <span data-ttu-id="a3428-1352"><dt><strong>FOLDERID_ResourceDir</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1352"><dt><strong>FOLDERID_ResourceDir</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1353">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1353">GUID</span></span></td>
<td><span data-ttu-id="a3428-1354">{8AD10C31-2ADB-4296-A8F7-E4701232C972}</span><span class="sxs-lookup"><span data-stu-id="a3428-1354">{8AD10C31-2ADB-4296-A8F7-E4701232C972}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1355">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1355">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1356">Ressources</span><span class="sxs-lookup"><span data-stu-id="a3428-1356">Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1357">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1357">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1358">FIXED</span><span class="sxs-lookup"><span data-stu-id="a3428-1358">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1359">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1359">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1360">%windir%\Resources</span><span class="sxs-lookup"><span data-stu-id="a3428-1360">%windir%\Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1361">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1361">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1362">CSIDL_RESOURCES</span><span class="sxs-lookup"><span data-stu-id="a3428-1362">CSIDL_RESOURCES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1363">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1363">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1364">Ressources</span><span class="sxs-lookup"><span data-stu-id="a3428-1364">Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1365">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1365">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1366">%windir%\Resources</span><span class="sxs-lookup"><span data-stu-id="a3428-1366">%windir%\Resources</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Ringtones"></span><span id="folderid_ringtones"></span><span id="FOLDERID_RINGTONES"></span><dl> <span data-ttu-id="a3428-1367"><dt><strong>FOLDERID_Ringtones</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1367"><dt><strong>FOLDERID_Ringtones</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1368">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1368">GUID</span></span></td>
<td><span data-ttu-id="a3428-1369">{C870044B-F49E-4126-A9C3-B52A1FF411E8}</span><span class="sxs-lookup"><span data-stu-id="a3428-1369">{C870044B-F49E-4126-A9C3-B52A1FF411E8}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1370">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1370">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1371">Sonneries</span><span class="sxs-lookup"><span data-stu-id="a3428-1371">Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1372">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1372">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1373">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1373">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1374">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1374">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1375">%LOCALAPPDATA%\Microsoft\Windows\Ringtones</span><span class="sxs-lookup"><span data-stu-id="a3428-1375">%LOCALAPPDATA%\Microsoft\Windows\Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1376">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1376">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1377">Aucun, valeur introduite dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3428-1377">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1378">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1378">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1379">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1379">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1380">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1380">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1381">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1381">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RoamingAppData"></span><span id="folderid_roamingappdata"></span><span id="FOLDERID_ROAMINGAPPDATA"></span><dl> <span data-ttu-id="a3428-1382"><dt><strong>FOLDERID_RoamingAppData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1382"><dt><strong>FOLDERID_RoamingAppData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1383">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1383">GUID</span></span></td>
<td><span data-ttu-id="a3428-1384">{3EB685DB-65F9-4CF6-A03A-E3EF65729F3D}</span><span class="sxs-lookup"><span data-stu-id="a3428-1384">{3EB685DB-65F9-4CF6-A03A-E3EF65729F3D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1385">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1385">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1386">Itinérance</span><span class="sxs-lookup"><span data-stu-id="a3428-1386">Roaming</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1387">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1387">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1388">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1388">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1389">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1389">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1390">% APPDATA% (%USERPROFILE%\AppData\Roaming)</span><span class="sxs-lookup"><span data-stu-id="a3428-1390">%APPDATA% (%USERPROFILE%\AppData\Roaming)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1391">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1391">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1392">CSIDL_APPDATA</span><span class="sxs-lookup"><span data-stu-id="a3428-1392">CSIDL_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1393">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1393">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1394">Données d'application</span><span class="sxs-lookup"><span data-stu-id="a3428-1394">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1395">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1395">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1396">% APPDATA% (%USERPROFILE%\Application données)</span><span class="sxs-lookup"><span data-stu-id="a3428-1396">%APPDATA% (%USERPROFILE%\Application Data)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RoamedTileImages"></span><span id="folderid_roamedtileimages"></span><span id="FOLDERID_ROAMEDTILEIMAGES"></span><dl> <span data-ttu-id="a3428-1397"><dt><strong>FOLDERID_RoamedTileImages</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1397"><dt><strong>FOLDERID_RoamedTileImages</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1398">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1398">GUID</span></span></td>
<td><span data-ttu-id="a3428-1399">{AAA8D5A5-F1D6-4259-BAA8-78E7EF60835E}</span><span class="sxs-lookup"><span data-stu-id="a3428-1399">{AAA8D5A5-F1D6-4259-BAA8-78E7EF60835E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1400">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1400">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1401">RoamedTileImages</span><span class="sxs-lookup"><span data-stu-id="a3428-1401">RoamedTileImages</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1402">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1402">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1403">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1403">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1404">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1404">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1405">%LOCALAPPDATA%\Microsoft\Windows\RoamedTileImages</span><span class="sxs-lookup"><span data-stu-id="a3428-1405">%LOCALAPPDATA%\Microsoft\Windows\RoamedTileImages</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1406">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1406">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1407">Aucun, valeur introduite dans Windows 8</span><span class="sxs-lookup"><span data-stu-id="a3428-1407">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1408">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1408">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1409">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1409">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1410">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1410">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1411">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1411">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RoamingTiles"></span><span id="folderid_roamingtiles"></span><span id="FOLDERID_ROAMINGTILES"></span><dl> <span data-ttu-id="a3428-1412"><dt><strong>FOLDERID_RoamingTiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1412"><dt><strong>FOLDERID_RoamingTiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1413">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1413">GUID</span></span></td>
<td><span data-ttu-id="a3428-1414">{00BCFC5A-ED94-4e48-96A1-3F6217F21990}</span><span class="sxs-lookup"><span data-stu-id="a3428-1414">{00BCFC5A-ED94-4e48-96A1-3F6217F21990}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1415">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1415">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1416">RoamingTiles</span><span class="sxs-lookup"><span data-stu-id="a3428-1416">RoamingTiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1417">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1417">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1418">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1418">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1419">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1419">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1420">%LOCALAPPDATA%\Microsoft\Windows\RoamingTiles</span><span class="sxs-lookup"><span data-stu-id="a3428-1420">%LOCALAPPDATA%\Microsoft\Windows\RoamingTiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1421">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1421">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1422">Aucun, valeur introduite dans Windows 8</span><span class="sxs-lookup"><span data-stu-id="a3428-1422">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1423">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1423">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1424">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1424">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1425">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1425">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1426">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1426">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SampleMusic"></span><span id="folderid_samplemusic"></span><span id="FOLDERID_SAMPLEMUSIC"></span><dl> <span data-ttu-id="a3428-1427"><dt><strong>FOLDERID_SampleMusic</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1427"><dt><strong>FOLDERID_SampleMusic</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1428">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1428">GUID</span></span></td>
<td><span data-ttu-id="a3428-1429">{B250C668-F57D-4EE1-A63C-290EE7D1AA1F}</span><span class="sxs-lookup"><span data-stu-id="a3428-1429">{B250C668-F57D-4EE1-A63C-290EE7D1AA1F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1430">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1430">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1431">Exemple de musique</span><span class="sxs-lookup"><span data-stu-id="a3428-1431">Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1432">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1432">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1433">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-1433">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1434">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1434">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1435">Musique%PUBLIC%\Music\Sample</span><span class="sxs-lookup"><span data-stu-id="a3428-1435">%PUBLIC%\Music\Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1436">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1436">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1437">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-1437">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1438">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1438">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1439">Exemple de musique</span><span class="sxs-lookup"><span data-stu-id="a3428-1439">Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1440">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1440">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1441">Musique%ALLUSERSPROFILE%\Documents\My Music\Sample</span><span class="sxs-lookup"><span data-stu-id="a3428-1441">%ALLUSERSPROFILE%\Documents\My Music\Sample Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SamplePictures"></span><span id="folderid_samplepictures"></span><span id="FOLDERID_SAMPLEPICTURES"></span><dl> <span data-ttu-id="a3428-1442"><dt><strong>FOLDERID_SamplePictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1442"><dt><strong>FOLDERID_SamplePictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1443">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1443">GUID</span></span></td>
<td><span data-ttu-id="a3428-1444">{C4900540-2379-4C75-844B-64E6FAF8716B}</span><span class="sxs-lookup"><span data-stu-id="a3428-1444">{C4900540-2379-4C75-844B-64E6FAF8716B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1445">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1445">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1446">Exemples d’images</span><span class="sxs-lookup"><span data-stu-id="a3428-1446">Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1447">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1447">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1448">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-1448">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1449">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1449">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1450">Images%PUBLIC%\Pictures\Sample</span><span class="sxs-lookup"><span data-stu-id="a3428-1450">%PUBLIC%\Pictures\Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1451">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1451">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1452">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-1452">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1453">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1453">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1454">Exemples d’images</span><span class="sxs-lookup"><span data-stu-id="a3428-1454">Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1455">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1455">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1456">Images \ échantillons%ALLUSERSPROFILE%\Documents\My</span><span class="sxs-lookup"><span data-stu-id="a3428-1456">%ALLUSERSPROFILE%\Documents\My Pictures\Sample Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SamplePlaylists"></span><span id="folderid_sampleplaylists"></span><span id="FOLDERID_SAMPLEPLAYLISTS"></span><dl> <span data-ttu-id="a3428-1457"><dt><strong>FOLDERID_SamplePlaylists</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1457"><dt><strong>FOLDERID_SamplePlaylists</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1458">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1458">GUID</span></span></td>
<td><span data-ttu-id="a3428-1459">{15CA69B3-30EE-49C1-ACE1-6B5EC372AFB5}</span><span class="sxs-lookup"><span data-stu-id="a3428-1459">{15CA69B3-30EE-49C1-ACE1-6B5EC372AFB5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1460">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1460">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1461">Exemples de sélections</span><span class="sxs-lookup"><span data-stu-id="a3428-1461">Sample Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1462">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1462">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1463">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-1463">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1464">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1464">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1465">%PUBLIC%\Music\Sample playlists</span><span class="sxs-lookup"><span data-stu-id="a3428-1465">%PUBLIC%\Music\Sample Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1466">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1466">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1467">Aucun, valeur introduite dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3428-1467">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1468">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1468">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1469">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1469">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1470">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1470">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1471">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1471">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SampleVideos"></span><span id="folderid_samplevideos"></span><span id="FOLDERID_SAMPLEVIDEOS"></span><dl> <span data-ttu-id="a3428-1472"><dt><strong>FOLDERID_SampleVideos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1472"><dt><strong>FOLDERID_SampleVideos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1473">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1473">GUID</span></span></td>
<td><span data-ttu-id="a3428-1474">{859EAD94-2E85-48AD-A71A-0969CB56A6CD}</span><span class="sxs-lookup"><span data-stu-id="a3428-1474">{859EAD94-2E85-48AD-A71A-0969CB56A6CD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1475">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1475">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1476">Exemples de vidéos</span><span class="sxs-lookup"><span data-stu-id="a3428-1476">Sample Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1477">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1477">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1478">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-1478">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1479">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1479">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1480">Vidéos%PUBLIC%\Videos\Sample</span><span class="sxs-lookup"><span data-stu-id="a3428-1480">%PUBLIC%\Videos\Sample Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1481">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1481">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1482">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-1482">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1483">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1483">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1484">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1484">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1485">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1485">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1486">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1486">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SavedGames"></span><span id="folderid_savedgames"></span><span id="FOLDERID_SAVEDGAMES"></span><dl> <span data-ttu-id="a3428-1487"><dt><strong>FOLDERID_SavedGames</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1487"><dt><strong>FOLDERID_SavedGames</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1488">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1488">GUID</span></span></td>
<td><span data-ttu-id="a3428-1489">{4C5C32FF-BB9D-43b0-B5B4-2D72E54EAAA4}</span><span class="sxs-lookup"><span data-stu-id="a3428-1489">{4C5C32FF-BB9D-43b0-B5B4-2D72E54EAAA4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1490">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1490">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1491">Parties enregistrées</span><span class="sxs-lookup"><span data-stu-id="a3428-1491">Saved Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1492">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1492">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1493">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1493">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1494">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1494">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1495">Jeux%USERPROFILE%\Saved</span><span class="sxs-lookup"><span data-stu-id="a3428-1495">%USERPROFILE%\Saved Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1496">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1496">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1497">Aucun, valeur introduite dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3428-1497">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1498">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1498">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1499">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1499">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1500">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1500">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1501">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1501">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SavedPictures"></span><span id="folderid_savedpictures"></span><span id="FOLDERID_SAVEDPICTURES"></span><dl> <span data-ttu-id="a3428-1502"><dt><strong>FOLDERID_SavedPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1502"><dt><strong>FOLDERID_SavedPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1503">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1503">GUID</span></span></td>
<td><span data-ttu-id="a3428-1504">{3B193882-D3AD-4eab-965A-69829D1FB59F}</span><span class="sxs-lookup"><span data-stu-id="a3428-1504">{3B193882-D3AD-4eab-965A-69829D1FB59F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1505">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1505">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1506">Images enregistrées</span><span class="sxs-lookup"><span data-stu-id="a3428-1506">Saved Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1507">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1507">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1508">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1508">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1509">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1509">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1510">Images%USERPROFILE%\Pictures\Saved</span><span class="sxs-lookup"><span data-stu-id="a3428-1510">%USERPROFILE%\Pictures\Saved Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1511">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1511">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1512">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-1512">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1513">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1513">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1514">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1514">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1515">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1515">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1516">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1516">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SavedPicturesLibrary"></span><span id="folderid_savedpictureslibrary"></span><span id="FOLDERID_SAVEDPICTURESLIBRARY"></span><dl> <span data-ttu-id="a3428-1517"><dt><strong>FOLDERID_SavedPicturesLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1517"><dt><strong>FOLDERID_SavedPicturesLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1518">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1518">GUID</span></span></td>
<td><span data-ttu-id="a3428-1519">{E25B5812-BE88-4bd9-94B0-29233477B6C3}</span><span class="sxs-lookup"><span data-stu-id="a3428-1519">{E25B5812-BE88-4bd9-94B0-29233477B6C3}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1520">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1520">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1521">Bibliothèque d’images enregistrées</span><span class="sxs-lookup"><span data-stu-id="a3428-1521">Saved Pictures Library</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1522">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1522">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1523">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1523">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1524">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1524">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1525">%APPDATE%\Microsoft\Windows\Libraries\SavedPictures.library-ms</span><span class="sxs-lookup"><span data-stu-id="a3428-1525">%APPDATE%\Microsoft\Windows\Libraries\SavedPictures.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1526">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1526">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1527">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-1527">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1528">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1528">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1529">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1529">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1530">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1530">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1531">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1531">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SavedSearches"></span><span id="folderid_savedsearches"></span><span id="FOLDERID_SAVEDSEARCHES"></span><dl> <span data-ttu-id="a3428-1532"><dt><strong>FOLDERID_SavedSearches</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1532"><dt><strong>FOLDERID_SavedSearches</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1533">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1533">GUID</span></span></td>
<td><span data-ttu-id="a3428-1534">{7d1d3a04-debb-4115-95cf-2f29da2920da}</span><span class="sxs-lookup"><span data-stu-id="a3428-1534">{7d1d3a04-debb-4115-95cf-2f29da2920da}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1535">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1535">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1536">Recherches</span><span class="sxs-lookup"><span data-stu-id="a3428-1536">Searches</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1537">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1537">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1538">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1538">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1539">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1539">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1540">%USERPROFILE%\Searches</span><span class="sxs-lookup"><span data-stu-id="a3428-1540">%USERPROFILE%\Searches</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1541">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1541">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1542">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-1542">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1543">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1543">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1544">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1544">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1545">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1545">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1546">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1546">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Screenshots"></span><span id="folderid_screenshots"></span><span id="FOLDERID_SCREENSHOTS"></span><dl> <span data-ttu-id="a3428-1547"><dt><strong>FOLDERID_Screenshots</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1547"><dt><strong>FOLDERID_Screenshots</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1548">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1548">GUID</span></span></td>
<td><span data-ttu-id="a3428-1549">{b7bede81-df94-4682-a7d8-57a52620b86f}</span><span class="sxs-lookup"><span data-stu-id="a3428-1549">{b7bede81-df94-4682-a7d8-57a52620b86f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1550">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1550">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1551">Captures d’écran.</span><span class="sxs-lookup"><span data-stu-id="a3428-1551">Screenshots</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1552">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1552">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1553">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1553">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1554">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1554">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1555">%USERPROFILE%\Pictures\Screenshots</span><span class="sxs-lookup"><span data-stu-id="a3428-1555">%USERPROFILE%\Pictures\Screenshots</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1556">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1556">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1557">Aucun, valeur introduite dans Windows 8</span><span class="sxs-lookup"><span data-stu-id="a3428-1557">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1558">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1558">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1559">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1559">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1560">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1560">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1561">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1561">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SEARCH_CSC"></span><span id="folderid_search_csc"></span><dl> <span data-ttu-id="a3428-1562"><dt><strong>FOLDERID_SEARCH_CSC</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1562"><dt><strong>FOLDERID_SEARCH_CSC</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1563">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1563">GUID</span></span></td>
<td><span data-ttu-id="a3428-1564">{ee32e446-31ca-4aba-814f-a5ebd2fd6d5e}</span><span class="sxs-lookup"><span data-stu-id="a3428-1564">{ee32e446-31ca-4aba-814f-a5ebd2fd6d5e}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1565">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1565">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1566">Fichiers hors connexion</span><span class="sxs-lookup"><span data-stu-id="a3428-1566">Offline Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1567">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1567">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1568">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-1568">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1569">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1569">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1570">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-1570">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1571">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1571">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1572">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-1572">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1573">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1573">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1574">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1574">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1575">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1575">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1576">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1576">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SearchHistory"></span><span id="folderid_searchhistory"></span><span id="FOLDERID_SEARCHHISTORY"></span><dl> <span data-ttu-id="a3428-1577"><dt><strong>FOLDERID_SearchHistory</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1577"><dt><strong>FOLDERID_SearchHistory</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1578">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1578">GUID</span></span></td>
<td><span data-ttu-id="a3428-1579">{0D4C3DB6-03A3-462F-A0E6-08924C41B5D4}</span><span class="sxs-lookup"><span data-stu-id="a3428-1579">{0D4C3DB6-03A3-462F-A0E6-08924C41B5D4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1580">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1580">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1581">Historique</span><span class="sxs-lookup"><span data-stu-id="a3428-1581">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1582">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1582">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1583">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1583">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1584">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1584">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1585">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\History</span><span class="sxs-lookup"><span data-stu-id="a3428-1585">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1586">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1586">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1587">Aucun, valeur introduite dans Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a3428-1587">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1588">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1588">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1589">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1589">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1590">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1590">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1591">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1591">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SearchHome"></span><span id="folderid_searchhome"></span><span id="FOLDERID_SEARCHHOME"></span><dl> <span data-ttu-id="a3428-1592"><dt><strong>FOLDERID_SearchHome</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1592"><dt><strong>FOLDERID_SearchHome</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1593">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1593">GUID</span></span></td>
<td><span data-ttu-id="a3428-1594">{190337d1-b8ca-4121-A639-6d472d16972a}</span><span class="sxs-lookup"><span data-stu-id="a3428-1594">{190337d1-b8ca-4121-a639-6d472d16972a}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1595">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1595">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1596">Résultats de la recherche</span><span class="sxs-lookup"><span data-stu-id="a3428-1596">Search Results</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1597">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1597">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1598">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-1598">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1599">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1599">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1600">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-1600">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1601">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1601">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1602">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-1602">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1603">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1603">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1604">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1604">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1605">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1605">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1606">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1606">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SEARCH_MAPI"></span><span id="folderid_search_mapi"></span><dl> <span data-ttu-id="a3428-1607"><dt><strong>FOLDERID_SEARCH_MAPI</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1607"><dt><strong>FOLDERID_SEARCH_MAPI</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1608">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1608">GUID</span></span></td>
<td><span data-ttu-id="a3428-1609">{98ec0e18-2098-4d44-8644-66979315a281}</span><span class="sxs-lookup"><span data-stu-id="a3428-1609">{98ec0e18-2098-4d44-8644-66979315a281}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1610">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1610">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1611">Microsoft Office Outlook</span><span class="sxs-lookup"><span data-stu-id="a3428-1611">Microsoft Office Outlook</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1612">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1612">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1613">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-1613">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1614">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1614">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1615">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-1615">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1616">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1616">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1617">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-1617">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1618">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1618">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1619">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1619">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1620">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1620">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1621">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1621">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SearchTemplates"></span><span id="folderid_searchtemplates"></span><span id="FOLDERID_SEARCHTEMPLATES"></span><dl> <span data-ttu-id="a3428-1622"><dt><strong>FOLDERID_SearchTemplates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1622"><dt><strong>FOLDERID_SearchTemplates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1623">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1623">GUID</span></span></td>
<td><span data-ttu-id="a3428-1624">{7E636BFE-DFA9-4D5E-B456-D7B39851D8A9}</span><span class="sxs-lookup"><span data-stu-id="a3428-1624">{7E636BFE-DFA9-4D5E-B456-D7B39851D8A9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1625">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1625">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1626">Modèles</span><span class="sxs-lookup"><span data-stu-id="a3428-1626">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1627">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1627">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1628">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1628">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1629">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1629">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1630">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\Templates</span><span class="sxs-lookup"><span data-stu-id="a3428-1630">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1631">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1631">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1632">Aucun, valeur introduite dans Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a3428-1632">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1633">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1633">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1634">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1634">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1635">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1635">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1636">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1636">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SendTo"></span><span id="folderid_sendto"></span><span id="FOLDERID_SENDTO"></span><dl> <span data-ttu-id="a3428-1637"><dt><strong>FOLDERID_SendTo</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1637"><dt><strong>FOLDERID_SendTo</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1638">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1638">GUID</span></span></td>
<td><span data-ttu-id="a3428-1639">{8983036C-27C0-404B-8F08-102D10DCFD74}</span><span class="sxs-lookup"><span data-stu-id="a3428-1639">{8983036C-27C0-404B-8F08-102D10DCFD74}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1640">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1640">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1641">SendTo</span><span class="sxs-lookup"><span data-stu-id="a3428-1641">SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1642">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1642">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1643">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1643">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1644">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1644">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1645">%APPDATA%\Microsoft\Windows\SendTo</span><span class="sxs-lookup"><span data-stu-id="a3428-1645">%APPDATA%\Microsoft\Windows\SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1646">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1646">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1647">CSIDL_SENDTO</span><span class="sxs-lookup"><span data-stu-id="a3428-1647">CSIDL_SENDTO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1648">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1648">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1649">SendTo</span><span class="sxs-lookup"><span data-stu-id="a3428-1649">SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1650">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1650">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1651">%USERPROFILE%\SendTo</span><span class="sxs-lookup"><span data-stu-id="a3428-1651">%USERPROFILE%\SendTo</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SidebarDefaultParts"></span><span id="folderid_sidebardefaultparts"></span><span id="FOLDERID_SIDEBARDEFAULTPARTS"></span><dl> <span data-ttu-id="a3428-1652"><dt><strong>FOLDERID_SidebarDefaultParts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1652"><dt><strong>FOLDERID_SidebarDefaultParts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1653">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1653">GUID</span></span></td>
<td><span data-ttu-id="a3428-1654">{7B396E54-9EC5-4300-BE0A-2482EBAE1A26}</span><span class="sxs-lookup"><span data-stu-id="a3428-1654">{7B396E54-9EC5-4300-BE0A-2482EBAE1A26}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1655">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1655">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1656">Gadgets</span><span class="sxs-lookup"><span data-stu-id="a3428-1656">Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1657">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1657">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1658">CLASSIQUES</span><span class="sxs-lookup"><span data-stu-id="a3428-1658">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1659">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1659">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1660">%ProgramFiles%\Windows Sidebar\Gadgets</span><span class="sxs-lookup"><span data-stu-id="a3428-1660">%ProgramFiles%\Windows Sidebar\Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1661">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1661">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1662">Aucun, nouveau pour Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3428-1662">None, new for Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1663">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1663">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1664">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1664">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1665">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1665">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1666">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1666">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SidebarParts"></span><span id="folderid_sidebarparts"></span><span id="FOLDERID_SIDEBARPARTS"></span><dl> <span data-ttu-id="a3428-1667"><dt><strong>FOLDERID_SidebarParts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1667"><dt><strong>FOLDERID_SidebarParts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1668">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1668">GUID</span></span></td>
<td><span data-ttu-id="a3428-1669">{A75D362E-50FC-4fb7-AC2C-A8BEAA314493}</span><span class="sxs-lookup"><span data-stu-id="a3428-1669">{A75D362E-50FC-4fb7-AC2C-A8BEAA314493}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1670">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1670">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1671">Gadgets</span><span class="sxs-lookup"><span data-stu-id="a3428-1671">Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1672">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1672">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1673">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1673">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1674">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1674">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1675">%LOCALAPPDATA%\Microsoft\Windows Sidebar\Gadgets</span><span class="sxs-lookup"><span data-stu-id="a3428-1675">%LOCALAPPDATA%\Microsoft\Windows Sidebar\Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1676">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1676">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1677">Aucun, nouveau pour Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3428-1677">None, new for Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1678">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1678">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1679">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1679">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1680">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1680">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1681">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1681">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SkyDrive"></span><span id="folderid_skydrive"></span><span id="FOLDERID_SKYDRIVE"></span><dl> <span data-ttu-id="a3428-1682"><dt><strong>FOLDERID_SkyDrive</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1682"><dt><strong>FOLDERID_SkyDrive</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1683">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1683">GUID</span></span></td>
<td><span data-ttu-id="a3428-1684">{A52BBA46-E9E1-435f-B3D9-28DAA648C0F6}</span><span class="sxs-lookup"><span data-stu-id="a3428-1684">{A52BBA46-E9E1-435f-B3D9-28DAA648C0F6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1685">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1685">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1686">OneDrive</span><span class="sxs-lookup"><span data-stu-id="a3428-1686">OneDrive</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1687">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1687">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1688">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1688">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1689">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1689">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1690">%USERPROFILE%\OneDrive</span><span class="sxs-lookup"><span data-stu-id="a3428-1690">%USERPROFILE%\OneDrive</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1691">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1691">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1692">Aucun, valeur introduite dans Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a3428-1692">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1693">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1693">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1694">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1694">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1695">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1695">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1696">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1696">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SkyDriveCameraRoll"></span><span id="folderid_skydrivecameraroll"></span><span id="FOLDERID_SKYDRIVECAMERAROLL"></span><dl> <span data-ttu-id="a3428-1697"><dt><strong>FOLDERID_SkyDriveCameraRoll</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1697"><dt><strong>FOLDERID_SkyDriveCameraRoll</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1698">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1698">GUID</span></span></td>
<td><span data-ttu-id="a3428-1699">{767E6811-49CB-4273-87C2-20F355E1085B}</span><span class="sxs-lookup"><span data-stu-id="a3428-1699">{767E6811-49CB-4273-87C2-20F355E1085B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1700">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1700">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1701">Pellicule</span><span class="sxs-lookup"><span data-stu-id="a3428-1701">Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1702">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1702">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1703">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1703">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1704">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1704">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1705">%USERPROFILE%\OneDrive\Pictures\Camera Roll</span><span class="sxs-lookup"><span data-stu-id="a3428-1705">%USERPROFILE%\OneDrive\Pictures\Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1706">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1706">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1707">Aucun, valeur introduite dans Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a3428-1707">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1708">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1708">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1709">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1709">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1710">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1710">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1711">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1711">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SkyDriveDocuments"></span><span id="folderid_skydrivedocuments"></span><span id="FOLDERID_SKYDRIVEDOCUMENTS"></span><dl> <span data-ttu-id="a3428-1712"><dt><strong>FOLDERID_SkyDriveDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1712"><dt><strong>FOLDERID_SkyDriveDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1713">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1713">GUID</span></span></td>
<td><span data-ttu-id="a3428-1714">{24D89E24-2F19-4534-9DDE-6A6671FBB8FE}</span><span class="sxs-lookup"><span data-stu-id="a3428-1714">{24D89E24-2F19-4534-9DDE-6A6671FBB8FE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1715">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1715">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1716">Documents</span><span class="sxs-lookup"><span data-stu-id="a3428-1716">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1717">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1717">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1718">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1718">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1719">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1719">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1720">%USERPROFILE%\OneDrive\Documents</span><span class="sxs-lookup"><span data-stu-id="a3428-1720">%USERPROFILE%\OneDrive\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1721">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1721">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1722">Aucun, valeur introduite dans Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a3428-1722">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1723">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1723">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1724">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1724">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1725">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1725">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1726">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1726">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SkyDrivePictures"></span><span id="folderid_skydrivepictures"></span><span id="FOLDERID_SKYDRIVEPICTURES"></span><dl> <span data-ttu-id="a3428-1727"><dt><strong>FOLDERID_SkyDrivePictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1727"><dt><strong>FOLDERID_SkyDrivePictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1728">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1728">GUID</span></span></td>
<td><span data-ttu-id="a3428-1729">{339719B5-8C47-4894-94C2-D8F77ADD44A6}</span><span class="sxs-lookup"><span data-stu-id="a3428-1729">{339719B5-8C47-4894-94C2-D8F77ADD44A6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1730">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1730">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1731">Images</span><span class="sxs-lookup"><span data-stu-id="a3428-1731">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1732">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1732">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1733">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1733">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1734">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1734">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1735">%USERPROFILE%\OneDrive\Pictures</span><span class="sxs-lookup"><span data-stu-id="a3428-1735">%USERPROFILE%\OneDrive\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1736">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1736">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1737">Aucun, valeur introduite dans Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a3428-1737">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1738">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1738">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1739">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1739">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1740">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1740">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1741">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1741">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_StartMenu"></span><span id="folderid_startmenu"></span><span id="FOLDERID_STARTMENU"></span><dl> <span data-ttu-id="a3428-1742"><dt><strong>FOLDERID_StartMenu</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1742"><dt><strong>FOLDERID_StartMenu</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1743">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1743">GUID</span></span></td>
<td><span data-ttu-id="a3428-1744">{625B53C3-AB48-4EC1-BA1F-A1EF4146FC19}</span><span class="sxs-lookup"><span data-stu-id="a3428-1744">{625B53C3-AB48-4EC1-BA1F-A1EF4146FC19}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1745">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1745">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1746">Menu Démarrer</span><span class="sxs-lookup"><span data-stu-id="a3428-1746">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1747">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1747">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1748">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1748">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1749">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1749">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1750">Menu%APPDATA%\Microsoft\Windows\Start</span><span class="sxs-lookup"><span data-stu-id="a3428-1750">%APPDATA%\Microsoft\Windows\Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1751">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1751">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1752">CSIDL_STARTMENU</span><span class="sxs-lookup"><span data-stu-id="a3428-1752">CSIDL_STARTMENU</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1753">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1753">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1754">Menu Démarrer</span><span class="sxs-lookup"><span data-stu-id="a3428-1754">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1755">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1755">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1756">Menu%USERPROFILE%\Start</span><span class="sxs-lookup"><span data-stu-id="a3428-1756">%USERPROFILE%\Start Menu</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Startup"></span><span id="folderid_startup"></span><span id="FOLDERID_STARTUP"></span><dl> <span data-ttu-id="a3428-1757"><dt><strong>FOLDERID_Startup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1757"><dt><strong>FOLDERID_Startup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1758">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1758">GUID</span></span></td>
<td><span data-ttu-id="a3428-1759">{B97D20BB-F46A-4C97-BA10-5E3608430854}</span><span class="sxs-lookup"><span data-stu-id="a3428-1759">{B97D20BB-F46A-4C97-BA10-5E3608430854}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1760">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1760">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1761">Démarrage</span><span class="sxs-lookup"><span data-stu-id="a3428-1761">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1762">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1762">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1763">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1763">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1764">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1764">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1765">%APPDATA%\Microsoft\Windows\Start Menu\Programs\StartUp</span><span class="sxs-lookup"><span data-stu-id="a3428-1765">%APPDATA%\Microsoft\Windows\Start Menu\Programs\StartUp</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1766">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1766">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1767">CSIDL_STARTUP, CSIDL_ALTSTARTUP</span><span class="sxs-lookup"><span data-stu-id="a3428-1767">CSIDL_STARTUP, CSIDL_ALTSTARTUP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1768">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1768">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1769">Démarrage</span><span class="sxs-lookup"><span data-stu-id="a3428-1769">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1770">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1770">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1771">%USERPROFILE%\Start Menu\Programs\StartUp</span><span class="sxs-lookup"><span data-stu-id="a3428-1771">%USERPROFILE%\Start Menu\Programs\StartUp</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SyncManagerFolder"></span><span id="folderid_syncmanagerfolder"></span><span id="FOLDERID_SYNCMANAGERFOLDER"></span><dl> <span data-ttu-id="a3428-1772"><dt><strong>FOLDERID_SyncManagerFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1772"><dt><strong>FOLDERID_SyncManagerFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1773">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1773">GUID</span></span></td>
<td><span data-ttu-id="a3428-1774">{43668BF8-C14E-49B2-97C9-747784D784B7}</span><span class="sxs-lookup"><span data-stu-id="a3428-1774">{43668BF8-C14E-49B2-97C9-747784D784B7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1775">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1775">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1776">Centre de synchronisation</span><span class="sxs-lookup"><span data-stu-id="a3428-1776">Sync Center</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1777">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1777">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1778">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-1778">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1779">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1779">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1780">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-1780">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1781">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1781">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1782">Aucun, valeur introduite dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3428-1782">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1783">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1783">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1784">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1784">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1785">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1785">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1786">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1786">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SyncResultsFolder"></span><span id="folderid_syncresultsfolder"></span><span id="FOLDERID_SYNCRESULTSFOLDER"></span><dl> <span data-ttu-id="a3428-1787"><dt><strong>FOLDERID_SyncResultsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1787"><dt><strong>FOLDERID_SyncResultsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1788">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1788">GUID</span></span></td>
<td><span data-ttu-id="a3428-1789">{289a9a43-be44-4057-a41b-587a76d7e7f9}</span><span class="sxs-lookup"><span data-stu-id="a3428-1789">{289a9a43-be44-4057-a41b-587a76d7e7f9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1790">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1790">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1791">Résultats de la synchronisation</span><span class="sxs-lookup"><span data-stu-id="a3428-1791">Sync Results</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1792">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1792">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1793">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-1793">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1794">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1794">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1795">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-1795">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1796">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1796">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1797">Aucun, valeur introduite dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3428-1797">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1798">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1798">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1799">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1799">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1800">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1800">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1801">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1801">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SyncSetupFolder"></span><span id="folderid_syncsetupfolder"></span><span id="FOLDERID_SYNCSETUPFOLDER"></span><dl> <span data-ttu-id="a3428-1802"><dt><strong>FOLDERID_SyncSetupFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1802"><dt><strong>FOLDERID_SyncSetupFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1803">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1803">GUID</span></span></td>
<td><span data-ttu-id="a3428-1804">{0F214138-B1D3-4a90-BBA9-27CBC0C5389A}</span><span class="sxs-lookup"><span data-stu-id="a3428-1804">{0F214138-B1D3-4a90-BBA9-27CBC0C5389A}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1805">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1805">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1806">Configuration de la synchronisation</span><span class="sxs-lookup"><span data-stu-id="a3428-1806">Sync Setup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1807">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1807">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1808">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-1808">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1809">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1809">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1810">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-1810">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1811">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1811">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1812">Aucun, valeur introduite dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3428-1812">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1813">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1813">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1814">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1814">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1815">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1815">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1816">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1816">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_System"></span><span id="folderid_system"></span><span id="FOLDERID_SYSTEM"></span><dl> <span data-ttu-id="a3428-1817"><dt><strong>FOLDERID_System</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1817"><dt><strong>FOLDERID_System</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1818">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1818">GUID</span></span></td>
<td><span data-ttu-id="a3428-1819">{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}</span><span class="sxs-lookup"><span data-stu-id="a3428-1819">{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1820">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1820">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1821">System32</span><span class="sxs-lookup"><span data-stu-id="a3428-1821">System32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1822">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1822">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1823">FIXED</span><span class="sxs-lookup"><span data-stu-id="a3428-1823">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1824">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1824">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1825">%windir%\system32</span><span class="sxs-lookup"><span data-stu-id="a3428-1825">%windir%\system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1826">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1826">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1827">CSIDL_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="a3428-1827">CSIDL_SYSTEM</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1828">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1828">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1829">system32</span><span class="sxs-lookup"><span data-stu-id="a3428-1829">system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1830">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1830">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1831">%windir%\system32</span><span class="sxs-lookup"><span data-stu-id="a3428-1831">%windir%\system32</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SystemX86"></span><span id="folderid_systemx86"></span><span id="FOLDERID_SYSTEMX86"></span><dl> <span data-ttu-id="a3428-1832"><dt><strong>FOLDERID_SystemX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1832"><dt><strong>FOLDERID_SystemX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1833">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1833">GUID</span></span></td>
<td><span data-ttu-id="a3428-1834">{D65231B0-B2F1-4857-A4CE-A8E7C6EA7D27}</span><span class="sxs-lookup"><span data-stu-id="a3428-1834">{D65231B0-B2F1-4857-A4CE-A8E7C6EA7D27}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1835">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1835">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1836">System32</span><span class="sxs-lookup"><span data-stu-id="a3428-1836">System32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1837">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1837">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1838">FIXED</span><span class="sxs-lookup"><span data-stu-id="a3428-1838">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1839">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1839">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1840">%windir%\system32</span><span class="sxs-lookup"><span data-stu-id="a3428-1840">%windir%\system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1841">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1841">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1842">CSIDL_SYSTEMX86</span><span class="sxs-lookup"><span data-stu-id="a3428-1842">CSIDL_SYSTEMX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1843">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1843">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1844">system32</span><span class="sxs-lookup"><span data-stu-id="a3428-1844">system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1845">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1845">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1846">%windir%\system32</span><span class="sxs-lookup"><span data-stu-id="a3428-1846">%windir%\system32</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Templates"></span><span id="folderid_templates"></span><span id="FOLDERID_TEMPLATES"></span><dl> <span data-ttu-id="a3428-1847"><dt><strong>FOLDERID_Templates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1847"><dt><strong>FOLDERID_Templates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1848">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1848">GUID</span></span></td>
<td><span data-ttu-id="a3428-1849">{A63293E8-664E-48DB-A079-DF759E0509F7}</span><span class="sxs-lookup"><span data-stu-id="a3428-1849">{A63293E8-664E-48DB-A079-DF759E0509F7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1850">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1850">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1851">Modèles</span><span class="sxs-lookup"><span data-stu-id="a3428-1851">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1852">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1852">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1853">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1853">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1854">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1854">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1855">%APPDATA%\Microsoft\Windows\Templates</span><span class="sxs-lookup"><span data-stu-id="a3428-1855">%APPDATA%\Microsoft\Windows\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1856">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1856">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1857">CSIDL_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="a3428-1857">CSIDL_TEMPLATES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1858">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1858">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1859">Modèles</span><span class="sxs-lookup"><span data-stu-id="a3428-1859">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1860">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1860">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1861">%USERPROFILE%\Templates</span><span class="sxs-lookup"><span data-stu-id="a3428-1861">%USERPROFILE%\Templates</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_TreeProperties"></span><span id="folderid_treeproperties"></span><span id="FOLDERID_TREEPROPERTIES"></span><dl> <span data-ttu-id="a3428-1862"><dt><strong>FOLDERID_TreeProperties</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1862"><dt><strong>FOLDERID_TreeProperties</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="a3428-1863">Non utilisé dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a3428-1863">Not used in Windows Vista.</span></span> <span data-ttu-id="a3428-1864">Non pris en charge à partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a3428-1864">Unsupported as of Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UserPinned"></span><span id="folderid_userpinned"></span><span id="FOLDERID_USERPINNED"></span><dl> <span data-ttu-id="a3428-1865"><dt><strong>FOLDERID_UserPinned</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1865"><dt><strong>FOLDERID_UserPinned</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1866">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1866">GUID</span></span></td>
<td><span data-ttu-id="a3428-1867">{9E3995AB-1F9C-4F13-B827-48B24B6C7174}</span><span class="sxs-lookup"><span data-stu-id="a3428-1867">{9E3995AB-1F9C-4F13-B827-48B24B6C7174}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1868">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1868">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1869">Utilisateur épinglé</span><span class="sxs-lookup"><span data-stu-id="a3428-1869">User Pinned</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1870">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1870">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1871">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1871">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1872">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1872">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1873">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User épinglé</span><span class="sxs-lookup"><span data-stu-id="a3428-1873">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User Pinned</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1874">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1874">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1875">Aucun, valeur introduite dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3428-1875">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1876">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1876">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1877">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1877">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1878">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1878">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1879">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1879">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UserProfiles"></span><span id="folderid_userprofiles"></span><span id="FOLDERID_USERPROFILES"></span><dl> <span data-ttu-id="a3428-1880"><dt><strong>FOLDERID_UserProfiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1880"><dt><strong>FOLDERID_UserProfiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1881">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1881">GUID</span></span></td>
<td><span data-ttu-id="a3428-1882">{0762D272-C50A-4BB0-A382-697DCD729B80}</span><span class="sxs-lookup"><span data-stu-id="a3428-1882">{0762D272-C50A-4BB0-A382-697DCD729B80}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1883">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1883">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1884">Utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a3428-1884">Users</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1885">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1885">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1886">FIXED</span><span class="sxs-lookup"><span data-stu-id="a3428-1886">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1887">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1887">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1888">%SystemDrive%\Users</span><span class="sxs-lookup"><span data-stu-id="a3428-1888">%SystemDrive%\Users</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1889">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1889">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1890">Aucun, nouveau pour Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3428-1890">None, new for Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1891">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1891">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1892">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1892">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1893">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1893">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1894">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1894">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UserProgramFiles"></span><span id="folderid_userprogramfiles"></span><span id="FOLDERID_USERPROGRAMFILES"></span><dl> <span data-ttu-id="a3428-1895"><dt><strong>FOLDERID_UserProgramFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1895"><dt><strong>FOLDERID_UserProgramFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1896">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1896">GUID</span></span></td>
<td><span data-ttu-id="a3428-1897">{5CD7AEE2-2219-4A67-B85D-6C9CE15660CB}</span><span class="sxs-lookup"><span data-stu-id="a3428-1897">{5CD7AEE2-2219-4A67-B85D-6C9CE15660CB}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1898">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1898">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1899">Programmes</span><span class="sxs-lookup"><span data-stu-id="a3428-1899">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1900">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1900">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1901">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1901">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1902">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1902">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1903">%LOCALAPPDATA%\Programs</span><span class="sxs-lookup"><span data-stu-id="a3428-1903">%LOCALAPPDATA%\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1904">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1904">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1905">Aucun, valeur introduite dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3428-1905">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1906">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1906">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1907">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1907">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1908">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1908">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1909">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1909">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UserProgramFilesCommon"></span><span id="folderid_userprogramfilescommon"></span><span id="FOLDERID_USERPROGRAMFILESCOMMON"></span><dl> <span data-ttu-id="a3428-1910"><dt><strong>FOLDERID_UserProgramFilesCommon</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1910"><dt><strong>FOLDERID_UserProgramFilesCommon</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1911">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1911">GUID</span></span></td>
<td><span data-ttu-id="a3428-1912">{BCBD3057-CA5C-4622-B42D-BC56DB0AE516}</span><span class="sxs-lookup"><span data-stu-id="a3428-1912">{BCBD3057-CA5C-4622-B42D-BC56DB0AE516}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1913">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1913">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1914">Programmes</span><span class="sxs-lookup"><span data-stu-id="a3428-1914">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1915">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1915">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1916">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1916">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1917">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1917">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1918">%LOCALAPPDATA%\Programs\Common</span><span class="sxs-lookup"><span data-stu-id="a3428-1918">%LOCALAPPDATA%\Programs\Common</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1919">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1919">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1920">Aucun, valeur introduite dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3428-1920">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1921">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1921">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1922">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1922">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1923">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1923">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1924">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1924">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UsersFiles"></span><span id="folderid_usersfiles"></span><span id="FOLDERID_USERSFILES"></span><dl> <span data-ttu-id="a3428-1925"><dt><strong>FOLDERID_UsersFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1925"><dt><strong>FOLDERID_UsersFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1926">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1926">GUID</span></span></td>
<td><span data-ttu-id="a3428-1927">{f3ce0f7c-4901-4ACC-8648-d5d44b04ef8f}</span><span class="sxs-lookup"><span data-stu-id="a3428-1927">{f3ce0f7c-4901-4acc-8648-d5d44b04ef8f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1928">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1928">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1929">Nom complet de l’utilisateur (par exemple, Jean Philippe bagel) entré lors de la création du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a3428-1929">The user's full name (for instance, Jean Philippe Bagel) entered when the user account was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1930">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1930">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1931">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-1931">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1932">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1932">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1933">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-1933">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1934">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1934">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1935">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-1935">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1936">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1936">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1937">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1937">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1938">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1938">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1939">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1939">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UsersLibraries"></span><span id="folderid_userslibraries"></span><span id="FOLDERID_USERSLIBRARIES"></span><dl> <span data-ttu-id="a3428-1940"><dt><strong>FOLDERID_UsersLibraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1940"><dt><strong>FOLDERID_UsersLibraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1941">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1941">GUID</span></span></td>
<td><span data-ttu-id="a3428-1942">{A302545D-DEFF-464b-ABE8-61C8648D939B}</span><span class="sxs-lookup"><span data-stu-id="a3428-1942">{A302545D-DEFF-464b-ABE8-61C8648D939B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1943">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1943">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1944">Bibliothèques</span><span class="sxs-lookup"><span data-stu-id="a3428-1944">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1945">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1945">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1946">MACHINES</span><span class="sxs-lookup"><span data-stu-id="a3428-1946">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1947">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1947">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1948">Non applicable — dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="a3428-1948">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1949">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1949">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1950">Aucun, valeur introduite dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3428-1950">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1951">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1951">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1952">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1952">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1953">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1953">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1954">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1954">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Videos"></span><span id="folderid_videos"></span><span id="FOLDERID_VIDEOS"></span><dl> <span data-ttu-id="a3428-1955"><dt><strong>FOLDERID_Videos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1955"><dt><strong>FOLDERID_Videos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1956">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1956">GUID</span></span></td>
<td><span data-ttu-id="a3428-1957">{18989B1D-99B5-455B-841C-AB7C74E4DDFC}</span><span class="sxs-lookup"><span data-stu-id="a3428-1957">{18989B1D-99B5-455B-841C-AB7C74E4DDFC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1958">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1958">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1959">Vidéos</span><span class="sxs-lookup"><span data-stu-id="a3428-1959">Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1960">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1960">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1961">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1961">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1962">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1962">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1963">%USERPROFILE%\Videos</span><span class="sxs-lookup"><span data-stu-id="a3428-1963">%USERPROFILE%\Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1964">CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1964">CSIDL</span></span></td>
<td><span data-ttu-id="a3428-1965">CSIDL_MYVIDEO</span><span class="sxs-lookup"><span data-stu-id="a3428-1965">CSIDL_MYVIDEO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1966">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1966">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1967">Mes vidéos</span><span class="sxs-lookup"><span data-stu-id="a3428-1967">My Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1968">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1968">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1969">%USERPROFILE%\My Documents\mes vidéos</span><span class="sxs-lookup"><span data-stu-id="a3428-1969">%USERPROFILE%\My Documents\My Videos</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_VideosLibrary"></span><span id="folderid_videoslibrary"></span><span id="FOLDERID_VIDEOSLIBRARY"></span><dl> <span data-ttu-id="a3428-1970"><dt><strong>FOLDERID_VideosLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1970"><dt><strong>FOLDERID_VideosLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1971">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1971">GUID</span></span></td>
<td><span data-ttu-id="a3428-1972">{491E922F-5643-4AF4-A7EB-4E7A138D8174}</span><span class="sxs-lookup"><span data-stu-id="a3428-1972">{491E922F-5643-4AF4-A7EB-4E7A138D8174}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1973">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1973">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1974">Vidéos</span><span class="sxs-lookup"><span data-stu-id="a3428-1974">Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1975">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1975">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1976">PerUser</span><span class="sxs-lookup"><span data-stu-id="a3428-1976">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1977">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1977">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1978">%APPDATA%\Microsoft\Windows\Libraries\Videos.library-ms</span><span class="sxs-lookup"><span data-stu-id="a3428-1978">%APPDATA%\Microsoft\Windows\Libraries\Videos.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1979">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1979">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1980">Aucun, valeur introduite dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3428-1980">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1981">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1981">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1982">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1982">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1983">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1983">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1984">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-1984">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Windows"></span><span id="folderid_windows"></span><span id="FOLDERID_WINDOWS"></span><dl> <span data-ttu-id="a3428-1985"><dt><strong>FOLDERID_Windows</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a3428-1985"><dt><strong>FOLDERID_Windows</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3428-1986">GUID</span><span class="sxs-lookup"><span data-stu-id="a3428-1986">GUID</span></span></td>
<td><span data-ttu-id="a3428-1987">{F38BF404-1D43-42F2-9305-67DE0B28FC23}</span><span class="sxs-lookup"><span data-stu-id="a3428-1987">{F38BF404-1D43-42F2-9305-67DE0B28FC23}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1988">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="a3428-1988">Display Name</span></span></td>
<td><span data-ttu-id="a3428-1989">Windows</span><span class="sxs-lookup"><span data-stu-id="a3428-1989">Windows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1990">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="a3428-1990">Folder Type</span></span></td>
<td><span data-ttu-id="a3428-1991">FIXED</span><span class="sxs-lookup"><span data-stu-id="a3428-1991">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1992">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-1992">Default Path</span></span></td>
<td><span data-ttu-id="a3428-1993">%windir%</span><span class="sxs-lookup"><span data-stu-id="a3428-1993">%windir%</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1994">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-1994">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="a3428-1995">CSIDL_WINDOWS</span><span class="sxs-lookup"><span data-stu-id="a3428-1995">CSIDL_WINDOWS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3428-1996">Nom complet hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1996">Legacy Display Name</span></span></td>
<td><span data-ttu-id="a3428-1997">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="a3428-1997">WINDOWS</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3428-1998">Chemin d’accès par défaut hérité</span><span class="sxs-lookup"><span data-stu-id="a3428-1998">Legacy Default Path</span></span></td>
<td><span data-ttu-id="a3428-1999">%windir%</span><span class="sxs-lookup"><span data-stu-id="a3428-1999">%windir%</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="a3428-2000">Notes</span><span class="sxs-lookup"><span data-stu-id="a3428-2000">Remarks</span></span>

<span data-ttu-id="a3428-2001">L’interprétation de certaines valeurs **KNOWNFOLDERID** varie selon que le dossier fait partie d’une application 32 bits ou 64 bits et si cette application s’exécute sur un système d’exploitation 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a3428-2001">The interpretation of certain **KNOWNFOLDERID** values depends on whether the folder is part of a 32-bit or 64-bit application and whether that application is running on a 32-bit or 64-bit operating system.</span></span> <span data-ttu-id="a3428-2002">Si votre application doit faire la distinction entre, par exemple, **Program Files** et **Program Files (x86)**, vous devez utiliser le bon **KNOWNFOLDERID** pour la situation.</span><span class="sxs-lookup"><span data-stu-id="a3428-2002">If your application needs to distinguish between, for example, **Program Files** and **Program Files (x86)**, you must use the right **KNOWNFOLDERID** for the situation.</span></span>

<span data-ttu-id="a3428-2003">Les tableaux suivants résument l’utilisation de **KNOWNFOLDERID** dans ces cas.</span><span class="sxs-lookup"><span data-stu-id="a3428-2003">The following tables summarize the **KNOWNFOLDERID** use in those cases.</span></span>


<span data-ttu-id="a3428-2004">**FOLDERID \_ ProgramFiles**</span><span class="sxs-lookup"><span data-stu-id="a3428-2004">**FOLDERID\_ProgramFiles**</span></span> 

| <span data-ttu-id="a3428-2005">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="a3428-2005">Operating System</span></span> | <span data-ttu-id="a3428-2006">Application</span><span class="sxs-lookup"><span data-stu-id="a3428-2006">Application</span></span> | <span data-ttu-id="a3428-2007">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="a3428-2007">KNOWNFOLDERID</span></span> | <span data-ttu-id="a3428-2008">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-2008">Default Path</span></span> | <span data-ttu-id="a3428-2009">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-2009">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="a3428-2010">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2010">32 bit</span></span> | <span data-ttu-id="a3428-2011">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2011">32 bit</span></span> | <span data-ttu-id="a3428-2012">FOLDERID \_ ProgramFiles</span><span class="sxs-lookup"><span data-stu-id="a3428-2012">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="a3428-2013">% SystemDrive% \\ Program Files</span><span class="sxs-lookup"><span data-stu-id="a3428-2013">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="a3428-2014">\_fichiers programme \_ CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-2014">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="a3428-2015">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2015">32 bit</span></span> | <span data-ttu-id="a3428-2016">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2016">32 bit</span></span> | <span data-ttu-id="a3428-2017">FOLDERID \_ ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="a3428-2017">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="a3428-2018">% SystemDrive% \\ Program Files</span><span class="sxs-lookup"><span data-stu-id="a3428-2018">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="a3428-2019">\_FILESX86 du programme CSIDL \_</span><span class="sxs-lookup"><span data-stu-id="a3428-2019">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="a3428-2020">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2020">32 bit</span></span> | <span data-ttu-id="a3428-2021">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2021">32 bit</span></span> | <span data-ttu-id="a3428-2022">FOLDERID \_ ProgramFilesX64 (non pris en charge sous les systèmes d’exploitation 32 bits)</span><span class="sxs-lookup"><span data-stu-id="a3428-2022">FOLDERID\_ProgramFilesX64 (not supported under 32-bit operating systems)</span></span> | <span data-ttu-id="a3428-2023">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-2023">Not applicable</span></span> | <span data-ttu-id="a3428-2024">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-2024">Not applicable</span></span> |
| <span data-ttu-id="a3428-2025">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2025">64 bit</span></span> | <span data-ttu-id="a3428-2026">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2026">64 bit</span></span> | <span data-ttu-id="a3428-2027">FOLDERID \_ ProgramFiles</span><span class="sxs-lookup"><span data-stu-id="a3428-2027">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="a3428-2028">% SystemDrive% \\ Program Files</span><span class="sxs-lookup"><span data-stu-id="a3428-2028">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="a3428-2029">\_fichiers programme \_ CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-2029">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="a3428-2030">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2030">64 bit</span></span> | <span data-ttu-id="a3428-2031">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2031">64 bit</span></span> | <span data-ttu-id="a3428-2032">FOLDERID \_ ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="a3428-2032">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="a3428-2033">% SystemDrive% \\ Program Files (x86)</span><span class="sxs-lookup"><span data-stu-id="a3428-2033">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="a3428-2034">\_FILESX86 du programme CSIDL \_</span><span class="sxs-lookup"><span data-stu-id="a3428-2034">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="a3428-2035">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2035">64 bit</span></span> | <span data-ttu-id="a3428-2036">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2036">64 bit</span></span> | <span data-ttu-id="a3428-2037">FOLDERID \_ ProgramFilesX64</span><span class="sxs-lookup"><span data-stu-id="a3428-2037">FOLDERID\_ProgramFilesX64</span></span> | <span data-ttu-id="a3428-2038">% SystemDrive% \\ Program Files</span><span class="sxs-lookup"><span data-stu-id="a3428-2038">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="a3428-2039">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-2039">None</span></span> |
| <span data-ttu-id="a3428-2040">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2040">64 bit</span></span> | <span data-ttu-id="a3428-2041">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2041">32 bit</span></span> | <span data-ttu-id="a3428-2042">FOLDERID \_ ProgramFiles</span><span class="sxs-lookup"><span data-stu-id="a3428-2042">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="a3428-2043">% SystemDrive% \\ Program Files (x86)</span><span class="sxs-lookup"><span data-stu-id="a3428-2043">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="a3428-2044">\_fichiers programme \_ CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-2044">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="a3428-2045">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2045">64 bit</span></span> | <span data-ttu-id="a3428-2046">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2046">32 bit</span></span> | <span data-ttu-id="a3428-2047">FOLDERID \_ ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="a3428-2047">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="a3428-2048">% SystemDrive% \\ Program Files (x86)</span><span class="sxs-lookup"><span data-stu-id="a3428-2048">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="a3428-2049">\_FILESX86 du programme CSIDL \_</span><span class="sxs-lookup"><span data-stu-id="a3428-2049">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="a3428-2050">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2050">64 bit</span></span> | <span data-ttu-id="a3428-2051">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2051">32 bit</span></span> | <span data-ttu-id="a3428-2052">FOLDERID \_ ProgramFilesX64 (non pris en charge pour les applications 32 bits)</span><span class="sxs-lookup"><span data-stu-id="a3428-2052">FOLDERID\_ProgramFilesX64 (not supported for 32-bit applications)</span></span> | <span data-ttu-id="a3428-2053">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-2053">Not applicable</span></span> | <span data-ttu-id="a3428-2054">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-2054">Not applicable</span></span> |


<span data-ttu-id="a3428-2055">**FOLDERID \_ ProgramFilesCommon**</span><span class="sxs-lookup"><span data-stu-id="a3428-2055">**FOLDERID\_ProgramFilesCommon**</span></span>

| <span data-ttu-id="a3428-2056">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="a3428-2056">Operating System</span></span> | <span data-ttu-id="a3428-2057">Application</span><span class="sxs-lookup"><span data-stu-id="a3428-2057">Application</span></span> | <span data-ttu-id="a3428-2058">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="a3428-2058">KNOWNFOLDERID</span></span> | <span data-ttu-id="a3428-2059">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-2059">Default Path</span></span> | <span data-ttu-id="a3428-2060">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-2060">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="a3428-2061">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2061">32 bit</span></span> | <span data-ttu-id="a3428-2062">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2062">32 bit</span></span> | <span data-ttu-id="a3428-2063">FOLDERID \_ ProgramFilesCommon</span><span class="sxs-lookup"><span data-stu-id="a3428-2063">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="a3428-2064">Fichiers communs% ProgramFiles% \\</span><span class="sxs-lookup"><span data-stu-id="a3428-2064">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="a3428-2065">\_fichiers programme \_ CSIDL \_ communs</span><span class="sxs-lookup"><span data-stu-id="a3428-2065">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="a3428-2066">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2066">32 bit</span></span> | <span data-ttu-id="a3428-2067">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2067">32 bit</span></span> | <span data-ttu-id="a3428-2068">FOLDERID \_ ProgramFilesCommonX86</span><span class="sxs-lookup"><span data-stu-id="a3428-2068">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="a3428-2069">Fichiers communs% ProgramFiles% \\</span><span class="sxs-lookup"><span data-stu-id="a3428-2069">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="a3428-2070">\_Fichiers programme \_ CSIDL \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="a3428-2070">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="a3428-2071">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2071">32 bit</span></span> | <span data-ttu-id="a3428-2072">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2072">32 bit</span></span> | <span data-ttu-id="a3428-2073">FOLDERID \_ ProgramFilesCommonX64 (non défini)</span><span class="sxs-lookup"><span data-stu-id="a3428-2073">FOLDERID\_ProgramFilesCommonX64 (undefined)</span></span> | <span data-ttu-id="a3428-2074">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-2074">Not applicable</span></span> | <span data-ttu-id="a3428-2075">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a3428-2075">Not applicable</span></span> |
| <span data-ttu-id="a3428-2076">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2076">64 bit</span></span> | <span data-ttu-id="a3428-2077">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2077">64 bit</span></span> | <span data-ttu-id="a3428-2078">FOLDERID \_ ProgramFilesCommon</span><span class="sxs-lookup"><span data-stu-id="a3428-2078">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="a3428-2079">Fichiers communs% ProgramFiles% \\</span><span class="sxs-lookup"><span data-stu-id="a3428-2079">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="a3428-2080">\_fichiers programme \_ CSIDL \_ communs</span><span class="sxs-lookup"><span data-stu-id="a3428-2080">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="a3428-2081">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2081">64 bit</span></span> | <span data-ttu-id="a3428-2082">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2082">64 bit</span></span> | <span data-ttu-id="a3428-2083">FOLDERID \_ ProgramFilesCommonX86</span><span class="sxs-lookup"><span data-stu-id="a3428-2083">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="a3428-2084">% ProgramFiles (x86)% \\ fichiers communs</span><span class="sxs-lookup"><span data-stu-id="a3428-2084">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="a3428-2085">\_Fichiers programme \_ CSIDL \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="a3428-2085">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="a3428-2086">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2086">64 bit</span></span> | <span data-ttu-id="a3428-2087">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2087">64 bit</span></span> | <span data-ttu-id="a3428-2088">FOLDERID \_ ProgramFilesCommonX64</span><span class="sxs-lookup"><span data-stu-id="a3428-2088">FOLDERID\_ProgramFilesCommonX64</span></span> | <span data-ttu-id="a3428-2089">Fichiers communs% ProgramFiles% \\</span><span class="sxs-lookup"><span data-stu-id="a3428-2089">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="a3428-2090">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-2090">None</span></span> |
| <span data-ttu-id="a3428-2091">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2091">64 bit</span></span> | <span data-ttu-id="a3428-2092">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2092">32 bit</span></span> | <span data-ttu-id="a3428-2093">FOLDERID \_ ProgramFilesCommon</span><span class="sxs-lookup"><span data-stu-id="a3428-2093">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="a3428-2094">% ProgramFiles (x86)% \\ fichiers communs</span><span class="sxs-lookup"><span data-stu-id="a3428-2094">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="a3428-2095">\_fichiers programme \_ CSIDL \_ communs</span><span class="sxs-lookup"><span data-stu-id="a3428-2095">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="a3428-2096">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2096">64 bit</span></span> | <span data-ttu-id="a3428-2097">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2097">32 bit</span></span> | <span data-ttu-id="a3428-2098">FOLDERID \_ ProgramFilesCommonX86</span><span class="sxs-lookup"><span data-stu-id="a3428-2098">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="a3428-2099">% ProgramFiles (x86)% \\ fichiers communs</span><span class="sxs-lookup"><span data-stu-id="a3428-2099">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="a3428-2100">\_Fichiers programme \_ CSIDL \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="a3428-2100">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="a3428-2101">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2101">64 bit</span></span> | <span data-ttu-id="a3428-2102">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2102">32 bit</span></span> | <span data-ttu-id="a3428-2103">FOLDERID \_ ProgramFilesCommonX64</span><span class="sxs-lookup"><span data-stu-id="a3428-2103">FOLDERID\_ProgramFilesCommonX64</span></span> | <span data-ttu-id="a3428-2104">Fichiers communs% ProgramFiles% \\</span><span class="sxs-lookup"><span data-stu-id="a3428-2104">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="a3428-2105">Aucun</span><span class="sxs-lookup"><span data-stu-id="a3428-2105">None</span></span> |


<span data-ttu-id="a3428-2106">**\_Système FOLDERID**</span><span class="sxs-lookup"><span data-stu-id="a3428-2106">**FOLDERID\_System**</span></span>

| <span data-ttu-id="a3428-2107">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="a3428-2107">Operating System</span></span> | <span data-ttu-id="a3428-2108">Application</span><span class="sxs-lookup"><span data-stu-id="a3428-2108">Application</span></span> | <span data-ttu-id="a3428-2109">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="a3428-2109">KNOWNFOLDERID</span></span> | <span data-ttu-id="a3428-2110">Default Path</span><span class="sxs-lookup"><span data-stu-id="a3428-2110">Default Path</span></span> | <span data-ttu-id="a3428-2111">Effet de CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-2111">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="a3428-2112">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2112">32 bit</span></span> | <span data-ttu-id="a3428-2113">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2113">32 bit</span></span> | <span data-ttu-id="a3428-2114">\_Système FOLDERID</span><span class="sxs-lookup"><span data-stu-id="a3428-2114">FOLDERID\_System</span></span> | <span data-ttu-id="a3428-2115">% windir% \\ system32</span><span class="sxs-lookup"><span data-stu-id="a3428-2115">%windir%\\system32</span></span> | <span data-ttu-id="a3428-2116">\_système CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-2116">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="a3428-2117">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2117">32 bit</span></span> | <span data-ttu-id="a3428-2118">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2118">32 bit</span></span> | <span data-ttu-id="a3428-2119">FOLDERID \_ SystemX86</span><span class="sxs-lookup"><span data-stu-id="a3428-2119">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="a3428-2120">% windir% \\ system32</span><span class="sxs-lookup"><span data-stu-id="a3428-2120">%windir%\\system32</span></span> | <span data-ttu-id="a3428-2121">CSIDL \_ SYSTEMX86</span><span class="sxs-lookup"><span data-stu-id="a3428-2121">CSIDL\_SYSTEMX86</span></span> |
| <span data-ttu-id="a3428-2122">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2122">64 bit</span></span> | <span data-ttu-id="a3428-2123">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2123">64 bit</span></span> | <span data-ttu-id="a3428-2124">\_Système FOLDERID</span><span class="sxs-lookup"><span data-stu-id="a3428-2124">FOLDERID\_System</span></span> | <span data-ttu-id="a3428-2125">% windir% \\ system32</span><span class="sxs-lookup"><span data-stu-id="a3428-2125">%windir%\\system32</span></span> | <span data-ttu-id="a3428-2126">\_système CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-2126">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="a3428-2127">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2127">64 bit</span></span> | <span data-ttu-id="a3428-2128">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2128">64 bit</span></span> | <span data-ttu-id="a3428-2129">FOLDERID \_ SystemX86</span><span class="sxs-lookup"><span data-stu-id="a3428-2129">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="a3428-2130">% windir% \\ SysWOW64</span><span class="sxs-lookup"><span data-stu-id="a3428-2130">%windir%\\syswow64</span></span> | <span data-ttu-id="a3428-2131">CSIDL \_ SYSTEMX86</span><span class="sxs-lookup"><span data-stu-id="a3428-2131">CSIDL\_SYSTEMX86</span></span> |
| <span data-ttu-id="a3428-2132">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2132">64 bit</span></span> | <span data-ttu-id="a3428-2133">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2133">32 bit</span></span> | <span data-ttu-id="a3428-2134">\_Système FOLDERID</span><span class="sxs-lookup"><span data-stu-id="a3428-2134">FOLDERID\_System</span></span> | <span data-ttu-id="a3428-2135">% windir% \\ system32</span><span class="sxs-lookup"><span data-stu-id="a3428-2135">%windir%\\system32</span></span> | <span data-ttu-id="a3428-2136">\_système CSIDL</span><span class="sxs-lookup"><span data-stu-id="a3428-2136">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="a3428-2137">64 bits</span><span class="sxs-lookup"><span data-stu-id="a3428-2137">64 bit</span></span> | <span data-ttu-id="a3428-2138">32 bit</span><span class="sxs-lookup"><span data-stu-id="a3428-2138">32 bit</span></span> | <span data-ttu-id="a3428-2139">FOLDERID \_ SystemX86</span><span class="sxs-lookup"><span data-stu-id="a3428-2139">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="a3428-2140">% windir% \\ SysWOW64</span><span class="sxs-lookup"><span data-stu-id="a3428-2140">%windir%\\syswow64</span></span> | <span data-ttu-id="a3428-2141">CSIDL \_ SYSTEMX86</span><span class="sxs-lookup"><span data-stu-id="a3428-2141">CSIDL\_SYSTEMX86</span></span> |


<span data-ttu-id="a3428-2142">Nous avons utilisé des chaînes d’environnement pour fournir des chemins d’accès génériques dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="a3428-2142">We have used environment strings to provide generic paths throughout this topic.</span></span> <span data-ttu-id="a3428-2143">Les tableaux suivants fournissent des exemples des chemins d’accès de ces chaînes d’environnement.</span><span class="sxs-lookup"><span data-stu-id="a3428-2143">The following tables give examples of the paths those environment strings represent.</span></span> <span data-ttu-id="a3428-2144">Dans certains cas, ces chemins d’accès peuvent ne pas correspondre à ceux d’un ordinateur particulier en raison des choix effectués au cours de l’installation ou de la redirection de dossiers ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a3428-2144">In some cases, these paths might not match those on a particular computer because of choices made during installation or later folder redirection.</span></span> <span data-ttu-id="a3428-2145">Notez que certains chemins d’accès ont été modifiés pour Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a3428-2145">Note that some paths have changed for Windows Vista.</span></span>


<span data-ttu-id="a3428-2146">**Windows Vista et versions ultérieures**</span><span class="sxs-lookup"><span data-stu-id="a3428-2146">**Windows Vista and later**</span></span>

| <span data-ttu-id="a3428-2147">Chaîne d’environnement</span><span class="sxs-lookup"><span data-stu-id="a3428-2147">Environment String</span></span> | <span data-ttu-id="a3428-2148">Exemple de chemin</span><span class="sxs-lookup"><span data-stu-id="a3428-2148">Example Path</span></span> |
|--------------------|--------------|
| <span data-ttu-id="a3428-2149">ALLUSERSPROFILE</span><span class="sxs-lookup"><span data-stu-id="a3428-2149">%ALLUSERSPROFILE%</span></span> | <span data-ttu-id="a3428-2150">C : \\ ProgramData</span><span class="sxs-lookup"><span data-stu-id="a3428-2150">C:\\ProgramData</span></span> |
| <span data-ttu-id="a3428-2151">%APPDATA%</span><span class="sxs-lookup"><span data-stu-id="a3428-2151">%APPDATA%</span></span> | <span data-ttu-id="a3428-2152">C : \\ utilisateurs \\ *nom_utilisateur* \\ AppData \\ itinérance</span><span class="sxs-lookup"><span data-stu-id="a3428-2152">C:\\Users\\*username*\\AppData\\Roaming</span></span> |
| <span data-ttu-id="a3428-2153">LocalAppData</span><span class="sxs-lookup"><span data-stu-id="a3428-2153">%LOCALAPPDATA%</span></span> | <span data-ttu-id="a3428-2154">C : \\ utilisateurs \\ *nom_utilisateur* \\ AppData \\ local</span><span class="sxs-lookup"><span data-stu-id="a3428-2154">C:\\Users\\*username*\\AppData\\Local</span></span> |
| <span data-ttu-id="a3428-2155">%ProgramData%</span><span class="sxs-lookup"><span data-stu-id="a3428-2155">%ProgramData%</span></span> | <span data-ttu-id="a3428-2156">C : \\ ProgramData</span><span class="sxs-lookup"><span data-stu-id="a3428-2156">C:\\ProgramData</span></span> |
| <span data-ttu-id="a3428-2157">%ProgramFiles%</span><span class="sxs-lookup"><span data-stu-id="a3428-2157">%ProgramFiles%</span></span> | <span data-ttu-id="a3428-2158">C : \\ Program Files</span><span class="sxs-lookup"><span data-stu-id="a3428-2158">C:\\Program Files</span></span> |
| <span data-ttu-id="a3428-2159">%ProgramFiles(x86)%</span><span class="sxs-lookup"><span data-stu-id="a3428-2159">%ProgramFiles(x86)%</span></span> | <span data-ttu-id="a3428-2160">C : \\ Program Files (x86)</span><span class="sxs-lookup"><span data-stu-id="a3428-2160">C:\\Program Files (x86)</span></span> |
| <span data-ttu-id="a3428-2161">PUBLIQUE</span><span class="sxs-lookup"><span data-stu-id="a3428-2161">%PUBLIC%</span></span> | <span data-ttu-id="a3428-2162">C : \\ utilisateurs \\ publics</span><span class="sxs-lookup"><span data-stu-id="a3428-2162">C:\\Users\\Public</span></span> |
| <span data-ttu-id="a3428-2163">%SystemDrive%</span><span class="sxs-lookup"><span data-stu-id="a3428-2163">%SystemDrive%</span></span> | <span data-ttu-id="a3428-2164">C :</span><span class="sxs-lookup"><span data-stu-id="a3428-2164">C:</span></span> |
| <span data-ttu-id="a3428-2165">PROFILS</span><span class="sxs-lookup"><span data-stu-id="a3428-2165">%USERPROFILE%</span></span> | <span data-ttu-id="a3428-2166">C : \\ utilisateurs \\ *nom_utilisateur*</span><span class="sxs-lookup"><span data-stu-id="a3428-2166">C:\\Users\\*username*</span></span> |
| <span data-ttu-id="a3428-2167">%windir%</span><span class="sxs-lookup"><span data-stu-id="a3428-2167">%windir%</span></span> | <span data-ttu-id="a3428-2168">C : \\ Windows</span><span class="sxs-lookup"><span data-stu-id="a3428-2168">C:\\Windows</span></span> |


<span data-ttu-id="a3428-2169">**Windows XP et versions antérieures**</span><span class="sxs-lookup"><span data-stu-id="a3428-2169">**Windows XP and earlier**</span></span>

| <span data-ttu-id="a3428-2170">Chaîne d’environnement</span><span class="sxs-lookup"><span data-stu-id="a3428-2170">Environment String</span></span> | <span data-ttu-id="a3428-2171">Exemple de chemin</span><span class="sxs-lookup"><span data-stu-id="a3428-2171">Example Path</span></span> |
|--------------------|--------------|
| <span data-ttu-id="a3428-2172">ALLUSERSPROFILE</span><span class="sxs-lookup"><span data-stu-id="a3428-2172">%ALLUSERSPROFILE%</span></span> | <span data-ttu-id="a3428-2173">C : \\ Documents and Settings \\ All Users</span><span class="sxs-lookup"><span data-stu-id="a3428-2173">C:\\Documents and Settings\\All Users</span></span> |
| <span data-ttu-id="a3428-2174">%APPDATA%</span><span class="sxs-lookup"><span data-stu-id="a3428-2174">%APPDATA%</span></span> | <span data-ttu-id="a3428-2175">C : \\ Documents and Settings \\ *nom d’utilisateur* \\ informations d’application</span><span class="sxs-lookup"><span data-stu-id="a3428-2175">C:\\Documents and Settings\\*username*\\Application Data</span></span> |
| <span data-ttu-id="a3428-2176">%ProgramFiles%</span><span class="sxs-lookup"><span data-stu-id="a3428-2176">%ProgramFiles%</span></span> | <span data-ttu-id="a3428-2177">C : \\ Program Files</span><span class="sxs-lookup"><span data-stu-id="a3428-2177">C:\\Program Files</span></span> |
| <span data-ttu-id="a3428-2178">%SystemDrive%</span><span class="sxs-lookup"><span data-stu-id="a3428-2178">%SystemDrive%</span></span> | <span data-ttu-id="a3428-2179">C :</span><span class="sxs-lookup"><span data-stu-id="a3428-2179">C:</span></span> |
| <span data-ttu-id="a3428-2180">PROFILS</span><span class="sxs-lookup"><span data-stu-id="a3428-2180">%USERPROFILE%</span></span> | <span data-ttu-id="a3428-2181">C : \\ documents et paramètres \\ *nom d’utilisateur*</span><span class="sxs-lookup"><span data-stu-id="a3428-2181">C:\\Documents and Settings\\*username*</span></span> |
| <span data-ttu-id="a3428-2182">%windir%</span><span class="sxs-lookup"><span data-stu-id="a3428-2182">%windir%</span></span> | <span data-ttu-id="a3428-2183">C : \\ Windows</span><span class="sxs-lookup"><span data-stu-id="a3428-2183">C:\\Windows</span></span> |


## <a name="requirements"></a><span data-ttu-id="a3428-2184">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a3428-2184">Requirements</span></span>


| <span data-ttu-id="a3428-2185">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3428-2185">Requirement</span></span> | <span data-ttu-id="a3428-2186">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3428-2186">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3428-2187">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3428-2187">Header</span></span><br/> | <dl> <span data-ttu-id="a3428-2188"><dt>Fichier KnownFolders. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3428-2188"><dt>Knownfolders.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3428-2189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3428-2189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3428-2190">**CSIDL**</span><span class="sxs-lookup"><span data-stu-id="a3428-2190">**CSIDL**</span></span>](csidl.md)
</dt> <dt>

[<span data-ttu-id="a3428-2191">Dossiers connus</span><span class="sxs-lookup"><span data-stu-id="a3428-2191">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="a3428-2192">Utilisation de dossiers connus dans les applications</span><span class="sxs-lookup"><span data-stu-id="a3428-2192">Working with Known Folders in Applications</span></span>](working-with-known-folders.md)
</dt> <dt>

[<span data-ttu-id="a3428-2193">Comment étendre des dossiers connus avec des dossiers personnalisés</span><span class="sxs-lookup"><span data-stu-id="a3428-2193">How to Extend Known Folders with Custom Folders</span></span>](how-to-extend-known-folders-with-custom-folders.md)
</dt> <dt>

<span data-ttu-id="a3428-2194">[Dossiers connus, exemple](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a3428-2194">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
