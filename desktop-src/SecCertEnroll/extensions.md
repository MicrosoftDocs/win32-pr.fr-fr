---
description: Le format de certificat X. 509 version 3 identifie plusieurs extensions qui peuvent être ajoutées à un certificat.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Extensions (API d’inscription de certificat)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5478b8edeff3524ada760cc5680f5c9dca359e7a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009039"
---
# <a name="extensions-certificate-enrollment-api"></a>Extensions (API d’inscription de certificat)

Le format de certificat X. 509 version 3 identifie plusieurs extensions qui peuvent être ajoutées à un certificat. Les extensions fournissent des informations améliorées sur l’utilisation de la clé, les stratégies de certificat et les contraintes, les autres formats de nom, et bien plus encore. Vous pouvez utiliser l’interface [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) pour définir une valeur d’extension. La plupart des extensions courantes peuvent être créées à l’aide d’interfaces prédéfinies dérivées de **IX509Extension**. Une collection d’extensions est ajoutée à une demande de certificat en incluant la collection dans les attributs de la demande. Pour plus d'informations, voir les rubriques suivantes :

-   [Extensions prises en charge](supported-extensions.md)
-   [\#Extensions PKCS 10](pkcs--10-extensions.md)
-   [Extensions CMC](cmc-extensions.md)

 

 



