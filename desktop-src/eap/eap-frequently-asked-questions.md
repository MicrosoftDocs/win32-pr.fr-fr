---
title: Forum aux questions sur EAP
description: Trouvez des réponses aux questions fréquemment posées (FAQ) sur les API EAP, telles que « quelle est la durée de vie d’une authentification EAP ? ».
ms.assetid: 4e26df7b-3cce-4522-ab39-e24f06b4c4b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08713b17491d4b0bd76540c09b9d4588116256f
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "103941524"
---
# <a name="eap-frequently-asked-questions"></a>Forum aux questions sur EAP

La rubrique suivante fournit des réponses aux questions fréquemment posées sur les API EAP.



| Question                                                                                        | Réponse                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Quelle est la durée de vie d’une authentification EAP ?                                                  | Dans une situation type, l’authentification se compose de tout ce qui se produit entre l’appel des fonctions [**RapEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) et [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) . Lorsqu’un utilisateur choisit de configurer un fournisseur EAP dans le composant logiciel enfichable RRAS, une authentification se compose de tout ce qui se produit entre l’appel des méthodes [**Initialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-initialize) et [**Uninitialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize) .<br/> |
| Qu’est-ce que la « stratégie de groupe » ?                                                                         | Pour obtenir une description de la stratégie de groupe, consultez [stratégie de groupe collection](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).                                                                                                                                                                                                                                                                                                                                                    |
| Les fonctions EAP peuvent-elles remplacer la stratégie de configuration spécifiée par la stratégie de groupe ?                      | Non, jamais. Si la stratégie de groupe est en cours d’utilisation, les paramètres de stratégie de groupe remplaceront toujours les paramètres de configuration EAP.                                                                                                                                                                                                                                                                                                                                                         |
| J’ai besoin d’avertir les utilisateurs des tentatives de code PIN non valides. Est-il possible de capturer un code confidentiel non valide ? | Lorsque l’utilisateur entre un code confidentiel incorrect, le protocole EAP-TLS (Extensible Authentication Protocol-Transport Layer Security) envoie un code d’erreur au demandeur VPN. Une fois qu’un code d’erreur est retourné, le demandeur peut implémenter sa logique de nouvelle tentative préférée.                                                                                                                                                                                                                    |
| Qu’est-ce que la sécurité de niveau EAP-Transport (EAP-TLS) ?                                                 | EAP-TLS est un protocole client-serveur dans lequel des profils de certificat distincts sont généralement utilisés pour le client et le serveur. Pour plus d’informations, consultez [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).<br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du protocole EAP (Extensible Authentication Protocol)](using-extenstible-authentication-protocol.md)
</dt> </dl>