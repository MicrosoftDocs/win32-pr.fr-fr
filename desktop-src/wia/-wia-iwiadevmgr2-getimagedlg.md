---
description: 'La méthode IWiaDevMgr2 :: GetImageDlg affiche une ou plusieurs boîtes de dialogue qui permettent à un utilisateur d’acquérir une image à partir d’un appareil WIA (Windows Image Acquisition) 2,0 et d’écrire l’image dans un fichier spécifié.'
ms.assetid: 30a63426-150e-44cf-a03e-7b6da14450f7
title: 'IWiaDevMgr2 :: GetImageDlg, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.GetImageDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6777b839beeb809383e524960e8882392be4bd24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518269"
---
# <a name="iwiadevmgr2getimagedlg-method"></a><span data-ttu-id="09d70-103">IWiaDevMgr2 :: GetImageDlg, méthode</span><span class="sxs-lookup"><span data-stu-id="09d70-103">IWiaDevMgr2::GetImageDlg method</span></span>

<span data-ttu-id="09d70-104">La méthode **IWiaDevMgr2 :: GetImageDlg** affiche une ou plusieurs boîtes de dialogue qui permettent à un utilisateur d’acquérir une image à partir d’un appareil WIA (Windows Image Acquisition) 2,0 et d’écrire l’image dans un fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="09d70-104">The **IWiaDevMgr2::GetImageDlg** method displays one or more dialog boxes that enable a user to acquire an image from a Windows Image Acquisition (WIA) 2.0 device and write the image to a specified file.</span></span> <span data-ttu-id="09d70-105">Cette méthode étend les fonctionnalités de [**IWiaDevMgr2 :: SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) pour encapsuler l’acquisition d’images dans un seul appel d’API.</span><span class="sxs-lookup"><span data-stu-id="09d70-105">This method extends the functionality of [**IWiaDevMgr2::SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) to encapsulate image acquisition within a single API call.</span></span>

## <a name="syntax"></a><span data-ttu-id="09d70-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09d70-106">Syntax</span></span>


```C++
HRESULT GetImageDlg(
  [in]      LONG      lFlags,
  [in]      BSTR      bstrDeviceID,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in]      BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppItem
);
```



## <a name="parameters"></a><span data-ttu-id="09d70-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09d70-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09d70-108">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09d70-108">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09d70-109">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="09d70-109">Type: **LONG**</span></span>

<span data-ttu-id="09d70-110">Spécifie le comportement de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="09d70-110">Specifies dialog box behavior.</span></span> <span data-ttu-id="09d70-111">Peut être défini avec les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="09d70-111">Can be set to the following values:</span></span>



| <span data-ttu-id="09d70-112">Indicateur</span><span class="sxs-lookup"><span data-stu-id="09d70-112">Flag</span></span>                                 | <span data-ttu-id="09d70-113">Signification</span><span class="sxs-lookup"><span data-stu-id="09d70-113">Meaning</span></span>                                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09d70-114">0</span><span class="sxs-lookup"><span data-stu-id="09d70-114">0</span></span>                                    | <span data-ttu-id="09d70-115">Comportement par défaut</span><span class="sxs-lookup"><span data-stu-id="09d70-115">Default behavior.</span></span>                                                                                                                                                           |
| <span data-ttu-id="09d70-116">\_boîte de dialogue de l’appareil WIA \_ \_ utiliser \_ \_ l’interface utilisateur commune</span><span class="sxs-lookup"><span data-stu-id="09d70-116">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="09d70-117">Utilisez l’interface utilisateur du système au lieu de l’interface utilisateur fournie par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="09d70-117">Use the system UI instead of the vendor-supplied UI.</span></span> <span data-ttu-id="09d70-118">Si l’interface utilisateur système n’est pas disponible, l’interface utilisateur du fournisseur est utilisée.</span><span class="sxs-lookup"><span data-stu-id="09d70-118">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="09d70-119">Si aucune interface utilisateur n’est disponible, la fonction retourne E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="09d70-119">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="09d70-120">*bstrDeviceID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09d70-120">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09d70-121">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="09d70-121">Type: **BSTR**</span></span>

<span data-ttu-id="09d70-122">Spécifie le scanneur à utiliser.</span><span class="sxs-lookup"><span data-stu-id="09d70-122">Specifies the scanner to use.</span></span>

</dd> <dt>

<span data-ttu-id="09d70-123">*hwndParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09d70-123">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09d70-124">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="09d70-124">Type: **HWND**</span></span>

