---
description: Représente une collection d’objets ExtendedProperty.
ms.assetid: 9de25994-9f0b-47a0-b4c8-781aec782f88
title: Objet ExtendedProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0225582217df56f486a44f12e3ca6ea0003130fdb209fb67e9f9e4ee258764d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007237"
---
# <a name="extendedproperties-object"></a>Objet ExtendedProperties

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler la fonction API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) et obtenir les propriétés. Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx). Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]

L’objet **ExtendedProperties** représente une collection d’objets [**ExtendedProperty**](extendedproperty.md) . Chaque objet représente une propriété étendue unique.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **ExtendedProperties** est utilisé pour effectuer les tâches suivantes :

-   Ajoutez ou supprimez un objet [**ExtendedProperty**](extendedproperty.md) de la collection.
-   Récupérez le nombre de propriétés étendues dans la collection.
-   Récupérez un objet [**ExtendedProperty**](extendedproperty.md) spécifique de la collection.
-   Itérez au sein de la collection.

## <a name="members"></a>Membres

L’objet **ExtendedProperties** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#extendedproperties-object)

### <a name="methods"></a>Méthodes

L’objet **ExtendedProperties** possède ces méthodes.



| Méthode                                      | Description                                                                                    |
|:--------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Complémentaires**](extendedproperties-add.md)       | Ajoute un objet [**ExtendedProperty**](extendedproperty.md) à la collection.<br/>      |
| [**Installez**](extendedproperties-remove.md) | Supprime un objet [**ExtendedProperty**](extendedproperty.md) de la collection.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **ExtendedProperties** possède ces propriétés.



| Propriété                                                   | Type d’accès          | Description                                                                                                                                                                                                                     |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](extendedproperties-newenum.md)<br/> | Lecture seule<br/> | Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection. cette propriété est masquée dans Visual Basic scripting Edition (VBScript).<br/> |
| [**Count**](extendedproperties-count.md)<br/>       | Lecture seule<br/> | Récupère le nombre d’objets [**ExtendedProperty**](extendedproperty.md) dans la collection.<br/>                                                                                                                      |
| [**Élément**](extendedproperties-item.md)<br/>         | Lecture seule<br/> | Récupère un objet [**ExtendedProperty**](extendedproperty.md) qui représente la propriété étendue indexée de la collection. Il s’agit de la propriété par défaut.<br/>                                                      |



 

## <a name="remarks"></a>Remarques

Impossible de créer l’objet **ExtendedProperties** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
