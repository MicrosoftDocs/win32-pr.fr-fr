---
description: Récupère l’objet EKU qui représente la propriété utilisation améliorée de la clé (EKU) indexée.
ms.assetid: b8c12a7a-e836-48c2-958c-937b3723f85b
title: 'IEKUs :: Item, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKUs.Item
- IEKUs.get_Item
- EKUs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e3eaf8d0b303207aae3ef78cc82771e1436b1027
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526803"
---
# <a name="iekusitem-property"></a>IEKUs :: Item, propriété

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **Item** récupère l’objet [**EKU**](eku.md) qui représente la propriété utilisation améliorée de la clé (EKU) indexée.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
EKUs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**EKU**](eku.md) qui représente la propriété utilisation améliorée de la clé (EKU) indexée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Utilisations améliorées de la clé**](ekus.md)
</dt> </dl>

 

 
