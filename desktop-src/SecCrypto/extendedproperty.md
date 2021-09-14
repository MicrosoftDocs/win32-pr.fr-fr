---
description: Représente une propriété étendue Microsoft.
ms.assetid: 91375fd5-b3af-4ed4-961d-5cc1db1a14e3
title: Objet ExtendedProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperty
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ec61da301dc1819c899a7da23da9a10efd81ae0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120989"
---
# <a name="extendedproperty-object"></a>Objet ExtendedProperty

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler la fonction API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) et obtenir les propriétés. Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx). Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]

L’objet **ExtendedProperty** représente une propriété étendue Microsoft.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **ExtendedProperty** est utilisé pour effectuer les tâches suivantes :

-   Définissez ou récupérez le type de la propriété étendue.
-   Définissez ou récupérez le type d’encodage utilisé pour encoder la propriété étendue.

## <a name="members"></a>Membres

L’objet **ExtendedProperty** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **ExtendedProperty** a ces propriétés.



| Propriété                                             | Type d’accès           | Description                                                                                                                                                                    |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PropID**](extendedproperty-propid.md)<br/> | Lecture/écriture<br/> | Valeur de l’énumération [**\_ propid propid**](capicom-propid.md) qui définit ou récupère le type de la propriété étendue.<br/> Il s’agit de la propriété par défaut.<br/> |
| [**Valeur**](extendedproperty-value.md)<br/>   | Lecture/écriture<br/> | Valeur de l’énumération de [**\_ \_ type d’encodage**](capicom-encoding-type.md) CAPICOM qui définit ou récupère les données de propriété étendues.<br/>                              |



 

## <a name="remarks"></a>Notes

L’objet **ExtendedProperty** est utilisé par la collection [**ExtendedProperties**](extendedproperties.md) .

L’objet **ExtendedProperty** peut être créé et il n’est pas sécurisé pour les scripts. Le ProgID de l’objet **ExtendedProperty** est CAPICOM. ExtendedProperty. 1.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
