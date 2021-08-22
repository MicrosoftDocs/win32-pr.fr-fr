---
description: à compter de Windows fournisseurs de service de téléphonie 2000 qui négocient une version de 3,0 ou version ultérieure doivent avoir un fournisseur de services de média correspondant.
ms.assetid: 9235c631-77bc-42c6-8139-9208c9c254b4
title: Communication du fournisseur de services de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3797d02c67fc86ebfb44ff9e0e7b2c85cd1604206a58f1d8f5c3ca293599e92d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404819"
---
# <a name="media-service-provider-communication"></a>Communication du fournisseur de services de média

à compter de Windows fournisseurs de service de téléphonie 2000 qui négocient une version de 3,0 ou version ultérieure doivent avoir un fournisseur de services de média correspondant. La Division précise des responsabilités opérationnelles dépend de l’implémentation. Par exemple, un TSP peut utiliser le MSP correspondant pour effectuer la détermination du type de média sur une session entrante. Toutefois, le TSP doit se conformer au TSPI, ce qui signifie obtenir cette détermination auprès du MSP et le signaler à TAPI.

TSPI fournit les fonctions et messages suivants pour autoriser une connexion virtuelle entre un TSP et un MSP :

-   [**TSPI \_ lineCloseMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [**TSPI \_ lineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [**TSPI \_ lineMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [**TSPI \_ lineReceiveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [**QOSINFO de ligne \_**](line-qosinfo.md)
-   [**SENDMSPDATA de ligne \_**](line-sendmspdata.md)

 

 
