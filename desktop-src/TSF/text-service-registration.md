---
title: Inscription du service de texte
description: En plus des entrées de Registre du serveur in-proc COM standard, un service de texte doit s’inscrire auprès de Text Services Framework (TSF) pour pouvoir être utilisé avec une application.
ms.assetid: 95676067-ab5c-470b-a4be-117ab6810d48
keywords:
- Text Services Framework (TSF), inscription
- TSF (Text Services Framework), inscription
- services de texte, inscription
- Text Services Framework (TSF), profils de langue
- TSF (Text Services Framework), profils de langue
- services de texte, profils de langue
- Text Services Framework (TSF), catégories
- TSF (Text Services Framework), catégories
- services de texte, catégories
- inscription des services de texte
- inscription des profils de langue
- inscription des catégories
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc1b91ad1a3b1fde9a2e49b92950ce2db4876f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463399"
---
# <a name="text-service-registration"></a><span data-ttu-id="da9a0-115">Inscription du service de texte</span><span class="sxs-lookup"><span data-stu-id="da9a0-115">Text Service Registration</span></span>

<span data-ttu-id="da9a0-116">En plus des entrées de Registre du serveur in-proc COM standard, un service de texte doit s’inscrire auprès de Text Services Framework (TSF) pour pouvoir être utilisé avec une application.</span><span class="sxs-lookup"><span data-stu-id="da9a0-116">In addition to the standard COM in-proc server registry entries, a text service must register itself with the Text Services Framework (TSF) so that it can be available for use with an application.</span></span> <span data-ttu-id="da9a0-117">TSF fournit l’interface [ITfInputProcessorProfiles](/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles) et [ITfCategoryMgr](/windows/desktop/api/msctf/nn-msctf-itfcategorymgr) pour simplifier le processus d’inscription.</span><span class="sxs-lookup"><span data-stu-id="da9a0-117">TSF supplies the [ITfInputProcessorProfiles](/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles) and [ITfCategoryMgr](/windows/desktop/api/msctf/nn-msctf-itfcategorymgr) interface to simplify the registration process.</span></span>

