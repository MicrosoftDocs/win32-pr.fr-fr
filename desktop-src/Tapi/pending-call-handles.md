---
description: Un fournisseur de services est requis pour créer un ou plusieurs handles d’appel (variables de type HDRVCALL) chaque fois que TAPI appelle l’une des fonctions suivantes.
ms.assetid: 0a9d9afd-9786-4d9e-b0a2-12c9a1e13887
title: Handles d’appel en attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c021ff10f2a1a812c46fb77663ac1a3a3a8d791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516639"
---
# <a name="pending-call-handles"></a>Handles d’appel en attente

Un fournisseur de services doit créer un ou plusieurs handles d’appel (variables de type [HDRVCALL](hdrvline.md)) chaque fois que TAPI appelle l’une des fonctions suivantes : [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall), [**TSPI \_ lineCompleteTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer), [**TSPI \_ lineForward**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward), [**TSPI \_ linePickup**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup), [**TSPI \_ linePrepareAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference), [**TSPI \_ lineSetupConference**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference), [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)et [**TSPI \_ lineUnpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark). Lorsqu’un fournisseur de services reçoit un tel appel, le fournisseur de services doit définir la variable fournie par l’interface TAPI sur la valeur du handle avant de retourner à partir de l’appel. L’interface TAPI considère ce « handle d’appel en attente » comme étant provisoirement valide. Quand le fournisseur de services crée réellement l’appel, il doit appeler le rappel d' [**\_ achèvement asynchrone**](/windows/win32/api/tspi/nc-tspi-async_completion) pour valider le handle de manière formelle.

Si l’interface TAPI appelle la fonction [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) avant que le fournisseur de services valide officiellement un handle d’appel en attente, le fournisseur de services doit arrêter tout traitement supplémentaire associé au handle d’appel et appeler la fonction de rappel d' [**\_ achèvement asynchrone**](/windows/win32/api/tspi/nc-tspi-async_completion) à l’aide de la valeur d’erreur LINEERR \_ OPERATIONFAILED.

 

 
