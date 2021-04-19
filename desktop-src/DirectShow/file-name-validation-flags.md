---
description: Ces indicateurs spécifient le comportement du localisateur de média.
ms.assetid: 60afb2e8-cdd1-493e-8fc8-6fa581720b8d
title: Indicateurs de validation du nom de fichier (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SFN_VALIDATEF_CHECK
- SFN_VALIDATEF_POPUP
- SFN_VALIDATEF_TELLME
- SFN_VALIDATEF_REPLACE
- SFN_VALIDATEF_USELOCAL
- SFN_VALIDATEF_NOFIND
- SFN_VALIDATEF_IGNOREMUTED
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: d8930241be0306c637bcab36207fec1de2e489c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528511"
---
# <a name="file-name-validation-flags"></a><span data-ttu-id="ac02e-103">Indicateurs de validation du nom de fichier</span><span class="sxs-lookup"><span data-stu-id="ac02e-103">File Name Validation Flags</span></span>

<span data-ttu-id="ac02e-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="ac02e-104">\[Deprecated.</span></span> <span data-ttu-id="ac02e-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ac02e-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="ac02e-106">Ces indicateurs spécifient le comportement du localisateur de média.</span><span class="sxs-lookup"><span data-stu-id="ac02e-106">These flags specify the behavior of the media locator.</span></span>



| <span data-ttu-id="ac02e-107">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="ac02e-107">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="ac02e-108">Description</span><span class="sxs-lookup"><span data-stu-id="ac02e-108">Description</span></span>                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFN_VALIDATEF_CHECK"></span><span id="sfn_validatef_check"></span><dl> <span data-ttu-id="ac02e-109"><dt>**SFN \_ \_Vérification VALIDATEF**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="ac02e-109"><dt>**SFN\_VALIDATEF\_CHECK**</dt> <dt>0x01</dt></span></span> </dl>                   | <span data-ttu-id="ac02e-110">Vérifiez la validité des noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="ac02e-110">Check the validity of file names.</span></span> <span data-ttu-id="ac02e-111">Vous devez définir cet indicateur pour valider les noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="ac02e-111">You must set this flag to validate file names.</span></span> <span data-ttu-id="ac02e-112">Si ce n’est pas le cas, les autres indicateurs n’ont aucun effet.</span><span class="sxs-lookup"><span data-stu-id="ac02e-112">If not, the other flags have no effect.</span></span><br/>                                                                                            |
| <span id="SFN_VALIDATEF_POPUP"></span><span id="sfn_validatef_popup"></span><dl> <span data-ttu-id="ac02e-113"><dt>**SFN \_ VALIDATEF \_ Popup**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="ac02e-113"><dt>**SFN\_VALIDATEF\_POPUP**</dt> <dt>0x02</dt></span></span> </dl>                   | <span data-ttu-id="ac02e-114">Si un fichier est introuvable, affichez une boîte de dialogue Ouvrir un fichier pour l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="ac02e-114">If a file is not located, display an Open File dialog box for the end user.</span></span><br/>                                                                                                                                         |
| <span id="SFN_VALIDATEF_TELLME"></span><span id="sfn_validatef_tellme"></span><dl> <span data-ttu-id="ac02e-115"><dt>**SFN \_ VALIDATEF \_ TELLME**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="ac02e-115"><dt>**SFN\_VALIDATEF\_TELLME**</dt> <dt>0x04</dt></span></span> </dl>                | <span data-ttu-id="ac02e-116">Si un fichier manquant est trouvé, affichez brièvement une boîte de message avec le nom et l’emplacement du fichier.</span><span class="sxs-lookup"><span data-stu-id="ac02e-116">If a missing file is located, briefly display a message box with the name and location of the file.</span></span> <span data-ttu-id="ac02e-117">Cet indicateur est surtout utile à des fins de test. la boîte de message n’est probablement pas adaptée à un produit de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="ac02e-117">This flag is mostly useful for testing purposes; the message box is probably not suitable for a retail product.</span></span><br/> |
| <span id="SFN_VALIDATEF_REPLACE"></span><span id="sfn_validatef_replace"></span><dl> <span data-ttu-id="ac02e-118"><dt>**SFN \_ VALIDATEF \_ remplace**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="ac02e-118"><dt>**SFN\_VALIDATEF\_REPLACE**</dt> <dt>0x08</dt></span></span> </dl>             | <span data-ttu-id="ac02e-119">Si un fichier manquant est trouvé, mettez à jour le nom de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="ac02e-119">If a missing file is located, update the name of the source object.</span></span> <span data-ttu-id="ac02e-120">(Valide uniquement dans la méthode [**IAMTimeline :: ValidateSourceNames**](iamtimeline-validatesourcenames.md) .)</span><span class="sxs-lookup"><span data-stu-id="ac02e-120">(Only valid in the [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md) method.)</span></span><br/>                                         |
| <span id="SFN_VALIDATEF_USELOCAL"></span><span id="sfn_validatef_uselocal"></span><dl> <span data-ttu-id="ac02e-121"><dt>**SFN \_ VALIDATEF \_ USELOCAL**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="ac02e-121"><dt>**SFN\_VALIDATEF\_USELOCAL**</dt> <dt>0x10</dt></span></span> </dl>          | <span data-ttu-id="ac02e-122">Utilisez toujours un fichier local, même si une version du fichier existe sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="ac02e-122">Always use a local file, even if a version of the file exists on the network.</span></span><br/>                                                                                                                                       |
| <span id="SFN_VALIDATEF_NOFIND"></span><span id="sfn_validatef_nofind"></span><dl> <span data-ttu-id="ac02e-123"><dt>**SFN \_ VALIDATEF \_ NoFind**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="ac02e-123"><dt>**SFN\_VALIDATEF\_NOFIND**</dt> <dt>0x20</dt></span></span> </dl>                | <span data-ttu-id="ac02e-124">Ne pas rechercher les fichiers manquants.</span><span class="sxs-lookup"><span data-stu-id="ac02e-124">Do not search for missing files.</span></span> <span data-ttu-id="ac02e-125">Les noms de fichiers sont toujours validés si vous définissez l' \_ indicateur de vérification SFN VALIDATEF \_ .</span><span class="sxs-lookup"><span data-stu-id="ac02e-125">File names are still validated if you set the SFN\_VALIDATEF\_CHECK flag.</span></span><br/>                                                                                                          |
| <span id="SFN_VALIDATEF_IGNOREMUTED"></span><span id="sfn_validatef_ignoremuted"></span><dl> <span data-ttu-id="ac02e-126"><dt>**SFN \_ VALIDATEF \_ IGNOREMUTED**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="ac02e-126"><dt>**SFN\_VALIDATEF\_IGNOREMUTED**</dt> <dt>0x40</dt></span></span> </dl> | <span data-ttu-id="ac02e-127">Ignorer les objets source muets.</span><span class="sxs-lookup"><span data-stu-id="ac02e-127">Ignore muted source objects.</span></span> <span data-ttu-id="ac02e-128">(Valide uniquement dans la méthode [**IAMTimeline :: ValidateSourceNames**](iamtimeline-validatesourcenames.md) .)</span><span class="sxs-lookup"><span data-stu-id="ac02e-128">(Only valid in the [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md) method.)</span></span><br/>                                                                                |



## <a name="requirements"></a><span data-ttu-id="ac02e-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac02e-129">Requirements</span></span>



| <span data-ttu-id="ac02e-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac02e-130">Requirement</span></span> | <span data-ttu-id="ac02e-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac02e-131">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ac02e-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="ac02e-132">Header</span></span><br/> | <dl> <span data-ttu-id="ac02e-133"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac02e-133"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac02e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac02e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac02e-135">**IMediaLocator::FindMediaFile**</span><span class="sxs-lookup"><span data-stu-id="ac02e-135">**IMediaLocator::FindMediaFile**</span></span>](imedialocator-findmediafile.md)
</dt> <dt>

[<span data-ttu-id="ac02e-136">**IRenderEngine::SetSourceNameValidation**</span><span class="sxs-lookup"><span data-stu-id="ac02e-136">**IRenderEngine::SetSourceNameValidation**</span></span>](irenderengine-setsourcenamevalidation.md)
</dt> </dl>

 

 




