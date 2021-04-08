---
title: Hôte de protocole EAP (Extensible Authentication Protocol)
description: En savoir plus sur l’hôte EAP (Extensible Authentication Protocol). Consultez Configuration requise pour l’exécution et afficher des ressources supplémentaires disponibles.
ms.assetid: caaef367-2952-44fc-ac4c-f0db6387850e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f007435c43969ad0f195b0a6a1e697ab817d9c4
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104102593"
---
# <a name="extensible-authentication-protocol-host"></a>Hôte de protocole EAP (Extensible Authentication Protocol)

## <a name="purpose"></a>Objectif


EAPHost est un composant de mise en réseau Microsoft Windows qui fournit une infrastructure EAP (Extensible Authentication Protocol) pour l’authentification des implémentations de protocole « demandeur », telles que [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) et PPP ( [point-to-point](https://go.microsoft.com/fwlink/p/?linkid=83919) ). Il permet également l’authentification avec des technologies « authentificateur », telles que le serveur NPS (Network Policy Server) Microsoft. Contrairement au serveur IAS précédent ([RADIUS](/windows/desktop/Nps/ias-about-internet-authentication-service)), NPS prend en charge la [protection d’accès réseau](/windows/desktop/NAP/network-access-protection-start-page) (NAP).


Les API EAPHost permettent aux applications de s’authentifier à l’aide du service EAPHost et fournissent un modèle pour le développement de méthodes d’authentification conformes pour une utilisation avec EAPHost.

## <a name="run-time-requirements"></a>Conditions d’exécution

Les API EAPHost sont uniquement prises en charge dans Windows Vista et les systèmes d’exploitation ultérieurs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos d’EAPHost](about-eap-host.md)
</dt> <dt>

[Utilisation d’EAPHost](using-eap-host.md)
</dt> <dt>

[Informations de référence sur l’API EAPHost](eaphost-api-reference.md)
</dt> </dl>

 

 