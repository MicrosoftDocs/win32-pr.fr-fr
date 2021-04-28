---
description: 'Structure DEVICEDIALOGDATA2 : définit les données nécessaires pour appeler une boîte de dialogue d’appareil.'
ms.assetid: 544238de-310f-4fc3-b519-bb4e6b309272
title: DEVICEDIALOGDATA2, structure (Wiadefd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA2
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: 82ca6cba81101e577eed882ad45272ab81546fed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089803"
---
# <a name="devicedialogdata2-structure"></a><span data-ttu-id="15aee-103">DEVICEDIALOGDATA2, structure</span><span class="sxs-lookup"><span data-stu-id="15aee-103">DEVICEDIALOGDATA2 structure</span></span>

<span data-ttu-id="15aee-104">Définit les données nécessaires pour appeler une boîte de dialogue d’appareil.</span><span class="sxs-lookup"><span data-stu-id="15aee-104">Defines the data needed to call a device dialog.</span></span>

## <a name="syntax"></a><span data-ttu-id="15aee-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15aee-105">Syntax</span></span>


```C++
typedef struct {
  DWORD     cbSize;
  IWiaItem2 *pIWiaItemRoot;
  DWORD     dwFlags;
  HWND      hwndParent;
  BSTR      bstrFolderName;
  BSTR      bstrFilename;
  LONG      lNumFiles;
  BSTR      *pbstrFilePaths;
  IWiaItem2 *ppWiaItem;
} DEVICEDIALOGDATA2;
```



## <a name="members"></a><span data-ttu-id="15aee-106">Membres</span><span class="sxs-lookup"><span data-stu-id="15aee-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="15aee-107">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="15aee-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="15aee-108">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="15aee-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="15aee-109">Spécifie la taille de cette structure en octets.</span><span class="sxs-lookup"><span data-stu-id="15aee-109">Specifies the size of this structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="15aee-110">**pIWiaItemRoot**</span><span class="sxs-lookup"><span data-stu-id="15aee-110">**pIWiaItemRoot**</span></span>
</dt> <dd>

<span data-ttu-id="15aee-111">Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\***</span><span class="sxs-lookup"><span data-stu-id="15aee-111">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="15aee-112">Pointe vers une interface [**IWiaItem2**](-wia-iwiaitem2.md) qui représente l’élément racine valide dans l’arborescence d’éléments de l’application.</span><span class="sxs-lookup"><span data-stu-id="15aee-112">Points to an [**IWiaItem2**](-wia-iwiaitem2.md) interface that represents the valid root item in the application item tree.</span></span>

</dd> <dt>

<span data-ttu-id="15aee-113">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="15aee-113">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="15aee-114">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="15aee-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="15aee-115">Spécifie un jeu d’indicateurs qui contrôlent l’opération de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="15aee-115">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="15aee-116">Peut être défini sur l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="15aee-116">Can be set to any of the following values:</span></span>



| <span data-ttu-id="15aee-117">Indicateur</span><span class="sxs-lookup"><span data-stu-id="15aee-117">Flag</span></span>                                 | <span data-ttu-id="15aee-118">Signification</span><span class="sxs-lookup"><span data-stu-id="15aee-118">Meaning</span></span>                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15aee-119">0</span><span class="sxs-lookup"><span data-stu-id="15aee-119">0</span></span>                                    | <span data-ttu-id="15aee-120">Comportement par défaut</span><span class="sxs-lookup"><span data-stu-id="15aee-120">Default behavior.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="15aee-121">IMAGE unique de la boîte de dialogue de l' \_ appareil WIA \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="15aee-121">WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE</span></span>   | <span data-ttu-id="15aee-122">Limitez la sélection d’image à une seule image dans la boîte de dialogue acquisition d’image d’appareil.</span><span class="sxs-lookup"><span data-stu-id="15aee-122">Restrict image selection to a single image in the device image acquisition dialog box.</span></span>                                                                                                      |
| <span data-ttu-id="15aee-123">\_boîte de dialogue de l’appareil WIA \_ \_ utiliser \_ \_ l’interface utilisateur commune</span><span class="sxs-lookup"><span data-stu-id="15aee-123">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="15aee-124">Utilisez l’interface utilisateur du système, si elle est disponible, au lieu de l’interface utilisateur fournie par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="15aee-124">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="15aee-125">Si l’interface utilisateur système n’est pas disponible, l’interface utilisateur du fournisseur est utilisée.</span><span class="sxs-lookup"><span data-stu-id="15aee-125">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="15aee-126">Si aucune interface utilisateur n’est disponible, la fonction retourne E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="15aee-126">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="15aee-127">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="15aee-127">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="15aee-128">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="15aee-128">Type: **HWND**</span></span>

</dd> <dd>

<span data-ttu-id="15aee-129">Spécifie le handle vers la fenêtre parente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="15aee-129">Specifies the handle to the parent window of the dialog.</span></span>

</dd> <dt>

<span data-ttu-id="15aee-130">**bstrFolderName**</span><span class="sxs-lookup"><span data-stu-id="15aee-130">**bstrFolderName**</span></span>
</dt> <dd>

<span data-ttu-id="15aee-131">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="15aee-131">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="15aee-132">Spécifie le nom du dossier dans lequel les fichiers sont transférés.</span><span class="sxs-lookup"><span data-stu-id="15aee-132">Specifies the folder name where the files are transferred.</span></span>

</dd> <dt>

<span data-ttu-id="15aee-133">**bstrFilename**</span><span class="sxs-lookup"><span data-stu-id="15aee-133">**bstrFilename**</span></span>
</dt> <dd>

<span data-ttu-id="15aee-134">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="15aee-134">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="15aee-135">Spécifie le modèle de nom de fichier à utiliser pour les fichiers transférés à partir d’éléments WIA vers le dossier de destination désigné par **bstrFolderName**.</span><span class="sxs-lookup"><span data-stu-id="15aee-135">Specifies the filename template to be used for files transferred from WIA items to the destination folder designated by **bstrFolderName**.</span></span> <span data-ttu-id="15aee-136">Il est possible de créer un nombre arbitraire de noms de fichiers uniques en ajoutant des caractères supplémentaires au modèle de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="15aee-136">An arbitrary number of unique file names can be created by appending additional characters to the file name template.</span></span>

</dd> <dt>

<span data-ttu-id="15aee-137">**lNumFiles**</span><span class="sxs-lookup"><span data-stu-id="15aee-137">**lNumFiles**</span></span>
</dt> <dd>

<span data-ttu-id="15aee-138">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="15aee-138">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="15aee-139">Reçoit le nombre de chaînes écrites dans le tableau **pbstrFilePaths** .</span><span class="sxs-lookup"><span data-stu-id="15aee-139">Receives the number of strings written to the **pbstrFilePaths** array.</span></span>

</dd> <dt>

<span data-ttu-id="15aee-140">**pbstrFilePaths**</span><span class="sxs-lookup"><span data-stu-id="15aee-140">**pbstrFilePaths**</span></span>
</dt> <dd>

<span data-ttu-id="15aee-141">Type : **BSTR \***</span><span class="sxs-lookup"><span data-stu-id="15aee-141">Type: **BSTR\***</span></span>

</dd> <dd>

<span data-ttu-id="15aee-142">Pointeur vers un tableau de pointeurs BSTR.</span><span class="sxs-lookup"><span data-stu-id="15aee-142">Pointer to an array of BSTR pointers.</span></span> <span data-ttu-id="15aee-143">Chaque élément de tableau pointe vers un BSTR qui contient le nom de destination d’un fichier qui a été transféré avec succès vers le dossier identifié par bstrFolderName.</span><span class="sxs-lookup"><span data-stu-id="15aee-143">Each array element points to a BSTR that contains the destination name of a file that was successfully transferred to the folder identified by bstrFolderName.</span></span> <span data-ttu-id="15aee-144">La méthode doit allouer le stockage de ce membre.</span><span class="sxs-lookup"><span data-stu-id="15aee-144">The method must allocate the storage for this member.</span></span>

</dd> <dt>

<span data-ttu-id="15aee-145">**ppWiaItem**</span><span class="sxs-lookup"><span data-stu-id="15aee-145">**ppWiaItem**</span></span>
</dt> <dd>

<span data-ttu-id="15aee-146">Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\***</span><span class="sxs-lookup"><span data-stu-id="15aee-146">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="15aee-147">Pointeur vers l’interface [**IWiaItem2**](-wia-iwiaitem2.md) de l’élément WIA qui transfère les données vers le ou les fichiers nommés dans le tableau **pbstrFilePaths** .</span><span class="sxs-lookup"><span data-stu-id="15aee-147">Pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the WIA item that transfers data to the file or files named in the **pbstrFilePaths** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15aee-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15aee-148">Requirements</span></span>



| <span data-ttu-id="15aee-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15aee-149">Requirement</span></span> | <span data-ttu-id="15aee-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="15aee-150">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="15aee-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15aee-151">Minimum supported client</span></span><br/> | <span data-ttu-id="15aee-152">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15aee-152">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="15aee-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15aee-153">Minimum supported server</span></span><br/> | <span data-ttu-id="15aee-154">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15aee-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="15aee-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="15aee-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="15aee-156"><dt>Wiadefd. h</dt></span><span class="sxs-lookup"><span data-stu-id="15aee-156"><dt>Wiadefd.h</dt></span></span> </dl> |



 

 




