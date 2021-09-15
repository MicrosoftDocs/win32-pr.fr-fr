---
description: Fournit des propriétés et des méthodes que vous pouvez utiliser pour choisir, gérer et utiliser des magasins de certificats et les certificats de ces magasins.
ms.assetid: de4eecf7-c03b-4733-ac29-d5b26b873dba
title: Objet Store
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4e8a14fcecf0ded2e4e1a56e2b98e4ac4838b776
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413451"
---
# <a name="store-object"></a>Objet Store

\[L’objet **Store** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L’objet **Store** fournit des propriétés et des méthodes que vous pouvez utiliser pour choisir, gérer et utiliser des [*magasins de certificats*](../secgloss/c-gly.md) et les certificats de ces magasins. CAPICOM peut utiliser les magasins de l’utilisateur actuel, de l’ordinateur local, de la mémoire et de la Active Directory. En outre, les magasins prennent en charge les magasins de certificats basés sur une carte à puce. Les développeurs doivent savoir que certaines méthodes peuvent échouer avec certains magasins si des opérations sont tentées pour lesquelles l’utilisateur ne dispose pas de droits.

## <a name="members"></a>Membres

L’objet **Store** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **Store** possède ces méthodes.



| Méthode                         | Description                                                                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Complémentaires**](store-add.md)       | Ajoute un objet [**certificat**](certificate.md) au magasin de certificats ouvert.<br/>                                                                                                                       |
| [**Plus**](store-close.md)   | Ferme un magasin de certificats ouvert.<br/> **CAPICOM 2.0.0.3 et versions antérieures :** La méthode [**Close**](store-close.md) n’est pas prise en charge.<br/>                                                               |
| [**Supprimer**](store-delete.md) | Supprime le magasin de certificats représenté par l’objet de [**magasin**](certificate.md) actuel.<br/> **CAPICOM 2.0.0.3 et versions antérieures :** La méthode [**Delete**](store-delete.md) n’est pas prise en charge.<br/> |
| [**Exporter**](store-export.md) | Exporte le magasin d’un [*objet BLOB*](../secgloss/b-gly.md)encodé.<br/>                                                                                                       |
| [**Importer**](store-import.md) | Importe un magasin précédemment exporté.<br/>                                                                                                                                                                  |
| [**Chargera**](store-load.md)     | Importe des objets de [**certificat**](certificate.md) à partir d’un fichier dans le magasin.<br/>                                                                                                                        |
| [**Ouvrir**](store-open.md)     | Ouvre un magasin de certificats.<br/>                                                                                                                                                                            |
| [**Supprimer**](store-remove.md) | Supprime un objet [**certificat**](certificate.md) d’un magasin ouvert.<br/>                                                                                                                               |



 

### <a name="properties"></a>Propriétés

L’objet **Store** a ces propriétés.



| Propriété                                              | Type d’accès          | Description                                                                                                                                                                                           |
|:------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificats**](store-certificates.md)<br/> | Lecture seule<br/> | Récupère la collection de [**certificats**](certificates.md) du magasin. Il s’agit de la propriété par défaut.<br/>                                                                                  |
| [**Emplacement**](store-location.md)<br/>         | Lecture seule<br/> | Récupère l’emplacement du magasin de certificats que cet objet représente.<br/> **CAPICOM 2.0.0.3 et versions antérieures :** La propriété d' [**emplacement**](store-location.md) n’est pas prise en charge.<br/> |
| [**Nomme**](store-name.md)<br/>                 | Lecture seule<br/> | Récupère le nom du magasin de certificats que cet objet représente.<br/> **CAPICOM 2.0.0.3 et versions antérieures :** La propriété [**Name**](store-name.md) n’est pas prise en charge.<br/>             |



 

## <a name="remarks"></a>Notes

L’objet **Store** peut être créé et il est sécurisé pour l’écriture de scripts. Le ProgID de l’objet **Store** est CAPICOM. Store. 2.

**CAPICOM 1. *x*:** le ProgID de l’objet **Store** est CAPICOM. Store. 1.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> </dl>

 

 
