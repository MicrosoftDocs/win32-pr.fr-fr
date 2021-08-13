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
ms.openlocfilehash: c956aacd7b61243fbaeb26ed1a29ed0fee4522d83d8b4ef3ac25b3b1921b42a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900806"
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

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur. Une application qui utilise cette méthode doit contenir du code pour gérer une exception levée par cette méthode.

## <a name="requirements"></a>Configuration requise



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

 

 
