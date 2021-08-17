---
description: Définit ou récupère le nom CAPICOM de l’attribut. Il s’agit de la propriété par défaut.
ms.assetid: 082f286e-f2ac-4e45-94b9-abdaa3f4c926
title: Propriété Attribute.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3234d02e5e0f68817896f2d0c9d05be25b55bbe97f49fea4d34bafbab627b2c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773653"
---
# <a name="attributename-property"></a>Propriété Attribute.Name

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP. Utilisez plutôt la [**classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography**](/previous-versions/windows/) .\]

La propriété **Name** définit ou récupère le nom CAPICOM de l’attribut. Il s’agit de la propriété par défaut.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
Attribute.Name As CAPICOM_ATTRIBUTE
```



## <a name="property-value"></a>Valeur de la propriété

Valeur de l’énumération d' [**\_ attribut CAPICOM**](capicom-attribute.md) qui spécifie le nom CAPICOM de l’attribut. Le tableau suivant répertorie les valeurs possibles.



| Value                                                                                                                                                                                                                                                                                 | Signification                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME"></span><span id="capicom_authenticated_attribute_signing_time"></span><dl> <dt>**\_heure de signature de l' \_ attribut \_ authentifié \_ CAPICOM**</dt> </dl>                         | L’attribut contient l’heure à laquelle la signature a été créée.<br/> |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME"></span><span id="capicom_authenticated_attribute_document_name"></span><dl> <dt>**\_nom du document de l' \_ attribut \_ authentifié \_ CAPICOM**</dt> </dl>                      | L’attribut contient le nom du document signé.<br/>         |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION"></span><span id="capicom_authenticated_attribute_document_description"></span><dl> <dt>**\_Description du document de l' \_ attribut \_ authentifié \_ CAPICOM**</dt> </dl> | L’attribut contient une description du document signé.<br/>    |



 

## <a name="remarks"></a>Remarques

Lorsque la valeur de cette propriété est réinitialisée, directement ou indirectement, l’intégralité de l’état de l’objet est réinitialisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attribut**](attribute.md)
</dt> </dl>

 

 
