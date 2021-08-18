---
title: Bluetooth et WSAAddressToString
description: la fonction WSAAddressToString Windows sockets est utilisée pour convertir une adresse d’appareil Bluetooth en une chaîne, qui est à son tour fournie à la fonction WSALookupServiceBegin via la structure WSAQUERYSET lors de la récupération des informations de service de l’appareil.
ms.assetid: 3489d29a-2b64-4051-b579-57878efc0c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bb49563355b3a85ff64d7168f77e8526ca1679cffaa565e7b9cd7070cf87f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004279"
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

 

 