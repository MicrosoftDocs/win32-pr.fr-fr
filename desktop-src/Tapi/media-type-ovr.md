---
description: Le type de média (ou mode) d’un appareil décrit le type d’informations qui peuvent être échangées, par exemple la voix interactive. Un appareil donné peut être en mesure de gérer un seul type de média, ou il peut être en mesure de traiter une plage de types.
ms.assetid: fccf85e9-3889-4ebc-b1bf-a60e27ab4586
title: Type de support
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369954a4b0d1f78e12f6ea42bcc2ec61ca425012
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522276"
---
# <a name="media-type"></a>Type de support

Le *type de média* (ou mode) d’un appareil décrit le type d’informations qui peuvent être échangées, par exemple la voix interactive. Un appareil donné peut être en mesure de gérer un seul type de média, ou il peut être en mesure de traiter une plage de types.

Les fournisseurs de services exposent le type de média ou les types pris en charge par les périphériques qu’ils contrôlent. Les applications interrogent le type de média, puis utilisent ces informations pour sélectionner une adresse appropriée sur laquelle lancer une session. La réponse d’application à une session proposée peut également être prédicat sur le type de média.

Une session de communication donnée, ou appel, peut impliquer plusieurs types de média. Pour plus d’informations, consultez type de média pour une session.

**TAPI 2. x :** Consultez [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), **dwAvailableMediaModes** , membre de la structure [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) pointée par *lpAddressCaps*, [ \_ constantes LINEMEDIAMODE](./linemediamode--constants.md).

**TAPI 3. x :** Consultez [**ITTerminal :: obtenir \_ MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [ \_ constantes TAPIMEDIATYPE](tapimediatype--constants.md).
