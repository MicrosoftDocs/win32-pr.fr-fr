---
description: Représente un identificateur d’objet (OID) utilisé par plusieurs propriétés CAPICOM.
ms.assetid: d9dc2a9a-920b-41e1-91fb-da1628df577d
title: Objet OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a524bfd8d2eb2edcf3c97919129dd694414d5ace
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123098"
---
# <a name="oid-object"></a>Objet OID

\[L’objet **OID** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe OID**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L’objet **OID** représente un [*identificateur d’objet*](../secgloss/o-gly.md) (OID) utilisé par plusieurs propriétés CAPICOM.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **OID** est utilisé pour effectuer les tâches suivantes :

-   Définissez ou récupérez un nom de CAPICOM et un nom d’affichage pour l’OID.
-   Définissez ou récupérez le nombre en pointillés de l’OID.

## <a name="members"></a>Membres

L’objet **OID** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **OID** possède ces propriétés.



| Propriété                                            | Type d’accès           | Description                                                                                      |
|:----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**FriendlyName**](oid-friendlyname.md)<br/> | Lecture/écriture<br/> | Définit ou récupère le nom complet de l’OID.<br/>                                       |
| [**Nom**](oid-name.md)<br/>                 | Lecture/écriture<br/> | Définit ou récupère le nom défini par CAPICOM pour l’OID. Il s’agit de la propriété par défaut.<br/> |
| [**Valeur**](oid-value.md)<br/>               | Lecture/écriture<br/> | Définit ou récupère la valeur du numéro d’OID en pointillés de l’OID.<br/>                      |



 

## <a name="remarks"></a>Notes

L’objet **OID** peut être créé et il est sécurisé pour l’écriture de scripts. Le ProgID de l’objet **OID** est CAPICOM. OID. 1.

Les propriétés suivantes de l’objet CAPICOM retournent un objet **OID** :

-   [**PolicyInformation. OID**](policyinformation-oid.md)
-   [**Qualificateur. OID**](qualifier-oid.md)
-   [**Extension. OID**](extension-oid.md)
-   [**Modèle. OID**](template-oid.md)

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
