---
description: Microsoft Negotiate est un fournisseur de support de sécurité qui agit comme une couche application entre l’interface du fournisseur de support de sécurité et les autres ssp.
ms.assetid: 3aa7e979-8b55-416d-bed1-28296055d38e
title: Négociation Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ce57a8f8924120dcce51e50e05de90fd6774b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123414"
---
# <a name="microsoft-negotiate"></a>Négociation Microsoft

Microsoft Negotiate est un [*fournisseur SSP (Security Support Provider*](../secgloss/s-gly.md) ) qui agit comme une couche application entre l’interface [SSPI](sspi.md)( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) et les autres ssp. Lorsqu'une application appelle un SSPI à se connecter à un réseau, il peut spécifier un SSP pour traiter la demande. Si l’application spécifie Negotiate, Negotiate analyse la demande et choisit le SSP le plus approprié pour gérer la demande en fonction de la stratégie de sécurité configurée par le client.

Actuellement, le package de sécurité Negotiate choisit entre [Kerberos](microsoft-kerberos.md) et [NTLM](microsoft-ntlm.md). Negotiate sélectionne Kerberos, sauf s’il ne peut pas être utilisé par l’un des systèmes impliqués dans l’authentification ou si l’application appelante n’a pas fourni suffisamment d’informations pour utiliser Kerberos.

Pour permettre à Negotiate de sélectionner le fournisseur de sécurité [Kerberos](microsoft-kerberos.md) , l’application cliente doit fournir un [*nom de principal du service*](../secgloss/s-gly.md) (SPN), un nom d’utilisateur principal (UPN) ou un nom de compte NetBIOS comme nom de cible. Dans le cas contraire, Negotiate sélectionne toujours le fournisseur de sécurité [NTLM](microsoft-ntlm.md) .

Un serveur qui utilise le package Negotiate peut répondre aux applications clientes qui sélectionnent spécifiquement le fournisseur de sécurité [Kerberos](microsoft-kerberos.md) ou [NTLM](microsoft-ntlm.md) . Toutefois, une application cliente doit savoir qu’un serveur prend en charge le package Negotiate pour demander l’authentification à l’aide de Negotiate. Un serveur qui ne prend pas en charge Negotiate ne peut pas toujours répondre aux demandes des clients qui spécifient Negotiate comme SSP.

## <a name="reasons-to-use-the-negotiate-package"></a>Raisons pour utiliser le package Negotiate

-   Permet au système d’utiliser le protocole disponible le plus fort (le plus sécurisé).
-   Garantit la compatibilité ascendante de votre application.
-   Garantit que votre application présente un comportement conforme à la stratégie de sécurité définie par le client.

 

 
