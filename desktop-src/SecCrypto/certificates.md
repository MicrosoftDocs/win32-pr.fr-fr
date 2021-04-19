---
description: Représente une collection d’objets de certificat.
ms.assetid: 82011c49-38fb-4261-8fb3-b76859da8a9e
title: Objet Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e8c12c16820342c5687720a35ce81aa7b94f180
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525109"
---
# <a name="certificates-object"></a>Objet Certificates

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L' **objet** [**Certificates**](certificate.md) représente une collection d’objets de certificat. Chaque objet [**certificat**](certificate.md) représente un seul [*certificat numérique*](../secgloss/d-gly.md).

L’objet **Certificates** expose les interfaces suivantes :

-   **ICertificates2**: introduit dans CAPICOM 2,0.
-   **ICertificates**: introduit dans CAPICOM 1,0.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **Certificates** est utilisé pour effectuer les tâches suivantes :

-   Ajoutez ou supprimez un objet de [**certificat**](certificate.md) à partir de la collection.
-   Générez un sous-ensemble de la collection en recherchant un ensemble de certificats ou en affichant une boîte de dialogue pour sélectionner les certificats.
-   Effacez tous les objets de [**certificat**](certificate.md) de la collection.
-   Récupérez le nombre de certificats dans la collection.
-   Récupérez un objet de [**certificat**](certificate.md) spécifique de la collection.
-   Itérez au sein de la collection.

## <a name="members"></a>Membres

L’objet **Certificates** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **Certificates** possède ces méthodes.



| Méthode                                | Description                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Complémentaires**](certificates-add.md)       | Ajoute un objet [**certificat**](certificate.md) à la collection.<br/> (Héritée de **CertificatesICertificates2**)                                        |
| [**Effacé**](certificates-clear.md)   | Supprime tous les objets de [**certificat**](certificate.md) de la collection.<br/> (Héritée de **CertificatesICertificates2**)                                |
| [**Trouver**](certificates-find.md)     | Retourne un objet de **certificats** qui contient tous les certificats qui correspondent aux critères de recherche spécifiés.<br/> (Héritée de **CertificatesICertificates2**) |
| [**Installez**](certificates-remove.md) | Supprime un objet de [**certificat**](certificate.md) unique de la collection.<br/> (Héritée de **CertificatesICertificates2**)                            |
| [**Enregistrer**](certificates-save.md)     | Enregistre les certificats dans un fichier spécifié.<br/> (Héritée de **CertificatesICertificates2**)                                                                |
| [**Sélectionner**](certificates-select.md) | Affiche une boîte de dialogue permettant de sélectionner des certificats et retourne une collection de ces certificats sélectionnés.<br/> (Héritée de **CertificatesICertificates2**)  |



 

### <a name="properties"></a>Propriétés

L’objet **Certificates** possède ces propriétés.



| Propriété                                             | Type d’accès          | Description                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](certificates-newenum.md)<br/> | Lecture seule<br/> | Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection. Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).<br/> |
| [**Saut**](certificates-count.md)<br/>       | Lecture seule<br/> | Récupère le nombre d’objets de [**certificat**](certificate.md) dans la collection.<br/>                                                                                                                                |
| [**Élément**](certificates-item.md)<br/>         | Lecture seule<br/> | Récupère un objet de [**certificat**](certificate.md) qui représente le certificat indexé de la collection. Il s’agit de la propriété par défaut.<br/> (Héritée de **CertificatesICertificates2ICertificates**)          |



 

## <a name="remarks"></a>Notes

L’objet **certificats** peut être créé et il est sécurisé pour l’écriture de scripts. Le ProgID de l’objet **Certificates** est «CAPICOM. Certificats. 2».

**CAPICOM 1. *x*:** le ProgID de l’objet **Certificates** est «CAPICOM. Certificats. 1».

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> </dl>

 

 
