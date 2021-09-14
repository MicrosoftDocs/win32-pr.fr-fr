---
title: Interfaces de passerelle Bureau à distance
description: L’API Bureau à distance Gateway (passerelle des services Bureau à distance) prend en charge les interfaces suivantes. Vous pouvez utiliser ces interfaces pour implémenter des plug-ins qui fournissent une authentification et une autorisation personnalisées.
ms.assetid: a457574a-d856-4490-b20d-48343a82acff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2b0a17c19431ea69419443459639d199219a61
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324647"
---
# <a name="remote-desktop-gateway-interfaces"></a>Interfaces de passerelle Bureau à distance

L’API Bureau à distance Gateway (passerelle des services Bureau à distance) prend en charge les interfaces suivantes. Vous pouvez utiliser ces interfaces pour implémenter des plug-ins qui fournissent une authentification et une autorisation personnalisées. Il n’existe aucune dépendance entre le plug-in d’authentification et le plug-in d’autorisation, et vous ne pouvez implémenter qu’un seul plug-in si vous le souhaitez.

Les plug-ins d’authentification sont [**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) et [**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine).

Les plug-ins d’autorisation sont [**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine), [**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink), [**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)et [**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine).

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine)
</dt> <dd>

Expose des méthodes qui fournissent des informations sur la création ou la fermeture de sessions pour une connexion.

</dd> <dt>

[**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink)
</dt> <dd>

Expose les méthodes qui notifient la passerelle des services Bureau à distance des événements d’authentification.

</dd> <dt>

[**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine)
</dt> <dd>

Expose des méthodes qui authentifient les utilisateurs pour la passerelle des services Bureau à distance.

</dd> <dt>

[**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink)
</dt> <dd>

Expose les méthodes qui notifient la passerelle des services Bureau à distance du résultat d’une tentative d’autorisation d’une connexion.

</dd> <dt>

[**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)
</dt> <dd>

Expose les méthodes qui notifient la passerelle des services Bureau à distance du résultat d’une tentative d’autorisation d’une ressource.

</dd> <dt>

[**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine)
</dt> <dd>

Expose des méthodes qui autorisent les connexions et les ressources.

</dd> </dl>

 

 




