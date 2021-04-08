---
title: Sécurité du client pendant un appel asynchrone
description: Sécurité du client pendant un appel asynchrone
ms.assetid: 26d1f2c2-cb08-49f1-8beb-b99b029f0d8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bea2f83bf6341704dd0265a37ec2f64b79e9b2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674825"
---
# <a name="client-security-during-an-asynchronous-call"></a>Sécurité du client pendant un appel asynchrone

Le gestionnaire de proxy créé par MIDL pour les objets qui utilisent le marshaling standard implémente l’interface [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) . Les clients peuvent gérer la sécurité des appels marshalés en interrogeant les **IClientSecurity** sur l’objet d’appel et en obtenant ou en modifiant les paramètres de sécurité.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exécution d’un appel asynchrone](making-an-asynchronous-call.md)
</dt> </dl>

 

 




