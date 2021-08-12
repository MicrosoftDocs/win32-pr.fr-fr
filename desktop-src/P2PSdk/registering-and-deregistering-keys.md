---
description: Inscription et annulation de l’inscription des clés
ms.assetid: 90fd8df0-e2a8-4183-a50c-e6f8ea5041cc
title: Inscription et annulation de l’inscription des clés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d586fc2bf399a30b8a962611a21a4e0994d88f4513453c071b110de1d4142b92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612162"
---
# <a name="registering-and-deregistering-keys"></a>Inscription et annulation de l’inscription des clés

## <a name="registering-keys"></a>Enregistrement des clés

Un nœud peut enregistrer des clés avec [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) à tout moment dans les États réseau **DRT \_ actif**, **DRT \_ seul** et **DRT \_ \_ non** . Les clés inscrites en **DRT \_** uniquement et **DRT \_ aucun état \_ réseau** ne peuvent être reconnues par d’autres DRTs une fois que le nœud local est passé à **DRT \_ actif**.

Les clés identiques ne peuvent pas être inscrites dans la même instance DRT lors de l’utilisation de [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider). Si l’inscription de clés identiques est tentée, l’inscription de la deuxième clé échoue. L’utilisation de clés identiques doit également être évitée entre différentes instances DRT. Recherche par rapport à la désignation de clé unique ces clés identiques peuvent retourner l’une des clés, quelles que soient les données associées à la clé.

> [!Note]  
> Si un comportement différent est requis pour l’implémentation, un fournisseur de sécurité peut être créé à la place de [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) pour prendre en charge.

 

## <a name="deregistering-keys"></a>Annulation de l’inscription des clés

Un nœud peut annuler l’inscription d’une clé à chaque fois qu’elle a été inscrite. Toutefois, seule l’application qui a inscrit la clé peut la supprimer. Une application peut annuler l’inscription d’une clé à partir du nœud local à l’aide de la fonction [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) . Une fois l’opération terminée, la fonction déclenche un événement de **\_ \_ \_ \_ modification de clé LEAFSET d’événement DRT** , en informant l’application et les autres nœuds qui participent à la maille DRT.

Dans l’état **d' \_ erreur DRT** , l’appel requis de [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) entraînera l’annulation de l’inscription de toutes les clés par l’infrastructure DRT.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recherche dans une table de routage distribuée](searching-a-distributed-routing-table.md)
</dt> <dt>

[À propos des tables de routage distribuées](about-distributed-routing-tables.md)
</dt> <dt>

[Référence de API Table de routage distribué](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



