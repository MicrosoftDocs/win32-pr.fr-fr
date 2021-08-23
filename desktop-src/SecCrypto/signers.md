---
description: Représente une collection d’objets signataires.
ms.assetid: 72e86acd-eb87-4eff-bd4e-327630ebbfc4
title: Objet des signataires
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 62c5f59fc90d0d34226b4442b8fa443ad734d474e8077bf210df8bfdf752b1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898332"
---
# <a name="signers-object"></a>Objet des signataires

\[L’objet **signataires** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt une collection d’objets CmsSigner. Pour plus d’informations, consultez la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L’objet **signataires** représente une collection d’objets [**signataires**](signer.md) .

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **signataires** est utilisé pour effectuer les tâches suivantes :

-   Récupérez le nombre de certificats dans la collection.
-   Récupérez un objet **signataires** spécifique de la collection.
-   Itérez au sein de la collection.

## <a name="members"></a>Membres

L’objet **signataires** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet des **signataires** possède ces propriétés.



| Propriété                                        | Type d’accès          | Description                                                                                                                                                                                                                     |
|:------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](signers-newenum.md)<br/> | Lecture seule<br/> | Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection. cette propriété est masquée dans Visual Basic scripting Edition (VBScript).<br/> |
| [**Count**](signers-count.md)<br/>       | Lecture seule<br/> | Nombre d’objets [**signataires**](signer.md) dans la collection.<br/>                                                                                                                                                        |
| [**Élément**](signers-item.md)<br/>         | Lecture seule<br/> | Récupère l’objet [**signataire**](signer.md) qui représente le signataire indexé. Il s’agit de la propriété par défaut.<br/>                                                                                                      |



 

## <a name="remarks"></a>Remarques

Impossible de créer l’objet des **signataires** .

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> </dl>

 

 
