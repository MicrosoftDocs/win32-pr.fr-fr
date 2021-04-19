---
description: Représente une collection d’objets EKU.
ms.assetid: 04b9f0bf-e1d4-4a2c-be5d-bae7c1090bdb
title: Objet EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 56fd6eaeb5a00549cbb4ee659b99ece391e0ebed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535330"
---
# <a name="ekus-object"></a>Objet EKU

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L’objet **EKU** représente une collection d’objets [**EKU**](eku.md) . Chaque objet [**EKU**](eku.md) représente une propriété d’utilisation améliorée de la clé (EKU) d’un certificat.

## <a name="when-to-use"></a>Quand l’utiliser

La collection de **EKU** est utilisée pour effectuer les tâches suivantes :

-   Récupérez le nombre de propriétés EKU dans la collection.
-   Récupérez un objet [**EKU**](eku.md) spécifique de la collection.
-   Itérez au sein de la collection.

## <a name="members"></a>Membres

L’objet **EKU** contient les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **EKU** possède ces propriétés.



| Propriété                                     | Type d’accès          | Description                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](ekus-newenum.md)<br/> | Lecture seule<br/> | Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection. Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).<br/> |
| [**Saut**](ekus-count.md)<br/>       | Lecture seule<br/> | Récupère le nombre d’objets [**EKU**](eku.md) dans la collection.<br/>                                                                                                                                                |
| [**Élément**](ekus-item.md)<br/>         | Lecture seule<br/> | Récupère l’objet [**EKU**](eku.md) qui représente la propriété EKU indexée. Il s’agit de la propriété par défaut.<br/>                                                                                                      |



 

## <a name="remarks"></a>Notes

Cette collection est récupérée par la propriété [**ExtendedKeyUsage. EKU**](extendedkeyusage-ekus.md) .

Impossible de créer l’objet **EKU** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
