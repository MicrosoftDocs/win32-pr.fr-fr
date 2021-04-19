---
description: Supprime un objet de certificat d’une collection de destinataires.
ms.assetid: bb75f6d0-4bab-40dd-9d0c-f0431da9c5f3
title: Recipients. Remove, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06d276e2d8e75e8822cee3503a7e8342a94a6b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539603"
---
# <a name="recipientsremove-method"></a>Recipients. Remove, méthode

\[La méthode **Remove** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La méthode **Remove** supprime un objet [**certificat**](certificate.md) d’une collection [**Recipients**](recipients.md) .

## <a name="syntax"></a>Syntaxe


```VB
Recipients.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* \[ dans\]
</dt> <dd>

Index de l’objet de [**certificat**](certificate.md) à supprimer de la collection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> <dt>

[**Destinataires**](recipients.md)
</dt> </dl>

 

 
