---
description: Les propriétés suivantes sont définies par l’interface ICertSrvSetupKeyInformation.
ms.assetid: d805a011-8728-4687-8e4a-ad331617abe7
title: Propriétés de ICertSrvSetupKeyInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2a41647c06015c011d4d7a36cddfd81466b3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865454"
---
# <a name="properties-of-icertsrvsetupkeyinformation"></a>Propriétés de ICertSrvSetupKeyInformation

Les propriétés suivantes sont définies par l’interface [**ICertSrvSetupKeyInformation**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) .



| Propriété                                                                           | Description                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ContainerName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_containername)                 | Obtient ou définit le nom utilisé par le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) pour générer, stocker ou accéder à la clé.                                                                       |
| [**Existing**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existing)                           | Obtient ou définit une valeur qui indique si la clé privée existe déjà.                                                                                                                                                                                                                       |
| [**ExistingCACertificate**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existingcacertificate) | Obtient ou définit la valeur binaire qui a été encodée à l’aide de [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) et qui est la valeur binaire du certificat d’autorité de certification qui correspond à une clé existante. |
| [**HashAlgorithm**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_hashalgorithm)                 | Obtient ou définit le nom de l’algorithme de hachage utilisé pour signer ou vérifier le certificat de l’autorité de certification pour la clé.                                                                                                                                                                                                |
| [**Longueur**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_length)                               | Obtient ou définit la force de la clé sur l’une des valeurs prises en charge par le fournisseur de services de chiffrement.                                                                                                                                                                                                                   |
| [**ProviderName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_providername)                   | Obtient ou définit le nom du fournisseur de services de chiffrement utilisé pour générer ou stocker la clé privée.                                                                                                                                                                                                               |



 

 

 
