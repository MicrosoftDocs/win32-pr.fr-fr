---
description: Les interfaces d’utilisation générales suivantes sont prises en charge par l’API d’inscription de certificats.
ms.assetid: 6b9d9761-6131-4408-8177-5418abd5e406
title: Interfaces d’assistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a0c6948e9b0fe09aee0b983d230f53bc8e76b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534056"
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

 

 



