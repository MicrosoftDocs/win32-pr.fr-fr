---
title: Mise à jour des licences
description: Mise à jour des licences
ms.assetid: b298badf-efcf-423c-8cc7-c3f50ab288a0
keywords:
- Windows Media Player Online stores, mise à jour des licences
- magasins en ligne, mise à jour des licences
- tapez 1 magasins en ligne, mise à jour des licences
- Windows Media Player Online stores, mise à jour de la licence
- magasins en ligne, mise à jour des licences
- tapez 1 magasins en ligne, mise à jour de la licence
- mise à jour des licences
- licences, mise à jour
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154959b01c93719184e310b60dffaa91fe2dcfa0
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314275"
---
# <a name="updating-licenses"></a><span data-ttu-id="7cc57-111">Mise à jour des licences</span><span class="sxs-lookup"><span data-stu-id="7cc57-111">Updating Licenses</span></span>

<span data-ttu-id="7cc57-112">Les magasins en ligne peuvent fournir du contenu qui est concédé sous licence pendant une période de temps spécifique ou jusqu’à une certaine date.</span><span class="sxs-lookup"><span data-stu-id="7cc57-112">Online stores can deliver content that is licensed for a specific period of time or until a certain date.</span></span> <span data-ttu-id="7cc57-113">Cela est normal pour le contenu musical fourni dans le cadre d’un contrat de service d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="7cc57-113">This would be normal for music content delivered as part of a subscription service agreement.</span></span> <span data-ttu-id="7cc57-114">Dans ce cas, le magasin en ligne a besoin d’une opportunité de mettre à jour ces licences avant d’expirer, en supposant, bien sûr, que l’utilisateur ait payé son abonnement.</span><span class="sxs-lookup"><span data-stu-id="7cc57-114">In this case, the online store needs an opportunity to update these licenses before they expire, assuming, of course, that the user has paid to renew his or her subscription.</span></span> <span data-ttu-id="7cc57-115">(Si l’utilisateur n’a pas renouvelé l’abonnement, les licences peuvent simplement être laissées à expiration.)</span><span class="sxs-lookup"><span data-stu-id="7cc57-115">(If the user has not renewed the subscription, the licenses can simply be left to expire.)</span></span>

<span data-ttu-id="7cc57-116">Le lecteur Windows Media interroge le plug-in du partenaire de contenu à propos de l’avertissement à l’avance que le joueur doit fournir sur une licence qui est sur le lieu d’expirer.</span><span class="sxs-lookup"><span data-stu-id="7cc57-116">Windows Media Player queries the content partner plug-in about how much advance warning the Player should provide about a license that is about to expire.</span></span> <span data-ttu-id="7cc57-117">Pour ce faire, il appelle [IWMPContentPartner :: GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo), en passant la constante g \_ szContentPartnerInfo \_ LicenseRefreshAdvanceWarning via le paramètre *bstrInfoName* .</span><span class="sxs-lookup"><span data-stu-id="7cc57-117">It does this by calling [IWMPContentPartner::GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo), passing the constant g\_szContentPartnerInfo\_LicenseRefreshAdvanceWarning through the *bstrInfoName* parameter.</span></span> <span data-ttu-id="7cc57-118">Pour alerter le plug-in à propos des licences qui sont sur le paragraphe d’expirer, le lecteur Windows Media appelle [IWMPContentPartner :: RefreshLicense](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense).</span><span class="sxs-lookup"><span data-stu-id="7cc57-118">To alert the plug-in about licenses that are about to expire, Windows Media Player calls [IWMPContentPartner::RefreshLicense](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense).</span></span> <span data-ttu-id="7cc57-119">Cet appel accepte des paramètres qui fournissent des détails sur le fichier en cours d’actualisation, par exemple si le fichier se trouve sur l’ordinateur de l’utilisateur et le chemin d’accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="7cc57-119">This call takes parameters that provide details about the file being refreshed, such as whether the file is on the user's computer, and the path to the file.</span></span> <span data-ttu-id="7cc57-120">Si la licence est actualisée dans le cadre d’une opération de synchronisation de l’appareil, le paramètre *pReasonContext* fournit le nom de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7cc57-120">If the license is being refreshed as part of a device synchronization operation, the *pReasonContext* parameter supplies the cannonical name of the device</span></span>

<span data-ttu-id="7cc57-121">Lorsque le lecteur Windows Media appelle **RefreshLicence**, il passe un cookie qui identifie la demande de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="7cc57-121">When Windows Media Player calls **RefreshLicence**, it passes a cookie that identifies the update request.</span></span> <span data-ttu-id="7cc57-122">Lorsque le plug-in a terminé le traitement de la demande de mise à jour, il avertit le lecteur Windows Media en appelant [IWMPContentPartnerCallback :: RefreshLicenseComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete), en passant le cookie, l’ID de l’élément multimédia et un **HRESULT** qui indique si la mise à jour a réussi.</span><span class="sxs-lookup"><span data-stu-id="7cc57-122">When the plug-in has finished processing the update request, it notifies Windows Media Player by calling [IWMPContentPartnerCallback::RefreshLicenseComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete), passing the cookie, the ID of the media item, and an **HRESULT** that indicates whether the update was successful.</span></span>

<span data-ttu-id="7cc57-123">Les plug-ins de magasin en ligne peuvent également effectuer une inspection et des mises à jour des licences en tant que processus en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="7cc57-123">Online store plug-ins can also do license inspection and updates as a background process.</span></span> <span data-ttu-id="7cc57-124">Le lecteur Windows Media notifie le plug-in à des moments où il est autorisé à effectuer des tâches de traitement en arrière-plan en appelant [IWMPContentPartner :: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify).</span><span class="sxs-lookup"><span data-stu-id="7cc57-124">Windows Media Player notifies the plug-in about times when it is permissible to perform background processing tasks by calling [IWMPContentPartner::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify).</span></span> <span data-ttu-id="7cc57-125">Pour signaler au plug-in de démarrer le traitement en arrière-plan, le joueur transmet la valeur d’énumération [WMPPartnerNotification](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) wmpsnBackgroundProcessingBegin ; pour signaler au plug-in d’arrêter le traitement en arrière-plan, le joueur transmet la valeur wmpsnBackgroundProcessingEnd.</span><span class="sxs-lookup"><span data-stu-id="7cc57-125">To signal the plug-in to start background processing, the Player passes the [WMPPartnerNotification](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) enumeration value wmpsnBackgroundProcessingBegin; to signal the plug-in to stop background processing, the Player passes the value wmpsnBackgroundProcessingEnd.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cc57-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7cc57-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cc57-127">**Guide de programmation pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="7cc57-127">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




