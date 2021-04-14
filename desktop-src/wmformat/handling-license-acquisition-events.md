---
title: Gestion des événements d’acquisition de licence
description: Gestion des événements d’acquisition de licence
ms.assetid: e118bf09-1fa6-41b6-a6bb-3e8cb6097994
keywords:
- Windows Media Format SDK, gestion des événements d’acquisition de licence
- Windows Media Format SDK, événements d’acquisition de licence
- ASF (Advanced Systems Format), gestion des événements d’acquisition de licence
- ASF (format de systèmes avancés), gestion des événements d’acquisition de licence
- ASF (Advanced Systems Format), événements d’acquisition de licence
- ASF (format de systèmes avancés), événements d’acquisition de licence
- gestion des droits numériques (DRM), gestion des événements d’acquisition de licence
- DRM (gestion des droits numériques), gestion des événements d’acquisition de licence
- gestion des droits numériques (DRM), événements d’acquisition de licence
- DRM (gestion des droits numériques), événements d’acquisition de licence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e31fd5b108f41d5b0925918fdf1c83764bcf7e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381519"
---
# <a name="handling-license-acquisition-events"></a><span data-ttu-id="72c35-113">Gestion des événements d’acquisition de licence</span><span class="sxs-lookup"><span data-stu-id="72c35-113">Handling License Acquisition Events</span></span>

