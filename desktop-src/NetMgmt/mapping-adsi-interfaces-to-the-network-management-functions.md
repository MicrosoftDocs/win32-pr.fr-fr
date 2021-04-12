---
title: Mappage des interfaces ADSI avec les fonctions de gestion de réseau
description: Les interfaces ADSI (Active Directory Service Interfaces) sont un ensemble d’interfaces COM utilisées pour accéder aux fonctionnalités des services d’annuaire à partir de différents fournisseurs de réseau.
ms.assetid: dfa81c58-3ce4-40ee-8bfc-a19a13781992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ec1a1055d3d016bf8b7b1bd3f357810b7ddd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316433"
---
# <a name="mapping-adsi-interfaces-to-the-network-management-functions"></a>Mappage des interfaces ADSI avec les fonctions de gestion de réseau

Les interfaces ADSI (Active Directory Service Interfaces) sont un ensemble d’interfaces COM utilisées pour accéder aux fonctionnalités des services d’annuaire à partir de différents fournisseurs de réseau. ADSI présente un ensemble unique d’interfaces de service d’annuaire pour la gestion des ressources réseau dans un environnement informatique distribué.

Si vous programmez pour Active Directory, vous pourrez peut-être appeler certaines méthodes d’interface ADSI pour obtenir les mêmes fonctionnalités que celles que vous pouvez obtenir en appelant certaines fonctions de gestion de réseau.

Le tableau suivant répertorie les fonctions de gestion de réseau et les groupes de fonctions, ainsi que les interfaces ADSI auxquelles les fonctions sont mappées.



| Fonctions                                                                  | Interfaces                                                                                             |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum), [ **NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource), [ **IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations) |
| [Groupe réseau](group-functions.md)\*                                          | [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)                                                                        |
| [NetLocalGroup](local-group-functions.md)\*                               | [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)                                                                        |
| [Serveur netserver](server-functions.md)\*                                        | [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer)                                                                  |
| [Session](session-functions.md)\*                                      | [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession), [ **IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)   |
| [NetShare](share-functions.md)\*                                          | [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare)                                                                |
| [Netuser](user-functions.md)\*                                            | [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser), [ **IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer)                                   |
| [NetUserModals](user-modal-functions.md)\*                                | [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain)                                                                      |



 

Pour plus d’informations sur les services d’annuaire et la programmation avec ADSI, consultez [Active Directory interfaces de service](/windows/desktop/ADSI/active-directory-service-interfaces-adsi). Pour plus d’informations sur les propriétés personnalisées que le fournisseur Winnt met à la disposition de la classe User et sur les méthodes de propriété de l’interface [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) que le fournisseur Winnt ne prend pas en charge, consultez [fournisseur Winnt ADSI](/windows/desktop/ADSI/adsi-winnt-provider).

 

 