---
description: Récupère la collection de destinataires du message enveloppé.
ms.assetid: de9cbf8e-f34c-4e08-89aa-b5ac842aa599
title: EnvelopedData. Recipients, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Recipients
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ffccb280bc41116a65b01cd0f4dcc04a6e2f815fa66306067457516b329c80e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874139"
---
# <a name="envelopeddatarecipients-property"></a>EnvelopedData. Recipients, propriété

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propriété **Recipients** récupère la collection de destinataires du message enveloppé.

## <a name="syntax"></a>Syntaxe


```VB
EnvelopedData.Recipients As Recipients
```



## <a name="property-value"></a>Valeur de la propriété

Collection de [**destinataires**](recipients.md) qui représente les destinataires du message enveloppé.

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

 

 
