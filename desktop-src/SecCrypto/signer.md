---
description: Établit le signataire d’un objet SignedData ou SignedCode.
ms.assetid: fca6489c-56cf-472f-ac0f-73ba531fa212
title: Objet signataire
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 974341eb996f2b5d3701757a5352ef56e2837390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539302"
---
# <a name="signer-object"></a>Objet signataire

\[L’objet **signataire** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L’objet **signataire** établit le signataire d’un objet [**SignedData**](signeddata.md) ou [**SignedCode**](signedcode.md) . Le [**certificat**](certificate.md) de l’objet **signataire** doit avoir une clé privée disponible qui peut être utilisée pour signer des données.

## <a name="members"></a>Membres

L’objet **signataire** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **signataire** possède ces méthodes.



| Méthode                      | Description                                                       |
|:----------------------------|:------------------------------------------------------------------|
| [**Load**](signer-load.md) | Charge un certificat de signature à partir d’un fichier PFX spécifié.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **signataire** possède ces propriétés.



| Propriété                                                                     | Type d’accès           | Description                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticatedAttributes**](signer-authenticatedattributes.md)<br/> | Lecture seule<br/>  | Collection d’attributs authentifiés.<br/>                                                                                                                                                                                                                                                                                      |
| [**Certificat**](signer-certificate.md)<br/>                         | Lecture/écriture<br/> | Objet de [**certificat**](certificate.md) qui représente le certificat d’un signataire des données.<br/> Lorsque la valeur de cette propriété est réinitialisée, directement ou indirectement, l’intégralité de l' [*État*](../secgloss/s-gly.md) de l’objet est réinitialisée.<br/> Il s’agit de la propriété par défaut.<br/> |
| [**Mutation**](signer-chain.md)<br/>                                     | Lecture seule<br/>  | Chaîne du signataire.<br/>                                                                                                                                                                                                                                                                                                         |
| [**Options**](signer-options.md)<br/>                                 | Lecture/écriture<br/> | Définit ou récupère l’option de certificat du signataire.<br/>                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Notes

L’objet **signataire** peut être créé et il est sécurisé pour les scripts. Le ProgID de l’objet **signataire** est CAPICOM. Signataire. 2.

**CAPICOM 1. *x*:** le ProgID de l’objet **signataire** est CAPICOM. Signataire. 1.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> </dl>

 

 
