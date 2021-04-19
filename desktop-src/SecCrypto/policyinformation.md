---
description: Fournit l’accès aux informations de stratégie d’une extension.
ms.assetid: 03d627b3-2d44-4637-97a4-85cdcaf3e4d3
title: Objet PolicyInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d0cc89d6f993b72763083e69bb88e848134e8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520799"
---
# <a name="policyinformation-object"></a>Objet PolicyInformation

\[L’objet **PolicyInformation** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les informations de stratégie dans l’extension des stratégies de certificat.\]

L’objet **PolicyInformation** fournit l’accès aux informations de stratégie d’une extension.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **PolicyInformation** est utilisé pour effectuer les tâches suivantes :

-   Récupérez l’OID de stratégie.
-   Récupère une collection des qualificateurs de la stratégie.

## <a name="members"></a>Membres

L’objet **PolicyInformation** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **PolicyInformation** a ces propriétés.



| Propriété                                                      | Description                                                                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**OID**](policyinformation-oid.md)<br/>               | Récupère l’OID de la stratégie, sous la forme d’un objet [**OID**](oid.md) . Il s’agit de la propriété par défaut.<br/>       |
| [**Qualificateurs**](policyinformation-qualifiers.md)<br/> | Récupère une collection des qualificateurs de la stratégie, sous la forme d’un objet [**qualificateurs**](qualifiers.md) .<br/> |



 

## <a name="remarks"></a>Notes

Impossible de créer l’objet **PolicyInformation** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