<span data-ttu-id="09d70-125">Handle de la fenêtre qui possède la boîte de dialogue **obtenir l’image** .</span><span class="sxs-lookup"><span data-stu-id="09d70-125">A handle of the window that owns the **Get Image** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="09d70-126">*bstrFolderName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09d70-126">*bstrFolderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09d70-127">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="09d70-127">Type: **BSTR**</span></span>

<span data-ttu-id="09d70-128">Spécifie le nom du dossier ITO qui stocke les fichiers analysés dans.</span><span class="sxs-lookup"><span data-stu-id="09d70-128">Specifies the name of the folder ito store the scanned files in.</span></span>

</dd> <dt>

<span data-ttu-id="09d70-129">*bstrFilename* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09d70-129">*bstrFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09d70-130">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="09d70-130">Type: **BSTR**</span></span>

<span data-ttu-id="09d70-131">Spécifie le nom du fichier dans lequel écrire les données de l’image.</span><span class="sxs-lookup"><span data-stu-id="09d70-131">Specifies the name of the file to write the image data to.</span></span>

</dd> <dt>

<span data-ttu-id="09d70-132">*plNumFiles* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09d70-132">*plNumFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09d70-133">Type : \**long \** _</span><span class="sxs-lookup"><span data-stu-id="09d70-133">Type: \**LONG\** _</span></span>

<span data-ttu-id="09d70-134">Pointeur vers le nombre de fichiers à analyser.</span><span class="sxs-lookup"><span data-stu-id="09d70-134">A pointer to the number of files to scan.</span></span>

</dd> <dt>

<span data-ttu-id="09d70-135">_ppbstrFilePaths \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09d70-135">_ppbstrFilePaths\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09d70-136">Type : **BSTR \* \***</span><span class="sxs-lookup"><span data-stu-id="09d70-136">Type: **BSTR\*\***</span></span>

<span data-ttu-id="09d70-137">Adresse d’un pointeur vers un tableau de chemins d’accès pour les fichiers analysés.</span><span class="sxs-lookup"><span data-stu-id="09d70-137">The address of a pointer to an array of paths for the scanned files.</span></span> <span data-ttu-id="09d70-138">Initialisez le pointeur pour pointer vers un tableau de taille zéro (0) avant l’appel de **IWiaDevMgr2 :: GetImageDlg** .</span><span class="sxs-lookup"><span data-stu-id="09d70-138">Initialize the pointer to point to an array of size zero (0) before **IWiaDevMgr2::GetImageDlg** is called.</span></span> <span data-ttu-id="09d70-139">Consultez la **section Notes**.</span><span class="sxs-lookup"><span data-stu-id="09d70-139">See **Remarks**.</span></span>

</dd> <dt>

<span data-ttu-id="09d70-140">*ppItem* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="09d70-140">*ppItem* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="09d70-141">Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="09d70-141">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="09d70-142">Adresse d’un pointeur vers le [**IWiaItem2**](-wia-iwiaitem2.md) à partir duquel les images ont été analysées.</span><span class="sxs-lookup"><span data-stu-id="09d70-142">The address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) that the images were scanned from.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09d70-143">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09d70-143">Return value</span></span>

<span data-ttu-id="09d70-144">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="09d70-144">Type: **HRESULT**</span></span>

<span data-ttu-id="09d70-145">**IWiaDevMgr2 :: GetImageDlg** retourne s \_ OK si les données sont transférées avec succès, retourne \_ la valeur false si l’utilisateur annule la boîte de dialogue ou retourne une erreur com standard.</span><span class="sxs-lookup"><span data-stu-id="09d70-145">**IWiaDevMgr2::GetImageDlg** returns S\_OK if the data is transferred successfully, returns S\_FALSE if the user cancels the dialog box, or returns a standard COM error.</span></span>

> [!Note]  
> <span data-ttu-id="09d70-146">Le paramètre *ppbstrFilePaths* n’est pas nécessairement vide si la fonction retourne S \_ false.</span><span class="sxs-lookup"><span data-stu-id="09d70-146">The *ppbstrFilePaths* parameter is not necessarily empty, if the function returns S\_FALSE.</span></span> <span data-ttu-id="09d70-147">Si l’utilisateur annule, les pages dont l’analyse est terminée sont traitées et retournées dans *ppbstrFilePaths*.</span><span class="sxs-lookup"><span data-stu-id="09d70-147">If the user cancels, the pages that have completed scanning are processed and returned in *ppbstrFilePaths*.</span></span> <span data-ttu-id="09d70-148">Même s’ils ne sont pas utilisés, vous devez libérer le tableau.</span><span class="sxs-lookup"><span data-stu-id="09d70-148">Even if they are not used, you must free the array.</span></span> <span data-ttu-id="09d70-149">Consultez la **section Notes**.</span><span class="sxs-lookup"><span data-stu-id="09d70-149">See **Remarks**.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="09d70-150">Notes</span><span class="sxs-lookup"><span data-stu-id="09d70-150">Remarks</span></span>

