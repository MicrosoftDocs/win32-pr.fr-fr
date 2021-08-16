---
description: Les interfaces d’utilisation générales suivantes sont prises en charge par l’API d’inscription de certificats.
ms.assetid: 6b9d9761-6131-4408-8177-5418abd5e406
title: Interfaces d’assistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec54f9e092bb7675f18a28e7af8599a4e870b5aec1d88d0c5d3332c33c2bef4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117779538"
---
# <a name="helper-interfaces"></a>Interfaces d’assistance

Les interfaces d’utilisation générales suivantes sont prises en charge par l’API d’inscription de certificats.



| Interface                                                                    | Description                                                                                                                                                            |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)                                 | Crée une chaîne encodée en Unicode à partir d’un tableau d’octets, crée un tableau d’octets à partir d’une chaîne encodée en Unicode et modifie le type d’encodage Unicode appliqué à une chaîne. |
| [**ICertificateAttestationChallenge**](/windows/desktop/api/Certenroll/nn-certenroll-icertificateattestationchallenge) | Prend en charge les défis liés à l’attestation de certificat.                                                                                                                           |
| [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid)                                               | Représente un identificateur d’objet.                                                                                                                                       |
| [**IObjectIds**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids)                                             | Gère une collection d’objets [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) .                                                                                                        |
| [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname)                     | Représente un nom unique X. 500.                                                                                                                                |
| [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey)                           | Interface de clé de type EK X. 509                                                                                                                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[CertEnroll, interfaces](certenroll-interfaces.md)
</dt> </dl>

 

 



