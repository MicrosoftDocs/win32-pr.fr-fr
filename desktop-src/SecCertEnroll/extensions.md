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
ms.openlocfilehash: 534c3cf9268f21c36d982a627de2e1b293ffdca1e1fd4ffc2acd0db9f7d6059b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867939"
---
# <a name="extensions-certificate-enrollment-api"></a>Extensions (API d’inscription de certificat)

Le format de certificat X. 509 version 3 identifie plusieurs extensions qui peuvent être ajoutées à un certificat. Les extensions fournissent des informations améliorées sur l’utilisation de la clé, les stratégies de certificat et les contraintes, les autres formats de nom, et bien plus encore. Vous pouvez utiliser l’interface [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) pour définir une valeur d’extension. La plupart des extensions courantes peuvent être créées à l’aide d’interfaces prédéfinies dérivées de **IX509Extension**. Une collection d’extensions est ajoutée à une demande de certificat en incluant la collection dans les attributs de la demande. Pour plus d'informations, voir les rubriques suivantes :

-   [Extensions prises en charge](supported-extensions.md)
-   [\#Extensions PKCS 10](pkcs--10-extensions.md)
-   [Extensions CMC](cmc-extensions.md)

 

 



