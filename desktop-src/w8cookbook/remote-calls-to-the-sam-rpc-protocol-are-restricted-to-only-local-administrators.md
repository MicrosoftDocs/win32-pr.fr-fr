---
title: Les appels distants au protocole SAM RPC sont limités aux seuls administrateurs locaux
description: Le protocole SAM RPC est limité. Cela signifie que seuls les membres du groupe Administrateurs local peuvent effectuer des appels distants par rapport aux méthodes de ce protocole. Active Directory comportement du contrôleur de domaine n’est pas affecté.
ms.assetid: 816BFB8C-A8EE-44F4-864D-748AF8BCF1F8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 669c20503551b0a380372524b898559dff472f2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100817"
---
# <a name="remote-calls-to-the-sam-rpc-protocol-are-restricted-to-only-local-administrators"></a>Les appels distants au protocole SAM RPC sont limités aux seuls administrateurs locaux

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Le protocole SAM RPC est limité. Cela signifie que seuls les membres du groupe Administrateurs local peuvent effectuer des appels distants par rapport aux méthodes de ce protocole. Active Directory comportement du contrôleur de domaine n’est pas affecté.

## <a name="mitigations"></a>Corrections

Vérifiez que les utilisateurs appropriés sont définis en tant qu’administrateurs sur le PC. La liste de contrôle d’accès utilisée pour la vérification d’accès est configurable via la stratégie de groupe.

 

 




