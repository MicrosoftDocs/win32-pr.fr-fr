---
description: Utilisation de Windows Media avec les services de modification DirectShow
ms.assetid: 26a88197-ec80-4443-9d50-e11df40dd1eb
title: Utilisation de Windows Media avec les services de modification DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fbfe715495834217b695f887305f1ecb21cb6f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106539786"
---
# <a name="using-windows-media-with-directshow-editing-services"></a><span data-ttu-id="dfaa6-103">Utilisation de Windows Media avec les services de modification DirectShow</span><span class="sxs-lookup"><span data-stu-id="dfaa6-103">Using Windows Media With DirectShow Editing Services</span></span>

<span data-ttu-id="dfaa6-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="dfaa6-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="dfaa6-105">Cette section décrit comment utiliser du contenu Windows Media dans une application des [services de modification DirectShow](directshow-editing-services.md) .</span><span class="sxs-lookup"><span data-stu-id="dfaa6-105">This section describes how to use Windows Media–based content in a [DirectShow Editing Services](directshow-editing-services.md) (DES) application.</span></span> <span data-ttu-id="dfaa6-106">Il existe deux scénarios principaux :</span><span class="sxs-lookup"><span data-stu-id="dfaa6-106">There are two main scenarios:</span></span>

-   <span data-ttu-id="dfaa6-107">Éléments sources.</span><span class="sxs-lookup"><span data-stu-id="dfaa6-107">Source clips.</span></span> <span data-ttu-id="dfaa6-108">Un projet DES peut contenir des clips audio et vidéo de fichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dfaa6-108">A DES project can contain audio and video clips from Windows Media files.</span></span>
-   <span data-ttu-id="dfaa6-109">Format cible.</span><span class="sxs-lookup"><span data-stu-id="dfaa6-109">Target format.</span></span> <span data-ttu-id="dfaa6-110">Windows Media est un format idéal pour la sortie finale d’un projet de montage vidéo.</span><span class="sxs-lookup"><span data-stu-id="dfaa6-110">Windows Media is an ideal format for the final output of a video editing project.</span></span>

<span data-ttu-id="dfaa6-111">Pour travailler avec des fichiers Windows Media, l’application doit fournir un certificat logiciel, également appelé clé.</span><span class="sxs-lookup"><span data-stu-id="dfaa6-111">To work with Windows Media files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="dfaa6-112">Pour ce faire, il implémente un objet de fournisseur de clés.</span><span class="sxs-lookup"><span data-stu-id="dfaa6-112">It does this by implementing a key provider object.</span></span> <span data-ttu-id="dfaa6-113">Le fournisseur de clé est un objet COM qui expose l’interface **IServiceProvider** .</span><span class="sxs-lookup"><span data-stu-id="dfaa6-113">The key provider is a COM object the exposes the **IServiceProvider** interface.</span></span> <span data-ttu-id="dfaa6-114">Pour plus d’informations sur l’implémentation du fournisseur de clé, consultez [déverrouillage du kit de développement logiciel (SDK) de format Windows Media](unlocking-the-windows-media-format-sdk.md).</span><span class="sxs-lookup"><span data-stu-id="dfaa6-114">For information about implementing the key provider, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="dfaa6-115">Pour utiliser DES avec des fichiers Windows Media, les objets DES suivants nécessitent la clé logicielle :</span><span class="sxs-lookup"><span data-stu-id="dfaa6-115">To use DES with Windows Media files, the following DES objects require the software key:</span></span>

-   <span data-ttu-id="dfaa6-116">Moteur de rendu, pour l’aperçu ou l’écriture de fichiers.</span><span class="sxs-lookup"><span data-stu-id="dfaa6-116">The render engine, for previewing or file writing.</span></span>
-   <span data-ttu-id="dfaa6-117">Objet MediaDet, pour récupérer des images vidéo ou des types de média à partir de fichiers ASF.</span><span class="sxs-lookup"><span data-stu-id="dfaa6-117">The MediaDet object, to get video frames or media types from ASF files.</span></span>
-   <span data-ttu-id="dfaa6-118">\[! Précieuse\]</span><span class="sxs-lookup"><span data-stu-id="dfaa6-118">\[!Important\]</span></span>  
    > <span data-ttu-id="dfaa6-119">N’utilisez pas le moteur de rendu intelligent pour lire ou écrire des fichiers Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dfaa6-119">Do not use the Smart Render Engine to read or write Windows Media files.</span></span> <span data-ttu-id="dfaa6-120">Utilisez toujours le moteur de rendu de base (CLSID \_ RenderEngine).</span><span class="sxs-lookup"><span data-stu-id="dfaa6-120">Always use the Basic Render Engine (CLSID\_RenderEngine).</span></span>

     

<span data-ttu-id="dfaa6-121">Pour attribuer à un objet la clé logicielle, interrogez cet objet pour l’interface **IObjectWithSite** et appelez **IObjectWithSite :: sets** avec un pointeur vers votre fournisseur de clés.</span><span class="sxs-lookup"><span data-stu-id="dfaa6-121">To give an object the software key, query that object for the **IObjectWithSite** interface and call **IObjectWithSite::SetSite** with a pointer to your key provider.</span></span> <span data-ttu-id="dfaa6-122">Par exemple, le code suivant fournit la clé logicielle au moteur de rendu :</span><span class="sxs-lookup"><span data-stu-id="dfaa6-122">For example, the following code provides the software key to the render engine:</span></span>


```C++
// Create your key provider, using an application-defined function:
IServiceProvider *pKey;
hr = MyCreateKeyProviderFunction(&pKey);  

// Query the Render Engine for IObjectWithSite.
IObjectWithSite *pOWS;
hr = pRenderEngine->QueryInterface(__uuidof(IObjectWithSite), 
    reinterpret_cast<void**>(&pOWS));
if (SUCCEEDED(hr))
{
    // Give it your key provider.
    hr = pOWS->SetSite(pKey);
    pOWS->Release();
}
pKey->Release();
```



<span data-ttu-id="dfaa6-123">Pour utiliser des clips source Windows Media dans un projet DES, appelez simplement **IObjectWithSite :: SetSite** sur le moteur de rendu avec un pointeur vers votre fournisseur de clés.</span><span class="sxs-lookup"><span data-stu-id="dfaa6-123">To use Windows Media source clips in a DES project, simply call **IObjectWithSite::SetSite** on the render engine with a pointer to your key provider.</span></span>

<span data-ttu-id="dfaa6-124">Pour plus d’informations sur l’écriture de fichiers Windows Media, consultez [écriture d’un fichier Windows Media dans des](writing-a-windows-media-file-in-des.md).</span><span class="sxs-lookup"><span data-stu-id="dfaa6-124">For information about writing Windows Media files, see [Writing a Windows Media File in DES](writing-a-windows-media-file-in-des.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dfaa6-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dfaa6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfaa6-126">Utilisation des services de modification DirectShow</span><span class="sxs-lookup"><span data-stu-id="dfaa6-126">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



