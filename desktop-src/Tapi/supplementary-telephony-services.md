---
description: Les services de téléphonie supplémentaires sont la collection de tous les services définis par l’API, à l’exception de ceux inclus dans le sous-ensemble de base de la téléphonie.
ms.assetid: a2a30a0d-fbfd-4317-8e3a-d1e1e8b86ae0
title: Services de téléphonie supplémentaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9762b2d9ca74d0212170e1e87662242d3983663db024ce52018d108cc37fb883
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760751"
---
# <a name="supplementary-telephony-services"></a>Services de téléphonie supplémentaires

Les services de téléphonie supplémentaires sont la collection de tous les services définis par l’API, à l’exception de ceux inclus dans le sous-ensemble de base de la téléphonie. Elle comprend toutes les fonctionnalités supplémentaires qui se trouvent sur les PBX modernes, telles que le maintien, le transfert, la Conférence, le stationnement, etc. Toutes les fonctionnalités supplémentaires sont considérées comme facultatives. autrement dit, le fournisseur de services décide quels services il fait ou ne fournit pas.

Une application peut interroger un appareil téléphonique ou une ligne pour l’ensemble des services supplémentaires qu’il fournit à l’aide de fonctions telles que [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) ou [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps). Un seul service supplémentaire peut être constitué de plusieurs appels et messages de fonction. L’API de téléphonie, et non le développeur du fournisseur de services, définit le comportement de chacune de ces fonctionnalités supplémentaires. Un fournisseur de services doit fournir un service de téléphonie supplémentaire uniquement s’il peut implémenter la signification exacte telle que définie par l’API. Si ce n’est pas le cas, la fonctionnalité doit être fournie en tant que service de téléphonie étendu.

Comme mentionné dans les services de téléphonie de base, les services de téléphone sont considérés comme facultatifs. Par conséquent, tous les services de l’appareil téléphonique font partie d’une téléphonie supplémentaire. Pour obtenir la liste des fonctions de téléphonie supplémentaire, consultez la page de référence sur les fonctions [rapides TAPI](./tapi-quick-function-reference.md).

 

 
