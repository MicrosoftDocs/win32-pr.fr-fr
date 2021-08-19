---
title: Vérifications du noyau pour les pilotes non signés WHQL
description: pour les appareils qui nettoient Windows 10, et où le démarrage sécurisé est activé (notez qu’il s’agit d’une norme pour tous les nouveaux appareils depuis la sortie de Windows 8.0), tous les nouveaux pilotes doivent être signés par WHQL/Sysdev plutôt que simplement à l’aide de certificats à signature croisée.
ms.assetid: D2A13F91-BA44-4044-B1F4-54393A9F1063
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2810d0549086d36f146ca80c0b9c83a7258bb3b120202432cdab6203a081cdd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852415"
---
# <a name="kernel-checks-for-non-whql-signed-drivers"></a>Vérifications du noyau pour les pilotes non signés WHQL

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

pour les appareils qui nettoient Windows 10, et où le démarrage sécurisé est activé (notez qu’il s’agit d’une norme pour tous les nouveaux appareils depuis la sortie de Windows 8.0), tous les nouveaux pilotes doivent être signés par WHQL/Sysdev plutôt que simplement à l’aide de certificats à signature croisée. Les appareils qui sont mis à niveau et les cas où les pilotes ont été signés avec un certificat croisé avant que cette stratégie soit appliquée sont exclus de cette stratégie pour garantir la compatibilité descendante. cette stratégie a été annoncée le 2015 avril, mais elle sera appliquée avec la Windows édition anniversaire, publiée le 2016 août.

Dans les cas où un pilote n’est pas signé correctement, il se manifeste en tant que notification PCA indiquant que le ou les pilotes sont bloqués lorsqu’il ne répond pas aux exigences de signature. Cela empêche une expérience utilisateur déconnectée ultérieure du pilote bloqué dans le noyau en toute transparence.

Pour plus d’informations, consultez ce billet de [blog](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/), qui annonce le changement de signature du pilote.

 

 




