---
description: Pour tirer parti des fonctions IPv6 activées, les administrateurs informatiques doivent définir au sein de leur script WPAD, une fonction appelée FindProxyForURLEx (URL, hôte) qui remplacera la fonction FindProxyForUrl (URL, hôte) héritée.
ms.assetid: e531a66d-5c50-4065-a12a-783fd4d1d310
title: Définitions de l’API d’assistance du proxy IPv6-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdf7c36b0f0d29f84a0dfc0eb7c21cb577ef1b9ef75cb69cec34a7f7858e7a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052077"
---
# <a name="ipv6-aware-proxy-helper-api-definitions"></a>Définitions de l’API d’assistance du proxy IPv6-Aware

Pour tirer parti des fonctions IPv6 activées, les administrateurs informatiques doivent définir au sein de leur script WPAD, une fonction appelée FindProxyForURLEx (URL, hôte) qui remplacera la fonction FindProxyForUrl (URL, hôte) héritée. Les administrateurs ne peuvent exécuter les nouvelles fonctions qu’à partir de la nouvelle fonction FindProxyForURLEx.

Nous avons également tenté de simplifier le travail pour les développeurs, en alignant nos fonctions pour qu’elles retournent différents types d’adresses IP dans le même ordre de préférence que les autres composants de mise en réseau, en particulier les adresses IPv6 suivies des adresses IPv4 (c’est-à-dire le comportement actuel de la fonction getaddrinfo (..) de Winsock).

Les fonctions suivantes sont des extensions de la [spécification de format de fichier de configuration automatique du proxy du navigateur](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) pour permettre aux scripts WPAD de gérer des réseaux compatibles IPv6.

## <a name="predefined-functions-and-environment-for-the-javascript-function-findproxyforurlex"></a>Fonctions et environnement prédéfinis pour la fonction JavaScript FindProxyforURLEx

Conditions basées sur un nom d’hôte

<dl> <dt>

[**isResolvableEx**](isresolvableex.md)
</dt> <dd>

Détermine si une chaîne d’hôte donnée peut être résolue en une adresse IP.

</dd> <dt>

[**isInNetEx**](isinnetex.md)
</dt> <dd>

Détermine si une adresse IP se trouve dans un sous-réseau spécifique.

</dd> </dl>

Fonctions utilitaires associées

<dl> <dt>

[**dnsResolveEx**](dnsresolveex.md)
</dt> <dd>

Résoudre une chaîne d’hôte en son adresse IP.

</dd> <dt>

[**myIPAddressEx**](myipaddressex.md)
</dt> <dd>

Recherche toutes les adresses IP pour localhost.

</dd> <dt>

[**sortIpAddressList**](sortipaddresslist.md)
</dt> <dd>

Trie une liste d’adresses IP.

</dd> <dt>

[**getClientVersion**](getclientversion.md)
</dt> <dd>

Obtient la version du moteur de traitement WPAD.

</dd> </dl>

> [!Note]  
> cette fonctionnalité nécessite Windows Internet Explorer 7 ou version ultérieure.

 

 

 



