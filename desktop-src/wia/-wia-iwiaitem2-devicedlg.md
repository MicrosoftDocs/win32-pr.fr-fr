---
description: Affiche une boîte de dialogue permettant à l’utilisateur de préparer l’acquisition d’images.
ms.assetid: 2d7246ec-fb90-4538-b717-b9e3813c1696
title: IWiaItem2 ::D méthode eviceDlg (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3337e74a621b6431b5bbfa429692717def447c82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113314"
---
# <a name="iwiaitem2devicedlg-method"></a><span data-ttu-id="f0271-103">IWiaItem2 ::D méthode eviceDlg</span><span class="sxs-lookup"><span data-stu-id="f0271-103">IWiaItem2::DeviceDlg method</span></span>

<span data-ttu-id="f0271-104">Affiche une boîte de dialogue permettant à l’utilisateur de préparer l’acquisition d’images.</span><span class="sxs-lookup"><span data-stu-id="f0271-104">Displays a dialog box to the user to prepare for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0271-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0271-105">Syntax</span></span>


```C++
HRESULT DeviceDlg(
  [in]      LONG      lFlags,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in, out] BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="f0271-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0271-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0271-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0271-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0271-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="f0271-108">Type: **LONG**</span></span>

<span data-ttu-id="f0271-109">Spécifie un jeu d’indicateurs qui contrôlent l’opération de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f0271-109">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="f0271-110">La valeur peut être 0 pour représenter le comportement par défaut ou l’un des \_ indicateurs de boîte de dialogue de périphérique WIA \_ décrits dans [**WiaFlag**](-wia-wiaflag.md).</span><span class="sxs-lookup"><span data-stu-id="f0271-110">The value can be either 0 to represent the default behavior or any of the WIA\_DEVICE\_DIALOG flags described in [**WiaFlag**](-wia-wiaflag.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0271-111">*hwndParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0271-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0271-112">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="f0271-112">Type: **HWND**</span></span>

<span data-ttu-id="f0271-113">Handle de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="f0271-113">A handle to the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="f0271-114">*bstrFolderName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0271-114">*bstrFolderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0271-115">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f0271-115">Type: **BSTR**</span></span>

<span data-ttu-id="f0271-116">Spécifie le nom du dossier dans lequel les fichiers doivent être transférés.</span><span class="sxs-lookup"><span data-stu-id="f0271-116">Specifies the folder name where the files are to be transferred.</span></span>

</dd> <dt>

<span data-ttu-id="f0271-117">*bstrFilename* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0271-117">*bstrFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0271-118">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f0271-118">Type: **BSTR**</span></span>

<span data-ttu-id="f0271-119">Spécifie le nom du fichier de modèle.</span><span class="sxs-lookup"><span data-stu-id="f0271-119">Specifies the template file name.</span></span>

</dd> <dt>

<span data-ttu-id="f0271-120">*plNumFiles* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f0271-120">*plNumFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0271-121">Type : \**long \** _</span><span class="sxs-lookup"><span data-stu-id="f0271-121">Type: \**LONG\** _</span></span>

<span data-ttu-id="f0271-122">Pointeur vers le nombre d’éléments dans le tableau _ppbstrFilePaths \*.</span><span class="sxs-lookup"><span data-stu-id="f0271-122">A pointer to the number of items in the _ppbstrFilePaths\* array.</span></span>

</dd> <dt>

<span data-ttu-id="f0271-123">*ppbstrFilePaths* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f0271-123">*ppbstrFilePaths* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0271-124">Type : **BSTR \* \***</span><span class="sxs-lookup"><span data-stu-id="f0271-124">Type: **BSTR\*\***</span></span>

<span data-ttu-id="f0271-125">Adresse d’un pointeur vers un tableau de chemins d’accès pour les fichiers analysés.</span><span class="sxs-lookup"><span data-stu-id="f0271-125">The address of a pointer to an array of paths for the scanned files.</span></span> <span data-ttu-id="f0271-126">Initialisez le pointeur pour pointer vers un tableau de taille zéro (0) avant **IWiaItem2 ::D evicedlg** est appelée.</span><span class="sxs-lookup"><span data-stu-id="f0271-126">Initialize the pointer to point to an array of size zero (0) before **IWiaItem2::DeviceDlg** is called.</span></span>

</dd> <dt>

<span data-ttu-id="f0271-127">*ppIWiaItem2* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f0271-127">*ppIWiaItem2* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0271-128">Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f0271-128">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="f0271-129">Adresse d’un tableau de pointeurs vers des interfaces [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="f0271-129">The address of an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0271-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f0271-130">Return value</span></span>

<span data-ttu-id="f0271-131">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f0271-131">Type: **HRESULT**</span></span>

<span data-ttu-id="f0271-132">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f0271-132">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f0271-133">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f0271-133">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0271-134">Notes</span><span class="sxs-lookup"><span data-stu-id="f0271-134">Remarks</span></span>

<span data-ttu-id="f0271-135">Cette méthode affiche une boîte de dialogue à l’utilisateur qu’une application utilise pour rassembler toutes les informations requises pour l’acquisition d’images.</span><span class="sxs-lookup"><span data-stu-id="f0271-135">This method displays a dialog box to the user that an application uses to gather all the information required for image acquisition.</span></span> <span data-ttu-id="f0271-136">Il est également utilisé pour spécifier des propriétés d’analyse d’images telles que la luminosité et le contraste.</span><span class="sxs-lookup"><span data-stu-id="f0271-136">It is also used to specify image scan properties such as brightness and contrast.</span></span>

<span data-ttu-id="f0271-137">Une fois que cette méthode a retourné une valeur, l’application peut utiliser l’interface [**IWiaTransfer**](-wia-iwiatransfer.md) pour acquérir l’image.</span><span class="sxs-lookup"><span data-stu-id="f0271-137">After this method returns, the application can use the [**IWiaTransfer**](-wia-iwiatransfer.md) interface to acquire the image.</span></span>

<span data-ttu-id="f0271-138">Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pour chaque élément du tableau de pointeurs d’interface qu’ils reçoivent via le paramètre *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="f0271-138">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method for each element in the array of interface pointers they receive through the *ppIWiaItem2* parameter.</span></span> <span data-ttu-id="f0271-139">Les applications doivent également libérer le tableau à l’aide de [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="f0271-139">Applications must also free the array using [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0271-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0271-140">Requirements</span></span>



| <span data-ttu-id="f0271-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0271-141">Requirement</span></span> | <span data-ttu-id="f0271-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0271-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f0271-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0271-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f0271-144">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0271-144">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f0271-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0271-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f0271-146">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0271-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f0271-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0271-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0271-148"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0271-148"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="f0271-149">MIDL</span><span class="sxs-lookup"><span data-stu-id="f0271-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f0271-150"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f0271-150"><dt>Wia.idl</dt></span></span> </dl> |



 

 
