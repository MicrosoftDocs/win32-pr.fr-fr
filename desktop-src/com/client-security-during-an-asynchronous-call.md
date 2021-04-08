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
# <a name="client-security-during-an-asynchronous-call"></a><span data-ttu-id="6b5de-103">Sécurité du client pendant un appel asynchrone</span><span class="sxs-lookup"><span data-stu-id="6b5de-103">Client Security During an Asynchronous Call</span></span>

<span data-ttu-id="6b5de-104">Le gestionnaire de proxy créé par MIDL pour les objets qui utilisent le marshaling standard implémente l’interface [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) .</span><span class="sxs-lookup"><span data-stu-id="6b5de-104">The proxy manager created by MIDL for objects that use standard marshaling implements the [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) interface.</span></span> <span data-ttu-id="6b5de-105">Les clients peuvent gérer la sécurité des appels marshalés en interrogeant les **IClientSecurity** sur l’objet d’appel et en obtenant ou en modifiant les paramètres de sécurité.</span><span class="sxs-lookup"><span data-stu-id="6b5de-105">Clients can manage the security of marshaled calls by querying for **IClientSecurity** on the call object and obtaining or changing security settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b5de-106">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6b5de-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b5de-107">Exécution d’un appel asynchrone</span><span class="sxs-lookup"><span data-stu-id="6b5de-107">Making an Asynchronous Call</span></span>](making-an-asynchronous-call.md)
</dt> </dl>

 

 