<span data-ttu-id="72c35-114">Une application de lecteur compatible DRM, dans sa méthode de rappel [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) , gère les quatre événements suivants liés au processus d’acquisition de licence :</span><span class="sxs-lookup"><span data-stu-id="72c35-114">A DRM-enabled reader application, in its [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method, handles the following four events related to the license acquisition process:</span></span>

-   <span data-ttu-id="72c35-115">**État de la \_ signature LICENSEURL WMT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="72c35-115">**WMT\_LICENSEURL\_SIGNATURE\_STATE**</span></span>
-   <span data-ttu-id="72c35-116">**WMT \_ aucun \_ droit**</span><span class="sxs-lookup"><span data-stu-id="72c35-116">**WMT\_NO\_RIGHTS**</span></span>
-   <span data-ttu-id="72c35-117">**WMT \_ aucun \_ droit \_ ex**</span><span class="sxs-lookup"><span data-stu-id="72c35-117">**WMT\_NO\_RIGHTS\_EX**</span></span>
-   <span data-ttu-id="72c35-118">**\_licence d’acquisition WMT \_**</span><span class="sxs-lookup"><span data-stu-id="72c35-118">**WMT\_ACQUIRE\_LICENSE**</span></span>

<span data-ttu-id="72c35-119">**État de la \_ signature LICENSEURL WMT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="72c35-119">**WMT\_LICENSEURL\_SIGNATURE\_STATE**</span></span>

<span data-ttu-id="72c35-120">Lorsque le composant DRM détecte un contenu protégé par la version 7 de DRM, il recherche d’abord une licence valide sur le système local.</span><span class="sxs-lookup"><span data-stu-id="72c35-120">When the DRM component detects content protected by DRM version 7, it first looks for a valid license on the local system.</span></span> <span data-ttu-id="72c35-121">S’il n’en existe aucun, il évalue l’URL d’acquisition de licence dans l’en-tête DRM du fichier et envoie un  événement d' **\_ \_ \_ État de signature LICENSEURL WMT** avec pValue défini sur l’une des valeurs d’approbation de l' [**\_ DRMLA \_ WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) , indiquant si l’URL est approuvée, non approuvée ou a été falsifiée.</span><span class="sxs-lookup"><span data-stu-id="72c35-121">If none exists, it then evaluates the license acquisition URL in the file's DRM header and sends a **WMT\_LICENSEURL\_SIGNATURE\_STATE** event with *pValue* set to one of the [**WMT\_DRMLA\_TRUST**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) values, indicating whether the URL is trusted, untrusted, or has been tampered with.</span></span> <span data-ttu-id="72c35-122">Si l’URL n’est pas approuvée, l’application doit avertir l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="72c35-122">If the URL is not trusted, then the application should warn the user.</span></span> <span data-ttu-id="72c35-123">Si l’URL a été falsifiée, le fichier doit être considéré comme endommagé, et l’application ne doit pas accéder à l’URL sans émettre de message d’avertissement fort à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="72c35-123">If the URL has been tampered with, then the file should be considered corrupted, and the application should not navigate to the URL without issuing a strong warning the user.</span></span>

<span data-ttu-id="72c35-124">**WMT \_ aucun \_ droit**</span><span class="sxs-lookup"><span data-stu-id="72c35-124">**WMT\_NO\_RIGHTS**</span></span>

<span data-ttu-id="72c35-125">L’événement **WMT \_ no \_ Rights** n’est envoyé que pour le contenu DRM version 1, ce qui signifie que la licence doit être acquise non silencieusement.</span><span class="sxs-lookup"><span data-stu-id="72c35-125">The **WMT\_NO\_RIGHTS** event is sent only for DRM version 1 content, which means that the license must be acquired non-silently.</span></span> <span data-ttu-id="72c35-126">En d’autres termes, l’utilisateur doit accéder à une page Web pour obtenir une licence.</span><span class="sxs-lookup"><span data-stu-id="72c35-126">In other words, the user must navigate to a Web page to acquire a license.</span></span> <span data-ttu-id="72c35-127">L’URL de la page est récupérée sous la forme d’une chaîne à caractères larges se terminant par un caractère null à partir du paramètre *pValue* dans la méthode **OnStatus** .</span><span class="sxs-lookup"><span data-stu-id="72c35-127">The URL for the page is retrieved as a wide-character null-terminated string from the *pValue* parameter in the **OnStatus** method.</span></span>

<span data-ttu-id="72c35-128">Le cas échéant, une application peut permettre à l’utilisateur de naviguer plus facilement vers la page Web, soit en ouvrant Internet Explorer dans un processus distinct, soit en hébergeant le contrôle de navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="72c35-128">If appropriate, an application can make it easier for the user to navigate to the Web page, either by opening up Internet Explorer in a separate process or else by hosting the Web Browser control.</span></span> <span data-ttu-id="72c35-129">Toutefois, cela n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="72c35-129">This is not required, however.</span></span> <span data-ttu-id="72c35-130">Au minimum, une application peut simplement afficher l’URL de l’utilisateur dans une boîte de message et l’inviter à la coller dans la barre d’adresses d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="72c35-130">At the very least, an application could simply display the URL to the user in a message box and prompt them to paste it into the address bar of Internet Explorer.</span></span> <span data-ttu-id="72c35-131">L’exemple audioplayer illustre la gestion appropriée de l’événement de **\_ non- \_ autorisation WMT** , notamment la mise en forme de la chaîne d’URL et l’utilisation de la méthode **CreateProcess** pour ouvrir Internet Explorer et accéder à l’URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="72c35-131">The Audioplayer sample demonstrates proper handling of the **WMT\_NO\_RIGHTS** event, including how to format the URL string, and how to use the **CreateProcess** method to open Internet Explorer and navigate to the specified URL.</span></span>

<span data-ttu-id="72c35-132">Étant donné que l’application n’a aucun moyen de savoir quand une licence DRM version 1 a été acquise, il revient à l’utilisateur d’essayer d’ouvrir à nouveau le fichier après avoir acquis la licence.</span><span class="sxs-lookup"><span data-stu-id="72c35-132">Because the application has no way of knowing when a DRM version 1 license has been acquired, it is up to the user to attempt to open the file again after acquiring the license.</span></span>

<span data-ttu-id="72c35-133">Ce même processus d’acquisition de licence non silencieuse peut également être utilisé pour les licences de la version 7, mais dans ce cas, l’application peut commencer par appeler [**IWMDRMReader :: MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition).</span><span class="sxs-lookup"><span data-stu-id="72c35-133">This same non-silent license acquisition process can also be used for version 7 licenses, but in this case the application can first call [**IWMDRMReader::MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition).</span></span> <span data-ttu-id="72c35-134">Cette méthode permet de vérifier la Banque de licences locale de manière répétée jusqu’à ce que la licence du nouveau fichier soit trouvée.</span><span class="sxs-lookup"><span data-stu-id="72c35-134">This method will cause the local license store to be checked repeatedly until the license for the new file is found.</span></span> <span data-ttu-id="72c35-135">À ce stade, l’application recevra un événement d' **\_ acquisition de \_ licence WMT** .</span><span class="sxs-lookup"><span data-stu-id="72c35-135">At that point, the application will receive a **WMT\_ACQUIRE\_LICENSE** event.</span></span> <span data-ttu-id="72c35-136">Pour toutes les licences de la version 7, il est recommandé que les applications offrent aux utilisateurs la possibilité d’obtenir des licences en mode silencieux ou non en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="72c35-136">For all version 7 licenses, it is recommended that applications give users the option to obtain licenses silently or non-silently.</span></span>

<span data-ttu-id="72c35-137">**WMT \_ aucun \_ droit \_ ex**</span><span class="sxs-lookup"><span data-stu-id="72c35-137">**WMT\_NO\_RIGHTS\_EX**</span></span>

<span data-ttu-id="72c35-138">L’événement **WMT \_ no \_ Rights \_** (par exemple) indique que le contenu est protégé par DRM version 7. par conséquent, le processus d’acquisition de licence peut être exécuté en mode silencieux ou non en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="72c35-138">The **WMT\_NO\_RIGHTS\_EX** event indicates that the content is protected by DRM version 7, and therefore the license acquisition process can proceed either silently or non-silently.</span></span> <span data-ttu-id="72c35-139">En général, l’acquisition de licence silencieuse est plus pratique pour les utilisateurs finaux, bien que certaines personnes préfèrent acquérir toutes les licences de manière non silencieuse.</span><span class="sxs-lookup"><span data-stu-id="72c35-139">In general, silent license acquisition is more convenient for end users, although some people prefer to acquire all licenses non-silently.</span></span> <span data-ttu-id="72c35-140">Lorsque l’acquisition de licence oblige l’utilisateur à soumettre des informations personnelles ou de paiement, le processus doit toujours être effectué de manière non silencieuse.</span><span class="sxs-lookup"><span data-stu-id="72c35-140">When license acquisition requires the user to submit payment or personal information, the process should always be performed non-silently.</span></span> <span data-ttu-id="72c35-141">L’acquisition de licence non silencieuse est décrite ci-dessus sous l’en-tête de **\_ non- \_ autorisation WMT** .</span><span class="sxs-lookup"><span data-stu-id="72c35-141">Non-silent license acquisition is described above under the **WMT\_NO\_RIGHTS** heading.</span></span> <span data-ttu-id="72c35-142">L’acquisition en mode silencieux se déroule comme suit :</span><span class="sxs-lookup"><span data-stu-id="72c35-142">Silent acquisition proceeds as follows:</span></span>

1.  <span data-ttu-id="72c35-143">Effectuez un cast du paramètre *pValue* en une structure de [**\_ \_ \_ données de licence WM**](wm-get-license-data.md) et stockez la structure au cas où elle serait nécessaire ultérieurement pour une acquisition de licence non silencieuse.</span><span class="sxs-lookup"><span data-stu-id="72c35-143">Cast the *pValue* parameter to a [**WM\_GET\_LICENSE\_DATA**](wm-get-license-data.md) structure and store the structure in case it is needed later for non-silent license acquisition.</span></span>
2.  <span data-ttu-id="72c35-144">Appelez **QueryInterface** sur l’objet lecteur pour obtenir l’interface [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) .</span><span class="sxs-lookup"><span data-stu-id="72c35-144">Call **QueryInterface** on the reader object to obtain the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface.</span></span>
3.  <span data-ttu-id="72c35-145">Appelez [**IWMDRMReader :: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) et spécifiez 0x1 dans le paramètre *dwFlags* pour indiquer l’acquisition en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="72c35-145">Call [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) and specify 0x1 in the *dwFlags* parameter to indicate silent language acquisition.</span></span> <span data-ttu-id="72c35-146">Il s’agit d’un appel asynchrone qui est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="72c35-146">This is an asynchronous call that returns immediately.</span></span>
4.  <span data-ttu-id="72c35-147">Attendez l’événement **d' \_ acquisition de \_ licence WMT** .</span><span class="sxs-lookup"><span data-stu-id="72c35-147">Wait for the **WMT\_ACQUIRE\_LICENSE** event.</span></span>

<span data-ttu-id="72c35-148">**\_licence d’acquisition WMT \_**</span><span class="sxs-lookup"><span data-stu-id="72c35-148">**WMT\_ACQUIRE\_LICENSE**</span></span>

<span data-ttu-id="72c35-149">L’événement d’acquisition de **\_ \_ licence WMT** est envoyé une fois que le processus d’acquisition de licence est terminé pour une licence DRM version 7.</span><span class="sxs-lookup"><span data-stu-id="72c35-149">The **WMT\_ACQUIRE\_LICENSE** event is sent after the license acquisition process is completed for a DRM version 7 license.</span></span> <span data-ttu-id="72c35-150">[**IWMDRMReader :: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) entraîne l’envoi de cet événement pour l’acquisition en mode silencieux, et [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) provoque son envoi pour une acquisition non silencieuse.</span><span class="sxs-lookup"><span data-stu-id="72c35-150">[**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) causes this event to be sent for silent acquisition, and [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) causes it to be sent for non-silent acquisition.</span></span> <span data-ttu-id="72c35-151">Dans votre gestionnaire d’événements, castez *pValue* en pointeur vers une structure de [**\_ \_ \_ données de licence WM**](wm-get-license-data.md) et examinez le membre **HR** pour déterminer si la licence a été acquise avec succès.</span><span class="sxs-lookup"><span data-stu-id="72c35-151">In your event handler, cast *pValue* to a pointer to a [**WM\_GET\_LICENSE\_DATA**](wm-get-license-data.md) structure and examine the **hr** member to determine whether the license was successfully acquired.</span></span> <span data-ttu-id="72c35-152">Si **HR** est égal \_ à NS E \_ DRM \_ no \_ Rights, cela signifie que la licence doit être acquise non silencieusement.</span><span class="sxs-lookup"><span data-stu-id="72c35-152">If **hr** equals NS\_E\_DRM\_NO\_RIGHTS, it indicates that the license must be acquired non-silently.</span></span> <span data-ttu-id="72c35-153">Les applications doivent permettre aux utilisateurs d’annuler le processus d’acquisition de licence à tout moment.</span><span class="sxs-lookup"><span data-stu-id="72c35-153">Applications should enable users to cancel the license acquisition process at any time.</span></span> <span data-ttu-id="72c35-154">Pour ce faire, appelez [**IWMDRMReader :: CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition).</span><span class="sxs-lookup"><span data-stu-id="72c35-154">This is done by calling [**IWMDRMReader::CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition).</span></span> <span data-ttu-id="72c35-155">L’appel de cette méthode enverra un événement d' **\_ acquisition de \_ licence WMT** avec une valeur **HRESULT** de NS \_ S \_ DRM \_ Acquire \_ Cancelled.</span><span class="sxs-lookup"><span data-stu-id="72c35-155">Calling this method will send a **WMT\_ACQUIRE\_LICENSE** event with an **HRESULT** value of NS\_S\_DRM\_ACQUIRE\_CANCELLED.</span></span>

<span data-ttu-id="72c35-156">Si **HR** est égal à \_ \_ la licence DRM de NS S \_ \_ acquise, la licence a été acquise et l’application peut tenter de lire le fichier, ou la copier sur un périphérique ou exécuter l’action pour laquelle il a demandé des droits.</span><span class="sxs-lookup"><span data-stu-id="72c35-156">If **hr** equals NS\_S\_DRM\_LICENSE\_ACQUIRED, then the license has been acquired and the application can attempt to play the file, or copy it to a device or perform whatever action it had requested rights for.</span></span>

<span data-ttu-id="72c35-157">Sur Windows XP, un nouveau code d’erreur a été introduit \_ : \_ NOTACQUIRED de licence DRM E \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="72c35-157">On Windows XP, a new error code was introduced: NS\_E\_DRM\_LICENSE\_NOTACQUIRED.</span></span> <span data-ttu-id="72c35-158">Ce code d’erreur est généré chaque fois que les composants Windows Media Format Runtime sur Windows XP ne parviennent pas à acquérir une licence lors de l’acquisition d’une licence en mode silencieux ou non silencieuse.</span><span class="sxs-lookup"><span data-stu-id="72c35-158">This error code is generated whenever the Windows Media Format run-time components on Windows XP fail to acquire a license during silent or non-silent license acquisition.</span></span> <span data-ttu-id="72c35-159">Sur les autres plateformes, une \_ \_ Erreur du magasin de licences DRM E \_ \_ \_ est généralement retournée lorsque l’acquisition de la licence échoue.</span><span class="sxs-lookup"><span data-stu-id="72c35-159">On other platforms, NS\_E\_DRM\_LICENSE\_STORE\_ERROR is usually returned when license acquisition fails.</span></span> <span data-ttu-id="72c35-160">Le nouveau code d’erreur est destiné à distinguer l’échec d’acquisition de licence des autres conditions d’échec où une \_ \_ erreur de magasin de licences DRM E \_ \_ \_ a été générée.</span><span class="sxs-lookup"><span data-stu-id="72c35-160">The new error code is intended to distinguish license acquisition failure from other failure conditions where NS\_E\_DRM\_LICENSE\_STORE\_ERROR is generated.</span></span>

<span data-ttu-id="72c35-161">La méthode recommandée pour gérer ces erreurs lorsqu’elles sont retournées après une tentative d’acquisition de licence en mode silencieux est indiquée dans l’extrait de code suivant :</span><span class="sxs-lookup"><span data-stu-id="72c35-161">The recommended way to handle these errors when they are returned after a silent license acquisition attempt is shown in the following code snippet:</span></span>


```C++
if( hrStatus == NS_E_DRM_LICENSE_NOTACQUIRED || 
    hrStatus == NS_E_DRM_LICENSE_STORE_ERROR )
{
  // Attempt non-silent license acquisition.
}
else if( hrStatus == NS_E_DRM_NEEDS_INDIVIDUALIZATION )
{
  // Individualize and then retry.
}
else if( FAILED(hrStatus) )
{
  // Display a helpful error message.
}
else
{
  // Success. Play content.
}
```



> [!Note]  
> <span data-ttu-id="72c35-162">DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="72c35-162">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="72c35-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="72c35-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72c35-164">**Lecture des fichiers protégés**</span><span class="sxs-lookup"><span data-stu-id="72c35-164">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 




