---
description: 'Destinataires, objet : représente une collection d’objets de certificat.'
ms.assetid: 11d294b5-0a8a-4970-be10-a3b22389d96e
title: Objet Recipients
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: adbcec006add6f06651869ae9c03c17f476ea4b3679f8ddba724a1890f73f1d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117975249"
---
# <a name="recipients-object"></a>Objet Recipients

\[L’objet **destinataires** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L’objet **Recipients** représente une collection d’objets [**Certificate**](certificate.md) . Chaque objet représente un destinataire prévu du message enveloppé. Les données d’un objet [**EnvelopedData**](envelopeddata.md) sont chiffrées à l’aide d’une clé de session [*symétrique*](../secgloss/s-gly.md) , et cette clé de session symétrique est ensuite chiffrée pour chaque destinataire à l’aide de la clé publique du certificat du destinataire prévu. Un destinataire ayant accès à la [*clé privée*](../secgloss/p-gly.md) associée à la [*clé publique*](../secgloss/p-gly.md) d’un certificat peut déchiffrer la [*clé de session*](../secgloss/s-gly.md) et utiliser la clé de session déchiffrée pour déchiffrer les données réelles.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **Recipients** est utilisé pour effectuer les tâches suivantes :

-   Ajoutez ou supprimez un objet [**certificat**](certificate.md) de la collection.
-   Récupérez le nombre de certificats dans la collection.
-   Récupérez un objet **destinataires** spécifique de la collection.
-   Itérez au sein de la collection.

## <a name="members"></a>Membres

L’objet **Recipients** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **Recipients** possède ces méthodes.



| Méthode                              | Description                                                                            |
|:------------------------------------|:---------------------------------------------------------------------------------------|
| [**Complémentaires**](recipients-add.md)       | Ajoute un objet [**certificat**](certificate.md) à la collection.<br/>         |
| [**Effacer**](recipients-clear.md)   | Supprime tous les objets de [**certificat**](certificate.md) de la collection.<br/> |
| [**Installez**](recipients-remove.md) | Supprime un objet [**certificat**](certificate.md) de la collection.<br/>    |



 

### <a name="properties"></a>Propriétés

L’objet **Recipients** possède ces propriétés.



| Propriété                                           | Type d’accès          | Description                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](recipients-newenum.md)<br/> | Lecture seule<br/> | Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection. cette propriété est masquée dans Visual Basic scripting Edition (VBScript).<br/> |
| [**Count**](recipients-count.md)<br/>       |                      | Nombre d’objets dans la collection **Recipients** .<br/>                                                                                                                                                              |
| [**Élément**](recipients-item.md)<br/>         |                      | Objet indexé dans la collection. Il s’agit de la propriété par défaut.<br/>                                                                                                                                                   |



 

## <a name="remarks"></a>Remarques

Impossible de créer l’objet **Recipients** .

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> </dl>

 

 
