---
description: Les certificats client et serveur doivent être stockés dans un magasin de certificats accessible par le processus d’application.
ms.assetid: 3be91b9b-ecc0-4cf2-88ca-77fd25d2dafc
title: Magasin de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64451ea7f568bb5e86289d5d9f1587d98b65aa1d53c14a4a251a5e61fe72b21d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883489"
---
# <a name="certificate-stores"></a>Magasin de certificats

Les certificats [*client*](/windows/desktop/SecGloss/c-gly) et [*serveur*](/windows/desktop/SecGloss/s-gly) doivent être stockés dans un [*magasin de certificats*](/windows/desktop/SecGloss/c-gly) accessible par le processus d’application. En règle générale, il s’agit du magasin mon magasin, également appelé magasin personnel. les applications clientes telles qu’Internet Explorer utilisent normalement le magasin mon magasin de l’utilisateur actuel, tandis que les serveurs tels que Internet Information Services (IIS) utilisent le magasin mon magasin de l’ordinateur local.

Le magasin racine et le magasin de l' [*autorité de certification*](/windows/desktop/SecGloss/c-gly) sont utilisés lorsque Schannel ou une application génère une chaîne de certificats à envoyer à l’ordinateur distant. Ces magasins sont utilisés pour valider une chaîne de certificats reçue. Pour plus d’informations, consultez [exécution de l’authentification à l’aide de Schannel](performing-authentication-using-schannel.md).

 

 
