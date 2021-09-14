---
description: Le protocole Kerberos définit la manière dont les clients interagissent avec un \[ Kit de développement logiciel (SDK) de plateforme de service d’authentification réseau \] .
ms.assetid: e7870e72-1386-4818-bf6f-73430ae942a8
title: Microsoft Kerberos (en anglais)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03787bcc65959838ea02c49958d9ca4e0405649
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123421"
---
# <a name="microsoft-kerberos"></a>Microsoft Kerberos (en anglais)

Le [*protocole Kerberos*](../secgloss/k-gly.md) définit la manière dont les clients interagissent avec un service d’authentification réseau. Les clients obtiennent des tickets du centre de distribution de clés Kerberos (KDC), et ils présentent ces tickets aux serveurs lorsque les connexions sont établies. Les tickets Kerberos représentent les [*informations d’identification*](../secgloss/c-gly.md)réseau du client.

Les informations de cette section fournissent un arrière-plan théorique sur l’utilisation du protocole Kerberos dans un processus d’authentification. Il s’agit d’informations générales qui peuvent permettre aux développeurs de comprendre ce qui se passe en arrière-plan dans un processus SSPI qui utilise le protocole Kerberos version 5.

Le protocole d’authentification Kerberos fournit un mécanisme d’authentification mutuelle entre les entités avant qu’une connexion réseau sécurisée soit établie. Tout au long de cette documentation, les deux entités sont appelées le client et le serveur même si des connexions réseau sécurisées peuvent être établies entre les serveurs. Le client et le serveur peuvent aussi être appelés [*principaux de sécurité*](../secgloss/s-gly.md).

Le protocole Kerberos suppose que les transactions entre les clients et les serveurs s’effectuent sur un réseau ouvert dans lequel la plupart des clients et de nombreux serveurs ne sont pas physiquement sécurisés, et les paquets circulant sur le réseau peuvent être surveillés et modifiés à la place. L’environnement supposé est comme Internet d’aujourd’hui, où une personne malveillante peut facilement se poser comme client ou serveur, et peut facilement espionner ou altérer les communications entre les clients et les serveurs légitimes.

Cette section fournit les informations suivantes :

-   [Concepts d’authentification de base](basic-authentication-concepts.md)
-   [Sous-protocoles Kerberos](kerberos-subprotocols.md)
-   [Modèle Kerberos](kerberos-components.md)
-   [Interopérabilité SSPI/Kerberos avec GSSAPI](sspi-kerberos-interoperability-with-gssapi.md)

Votre application ne doit pas accéder directement au [*package de sécurité*](../secgloss/s-gly.md) Kerberos. au lieu de cela, il doit utiliser le package de sécurité [*Negotiate*](../secgloss/n-gly.md) . Negotiate permet à votre application de tirer parti de [*protocoles de sécurité*](../secgloss/s-gly.md) plus avancés s’ils sont pris en charge par les systèmes impliqués dans l’authentification. Actuellement, le package de sécurité Negotiate choisit entre [*Kerberos*](../secgloss/k-gly.md) et NTLM. Negotiate sélectionne Kerberos, sauf s’il ne peut pas être utilisé par l’un des systèmes impliqués dans l’authentification.

 

 
