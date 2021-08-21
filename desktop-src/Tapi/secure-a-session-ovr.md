---
description: Si une application ne souhaite aucune interférence par des événements extérieurs pour une session de la part de l’interface TAPI ou du fournisseur de services, elle doit sécuriser l’appel.
ms.assetid: 0a3be209-e3ff-4177-abb2-ad0facbdf569
title: Sécuriser une session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64ee16dc0854c6502f1347a3aa676e709920555ad91a02190db001bd80b34824
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080459"
---
# <a name="secure-a-session"></a>Sécuriser une session

Si une application ne souhaite aucune interférence par des événements extérieurs pour une session de la part de l’interface TAPI ou du fournisseur de services, elle doit sécuriser l’appel. Par exemple, dans un environnement analogique, l’appel de tonalités peut détruire une télécopie ou une session de modem sur l’appel d’origine.

Une application peut sécuriser un appel au moment où l’appel est effectué ou après que l’appel existe déjà.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de cette opération.

**TAPI 2. x :** Consultez [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).

**TAPI 3. x :** Consultez [**ITAddress :: Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).

 

 
