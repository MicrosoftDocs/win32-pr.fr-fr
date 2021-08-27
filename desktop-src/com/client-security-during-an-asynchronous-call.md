---
title: Sécurité du client pendant un appel asynchrone
description: Sécurité du client pendant un appel asynchrone
ms.assetid: 26d1f2c2-cb08-49f1-8beb-b99b029f0d8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c4c25e17712d0164938f3de9895d1e6b02582f2d86cba9957297e23aa4e7f1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071039"
---
# <a name="client-security-during-an-asynchronous-call"></a>Sécurité du client pendant un appel asynchrone

Le gestionnaire de proxy créé par MIDL pour les objets qui utilisent le marshaling standard implémente l’interface [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) . Les clients peuvent gérer la sécurité des appels marshalés en interrogeant les **IClientSecurity** sur l’objet d’appel et en obtenant ou en modifiant les paramètres de sécurité.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exécution d’un appel asynchrone](making-an-asynchronous-call.md)
</dt> </dl>

 

 




