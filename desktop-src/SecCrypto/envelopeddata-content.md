---
description: Définit ou récupère le contenu en texte en clair d’un message à envelopper. Il s’agit de la propriété par défaut.
ms.assetid: 7927321f-fbda-45e0-9b9f-c10ecd3a98b1
title: EnvelopedData. Content, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4115b55b7f9542c5a31c9abd3bcbbaec5256be4283675becac2f011ec76c8cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766070"
---
# <a name="envelopeddatacontent-property"></a>EnvelopedData. Content, propriété

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propriété de **contenu** définit ou récupère le contenu en texte en clair d’un message à envelopper. Il s’agit de la propriété par défaut.

## <a name="syntax"></a>Syntaxe


```VB
EnvelopedData.Content As String
```



## <a name="property-value"></a>Valeur de la propriété

Contenu en texte clair d’un message à envelopper.

## <a name="remarks"></a>Remarques

La définition de cette propriété doit être effectuée avant l’appel de la méthode [**Encrypt**](envelopeddata-encrypt.md) . Lorsque la valeur de cette propriété est réinitialisée, directement ou indirectement, l’intégralité de l' [*État*](../secgloss/s-gly.md) de l’objet est réinitialisée et tout contenu chiffré dans l’objet est perdu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
