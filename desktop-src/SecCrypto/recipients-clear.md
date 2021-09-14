---
description: Supprime tous les objets de certificat d’une collection de destinataires.
ms.assetid: 456fcfbc-4388-40f4-ab58-04508ee2141b
title: Recipients. Clear, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d9bd711bbc97997045989f2eb4ffdbc51ae3559
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416387"
---
# <a name="recipientsclear-method"></a>Recipients. Clear, méthode

\[La méthode **Clear** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Utilisez plutôt la [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La méthode **Clear** supprime tous les objets de [**certificat**](certificate.md) d’une collection [**Recipients**](recipients.md) .

## <a name="syntax"></a>Syntaxe


```VB
Recipients.Clear()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur. Une application qui utilise cette méthode doit contenir du code pour gérer une exception levée par cette méthode.

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

 

 