<span data-ttu-id="09d70-151">Si l’application transmet **null** pour la valeur du paramètre *bstrDeviceID* , **IWiaDevMgr2 :: GetImageDlg** affiche la boîte de dialogue **Sélectionner un appareil** afin que l’utilisateur puisse sélectionner l’appareil d’entrée WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="09d70-151">If the application passes **NULL** for the value of the *bstrDeviceID* parameter, **IWiaDevMgr2::GetImageDlg** displays the **Select Device** dialog box so that the user can select the WIA 2.0 input device.</span></span>

<span data-ttu-id="09d70-152">Utilisez un élément de menu nommé **à partir de scanner** dans le menu **fichier** pour que les sélections d’appareil et d’image soient disponibles dans votre application.</span><span class="sxs-lookup"><span data-stu-id="09d70-152">Use a menu item named **From scanner** on the **File** menu so that device and image selections are available in your application.</span></span>

<span data-ttu-id="09d70-153">Appelez [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) sur chaque BSTR du tableau sur lequel *ppbstrFilePaths* \[ i \] pointe, puis appelez [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) sur le tableau lui-même pour libérer de la mémoire associée.</span><span class="sxs-lookup"><span data-stu-id="09d70-153">Call [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) on each BSTR in the array that *ppbstrFilePaths*\[i\] points to, and call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) on the array itself to free associated memory.</span></span> <span data-ttu-id="09d70-154">Si S \_ false est retourné, vérifiez si la valeur vers laquelle pointe *plNumFiles* est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="09d70-154">If S\_FALSE is returned, check to see if the value that *plNumFiles* points to is not zero.</span></span> <span data-ttu-id="09d70-155">Si la valeur n’est pas égale à zéro, libérez les ressources *ppbstrFilePaths* \[ i \] dans l’application, car l’utilisateur peut annuler après avoir analysé une ou plusieurs pages.</span><span class="sxs-lookup"><span data-stu-id="09d70-155">If the value is not zero, free the *ppbstrFilePaths*\[i\] resources in the application, because the user might cancel after scanning one or more pages.</span></span> <span data-ttu-id="09d70-156">Initialisez *plNumFiles* sur zéro avant d’appeler **IWiaDevMgr2 :: GetImageDlg**.</span><span class="sxs-lookup"><span data-stu-id="09d70-156">Initialize *plNumFiles* to zero before you call **IWiaDevMgr2::GetImageDlg**.</span></span> <span data-ttu-id="09d70-157">Si *plNumFiles* n’est pas initialisé à zéro et qu’une défaillance dans l’infrastructure com entraîne le retour de S \_ false par la fonction avant l’appel de **IWiaDevMgr2 :: GetImageDlg** , *plNumFiles* aura une valeur de garbage collector trompeuse.</span><span class="sxs-lookup"><span data-stu-id="09d70-157">If *plNumFiles* is not initialized to zero and a failure in the COM infrastructure causes the function to return S\_FALSE before **IWiaDevMgr2::GetImageDlg** is called, then *plNumFiles* will have a misleading garbage value.</span></span>

<span data-ttu-id="09d70-158">La boîte de dialogue doit avoir des droits suffisants sur *bstrFolderName* pour pouvoir enregistrer les fichiers avec des noms de fichiers uniques.</span><span class="sxs-lookup"><span data-stu-id="09d70-158">The dialog box must have sufficient rights to *bstrFolderName* so that it can save the files with unique file names.</span></span> <span data-ttu-id="09d70-159">Protégez le dossier à l’aide d’une liste de contrôle d’accès (ACL), car il contient des données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="09d70-159">Protect the folder with an access control list (ACL) because it contains user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="09d70-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09d70-160">Requirements</span></span>



| <span data-ttu-id="09d70-161">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09d70-161">Requirement</span></span> | <span data-ttu-id="09d70-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="09d70-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="09d70-163">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09d70-163">Minimum supported client</span></span><br/> | <span data-ttu-id="09d70-164">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09d70-164">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="09d70-165">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09d70-165">Minimum supported server</span></span><br/> | <span data-ttu-id="09d70-166">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09d70-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="09d70-167">En-tête</span><span class="sxs-lookup"><span data-stu-id="09d70-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="09d70-168"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="09d70-168"><dt>Wia.h</dt></span></span> </dl> |



 

 
