---
description: Si une application ne souhaite aucune interférence par des événements extérieurs pour une session de la part de l’interface TAPI ou du fournisseur de services, elle doit sécuriser l’appel.
ms.assetid: 0a3be209-e3ff-4177-abb2-ad0facbdf569
title: Sécuriser une session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b1567303efb61f28f9c6b3e92c24287d23d4af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414681"
---
# <a name="secure-a-session"></a>Sécuriser une session

Si une application ne souhaite aucune interférence par des événements extérieurs pour une session de la part de l’interface TAPI ou du fournisseur de services, elle doit sécuriser l’appel. Par exemple, dans un environnement analogique, l’appel de tonalités peut détruire une télécopie ou une session de modem sur l’appel d’origine.

Une application peut sécuriser un appel au moment où l’appel est effectué ou après que l’appel existe déjà.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de cette opération.

**TAPI 2. x :** Consultez [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).

**TAPI 3. x :** Consultez [**ITAddress :: Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).

 

 
