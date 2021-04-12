---
description: Les sections suivantes contiennent une liste alphabétique des fonctions regroupées par zone. Les informations de chaque fonction incluent une liste des États d’appel valides à l’entrée de la fonction et des transitions d’état d’appel standard lorsque la demande est terminée.
ms.assetid: 555d6af2-b440-4636-b90e-da297a369753
title: Fonctions TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38532fa1c0b978e3e59e54b08fbc43152fa0bd64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529212"
---
# <a name="tapi-functions"></a>Fonctions TAPI

Les sections suivantes contiennent une liste alphabétique des fonctions regroupées par zone. Les informations de chaque fonction incluent une liste des États d’appel valides à l’entrée de la fonction et des transitions d’état d’appel standard lorsque la demande est terminée.

-   [Fonctions de téléphonie assistée](assisted-telephony-functions.md)
-   [Fonctions du centre d’appels](call-center-functions.md)
-   [Fonctions du périphérique de ligne](line-device-functions.md)
-   [Fonctions des appareils téléphoniques](phone-device-functions.md)

Pour les fonctions TAPI catégorisées par niveau de service et tâche, consultez [référence des fonctions rapides TAPI](tapi-quick-function-reference.md).

Notez que les limitations du fournisseur de services peuvent exister en ce qui concerne les États réels dans lesquels une fonction peut être exécutée. Les applications doivent vérifier le membre **dwCallFeatures** dans la structure [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) , le membre **dwAddressFeatures** dans la structure [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) et le membre **dwLineFeatures** dans la structure [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) pour déterminer si une fonction est autorisée ou non dans l’état d’appel actuel.

 

 



