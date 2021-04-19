---
description: Comment lire des fichiers qui contiennent des médias protégés par DRM.
ms.assetid: 85d98f49-8af2-42ce-9b36-a025aee93f73
title: Comment lire des fichiers multimédias protégés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f8f7af78881e43f2f7f85e8f333ab31b1bc2de
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106537170"
---
# <a name="how-to-play-protected-media-files"></a><span data-ttu-id="343fe-103">Comment lire des fichiers multimédias protégés</span><span class="sxs-lookup"><span data-stu-id="343fe-103">How to Play Protected Media Files</span></span>

<span data-ttu-id="343fe-104">Un fichier multimédia protégé est un fichier multimédia associé à des règles d’utilisation du contenu.</span><span class="sxs-lookup"><span data-stu-id="343fe-104">A protected media file is any media file that has associated rules for using the content.</span></span> <span data-ttu-id="343fe-105">Dans certains cas, un fichier multimédia protégé est chiffré à l’aide d’une forme de chiffrement DRM (Digital Rights Management).</span><span class="sxs-lookup"><span data-stu-id="343fe-105">In some cases, a protected media file is encrypted using some form of digital rights management (DRM) encryption.</span></span> <span data-ttu-id="343fe-106">Pour lire un fichier multimédia protégé, la lecture doit être effectuée à l’intérieur du chemin d’accès du support protégé (PMP).</span><span class="sxs-lookup"><span data-stu-id="343fe-106">To play a protected media file, playback must occur inside the protected media path (PMP).</span></span> <span data-ttu-id="343fe-107">En outre, l’utilisateur peut avoir à acquérir des droits sur le contenu.</span><span class="sxs-lookup"><span data-stu-id="343fe-107">In addition, the user might have to acquire rights to the content.</span></span>

