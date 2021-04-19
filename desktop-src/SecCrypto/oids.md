---
description: Représente une collection d’objets OID.
ms.assetid: 2c4ff87a-58e1-46aa-9680-29062b05308c
title: Objet OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 894689c214d8b7d352a2453d2d62c847866b9bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542462"
---
# <a name="oids-object"></a>Objet OID

\[L’objet **OID** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L’objet **OID** représente une collection d’objets [**OID**](oid.md) . Chaque objet [**OID**](oid.md) représente un identificateur d’objet unique.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **OID** est utilisé pour effectuer les tâches suivantes :

-   Ajoutez ou supprimez un objet [**OID**](oid.md) de la collection.
-   Effacez tous les objets [**OID**](oid.md) de la collection.
-   Récupérez le nombre d’identificateurs d’objet dans la collection.
-   Récupérez un objet [**OID**](oid.md) spécifique de la collection.
-   Itérez au sein de la collection.

## <a name="members"></a>Membres

L’objet **OID** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **OID** possède les méthodes suivantes.



| Méthode                        | Description                                                                  |
|:------------------------------|:-----------------------------------------------------------------------------|
| [**Complémentaires**](oids-add.md)       | Ajoute un objet [**OID**](oid.md) à la collection.<br/>              |
| [**Effacé**](oids-clear.md)   | Efface tous les objets [**OID**](oid.md) de la collection.<br/>        |
| [**Installez**](oids-remove.md) | Supprime un objet [**OID**](oid.md) indexé de la collection.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **OID** possède ces propriétés.



| Propriété                                     | Type d’accès          | Description                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](oids-newenum.md)<br/> | Lecture seule<br/> | Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection. Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).<br/> |
| [**Saut**](oids-count.md)<br/>       | Lecture seule<br/> | Récupère le nombre d’objets [**OID**](oid.md) de la collection.<br/>                                                                                                                                                |
| [**Élément**](oids-item.md)<br/>         | Lecture seule<br/> | Récupère un objet [**OID**](oid.md) indexé de la collection. Il s’agit de la propriété par défaut.<br/>                                                                                                                    |



 

## <a name="remarks"></a>Notes

Impossible de créer l’objet **OID** .

L’objet **OID** est utilisé par les propriétés suivantes :

-   [**CertificateStatus.ApplicationPolicies**](certificatestatus-applicationpolicies.md)
-   [**CertificateStatus.CertificatePolicies**](certificatestatus-certificatepolicies.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
