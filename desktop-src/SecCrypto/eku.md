---
description: Représente une propriété d’utilisation améliorée de la clé (EKU) d’un certificat.
ms.assetid: 08eb7c77-0224-4ab5-99e7-edf18eb23c60
title: Objet EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ff397ae747ecd09dd1292e5c15eb4291692d9651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531060"
---
# <a name="eku-object"></a>Objet EKU

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L’objet **EKU** représente une propriété unique de l’utilisation de la clé étendue (EKU) d’un certificat.

## <a name="members"></a>Membres

L’objet **EKU** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **EKU** possède les propriétés suivantes.



| Propriété                            | Type d’accès           | Description                                                                                                                                                                                                   |
|:------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nom**](eku-name.md)<br/> | Lecture/écriture<br/> | Définit ou récupère une valeur d’énumération qui spécifie le nom CAPICOM de l’utilisation améliorée de la valeur. Il s’agit de la propriété par défaut.<br/>                                                                                   |
| [**OID**](eku-oid.md)<br/>   | Lecture/écriture<br/> | Définit ou récupère une chaîne qui contient une valeur de chaîne d' [*identificateur d’objet*](../secgloss/o-gly.md) (OID) EKU telle que définie dans wincrypt. h.<br/> |



 

## <a name="remarks"></a>Notes

L’objet **EKU** est utilisé par la collection et la propriété suivantes :

-   Collection de [**EKU**](ekus.md)
-   [**CertificateStatus. EKU,**](certificatestatus-eku.md) propriété

Impossible de créer l’objet **EKU** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