<span data-ttu-id="343fe-108">Le terme acquisition des droits fait référence à toute action que l’application doit exécuter avant que l’utilisateur puisse lire le contenu.</span><span class="sxs-lookup"><span data-stu-id="343fe-108">The term rights acquisition refers to any action that the application must perform before the user can play the content.</span></span> <span data-ttu-id="343fe-109">L’exemple le plus courant consiste à obtenir une licence DRM, mais Media Foundation définit un mécanisme générique qui peut prendre en charge d’autres types d’acquisition de droits.</span><span class="sxs-lookup"><span data-stu-id="343fe-109">The most common example is obtaining a DRM license, but Media Foundation defines a generic mechanism that can support other types of rights acquisition.</span></span> <span data-ttu-id="343fe-110">L’interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) définit ce mécanisme générique.</span><span class="sxs-lookup"><span data-stu-id="343fe-110">The [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface defines this generic mechanism.</span></span>

<span data-ttu-id="343fe-111">L’acquisition des droits doit être effectuée en dehors du PMP, du processus de l’application.</span><span class="sxs-lookup"><span data-stu-id="343fe-111">Rights acquisition must be done outside of the PMP, from the application process.</span></span> <span data-ttu-id="343fe-112">La session multimédia avertit l’application par le biais de l’interface [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) , qui est implémentée par l’application.</span><span class="sxs-lookup"><span data-stu-id="343fe-112">The Media Session notifies the application through the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface, which is implemented by the application.</span></span> <span data-ttu-id="343fe-113">La session multimédia utilise l’interface **IMFContentProtectionManager** pour transférer un objet d’activateur de contenu à l’application.</span><span class="sxs-lookup"><span data-stu-id="343fe-113">The Media Session uses the **IMFContentProtectionManager** interface to forward a content enabler object to the application.</span></span> <span data-ttu-id="343fe-114">Les activateurs de contenu implémentent l’interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .</span><span class="sxs-lookup"><span data-stu-id="343fe-114">Content enablers implement the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span> <span data-ttu-id="343fe-115">L’application utilise cette interface pour acquérir les droits nécessaires.</span><span class="sxs-lookup"><span data-stu-id="343fe-115">The application uses this interface to acquire the necessary rights.</span></span>

<span data-ttu-id="343fe-116">Un activateur de contenu peut prendre en charge l’acquisition de droits automatique, auquel cas l’activateur de contenu implémente l’ensemble du processus, et l’application surveille simplement l’État.</span><span class="sxs-lookup"><span data-stu-id="343fe-116">A content enabler might support automatic rights acquisition, in which case the content enabler implements the entire process, and the application simply monitors the status.</span></span> <span data-ttu-id="343fe-117">Dans le cas contraire, l’application doit utiliser l’acquisition des droits non silencieux, qui est un processus dans lequel l’application envoie des données HTTP après à une URL fournie par l’activateur de contenu.</span><span class="sxs-lookup"><span data-stu-id="343fe-117">Otherwise, the application must use non-silent rights acquisition, which is a process where the application sends HTTP POST data to a URL provided by the content enabler.</span></span>

<span data-ttu-id="343fe-118">Pour lire un média protégé, une application suit les mêmes étapes que celles indiquées dans la rubrique [Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md), en suivant les étapes supplémentaires suivantes :</span><span class="sxs-lookup"><span data-stu-id="343fe-118">To play protected media, an application follows the same steps given in the topic [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md), with the following additional steps:</span></span>

1.  <span data-ttu-id="343fe-119">Demander si la source du média contient du contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="343fe-119">Query whether the media source contains protected content.</span></span> <span data-ttu-id="343fe-120">(Facultatif.)</span><span class="sxs-lookup"><span data-stu-id="343fe-120">(Optional.)</span></span>
2.  <span data-ttu-id="343fe-121">Créez la session multimédia dans le processus PMP au lieu du processus d’application.</span><span class="sxs-lookup"><span data-stu-id="343fe-121">Create the Media Session in the PMP process, instead of the application process.</span></span>
3.  <span data-ttu-id="343fe-122">Effectuer l’acquisition des droits, si elle est notifiée par la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="343fe-122">Perform rights acquisition, if notified to do so by the Media Session.</span></span> <span data-ttu-id="343fe-123">Cette opération est effectuée de façon asynchrone par l’application.</span><span class="sxs-lookup"><span data-stu-id="343fe-123">This operation is performed asynchronously by the application.</span></span>
4.  <span data-ttu-id="343fe-124">Terminez l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="343fe-124">Complete the asynchronous operation.</span></span>

## <a name="query-for-protected-content"></a><span data-ttu-id="343fe-125">Rechercher du contenu protégé</span><span class="sxs-lookup"><span data-stu-id="343fe-125">Query for Protected Content</span></span>

<span data-ttu-id="343fe-126">Pour demander si une source multimédia contient du contenu protégé, appelez la fonction [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) sur le descripteur de présentation de la source du média.</span><span class="sxs-lookup"><span data-stu-id="343fe-126">To query whether a media source contains protected content, call the [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) function on the media source's presentation descriptor.</span></span> <span data-ttu-id="343fe-127">Si la fonction retourne la valeur \_ OK, vous devez utiliser le PMP pour lire le contenu.</span><span class="sxs-lookup"><span data-stu-id="343fe-127">If the function returns S\_OK, you must use the PMP to play the content.</span></span> <span data-ttu-id="343fe-128">Si la fonction retourne la \_ valeur false, l’PMP n’est pas obligatoire et vous pouvez créer la session multimédia dans le processus d’application.</span><span class="sxs-lookup"><span data-stu-id="343fe-128">If the function returns S\_FALSE, the PMP is not required, and you can create the Media Session in the application process.</span></span> <span data-ttu-id="343fe-129">Vous pouvez également utiliser le PMP pour lire les deux types de contenu, protégés et non protégés.</span><span class="sxs-lookup"><span data-stu-id="343fe-129">Alternatively, you can use the PMP to play both types of content, protected and unprotected.</span></span> <span data-ttu-id="343fe-130">Dans ce cas, vous n’avez pas besoin d’appeler **MFRequireProtectedEnvironment**.</span><span class="sxs-lookup"><span data-stu-id="343fe-130">If you do that, you do not need to call **MFRequireProtectedEnvironment**.</span></span>

<span data-ttu-id="343fe-131">Pour plus d’informations sur les descripteurs de présentation, consultez [descripteurs de présentation](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="343fe-131">For more information about presentation descriptors, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

## <a name="create-the-pmp-media-session"></a><span data-ttu-id="343fe-132">Créer la session de média PMP</span><span class="sxs-lookup"><span data-stu-id="343fe-132">Create the PMP Media Session</span></span>

<span data-ttu-id="343fe-133">Pour créer la session multimédia dans le PMP, appelez [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span><span class="sxs-lookup"><span data-stu-id="343fe-133">To create the Media Session in the PMP, call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="343fe-134">Cette fonction est similaire à [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession), mais au lieu de créer la session multimédia dans le processus de l’application, elle crée la session multimédia dans le processus PMP.</span><span class="sxs-lookup"><span data-stu-id="343fe-134">This function is similar to [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession), but instead of creating the Media Session in the application's process, it creates the Media Session in the PMP process.</span></span> <span data-ttu-id="343fe-135">L’application reçoit un pointeur vers un objet proxy pour la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="343fe-135">The application receives a pointer to a proxy object for the Media Session.</span></span> <span data-ttu-id="343fe-136">L’application appelle les méthodes [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) sur l’objet proxy, tout comme il le ferait sur la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="343fe-136">The application calls [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) methods on the proxy object, just as it would on the Media Session.</span></span> <span data-ttu-id="343fe-137">L’objet proxy transfère les appels à la session multimédia à travers la limite de processus.</span><span class="sxs-lookup"><span data-stu-id="343fe-137">The proxy object forwards the calls to the Media Session across the process boundary.</span></span>

<span data-ttu-id="343fe-138">Créez la session de média PMP comme suit :</span><span class="sxs-lookup"><span data-stu-id="343fe-138">Create the PMP Media Session as follows:</span></span>

1.  <span data-ttu-id="343fe-139">Créez un nouveau magasin d’attributs en appelant [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span><span class="sxs-lookup"><span data-stu-id="343fe-139">Create a new attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="343fe-140">Définissez l' [**attribut \_ \_ Content \_ protection \_ Manager de la session MF**](mf-session-content-protection-manager-attribute.md) sur le magasin d’attributs.</span><span class="sxs-lookup"><span data-stu-id="343fe-140">Set the [**MF\_SESSION\_CONTENT\_PROTECTION\_MANAGER**](mf-session-content-protection-manager-attribute.md) attribute on the attribute store.</span></span> <span data-ttu-id="343fe-141">La valeur de cet attribut est un pointeur vers l’implémentation de [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)de votre application.</span><span class="sxs-lookup"><span data-stu-id="343fe-141">The value of this attribute is a pointer to your application's implementation of [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager).</span></span> <span data-ttu-id="343fe-142">Appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) pour définir l’attribut.</span><span class="sxs-lookup"><span data-stu-id="343fe-142">Call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) to set the attribute.</span></span>
3.  <span data-ttu-id="343fe-143">Appelez [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) pour créer la session multimédia dans le processus PMP.</span><span class="sxs-lookup"><span data-stu-id="343fe-143">Call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the Media Session in the PMP process.</span></span> <span data-ttu-id="343fe-144">Le paramètre *pConfiguration* est un pointeur vers l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) du magasin d’attributs.</span><span class="sxs-lookup"><span data-stu-id="343fe-144">The *pConfiguration* parameter is a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface of the attribute store.</span></span>


```C++
IMFAttributes *pAttributes = NULL;
IMFMediaSession *pSession = NULL;

// Create the attribute store.
hr = MFCreateAttributes(&pAttributes, 1);

// Set the IMFContentProtectionManager pointer.
if (SUCCEEDED(hr))
{
    hr = pAttributes->SetUnknown(
        MF_SESSION_CONTENT_PROTECTION_MANAGER, 
        pCPM  // Your implementation of IMFContentProtectionManager.
        );
}

// Create the Media Session.
if (SUCCEEDED(hr))
{
    hr = MFCreatePMPMediaSession(
        0,
        pAttributes, 
        &pSession,
        NULL
    );
}

SAFE_RELEASE(pAttributes); // Release the attribute store.
// Use the Media Session to control playback (not shown).
```



<span data-ttu-id="343fe-145">Ensuite, créez une topologie de lecture et la met en file d’attente sur la session multimédia, comme décrit dans [création de topologies de lecture](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="343fe-145">Next, create a playback topology and queue it on the Media Session, as described in [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

## <a name="perform-rights-acquisition"></a><span data-ttu-id="343fe-146">Effectuer une acquisition de droits</span><span class="sxs-lookup"><span data-stu-id="343fe-146">Perform Rights Acquisition</span></span>

<span data-ttu-id="343fe-147">Si la lecture nécessite une acquisition de droits, la session multimédia appelle [**IMFContentProtectionManager :: BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span><span class="sxs-lookup"><span data-stu-id="343fe-147">If playback requires rights acquisition, the Media Session calls [**IMFContentProtectionManager::BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span></span> <span data-ttu-id="343fe-148">Le paramètre *pEnablerActivate* de cette méthode est un pointeur vers l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="343fe-148">The *pEnablerActivate* parameter of this method is a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="343fe-149">Utilisez cette interface pour créer l’objet activateur de contenu, qui expose l’interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .</span><span class="sxs-lookup"><span data-stu-id="343fe-149">Use this interface to create the content enabler object, which exposes the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span> <span data-ttu-id="343fe-150">Utilisez ensuite l’activateur de contenu pour effectuer l’opération d’acquisition de droits.</span><span class="sxs-lookup"><span data-stu-id="343fe-150">Then use the content enabler to perform the rights acquisition step.</span></span>

<span data-ttu-id="343fe-151">Pour créer l’activateur de contenu, appelez [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject):</span><span class="sxs-lookup"><span data-stu-id="343fe-151">To create the content enabler, call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject):</span></span>


```C++
IMFContentEnabler *pEnabler = NULL;
hr = pEnablerActivate->ActivateObject(
    IID_IMFContentEnabler, 
    (void**)&pEnabler
    );
```



<span data-ttu-id="343fe-152">Interrogez le pointeur [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) retourné pour l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="343fe-152">Query the returned [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) pointer for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="343fe-153">Utilisez cette interface pour récupérer des événements de l’objet d’activation du contenu.</span><span class="sxs-lookup"><span data-stu-id="343fe-153">Use this interface to get events from the content enabler object.</span></span> <span data-ttu-id="343fe-154">Pour plus d’informations sur les événements, consultez [Media Event Generator](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="343fe-154">For more information about events, see [Media Event Generators](media-event-generators.md).</span></span>

<span data-ttu-id="343fe-155">Pour déterminer si l’activateur de contenu prend en charge l’acquisition automatique, appelez [**IMFContentEnabler :: IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported).</span><span class="sxs-lookup"><span data-stu-id="343fe-155">To find out whether the content enabler supports automatic acquisition, call [**IMFContentEnabler::IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported).</span></span> <span data-ttu-id="343fe-156">Si cette méthode retourne la valeur **true**, l’application doit utiliser l’acquisition automatique.</span><span class="sxs-lookup"><span data-stu-id="343fe-156">If this method returns the value **TRUE**, the application should use automatic acquisition.</span></span> <span data-ttu-id="343fe-157">Dans le cas contraire, utilisez une acquisition non silencieuse.</span><span class="sxs-lookup"><span data-stu-id="343fe-157">Otherwise, use non-silent acquisition.</span></span>

<span data-ttu-id="343fe-158">La méthode [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) est asynchrone.</span><span class="sxs-lookup"><span data-stu-id="343fe-158">The [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) method is asynchronous.</span></span> <span data-ttu-id="343fe-159">L’application doit effectuer l’étape d’acquisition sur le thread de l’application.</span><span class="sxs-lookup"><span data-stu-id="343fe-159">The application should perform the acquisition step on the application's thread.</span></span> <span data-ttu-id="343fe-160">Une approche consiste à poster un message de fenêtre privée dans la fenêtre principale de l’application, en notifiant au thread d’application d’effectuer l’acquisition.</span><span class="sxs-lookup"><span data-stu-id="343fe-160">One approach is to post a private window message to the application's main window, notifying the application thread to perform the acquisition.</span></span> <span data-ttu-id="343fe-161">Pendant que l’opération est en attente, l’application doit stocker le pointeur de rappel et l’objet d’État qu’il a reçu dans les paramètres *pCallback* et *punkState* de **BeginEnableContent**.</span><span class="sxs-lookup"><span data-stu-id="343fe-161">While the operation is pending, the application must store the callback pointer and the state object that it received in the *pCallback* and *punkState* parameters of **BeginEnableContent**.</span></span> <span data-ttu-id="343fe-162">Elles seront utilisées pour terminer l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="343fe-162">These will be used to complete the asynchronous operation.</span></span>

### <a name="automatic-acquisition"></a><span data-ttu-id="343fe-163">Acquisition automatique</span><span class="sxs-lookup"><span data-stu-id="343fe-163">Automatic Acquisition</span></span>

<span data-ttu-id="343fe-164">Pour effectuer une acquisition automatique, appelez [**IMFContentEnabler :: AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable).</span><span class="sxs-lookup"><span data-stu-id="343fe-164">To perform automatic acquisition, call [**IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable).</span></span> <span data-ttu-id="343fe-165">Cette méthode est asynchrone.</span><span class="sxs-lookup"><span data-stu-id="343fe-165">This method is asynchronous.</span></span> <span data-ttu-id="343fe-166">Une fois l’opération terminée, l’activateur de contenu envoie un événement [MEEnablerCompleted](meenablercompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="343fe-166">When the operation is completed, the content enabler sends an [MEEnablerCompleted](meenablercompleted.md) event.</span></span> <span data-ttu-id="343fe-167">Le code d’état de l’événement indique si l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="343fe-167">The event's status code indicates whether the operation was successful.</span></span> <span data-ttu-id="343fe-168">Si le code d’état de l’événement MEEnablerCompleted est NS \_ E \_ DRM \_ License \_ NOTACQUIRED, l’application doit essayer d’utiliser une acquisition non silencieuse.</span><span class="sxs-lookup"><span data-stu-id="343fe-168">If the status code from the MEEnablerCompleted event is NS\_E\_DRM\_LICENSE\_NOTACQUIRED, the application should try using non-silent acquisition.</span></span>

<span data-ttu-id="343fe-169">Pendant que l’opération d’acquisition est en cours, l’objet activateur peut envoyer l’événement [MEEnablerProgress](meenablerprogress.md) pour indiquer la progression de l’opération.</span><span class="sxs-lookup"><span data-stu-id="343fe-169">While the acquisition operation is in progress, the enabler object might send the [MEEnablerProgress](meenablerprogress.md) event to indicate the progress of the operation.</span></span> <span data-ttu-id="343fe-170">Pour annuler l’opération, appelez [**IMFContentEnabler :: Cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel).</span><span class="sxs-lookup"><span data-stu-id="343fe-170">To cancel the operation, call [**IMFContentEnabler::Cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel).</span></span>

### <a name="non-silent-acquisition"></a><span data-ttu-id="343fe-171">Acquisition non silencieuse</span><span class="sxs-lookup"><span data-stu-id="343fe-171">Non-Silent Acquisition</span></span>

<span data-ttu-id="343fe-172">Si la méthode [**IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) retourne la **valeur false** ou si la méthode [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) échoue avec le code d’erreur \_ NOTACQUIRED de \_ licence DRM E \_ \_ , l’application doit effectuer une acquisition non silencieuse comme décrit dans les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="343fe-172">If the [**IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) method returns **FALSE** or the [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) method fails with the error code NS\_E\_DRM\_LICENSE\_NOTACQUIRED, the application should perform non-silent acquisition as described in the following steps:</span></span>

1.  <span data-ttu-id="343fe-173">Appelez [**IMFContentEnabler :: GetEnableURL**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) pour obtenir l’URL de l’acquisition de droits.</span><span class="sxs-lookup"><span data-stu-id="343fe-173">Call [**IMFContentEnabler::GetEnableURL**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) to get the URL for the rights acquisition.</span></span> <span data-ttu-id="343fe-174">Cette méthode retourne également un indicateur qui spécifie si l’URL est approuvée.</span><span class="sxs-lookup"><span data-stu-id="343fe-174">This method also returns a flag indicating whether the URL is trusted.</span></span>
2.  <span data-ttu-id="343fe-175">Appelez [**IMFContentEnabler :: GetEnableData**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) pour accéder aux données http de publication.</span><span class="sxs-lookup"><span data-stu-id="343fe-175">Call [**IMFContentEnabler::GetEnableData**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) to get the HTTP POST data.</span></span>
3.  <span data-ttu-id="343fe-176">Appelez [**IMFContentEnabler :: MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable).</span><span class="sxs-lookup"><span data-stu-id="343fe-176">Call [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable).</span></span> <span data-ttu-id="343fe-177">Cette méthode permet à l’activateur du contenu de surveiller la progression de l’action d’acquisition des droits.</span><span class="sxs-lookup"><span data-stu-id="343fe-177">This method causes the content enabler to monitor the progress of the rights acquisition action.</span></span>

4.  <span data-ttu-id="343fe-178">Envoyer les données à l’URL d’acquisition des droits à l’aide d’une action HTTP POSTALe.</span><span class="sxs-lookup"><span data-stu-id="343fe-178">Submit the data to the rights acquisition URL by using an HTTP POST action.</span></span> <span data-ttu-id="343fe-179">Vous pouvez utiliser le contrôle Internet Explorer ou les API Windows Internet (WinINet).</span><span class="sxs-lookup"><span data-stu-id="343fe-179">You can use the Internet Explorer control or the Windows Internet (WinINet) APIs.</span></span>

<span data-ttu-id="343fe-180">Le code suivant illustre les étapes 1 à 3.</span><span class="sxs-lookup"><span data-stu-id="343fe-180">The following code shows steps 1–3.</span></span> <span data-ttu-id="343fe-181">L’étape 4 dépend des exigences spécifiques de votre application.</span><span class="sxs-lookup"><span data-stu-id="343fe-181">Step 4 depends on your application's particular requirements.</span></span>


```C++
WCHAR   *sURL = NULL;  // URL.
DWORD   cchURL = 0;    // Size of the URL in characters.

// Trust status of the URL.
MF_URL_TRUST_STATUS  trustStatus = MF_LICENSE_URL_UNTRUSTED;

BYTE    *pPostData = NULL;  // Buffer to hold HTTP POST data.
DWORD   cbPostDataSize = 0; // Size of the buffer, in bytes.

HRESULT hr = S_OK;

// Get the URL. 
hr = m_pEnabler->GetEnableURL(&sURL, &cchURL, &trustStatus);

if (SUCCEEDED(hr))
{
    if (trustStatus != MF_LICENSE_URL_TRUSTED)
    {
        // The URL is not trusted. Do not proceed.
        hr = E_FAIL;
    }
}

// Monitor the rights acquisition. 
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->MonitorEnable();
}

// Get the HTTP POST data.
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->GetEnableData(&pPostData, &cbPostDataSize);
}

// Open the URL and send the HTTP POST data. (Not shown.)

// Release the buffers.
CoTaskMemFree(pPostData);
CoTaskMemFree(sURL);
```



<span data-ttu-id="343fe-182">Une fois l’opération terminée, l’activateur de contenu envoie un événement [MEEnablerCompleted](meenablercompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="343fe-182">When the operation is completed, the content enabler sends an [MEEnablerCompleted](meenablercompleted.md) event.</span></span>

## <a name="complete-the-asynchronous-operation"></a><span data-ttu-id="343fe-183">Terminer l’opération asynchrone</span><span class="sxs-lookup"><span data-stu-id="343fe-183">Complete the Asynchronous Operation</span></span>

<span data-ttu-id="343fe-184">Lorsque l’acquisition des droits est terminée, avec succès ou dans le cas contraire, l’application doit notifier la session multimédia en appelant le pointeur de rappel fourni dans la méthode [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) .</span><span class="sxs-lookup"><span data-stu-id="343fe-184">When the rights acquisition is completed, successfully or otherwise, the application must notify the Media Session, by invoking the callback pointer given in the [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) method.</span></span>

1.  <span data-ttu-id="343fe-185">Créez un objet de résultat asynchrone en appelant [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult).</span><span class="sxs-lookup"><span data-stu-id="343fe-185">Create an asynchronous result object by calling [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult).</span></span>
2.  <span data-ttu-id="343fe-186">Appelez le rappel de la session multimédia en appelant [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span><span class="sxs-lookup"><span data-stu-id="343fe-186">Invoke the Media Session's callback by calling [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span></span>
3.  <span data-ttu-id="343fe-187">La session multimédia appellera [**IMFContentProtectionManager :: EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent).</span><span class="sxs-lookup"><span data-stu-id="343fe-187">The Media Session will call [**IMFContentProtectionManager::EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent).</span></span> <span data-ttu-id="343fe-188">Dans votre implémentation de cette méthode, libérez tous les pointeurs ou ressources que vous avez alloués dans [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span><span class="sxs-lookup"><span data-stu-id="343fe-188">In your implementation of this method, release any pointers or resources that you allocated inside [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent).</span></span> <span data-ttu-id="343fe-189">Retourne un **HRESULT** qui indique la réussite globale de l’opération.</span><span class="sxs-lookup"><span data-stu-id="343fe-189">Return an **HRESULT** that indicates the overall success of the operation.</span></span> <span data-ttu-id="343fe-190">Si l’acquisition des droits a échoué ou si l’utilisateur a annulé son exécution, retournez un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="343fe-190">If the rights acquisition failed or the user canceled before it was completed, return an error code.</span></span>

<span data-ttu-id="343fe-191">Le code suivant montre comment créer le résultat asynchrone et appeler le rappel.</span><span class="sxs-lookup"><span data-stu-id="343fe-191">The following code shows how to create the asynchronous result and invoke the callback.</span></span>


```C++
IMFAsyncResult  *pResult = NULL;

// Create the asynchronous result object.
hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);

// Invoke the callback.
if (SUCCEEDED(hr))
{
    pResult->SetStatus(hrStatus);
    hr = MFInvokeCallback(pResult);
}
SAFE_RELEASE(pResult);
```



## <a name="related-topics"></a><span data-ttu-id="343fe-192">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="343fe-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="343fe-193">Session multimédia</span><span class="sxs-lookup"><span data-stu-id="343fe-193">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="343fe-194">Lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="343fe-194">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



