---
title: Pour définir les paramètres d’entrée
description: Pour définir les paramètres d’entrée
ms.assetid: 288801a7-793f-43bd-9c5a-f9e1bd86ecc3
keywords:
- ASF (Advanced Systems Format), paramètres d’entrée
- ASF (format des systèmes avancés), paramètres d’entrée
- profils, paramètres d’entrée
- codecs, paramètres d’entrée
- flux, paramètres d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e7b2db64a7346cc8b9d46c48f0add79dafcac95
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103940693"
---
# <a name="to-set-input-settings"></a><span data-ttu-id="881f7-108">Pour définir les paramètres d’entrée</span><span class="sxs-lookup"><span data-stu-id="881f7-108">To Set Input Settings</span></span>

<span data-ttu-id="881f7-109">Les propriétés de base des médias d’entrée et de flux de données sont définies par la structure du [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) .</span><span class="sxs-lookup"><span data-stu-id="881f7-109">The basic properties of input media and stream media are defined by the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="881f7-110">Pour les formats d’entrée, les informations sur le type de média sont définies par votre application.</span><span class="sxs-lookup"><span data-stu-id="881f7-110">For input formats, the media type information is set by your application.</span></span> <span data-ttu-id="881f7-111">Pour les formats de flux, les informations sur le type de média sont définies dans le profil que vous attribuez au writer.</span><span class="sxs-lookup"><span data-stu-id="881f7-111">For stream formats, the media type information is set in the profile you assign to the writer.</span></span> <span data-ttu-id="881f7-112">Certaines propriétés sont indépendantes du type de média et doivent être définies pour une entrée avant le début de l’écriture.</span><span class="sxs-lookup"><span data-stu-id="881f7-112">Some properties are independent of media type and must be set for an input before writing begins.</span></span> <span data-ttu-id="881f7-113">Ces propriétés sont des fonctionnalités de codec et d’écriture indépendantes du type de flux. elles doivent être définies une fois que le profil a été affecté dans le writer, mais avant le début de l’écriture.</span><span class="sxs-lookup"><span data-stu-id="881f7-113">These properties are codec and writer features that are independent of stream type, and must be set after the profile is assigned in the writer but before writing begins.</span></span>

<span data-ttu-id="881f7-114">La définition d’un paramètre d’entrée requiert un appel à [**IWMWriterAdvanced2 :: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span><span class="sxs-lookup"><span data-stu-id="881f7-114">Setting an input setting requires a call to [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span></span> <span data-ttu-id="881f7-115">Vous pouvez également vérifier la valeur actuelle d’un paramètre à l’aide d’un appel à [**IWMWriterAdvanced2 :: GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting).</span><span class="sxs-lookup"><span data-stu-id="881f7-115">You can also check the current value of a setting with a call to [**IWMWriterAdvanced2::GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting).</span></span>

## <a name="related-topics"></a><span data-ttu-id="881f7-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="881f7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="881f7-117">**Pour utiliser des profils avec l’auteur**</span><span class="sxs-lookup"><span data-stu-id="881f7-117">**To Use Profiles with the Writer**</span></span>](to-use-profiles-with-the-writer.md)
</dt> <dt>

[<span data-ttu-id="881f7-118">**Écriture de fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="881f7-118">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> <dt>

[<span data-ttu-id="881f7-119">**Écriture de flux d’images**</span><span class="sxs-lookup"><span data-stu-id="881f7-119">**Writing Image Streams**</span></span>](writing-image-streams.md)
</dt> </dl>

 

 




