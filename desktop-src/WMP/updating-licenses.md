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
# <a name="updating-licenses"></a>Mise à jour des licences

Les magasins en ligne peuvent fournir du contenu qui est concédé sous licence pendant une période de temps spécifique ou jusqu’à une certaine date. Cela est normal pour le contenu musical fourni dans le cadre d’un contrat de service d’abonnement. Dans ce cas, le magasin en ligne a besoin d’une opportunité de mettre à jour ces licences avant d’expirer, en supposant, bien sûr, que l’utilisateur ait payé son abonnement. (Si l’utilisateur n’a pas renouvelé l’abonnement, les licences peuvent simplement être laissées à expiration.)

Le lecteur Windows Media interroge le plug-in du partenaire de contenu à propos de l’avertissement à l’avance que le joueur doit fournir sur une licence qui est sur le lieu d’expirer. Pour ce faire, il appelle [IWMPContentPartner :: GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo), en passant la constante g \_ szContentPartnerInfo \_ LicenseRefreshAdvanceWarning via le paramètre *bstrInfoName* . Pour alerter le plug-in à propos des licences qui sont sur le paragraphe d’expirer, le lecteur Windows Media appelle [IWMPContentPartner :: RefreshLicense](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense). Cet appel accepte des paramètres qui fournissent des détails sur le fichier en cours d’actualisation, par exemple si le fichier se trouve sur l’ordinateur de l’utilisateur et le chemin d’accès au fichier. Si la licence est actualisée dans le cadre d’une opération de synchronisation de l’appareil, le paramètre *pReasonContext* fournit le nom de l’appareil.

Lorsque le lecteur Windows Media appelle **RefreshLicence**, il passe un cookie qui identifie la demande de mise à jour. Lorsque le plug-in a terminé le traitement de la demande de mise à jour, il avertit le lecteur Windows Media en appelant [IWMPContentPartnerCallback :: RefreshLicenseComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete), en passant le cookie, l’ID de l’élément multimédia et un **HRESULT** qui indique si la mise à jour a réussi.

Les plug-ins de magasin en ligne peuvent également effectuer une inspection et des mises à jour des licences en tant que processus en arrière-plan. Le lecteur Windows Media notifie le plug-in à des moments où il est autorisé à effectuer des tâches de traitement en arrière-plan en appelant [IWMPContentPartner :: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify). Pour signaler au plug-in de démarrer le traitement en arrière-plan, le joueur transmet la valeur d’énumération [WMPPartnerNotification](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) wmpsnBackgroundProcessingBegin ; pour signaler au plug-in d’arrêter le traitement en arrière-plan, le joueur transmet la valeur wmpsnBackgroundProcessingEnd.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation pour les magasins de type 1 en ligne**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




