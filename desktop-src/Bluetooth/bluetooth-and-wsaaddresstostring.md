---
title: Bluetooth et WSAAddressToString
description: La fonction Windows Sockets WSAAddressToString permet de convertir une adresse de périphérique Bluetooth en une chaîne, qui est à son tour fournie à la fonction WSALookupServiceBegin via la structure WSAQUERYSET lors de la récupération des informations de service de l’appareil.
ms.assetid: 3489d29a-2b64-4051-b579-57878efc0c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e8a9ae3ea6a0f853619a3f3610a64204ad3c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031320"
---
# <a name="bluetooth-and-wsaaddresstostring"></a><span data-ttu-id="dbf09-103">Bluetooth et WSAAddressToString</span><span class="sxs-lookup"><span data-stu-id="dbf09-103">Bluetooth and WSAAddressToString</span></span>

<span data-ttu-id="dbf09-104">La fonction Windows Sockets [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) permet de convertir une adresse de périphérique Bluetooth en une chaîne, qui est à son tour fournie à la fonction [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) via la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) lors de la récupération des informations de service de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dbf09-104">The [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Windows Sockets function is used to convert a Bluetooth Device Address to a string, which is in turn provided to the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function via the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure when retrieving device service information.</span></span>

<span data-ttu-id="dbf09-105">Bien qu’une adresse de périphérique Bluetooth tienne dans une mémoire tampon de 20 caractères, la fonction [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) retourne actuellement **WSAEFAULT** pour les adresses de périphérique Bluetooth, à moins que la mémoire tampon et la valeur *lpdwAddressStringLength* spécifiée soient définies sur une longueur de caractères de 40.</span><span class="sxs-lookup"><span data-stu-id="dbf09-105">While a Bluetooth Device Address fits within a 20 character buffer, the [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) function currently returns **WSAEFAULT** for Bluetooth Device Addresses unless the buffer and the specified *lpdwAddressStringLength* value are set to a character length of 40.</span></span>

> [!Note]  
> <span data-ttu-id="dbf09-106">Quand **WSAEFAULT** est retourné par [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) en tant que résultat d’une mémoire tampon insuffisante, le paramètre *lpdwAddressStringLength* n’est pas mis à jour avec la taille de mémoire tampon requise pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="dbf09-106">When **WSAEFAULT** is returned by [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) as the result of an insufficient buffer, the *lpdwAddressStringLength* parameter is not updated with the buffer size required for the operation.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="dbf09-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dbf09-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbf09-108">**WSAAddressToString**</span><span class="sxs-lookup"><span data-stu-id="dbf09-108">**WSAAddressToString**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[<span data-ttu-id="dbf09-109">Bluetooth et WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="dbf09-109">Bluetooth and WSALookupServiceBegin</span></span>](bluetooth-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="dbf09-110">Bluetooth et WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="dbf09-110">Bluetooth and WSAQUERYSET</span></span>](bluetooth-and-wsaqueryset.md)
</dt> </dl>

 

 