---
title: Obtention des SDOs de service et d’utilisateur
description: Pour obtenir SDOs pour NPS (IAS) ou un utilisateur particulier, appelez les méthodes ISdoMachine GetServiceSDO ou ISdoMachine GetUserSDO.
ms.assetid: 23e23fb3-0102-4c36-b30f-18604131ee32
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebef1e695236bd1449ab886cb998a67f09c2cafc8ded446b0b7e1ad89b01181
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128589"
---
# <a name="obtaining-service-and-user-sdos"></a>Obtention des SDOs de service et d’utilisateur

> [!Note]  
> le Service d’authentification Internet (IAS) a été renommé serveur nps (network Policy Server) à partir de Windows Server 2008.

 

Pour obtenir SDOs pour NPS (IAS) ou un utilisateur particulier, appelez les méthodes [**ISdoMachine :: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) ou [**ISdoMachine :: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) . Ces méthodes retournent des pointeurs vers des interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pour ces objets. Pour l’utilisateur SDO, utilisez la méthode [**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour obtenir une interface [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) pour l’objet. Pour le service SDO, utilisez **IUnknown :: QueryInterface** pour obtenir une interface [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) ou une interface [**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) .

Avant d’appeler [**ISdoMachine :: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) ou [**ISdoMachine :: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo), appelez [**ISdoMachine :: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) pour associer l’objet ordinateur à l’ordinateur local.

Consultez [récupération d’un SDO de service](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) et [récupération d’un utilisateur SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) pour obtenir un exemple de code qui montre comment obtenir ces SDOs.

 

 