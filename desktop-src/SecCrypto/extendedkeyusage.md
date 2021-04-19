---
description: Fournit un accès en lecture seule aux propriétés d’utilisation améliorée de la clé d’un certificat.
ms.assetid: 636d7f65-d286-4800-a576-a23e6e9811b2
title: Objet ExtendedKeyUsage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5a93be1f6fe75559d0284ca955ca5b6e9c516eed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537567"
---
# <a name="extendedkeyusage-object"></a>Objet ExtendedKeyUsage

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L’objet **ExtendedKeyUsage** fournit un accès en lecture seule aux propriétés d’utilisation améliorée de la clé d’un certificat.

## <a name="members"></a>Membres

L’objet **ExtendedKeyUsage** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **ExtendedKeyUsage** a ces propriétés.



| Propriété                                                     | Type d’accès          | Description                                                                                                                             |
|:-------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**Utilisations améliorées de la clé**](extendedkeyusage-ekus.md)<br/>             | Lecture seule<br/> | [**Collection de EKU qui**](ekus.md) contient les objets [**EKU**](eku.md) pour le certificat.<br/>                            |
| [**IsCritical**](extendedkeyusage-iscritical.md)<br/> | Lecture seule<br/> | Récupère une valeur **booléenne** qui indique si l’extension d’utilisation améliorée de la clé est marquée comme critique.<br/>                                   |
| [**IsPresent**](extendedkeyusage-ispresent.md)<br/>   | Lecture seule<br/> | Récupère une valeur **booléenne** qui indique si l’extension EKU est présente.<br/> Il s’agit de la propriété par défaut. <br/> |



 

## <a name="remarks"></a>Notes

Impossible de créer l’objet **ExtendedKeyUsage** .

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

 

 
