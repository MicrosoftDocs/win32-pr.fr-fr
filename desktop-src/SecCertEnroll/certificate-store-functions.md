---
description: 'La bibliothèque Xenroll.dll contient les méthodes et les propriétés suivantes que vous pouvez utiliser pour gérer les magasins de certificats. FunctionsDescriptionCAStoreFlagsSpecifies ou retourne des indicateurs qui contrôlent l’accès au magasin de l’autorité de certification (CA). CAStoreNameWStrSpecifies ou retourne le nom du magasin de l’autorité de certification. CAStoreTypeWStrSpecifies ou retourne le type du magasin identifié par la propriété CAStoreName. MyStoreFlagsSpecifies ou retourne un indicateur qui détermine le chemin d’accès du magasin personnel. MyStoreNameWStrSpecifies ou retourne le nom du magasin personnel. MyStoreTypeWStrSpecifies ou retourne le type du magasin personnel. RequestStoreFlagsSpecifies ou retourne un indicateur qui détermine le chemin d’accès du magasin de demandes. RequestStoreNameWStrSpecifies ou retourne le nom du magasin de demandes. RequestStoreTypeWStrSpecifies ou retourne le type du magasin de demandes. RootStoreFlagsSpecifies ou retourne un indicateur qui détermine le chemin d’accès du magasin racine. RootStoreNameWStrSpecifies ou retourne le nom du magasin racine. RootStoreTypeWStrSpecifies ou retourne le type du magasin racine. SetHStoreCASpecifies le descripteur du magasin de l’autorité de certification. SetHStoreMySpecifies le descripteur du magasin personnel. SetHStoreRequestSpecifies handle du magasin de demandes. SetHStoreROOTSpecifies handle du magasin racine. '
ms.assetid: 15e4368b-4199-415a-9c2c-2c1351b717e6
title: Fonctions du magasin de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53a90a6fd2146517d4d70f653da42961274301a3058f8dbad9e72b8b90228bc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902173"
---
# <a name="certificate-store-functions"></a>Fonctions du magasin de certificats

La bibliothèque Xenroll.dll contient les méthodes et les propriétés suivantes que vous pouvez utiliser pour gérer les magasins de certificats.

| Fonctions                                                          | Description                                                                                                                                                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CAStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoreflags)                 | Spécifie ou retourne des indicateurs qui contrôlent l’accès au magasin de l' [*autorité de certification*](/windows/desktop/SecGloss/c-gly) .<br/> |
| [**CAStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castorenamewstr)           | Spécifie ou retourne le nom du magasin d’autorités de certification.<br/>                                                                                                                                            |
| [**CAStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoretypewstr)           | Spécifie ou retourne le type du magasin identifié par la propriété **CAStoreName** .<br/>                                                                                                    |
| [**MyStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoreflags)                 | Spécifie ou retourne un indicateur qui détermine le chemin d’accès du magasin personnel.<br/>                                                                                                               |
| [**MyStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystorenamewstr)           | Spécifie ou retourne le nom du magasin personnel.<br/>                                                                                                                                      |
| [**MyStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoretypewstr)           | Spécifie ou retourne le type du magasin personnel.<br/>                                                                                                                                      |
| [**RequestStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoreflags)       | Spécifie ou retourne un indicateur qui détermine le chemin d’accès du magasin de demandes.<br/>                                                                                                                |
| [**RequestStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststorenamewstr) | Spécifie ou retourne le nom du magasin de demandes.<br/>                                                                                                                                       |
| [**RequestStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoretypewstr) | Spécifie ou retourne le type du magasin de demandes.<br/>                                                                                                                                       |
| [**RootStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoreflags)             | Spécifie ou retourne un indicateur qui détermine le chemin d’accès du magasin racine.<br/>                                                                                                                   |
| [**RootStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstorenamewstr)       | Spécifie ou retourne le nom du magasin racine.<br/>                                                                                                                                          |
| [**RootStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoretypewstr)       | Spécifie ou retourne le type du magasin racine.<br/>                                                                                                                                          |
| [**SetHStoreCA**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoreca)                   | Spécifie le descripteur du magasin de l’autorité de certification.<br/>                                                                                                                                                     |
| [**SetHStoreMy**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoremy)                   | Spécifie le descripteur du magasin personnel.<br/>                                                                                                                                               |
| [**SetHStoreRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstorerequest)         | Spécifie le handle du magasin de demandes.<br/>                                                                                                                                                |
| [**SetHStoreROOT**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoreroot)               | Spécifie le handle du magasin racine.<br/>                                                                                                                                                   |



 

CertEnroll.dll n’exporte pas la fonctionnalité qui vous permet de spécifier ou de récupérer des valeurs de propriété de stockage ou de copier des certificats vers des magasins spécifiques.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mappage de Xenroll.dll à CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

