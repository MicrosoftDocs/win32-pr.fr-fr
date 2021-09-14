---
description: Ajoute un objet certificat à une collection Recipients.
ms.assetid: 2a1b9e0f-ccbf-4042-871b-397de6b6fc35
title: Recipients. Add, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 255d17485e3423d50cd86b092c2120605f0f1106
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416388"
---
# <a name="recipientsadd-method"></a>Recipients. Add, méthode

\[La méthode **Add** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Utilisez plutôt la [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La méthode **Add** ajoute un objet [**certificat**](certificate.md) à une collection [**Recipients**](recipients.md) .

## <a name="syntax"></a>Syntaxe


```VB
Recipients.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Certificat* \[ dans\]
</dt> <dd>

Expression qui correspond à l’objet de [**certificat**](certificate.md) à ajouter à la collection.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> <dt>

[**Destinataires**](recipients.md)
</dt> </dl>

 

 
