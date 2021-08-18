---
description: La spécification TSPI est très étroitement liée aux spécifications de TAPI 2,2 (TAPI/C).
ms.assetid: 2c51f7e3-c741-4736-9611-2327d65b427e
title: Comparaison générale avec TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecedd5a53fd30e2a49b6d44e90d30f86ff8469f002166ca3328f3146a2748b78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002807"
---
# <a name="overall-comparison-with-tapi"></a>Comparaison générale avec TAPI

La spécification TSPI est très étroitement liée aux spécifications de TAPI 2,2 (TAPI/C). La plupart des fonctions dans l’une ont une fonction correspondante dans l’autre. La correspondance habituelle est la suivante :

-   Les fonctions TSPI ont les mêmes noms que les fonctions TAPI, sauf qu’elles sont précédées de «**TSPI \_**». Par exemple, la fonction TAPI [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept) correspond à la fonction TSPI [**TSPI \_ lineAccept**](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept).
-   Les procédures qui autorisent une opération asynchrone insèrent un paramètre *dwRequestID* de type [DRV \_ REQUESTID](drv-requestid.md) comme premier paramètre. Ce paramètre spécifie la valeur à retourner pour indiquer l’opération asynchrone et pour signaler l’achèvement asynchrone.
-   les paramètres *hCall* de type hCall sont remplacés par les paramètres *HdCall* de type [HDRVCALL](hdrvline.md), ce qui indique le handle du fournisseur de services pour l’appel.
-   les paramètres *hLine* de type hLine sont remplacés par les paramètres *hdLine* de-type [HDRVLINE](hdrvline.md), ce qui indique le handle du fournisseur de services pour la ligne.
-   les paramètres *hPhone* de type hPhone sont remplacés par les paramètres *HdPhone* de type [HDRVPHONE](hdrvphone.md), ce qui indique le handle du fournisseur de services pour le téléphone.
-   Les procédures qui créent un nouvel appel, telles que [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall), remplacent un seul paramètre *lphCall* avec deux paramètres : un *htCall* de type [HTAPICALL](htapicall.md) qui passe dans le handle TAPI pour l’appel, et un *lphdCall* de type LPHDRVCALL qui indique l’emplacement auquel le fournisseur de services doit écrire son nouveau handle pour l’appel. Un fractionnement de paramètres similaire se produit dans [**TSPI \_ LineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) et [**TSPI \_ phoneOpen**](/windows/win32/api/tspi/nf-tspi-tspi_phoneopen).
-   Au niveau TSPI, il n’existe aucune notion de « privilège » associée aux descripteurs d’appareil. En outre, au niveau de l’API, chaque application qui a un handle d’appareil ou d’appel a un handle différent, mais TAPI fusionne ces derniers en un seul descripteur du côté du fournisseur de services. Par conséquent, les codes d’erreur et les messages d’État relatifs au privilège et au nombre de clients utilisant un appareil ne s’affichent pas au niveau TSPI.

L’ensemble de fonctions TAPI ne mappe pas un à un sur l’ensemble de fonctions TSPI. En particulier, les fonctions liées aux privilèges, à la traduction des numéros de téléphone et à la communication entre les applications sont gérées par TAPI et n’ont pas de fonction correspondante dans TSPI. D’autres fonctions, telles que celles utilisées pour la configuration et l’initialisation du fournisseur de service, n’ont pas de fonctions correspondantes dans l’interface TAPI.

 

 
