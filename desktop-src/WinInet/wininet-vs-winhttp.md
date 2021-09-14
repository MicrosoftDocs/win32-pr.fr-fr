---
title: WinINet et WinHTTP
description: Découvrez comment choisir entre WinInet et WinHTTP. Lisez une comparaison des fonctionnalités et passez en revue les rubriques connexes.
ms.assetid: 77386b54-2c86-4a30-8c4c-88d5f15313d7
keywords:
- WinINet et WinHTTP
ms.topic: article
ms.date: 02/22/2019
ms.openlocfilehash: 8ced80dd048559fee483e8cf121918eed75fc462
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013117"
---
# <a name="wininet-vs-winhttp"></a>WinINet et WinHTTP

À quelques exceptions près, [WinInet](portal.md) est un sur-ensemble de [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page). Lorsque vous sélectionnez entre les deux, vous devez utiliser WinINet, sauf si vous envisagez de l’exécuter au sein d’un service ou d’un processus de type service qui requiert l’isolation d’emprunt d’identité et de session.

## <a name="comparison-of-features"></a>Comparaison des fonctionnalités

| Fonctionnalité | WinINet | WinHTTP |
|-|-|-|
| **Cache des informations d’identification** permet à toutes les applications intégrées dans Windows Internet Explorer d’accéder automatiquement aux informations d’identification. Il permet également à une application en cours d’exécution en dehors d’Internet Explorer de demander/spécifier les informations d’identification du serveur une seule fois. À partir de là, les demandes sont automatiques. | Oui | non |
| **Demande d’informations d’identification** Fournit une API qui permet au code appelant d’inviter l’utilisateur à fournir des informations d’identification. | Oui | non |
| **FTP** | Oui | non |
| **Support AutoDial/RAS** Il s’agit d’une fonctionnalité héritée. Utilisez [à la place l’accès à distance](/windows/desktop/RRAS/portal) . | Oui | non |
| **Zones** Intégration automatique aux zones de sécurité d’Internet Explorer. | Oui | non |
| **Prise en charge de IDNA** Prise en charge intégrée de la norme IDNA RFC/Punycode. | Oui | Oui |
| **API jar de cookie** Les cookies persistants et non persistants sont pris en charge. Une application ou un script peut l’utiliser pour afficher les mêmes cookies que le navigateur. | Oui | non |
| **Prise en charge d’IE en mode protégé** | Oui | non |
| **Prise en charge de la décompression** Prise en charge du schéma de compression gzip et deflate. | Oui | Oui |
| **prise en charge des Télécharger en bloc** Le code client doit effectuer la segmentation. | non | Oui |
| **Prise en charge de SOCKS v4** N’inclut pas V4A ou V5. | Oui | non |
| **Envoi et réception bidirectionnels** | non | non |
| **E/s avec chevauchement** | non | non |
| **Prise en charge du schéma de fichier** Utile pour les scripts de proxy avec un schéma de fichier. | Oui | non |
| **InternetOpenUrl** Code simplifié pour ouvrir une URL. | Oui | non |
| **Prise en charge des services** Peut être exécuté à partir d’un service ou d’un compte de service. | non | Oui |
| **Isolation** de la session Les sessions distinctes n’affectent pas les unes les autres. | non | Oui |
| **Emprunt d’identité** Prend en charge l’appel de lorsque le thread emprunte l’identité d’un autre utilisateur. | non | Oui |

## <a name="related-topics"></a>Rubriques connexes

* [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
* [WinINet](/windows/desktop/WinInet/about-wininet)