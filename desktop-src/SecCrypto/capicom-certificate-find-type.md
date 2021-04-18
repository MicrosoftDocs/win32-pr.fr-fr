---
description: Le \_ \_ \_ type d’énumération de type d’énumération de certificat CAPICOM définit le type de critère de recherche utilisé pour rechercher des certificats spécifiques. Ce type d’énumération a été introduit dans CAPICOM 2,0.
ms.assetid: d71436e5-d921-4b84-8028-301d8fc4aedb
title: Énumération CAPICOM_CERTIFICATE_FIND_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_FIND_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: c5c867b230ba2045d97619d7f55e257bd7803b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525979"
---
# <a name="capicom_certificate_find_type-enumeration"></a>L' \_ \_ \_ énumération de type de certificat CAPICOM

Le type d’énumération de **\_ \_ \_ type** d’énumération de certificat CAPICOM définit le type de critère de recherche utilisé pour rechercher des certificats spécifiques. Ce type d’énumération a été introduit dans CAPICOM 2,0.

## <a name="members"></a>Membres



| Membre                                                | Description                                                                                                                                 | Valeur |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **Le certificat CAPICOM \_ \_ trouve un \_ \_ hachage SHA1**            | Retourne les certificats correspondant à un hachage SHA1 spécifié.<br/>                                                                             | 0     |
| **le certificat CAPICOM \_ trouve le nom de l' \_ \_ objet \_**         | Retourne les certificats dont le nom de sujet correspond exactement ou partiellement à un nom d’objet spécifié.<br/>                                   | 1     |
| **le certificat CAPICOM \_ trouve le nom de l' \_ \_ émetteur \_**          | Retourne les certificats dont le nom d’émetteur correspond exactement ou partiellement à un nom d’émetteur spécifié.<br/>                                     | 2     |
| **\_ \_ \_ nom racine de la recherche du certificat CAPICOM \_**            | Retourne les certificats dont le nom d’objet racine correspond exactement ou partiellement à un nom d’objet racine spécifié.<br/>                         | 3     |
| **\_nom du modèle de \_ recherche de certificat \_ CAPICOM \_**        | Retourne les certificats dont le nom de modèle correspond à un nom de modèle spécifié.<br/>                                                      | 4     |
| **EXTENSION de recherche de \_ certificat CAPICOM \_ \_**             | Retourne les certificats qui ont une extension qui correspond à une extension spécifiée.<br/>                                                  | 5     |
| **la \_ \_ \_ \_ propriété étendue de la recherche du certificat CAPICOM**    | Retourne les certificats qui ont une propriété étendue dont l’identificateur de propriété correspond à un identificateur de propriété spécifié.<br/>           | 6     |
| **certificat CAPICOM- \_ \_ stratégie d' \_ application de recherche \_**   | Retourne les certificats dans le magasin qui ont une extension ou une propriété d’utilisation avancée de la clé associée à un identificateur d’utilisation.<br/> | 7     |
| **certificat CAPICOM- \_ \_ Rechercher la \_ stratégie de certificat \_**   | Retourne les certificats contenant un OID de stratégie spécifié.<br/>                                                                          | 8     |
| **\_temps de recherche du certificat CAPICOM \_ \_ \_ valide**           | Retourne les certificats dont l’heure est valide.<br/>                                                                                        | 9     |
| **l’heure de la \_ recherche du certificat CAPICOM n’est \_ \_ \_ pas \_ encore \_ valide** | Retourne des certificats dont l’heure n’est pas encore valide.<br/>                                                                                | 10    |
| **\_temps de recherche du certificat CAPICOM \_ \_ \_ expiré**         | Retourne les certificats dont le temps a expiré.<br/>                                                                                     | 11    |
| **utilisation de la \_ \_ clé de recherche de certificat CAPICOM \_ \_**            | Retourne les certificats contenant une clé qui peut être utilisée de la manière spécifiée.<br/>                                                  | 12    |



## <a name="remarks"></a>Notes

Le type d’énumération de **\_ \_ \_ type du certificat CAPICOM** est utilisé par la méthode [**Certificates. Find**](certificates-find.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