<span data-ttu-id="da9a0-118">Les fournisseurs de services de texte doivent également fournir des signatures numériques avec leurs exécutables binaires.</span><span class="sxs-lookup"><span data-stu-id="da9a0-118">Text service providers should also provide digital signatures with their binary executables.</span></span> <span data-ttu-id="da9a0-119">Consultez [Présentation de la signature de code](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="da9a0-119">See [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span></span>

## <a name="registering-the-text-service"></a><span data-ttu-id="da9a0-120">Inscription du service de texte</span><span class="sxs-lookup"><span data-stu-id="da9a0-120">Registering the Text Service</span></span>

<span data-ttu-id="da9a0-121">Un service de texte s’inscrit auprès de TSF en appelant [ITfInputProcessorProfiles :: Register](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register) avec l’identificateur de classe du service de texte.</span><span class="sxs-lookup"><span data-stu-id="da9a0-121">A text service registers itself with TSF by calling [ITfInputProcessorProfiles::Register](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register) with the class identifier of the text service.</span></span> <span data-ttu-id="da9a0-122">Une instance de l’interface **ITfInputProcessorProfiles** est obtenue en appelant **COCREATEINSTANCE** avec le CLSID \_ tf \_ InputProcessorProfiles.</span><span class="sxs-lookup"><span data-stu-id="da9a0-122">An instance of the **ITfInputProcessorProfiles** interface is obtained by calling **CoCreateInstance** with CLSID\_TF\_InputProcessorProfiles.</span></span>

<span data-ttu-id="da9a0-123">L’exemple suivant montre comment créer un objet **ITfInputProcessorProfiles** et inscrire le service de texte.</span><span class="sxs-lookup"><span data-stu-id="da9a0-123">The following example demonstrates how to create an **ITfInputProcessorProfiles** object and register the text service.</span></span>


```C++
BOOL RegisterTextService(CLSID clsidTextService)
{
    HRESULT hr;
    ITfInputProcessorProfiles *pInputProcessProfiles;

    hr = CoCreateInstance(  CLSID_TF_InputProcessorProfiles, 
                            NULL, 
                            CLSCTX_INPROC_SERVER,
                            IID_ITfInputProcessorProfiles, 
                            (LPVOID*)&pInputProcessProfiles);

    if (hr != S_OK)
    {
        return FALSE;
    }

    hr = pInputProcessProfiles->Register(clsidTextService);

    pInputProcessProfiles->Release();
    
    return (S_OK == hr);
}
```



[<span data-ttu-id="da9a0-124">ITfInputProcessorProfiles :: Unregister</span><span class="sxs-lookup"><span data-stu-id="da9a0-124">ITfInputProcessorProfiles::Unregister</span></span>](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-unregister)

## <a name="registering-language-profiles"></a><span data-ttu-id="da9a0-125">Inscription des profils de langue</span><span class="sxs-lookup"><span data-stu-id="da9a0-125">Registering Language Profiles</span></span>

<span data-ttu-id="da9a0-126">Un service de texte est disponible uniquement lorsqu’une application a le focus et que la langue appropriée est sélectionnée dans la barre de langue.</span><span class="sxs-lookup"><span data-stu-id="da9a0-126">A text service is only available when an application has the focus and the proper language is selected in the language bar.</span></span> <span data-ttu-id="da9a0-127">Pour faciliter cette opération, TSF requiert qu’un service de texte s’inscrit lui-même pour tous les langages qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="da9a0-127">To facilitate this, TSF requires that a text service register itself for all of the languages that it supports.</span></span> <span data-ttu-id="da9a0-128">Le service de texte inscrit ses profils de langage en appelant [ITfInputProcessorProfiles :: AddLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile) avec l’identificateur de classe de service de texte, cet identificateur de langue du profil et un **GUID** défini par le service de texte qui identifie le profil de langue.</span><span class="sxs-lookup"><span data-stu-id="da9a0-128">The text service registers its language profiles by calling [ITfInputProcessorProfiles::AddLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile) with the text service class identifier, that language identifier of the profile, and a text service defined **GUID** that identifies the language profile.</span></span>

<span data-ttu-id="da9a0-129">Vous pouvez supprimer un profil de langue en appelant [ITfInputProcessorProfiles :: RemoveLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile).</span><span class="sxs-lookup"><span data-stu-id="da9a0-129">A language profile can be removed by calling [ITfInputProcessorProfiles::RemoveLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile).</span></span> <span data-ttu-id="da9a0-130">**ITfInputProcessorProfiles :: Unregister** supprime tous les profils de langue pour le service de texte ; Lorsqu’un service de texte est désinstallé, il est nécessaire de supprimer les profils de langue individuels.</span><span class="sxs-lookup"><span data-stu-id="da9a0-130">**ITfInputProcessorProfiles::Unregister** removes all language profiles for the text service; when a text service is uninstalled, it does require removal of the individual language profiles.</span></span>

## <a name="registering-categories"></a><span data-ttu-id="da9a0-131">Inscription des catégories</span><span class="sxs-lookup"><span data-stu-id="da9a0-131">Registering Categories</span></span>

<span data-ttu-id="da9a0-132">Un service de texte doit également inscrire la catégorie à laquelle s’applique le service de texte.</span><span class="sxs-lookup"><span data-stu-id="da9a0-132">A text service must also register the category that the text service applies to.</span></span> <span data-ttu-id="da9a0-133">Par exemple, si le service de texte fournit des informations sur les attributs d’affichage, il doit s’inscrire en tant que fournisseur d’attributs d’affichage en appelant [ITfCategoryMgr :: RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) avec l’identificateur de classe du service de texte pour le premier paramètre, Guid \_ TFCAT \_ DISPLAYATTRIBUTEPROVIDER pour le deuxième paramètre et l’identificateur de classe du service de texte pour le troisième paramètre.</span><span class="sxs-lookup"><span data-stu-id="da9a0-133">For example, if the text service supplies display attribute information, it must register itself as a display attribute provider by calling [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) with the class identifier of the text service for the first parameter, GUID\_TFCAT\_DISPLAYATTRIBUTEPROVIDER for the second parameter and the class identifier of the text service again for the third parameter.</span></span> <span data-ttu-id="da9a0-134">Les catégories possibles sont répertoriées sous [valeurs des catégories prédéfinies](predefined-category-values.md).</span><span class="sxs-lookup"><span data-stu-id="da9a0-134">The possible categories are listed under [Predefined Category Values](predefined-category-values.md).</span></span>

<span data-ttu-id="da9a0-135">Supprimez les catégories précédemment inscrites en appelant [ITfCategoryMgr :: UnregisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-unregistercategory).</span><span class="sxs-lookup"><span data-stu-id="da9a0-135">Remove previously registered categories by calling [ITfCategoryMgr::UnregisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-unregistercategory).</span></span> <span data-ttu-id="da9a0-136">ITfInputProcessorProfiles :: unregister Supprime toutes les catégories pour le service de texte ; Lorsqu’un service de texte est désinstallé, il doit supprimer les différentes catégories.</span><span class="sxs-lookup"><span data-stu-id="da9a0-136">ITfInputProcessorProfiles::Unregister removes all categories for the text service; when a text service is uninstalled, it must remove the individual categories.</span></span>

 

 