---
description: Suggère la stratégie de sécurité à appliquer au navigateur.
ms.assetid: 73541611-2024-4c33-ab03-e3204244c46c
title: 'IItemPreviewerExt :: SuggestBrowserPolicy, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.SuggestBrowserPolicy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0a4f248edbfa4a1779016e40d73051d8c1d9acac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484425"
---
# <a name="iitempreviewerextsuggestbrowserpolicy-method"></a><span data-ttu-id="e87fd-103">IItemPreviewerExt :: SuggestBrowserPolicy, méthode</span><span class="sxs-lookup"><span data-stu-id="e87fd-103">IItemPreviewerExt::SuggestBrowserPolicy method</span></span>

<span data-ttu-id="e87fd-104">Suggère la stratégie de sécurité à appliquer au navigateur.</span><span class="sxs-lookup"><span data-stu-id="e87fd-104">Suggests the security policy to be applied to the browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="e87fd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e87fd-105">Syntax</span></span>


```C++
HRESULT SuggestBrowserPolicy(
  [in]          DWORD dwContext,
  [out, retval] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e87fd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e87fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e87fd-107">*dwContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e87fd-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e87fd-108">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e87fd-108">Type: **DWORD**</span></span>

<span data-ttu-id="e87fd-109">Identificateur de contexte de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e87fd-109">The context identifier for the operation.</span></span> <span data-ttu-id="e87fd-110">Remplacez la valeur par défaut de *dwContext* pour définir l’identificateur de contexte sur la valeur de votre choix.</span><span class="sxs-lookup"><span data-stu-id="e87fd-110">Override the *dwContext* default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="e87fd-111">*pdwFlags* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e87fd-111">*pdwFlags* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e87fd-112">Type : \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="e87fd-112">Type: \**DWORD\** _</span></span>

<span data-ttu-id="e87fd-113">Pointeur vers une valeur DWORD contenant des indicateurs de contrôle de vérification.</span><span class="sxs-lookup"><span data-stu-id="e87fd-113">A pointer to a DWORD value containing verification check flags.</span></span> <span data-ttu-id="e87fd-114">L’indicateur _ *BROWSERPOLICY \_ non fiable \_ content*\* désactive toute possibilité de la préversion de l’exécution d’un script ou d’un ActiveX.</span><span class="sxs-lookup"><span data-stu-id="e87fd-114">The _ *BROWSERPOLICY\_UNTRUSTED\_CONTENT*\* flag disables any possibility of the preview being able to run script or ActiveX.</span></span> <span data-ttu-id="e87fd-115">Le paramètre *pdwFlags* ne doit pas être un pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="e87fd-115">The parameter *pdwFlags* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e87fd-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e87fd-116">Return value</span></span>

<span data-ttu-id="e87fd-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e87fd-117">Type: **HRESULT**</span></span>

<span data-ttu-id="e87fd-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e87fd-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e87fd-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e87fd-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e87fd-120">Notes</span><span class="sxs-lookup"><span data-stu-id="e87fd-120">Remarks</span></span>

<span data-ttu-id="e87fd-121">L’interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.</span><span class="sxs-lookup"><span data-stu-id="e87fd-121">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="e87fd-122">Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser l’interface [**IItemPreviewerExt**](-search-iitempreviewerext.md) et les API suivantes : les interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) et [**ISearchItem**](-search-isearchitem.md) , la structure [**LINKINFO**](-search-linkinfo.md) et l’énumération [**LinkType**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="e87fd-122">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

<span data-ttu-id="e87fd-123">L’utilisation de l’indicateur de **\_ \_ contenu non approuvé BROWSERPOLICY** est fortement recommandée pour désactiver toute possibilité de la version préliminaire de pouvoir exécuter un script ou un ActiveX.</span><span class="sxs-lookup"><span data-stu-id="e87fd-123">Using the **BROWSERPOLICY\_UNTRUSTED\_CONTENT** flag is strongly recommended to disable any possibility of the preview being able to run script or ActiveX.</span></span> <span data-ttu-id="e87fd-124">La méthode **IItemPreviewerExt :: SuggestBrowserPolicy** peut retourner des informations indiquant si l’aperçu de l’élément est approuvé ou non.</span><span class="sxs-lookup"><span data-stu-id="e87fd-124">The **IItemPreviewerExt::SuggestBrowserPolicy** method can return information on whether the item being previewed is trusted or not.</span></span> <span data-ttu-id="e87fd-125">Cela permet au contrôle d’affichage Trident d’exécuter le script, et même les contrôles ActiveX.</span><span class="sxs-lookup"><span data-stu-id="e87fd-125">This will allow the previewer trident control to execute script, and even ActiveX controls.</span></span> <span data-ttu-id="e87fd-126">Étant donné que le générateur d’aperçu utilise souvent des fichiers temporaires pour générer la version préliminaire, cela peut entraîner l’exécution d’un script et d’une exécution de code inattendus dans la zone de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="e87fd-126">Because the previewer often uses temporary files to generate the preview, doing so can result in unexpected script and code execution in the Local Computer zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="e87fd-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e87fd-127">Requirements</span></span>



| <span data-ttu-id="e87fd-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e87fd-128">Requirement</span></span> | <span data-ttu-id="e87fd-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="e87fd-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e87fd-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e87fd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e87fd-131">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e87fd-131">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e87fd-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e87fd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e87fd-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e87fd-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e87fd-134">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="e87fd-134">Redistributable</span></span><br/>          | <span data-ttu-id="e87fd-135">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="e87fd-135">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="e87fd-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e87fd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e87fd-137">**IItemPreviewerExt**</span><span class="sxs-lookup"><span data-stu-id="e87fd-137">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




