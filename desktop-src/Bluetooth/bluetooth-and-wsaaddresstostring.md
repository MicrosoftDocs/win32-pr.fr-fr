---
title: Bluetooth et WSAAddressToString
description: la fonction WSAAddressToString Windows sockets est utilisée pour convertir une adresse d’appareil Bluetooth en une chaîne, qui est à son tour fournie à la fonction WSALookupServiceBegin via la structure WSAQUERYSET lors de la récupération des informations de service de l’appareil.
ms.assetid: 3489d29a-2b64-4051-b579-57878efc0c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e8a9ae3ea6a0f853619a3f3610a64204ad3c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122041"
---
# <a name="bluetooth-and-wsaaddresstostring"></a>Bluetooth et WSAAddressToString

la fonction [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Windows sockets est utilisée pour convertir une adresse d’appareil Bluetooth en une chaîne, qui est à son tour fournie à la fonction [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) via la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) lors de la récupération des informations de service de l’appareil.

alors qu’une Bluetooth adresse de l’appareil tient dans une mémoire tampon de 20 caractères, la fonction [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) retourne actuellement **WSAEFAULT** pour Bluetooth adresses d’appareils, sauf si la mémoire tampon et la valeur *lpdwAddressStringLength* spécifiée sont définies sur une longueur de caractères de 40.

> [!Note]  
> Quand **WSAEFAULT** est retourné par [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) en tant que résultat d’une mémoire tampon insuffisante, le paramètre *lpdwAddressStringLength* n’est pas mis à jour avec la taille de mémoire tampon requise pour l’opération.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[Bluetooth et WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin.md)
</dt> <dt>

[Bluetooth et WSAQUERYSET](bluetooth-and-wsaqueryset.md)
</dt> </dl>

 

 