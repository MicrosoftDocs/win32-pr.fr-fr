---
description: Au fil du temps, différentes versions peuvent exister pour les applications TAPI, TAPI et les fournisseurs de services.
ms.assetid: 39b16328-931e-4d75-a6ec-1edc97f1a287
title: Négociation de version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beffff7ceeb90ccf419e138986562ca90f83c204
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008699"
---
# <a name="version-negotiation"></a>Négociation de version

Au fil du temps, différentes versions peuvent exister pour les applications TAPI, TAPI et les fournisseurs de services. L’interopérabilité optimale d’une application TAPI nécessite de connaître non seulement la version TAPI de l’application, mais également les versions de la DLL, TAPISVR et du fournisseur de services TAPI.

L’échec de la négociation de version appropriée peut entraîner des problèmes sérieux. Par exemple, certaines structures fortement utilisées ont des membres de données ajoutés d’une version à la suivante. Si la taille de la structure ne correspond pas à la valeur attendue par l’application ou l’interface TAPI, les conséquences sont comprises entre les fuites de mémoire et la synchronisation AVs intermittente.

Pour plus d’informations, consultez contrôle de [version TAPI](./tapi-versioning.md).

**TAPI 2. x :** Les applications négocient avec TAPI et TAPISVR pendant [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa). Les applications effectuent la négociation des appareils avec les fournisseurs de services en appelant [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) pour chaque ligne que l’application peut utiliser.

**TAPI 3. x :** Il n’est pas nécessaire d’effectuer une négociation de version ; Toutefois, vous pouvez utiliser [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour déterminer si une interface est disponible sur leur version.

 

 
