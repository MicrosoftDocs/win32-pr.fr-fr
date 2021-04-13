---
description: L’interface IUpdateSearcher définit les propriétés suivantes.
ms.assetid: 65a39383-f326-4735-b2af-6df7a77ffba6
title: Propriétés IUpdateSearcher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777c2489afe10f73c41badfb346053aefad7022
ms.sourcegitcommit: aab10824ee4883c70e1afba428b679a17915a5aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/11/2021
ms.locfileid: "104322582"
---
# <a name="iupdatesearcher-properties"></a>Propriétés IUpdateSearcher

L’interface [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) définit les propriétés suivantes.



| Propriété                                                                                           | Description                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanAutomaticallyUpgradeService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_canautomaticallyupgradeservice)            | Obtient et définit une valeur booléenne qui indique si les appels futurs aux méthodes [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) et [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) entraînent une mise à niveau automatique vers Windows Update Agent (WUA). |
| [**ClientApplicationID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_clientapplicationid)                                  | Identifie l’application cliente actuelle.                                                                                                                                                                                                   |
| [**IncludePotentiallySupersededUpdates**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates) | Obtient et définit une valeur booléenne qui indique si les résultats de la recherche incluent des mises à jour qui sont remplacées par d’autres mises à jour dans les résultats de la recherche.                                                                                          |
| [**En ligne**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_online)                                                            | Obtient et définit une valeur booléenne qui indique si le [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) se met en ligne pour rechercher des mises à jour.                                                                                                        |
| [**ServiceID**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serviceid)                                                      | Obtient et définit un site à rechercher lorsque le site à rechercher n’est pas un site Windows Update.                                                                                                                                                         |
| [**ServerSelection**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serverselection)                                          | Obtient et définit une valeur [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) qui indique le serveur dans lequel Rechercher des mises à jour.                                                                                                                            |




 

 

 



