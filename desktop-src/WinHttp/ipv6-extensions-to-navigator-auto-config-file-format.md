---
description: Microsoft a implémenté un tableau d’extensions pour le format de fichier de configuration automatique du navigateur afin d’ajouter la prise en charge IPv6 dans les fonctions d’assistance WPAD WinINet et WinHTTP.
ms.assetid: 40116a01-b18f-432a-8542-b56b3f55c692
title: Extensions IPv6 du format de fichier de configuration automatique du navigateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b57fce93caaf7790136ee9ac7db04017d9ac11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228330"
---
# <a name="ipv6-extensions-to-navigator-auto-config-file-format"></a>Extensions IPv6 du format de fichier de configuration automatique du navigateur

Microsoft a implémenté un tableau d’extensions pour le format de fichier de configuration automatique du navigateur afin d’ajouter la prise en charge IPv6 dans les fonctions d’assistance WPAD WinINet et WinHTTP.

L’explosion d’Internet à la fin des années 1990 a provoqué un manque inattendu d’adresses IPv4, le pool étant épuisé quotidiennement. IPv6 fournit une solution à ce problème et, bien qu’il ne soit pas largement déployé, son utilisation sera de plus en plus répandue à l’avenir. [WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) est un protocole qui permet aux clients Web de détecter automatiquement la configuration de proxy appropriée pour le trafic sortant. Cette fonctionnalité est très utile pour les déploiements d’entreprise, car elle permet aux administrateurs informatiques de configurer des scripts complexes capables d’acheminer le trafic de tous les clients vers des proxies spécifiques en fonction du serveur cible auquel les clients tentent de se connecter. WinINet et WinHTTP prennent en charge les fonctions d’assistance WPAD, telles que définies par la [spécification de format de fichier de configuration automatique du proxy du navigateur (PAC)](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html), qui est devenue une norme de facto. Malheureusement, cette spécification a été écrite en 1996 et ne définit pas les comportements de fonction lorsqu’un script WPAD est déployé sur un réseau compatible IPv6.

étant donné que le protocole IPv6 est la vague du futur, tous les composants Windows prennent désormais en charge les réseaux à double pile (IPv4 et ipv6) et ipv6 uniquement. Pour prendre en charge IPv6 sans affecter le déploiement existant, Microsoft a ajouté 6 nouvelles fonctions de classe d’assistance en tant qu’extension de la spécification de format de fichier de configuration automatique du proxy du navigateur (PAC) et a également ajouté une nouvelle fonction compatible IPv6 appelée **FindProxyForURLEx** que les administrateurs peuvent implémenter dans le script WPAD.

<dl> <dt>

[Définitions d’API d’assistance du proxy compatibles IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dd></dd> <dt>

[Différences entre les fonctions d’assistance WPAD IPv6-Aware et les fonctions d’assistance WPAD héritées](differences-between-ipv6-aware-wpad-helper-functions-and-legacy-wpad-helper-functions.md)
</dt> <dd></dd> </dl>

> [!Note]  
> cette fonctionnalité nécessite Windows Internet Explorer 7 ou version ultérieure.

 

 

 



