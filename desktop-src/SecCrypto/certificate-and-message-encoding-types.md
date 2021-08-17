---
description: La plupart des fonctions requièrent des types d’encodage de message ou de certificat.
ms.assetid: 97b25435-aec2-4fdb-a4c6-89ec2e26f51d
title: Types d’encodage de message et de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 185be8d3cc781786c93ac809c042c86d3601a45d86eaa39452f0bcbf44203a1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771975"
---
# <a name="certificate-and-message-encoding-types"></a>Types d’encodage de message et de certificat

La plupart des fonctions requièrent des [*types d’encodage de message*](../secgloss/m-gly.md)ou de certificat. Ce type d’encodage est une **valeur DWORD** qui contient éventuellement le certificat et les types d’encodage de message. Le type d’encodage de certificat est stocké dans le mot de poids faible. Le type d’encodage de message est stocké dans le mot de poids fort. Certains champs de fonction ou de structure nécessitent uniquement l’un des types d’encodage, mais il est toujours acceptable de spécifier les deux types d’encodage. Pour obtenir un exemple de spécification des deux types d’encodage, consultez [ \# includes et \# definis](-includes-and--defines.md).

La Convention d’affectation de noms de paramètres suivante est utilisée pour indiquer les types d’encodage requis.



| Nom                       | Commentaires                                                                                                                                                                                                                                                                                                                |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *dwMsgAndCertEncodingType* | Les deux types d’encodage sont requis.                                                                                                                                                                                                                                                                                       |
| *dwMsgEncodingType*        | Seul le type d’encodage de message est requis.                                                                                                                                                                                                                                                                             |
| *dwCertEncodingType*       | Seul le type d’encodage de certificat est obligatoire.                                                                                                                                                                                                                                                                         |
| *dwEncodingType*           | Un message ou un type d’encodage de certificat est requis. Si le mot de poids faible contenant le type d’encodage de certificat est différent de zéro, il est utilisé. Dans le cas contraire, le mot de poids fort contenant le type d’encodage de message est utilisé. Si les deux sont spécifiés, le type d’encodage de certificat dans le mot de poids faible est utilisé. |



 

Les types d’encodage actuellement définis sont présentés dans le tableau suivant.



| Type d’encodage          | Valeur      |
|------------------------|------------|
| CRYPTer l' \_ \_ encodage ASN   | 0x00000001 |
| \_Codage ASN \_ x509    | 0x00000001 |
| Encodage ASN de PKCS \_ 7 \_ \_ | 0x00010000 |



 

 

 
