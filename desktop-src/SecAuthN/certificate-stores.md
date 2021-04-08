---
description: Les certificats client et serveur doivent être stockés dans un magasin de certificats accessible par le processus d’application.
ms.assetid: 3be91b9b-ecc0-4cf2-88ca-77fd25d2dafc
title: Magasin de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba46318f095c78e7813ed962e066fd7e4650126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034265"
---
# <a name="certificate-stores"></a>Magasin de certificats

Les certificats [*client*](/windows/desktop/SecGloss/c-gly) et [*serveur*](/windows/desktop/SecGloss/s-gly) doivent être stockés dans un [*magasin de certificats*](/windows/desktop/SecGloss/c-gly) accessible par le processus d’application. En règle générale, il s’agit du magasin mon magasin, également appelé magasin personnel. Les applications clientes telles qu’Internet Explorer utilisent normalement le magasin mon magasin de l’utilisateur actuel, tandis que les serveurs tels que Internet Information Services (IIS) utilisent le magasin mon magasin de l’ordinateur local.

Le magasin racine et le magasin de l' [*autorité de certification*](/windows/desktop/SecGloss/c-gly) sont utilisés lorsque Schannel ou une application génère une chaîne de certificats à envoyer à l’ordinateur distant. Ces magasins sont utilisés pour valider une chaîne de certificats reçue. Pour plus d’informations, consultez [exécution de l’authentification à l’aide de Schannel](performing-authentication-using-schannel.md).

 

 
