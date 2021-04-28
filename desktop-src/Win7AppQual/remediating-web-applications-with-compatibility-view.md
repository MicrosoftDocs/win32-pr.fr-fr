---
description: Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5acb7249854d9ac89b5601fdf83efa397c11c17
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116357"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a>Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité

Cette section décrit les étapes de base de la prévention et la planification de la prochaine compatibilité des applications pendant que vous résolvez les problèmes maintenant.

Dans la mesure du possible, Windows Internet Explorer prend en charge les modèles Internet Explorer hérités afin que les sites que vous développez continuent de se comporter comme prévu dans les versions plus récentes d’Internet Explorer. À compter de Windows Internet Explorer 8, vous pouvez choisir de prendre en charge les comportements hérités en sélectionnant le mode de rendu page par page.

Internet Explorer 8 comprend les modes de rendu suivants que vous pouvez définir à l’aide de l’en-tête X-UA-compatible.



| Valeur content | Description                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| IE=5          | Utilisez le mode Quirks.                                                                      |
| IE = 7          | Utilisez toujours le mode Windows Internet Explorer 7.                                          |
| IE=EmulateIE7 | Affichez en mode Internet Explorer 7, sauf si le site contient le DOCTYPE excentrique.           |
| IE = 8          | Utilisez toujours le mode Internet Explorer 8.                                                  |
| IE=EmulateIE8 | Remplacez l’affichage de compatibilité sur les ordinateurs clients et utilisez le mode Internet Explorer 8.      |
| IE=Edge       | Affichez dans le dernier mode. Dans Internet Explorer 8, cette valeur est équivalente à IE = 8. |



 

Les rubriques suivantes expliquent comment mettre à jour des applications Web à l’aide de l’affichage de compatibilité.



| Rubrique                                                                                                  | Description                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Qu’est-ce que l’affichage de compatibilité ?](what-is-compatibility-view-.md)                                          | Décrit l’affichage de compatibilité.                                                  |
| [Pourquoi avez-vous besoin d’un affichage de compatibilité ?](why-do-you-need-compatibility-view-.md)                         | Explique pourquoi vous devez utiliser l’affichage de compatibilité.                               |
| [Utiliser la balise meta pour garantir la compatibilité future](use-the-meta-tag-to-ensure-future-compatibility.md) | Décrit comment vous pouvez utiliser l’élément **meta** pour garantir la compatibilité future. |



 

 

 



