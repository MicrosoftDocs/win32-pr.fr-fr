---
title: Prise en charge d’IP version 6
description: Depuis IE7 et versions ultérieures, WinINet prend en charge les littéraux IPv6 dans le nom d’hôte et le composant d’autorité de l’URI.
ms.assetid: cbbb9f93-15b0-4017-ac39-8a396203532e
keywords:
- Prise en charge d’IP version 6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ed0857d9a0968bcd3e6c18e54623fb0c7d86cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382475"
---
# <a name="ip-version-6-support"></a>Prise en charge d’IP version 6

Depuis IE7 et versions ultérieures, WinINet prend en charge les littéraux IPv6 dans le nom d’hôte et le composant d’autorité de l’URI. WinINet prend également en charge l’utilisation de littéraux IPv6 dans des parties pertinentes du protocole HTTP, telles que dans l’en-tête Location.

## <a name="hostname-ipv6-literals-and-uri-components"></a>Littéraux et composants d’URI IPv6 de nom d’hôte

WinINet implémente les littéraux IPv6 conformément aux spécifications de la RFC 3513. Comme spécifié dans cette RFC, les littéraux IPv6 d’un URI doivent être mis entre crochets. Par exemple, https:// \[ :: 1 \] /est un URI IPv6 valide ; le formulaire sans crochets ( https://::1/) n’est pas valide. Toutefois, les littéraux IPv6 de nom d’hôte qui ne font pas partie de l’URI n’ont pas besoin d’être placés entre crochets ; l’une ou l’autre forme est acceptable pour WinINet. Par exemple, «  :: 1 » et « \[ :: 1 \] » sont tous deux des formes acceptables de littéraux de nom d’hôte IPv6. D’autres API, telles que l’API WinSock, acceptent également les deux formulaires. Les applications doivent donc être prêtes à gérer les deux types de littéraux de nom d’hôte IPv6.

## <a name="scope-id"></a>ID d’étendue

L’adresse littérale IPv6 dans l’URI peut inclure un ID d’étendue. Un ID d’étendue peut être un ID d’interface comme \[ FE80 :: 1% 1 \] . La norme d’URI, documentée dans le document RFC 3986, ne définit pas la syntaxe de l’ID de portée et l’URI est considéré comme non uniforme lorsque l’ID d’étendue est présent. Toutefois, WinINet accepte un ID d’étendue dans le composant d’autorité de l’URI et dans le littéral IPv6 du nom d’hôte.

Le caractère de pourcentage (%) dans l’adresse littérale IPv6 doit être un pourcentage d’échappement lorsqu’il est présent dans l’URI. Par exemple, l’ID d’étendue FE80 :: 2% 3, doit apparaître dans l’URI sous la forme « https:// \[ FE80 :: 2% 253 \] / », où %25 est le caractère de pourcentage encodé en hex (%). Si l’application récupère l’URI à partir d’une API Unicode, telle que l’API Winsock [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) , l’application doit ajouter la version d’échappement du caractère de pourcentage (%) dans le nom d’hôte de l’URI. Pour créer la version échappée de l’URI, les applications appellent [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) avec le paramètre *dwFlags* défini sur l' **\_ \_ autorité d’échappement ICU** et le nom d’hôte IPv6 spécifié dans la structure de composants URL spécifiée dans le paramètre *lpUrlComponents* .

Pour toutes les opérations de sockets, WinINet utilise l’ID d’étendue. Toutefois, étant donné que l’ID d’étendue a uniquement l’importance de l’hôte local, il n’est pas envoyé dans le cadre des en-têtes de protocole HTTP de la demande. Par exemple, l’appel à [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) est appelé avec l’URL suivante dans le paramètre *lpszUrl* .

``` syntax
https://[fec0::2%251]:80/path.htm
```

La partie ID d’étendue de l’URL est supprimée par WinINet lorsque la requête HTTP est envoyée pour cette URL. La demande contient les en-têtes suivants :

``` syntax
GET path.htm HTTP/1.1
Host: [fec0::2]
```

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 