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
ms.openlocfilehash: ee009e3f346c7e7a179a324ec68834999acd711934ab5c64a3cae1845372dbdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211334"
---
# <a name="remote-calls-to-the-sam-rpc-protocol-are-restricted-to-only-local-administrators"></a>Les appels distants au protocole SAM RPC sont limités aux seuls administrateurs locaux

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

Le protocole SAM RPC est limité. Cela signifie que seuls les membres du groupe Administrateurs local peuvent effectuer des appels distants par rapport aux méthodes de ce protocole. Active Directory comportement du contrôleur de domaine n’est pas affecté.

## <a name="mitigations"></a>Corrections

Vérifiez que les utilisateurs appropriés sont définis en tant qu’administrateurs sur le PC. La liste de contrôle d’accès utilisée pour la vérification d’accès est configurable via la stratégie de groupe.

 

 




