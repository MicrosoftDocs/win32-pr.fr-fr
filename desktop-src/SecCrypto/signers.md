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
ms.openlocfilehash: 75eba0ecb2592bf7efc27ecdd63288179e306651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532533"
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
| [**\_NewEnum**](signers-newenum.md)<br/> | Lecture seule<br/> | Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection. Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).<br/> |
| [**Saut**](signers-count.md)<br/>       | Lecture seule<br/> | Nombre d’objets [**signataires**](signer.md) dans la collection.<br/>                                                                                                                                                        |
| [**Élément**](signers-item.md)<br/>         | Lecture seule<br/> | Récupère l’objet [**signataire**](signer.md) qui représente le signataire indexé. Il s’agit de la propriété par défaut.<br/>                                                                                                      |



 

## <a name="remarks"></a>Notes

Impossible de créer l’objet des **signataires** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> </dl>

 

 
