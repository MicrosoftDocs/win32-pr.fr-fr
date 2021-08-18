---
description: L’interface IUpdateSearcher définit les propriétés suivantes.
ms.assetid: 65a39383-f326-4735-b2af-6df7a77ffba6
title: Propriétés IUpdateSearcher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dc3af2635fff4260a44261333b23cbfcf1661793ad613f08bb288db452b93d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130431"
---
# <a name="iupdatesearcher-properties"></a>Propriétés IUpdateSearcher

L’interface [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) définit les propriétés suivantes.



| Propriété                                                                                           | Description                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanAutomaticallyUpgradeService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_canautomaticallyupgradeservice)            | obtient et définit une valeur booléenne qui indique si les appels futurs aux méthodes [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) et [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) entraînent une mise à niveau automatique vers Windows Update Agent (WUA). |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_clientapplicationid)                                  | Identifie l’application cliente actuelle.                                                                                                                                                                                                   |
| [**IncludePotentiallySupersededUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates) | Obtient et définit une valeur booléenne qui indique si les résultats de la recherche incluent des mises à jour qui sont remplacées par d’autres mises à jour dans les résultats de la recherche.                                                                                          |
| [**En ligne**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_online)                                                            | Obtient et définit une valeur booléenne qui indique si le [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) se met en ligne pour rechercher des mises à jour.                                                                                                        |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serviceid)                                                      | obtient et définit un site à rechercher lorsque le site à rechercher n’est pas un site Windows Update.                                                                                                                                                         |
| [**ServerSelection**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serverselection)                                          | Obtient et définit une valeur [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) qui indique le serveur dans lequel Rechercher des mises à jour.                                                                                                                            |




 

 

 



