---
description: Représente une collection d’objets Attribute.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Objet Attributes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61936fff0421c43a07483fb8489cca755154a8cfbdd524da5837b12f90add969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773180"
---
# <a name="attributes-object"></a>Objet Attributes

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP. Utilisez plutôt la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L' **objet** Attributes représente une collection d’objets [**attribute**](attribute.md) . Chaque objet d' [**attribut**](attribute.md) représente un attribut unique d’un message.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **attributes** est utilisé pour effectuer les tâches suivantes :

-   Ajoutez ou supprimez un objet [**attribut**](attribute.md) spécifique de la collection.
-   Efface la collection.
-   Récupérez le nombre d’attributs dans la collection.
-   Récupérez un objet [**attribut**](attribute.md) spécifique de la collection.
-   Itérez au sein de la collection.

## <a name="members"></a>Membres

L’objet **attributes** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **attributes** possède ces méthodes.



| Méthode                              | Description                                                                       |
|:------------------------------------|:----------------------------------------------------------------------------------|
| [**Complémentaires**](attributes-add.md)       | Ajoute un objet d' [**attribut**](attribute.md) à la collection.<br/>       |
| [**Effacer**](attributes-clear.md)   | Efface tous les objets [**attribut**](attribute.md) de la collection.<br/> |
| [**Installez**](attributes-remove.md) | Supprime un objet d' [**attribut**](attribute.md) de la collection.<br/>  |



 

### <a name="properties"></a>Propriétés

L’objet **attributes** possède ces propriétés.



| Propriété                                           | Type d’accès          | Description                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](attributes-newenum.md)<br/> | Lecture seule<br/> | Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection. cette propriété est masquée dans Visual Basic scripting Edition (VBScript).<br/> |
| [**Count**](attributes-count.md)<br/>       | Lecture seule<br/> | Récupère le nombre d’objets [**attribute**](attribute.md) dans la collection.<br/>                                                                                                                                    |
| [**Élément**](attributes-item.md)<br/>         | Lecture seule<br/> | Récupère l’objet d' [**attribut**](attribute.md) qui représente l’attribut indexé. Il s’agit de la propriété par défaut.<br/>                                                                                             |



 

## <a name="remarks"></a>Remarques

Impossible de créer l’objet **attributes** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets de chiffrement](cryptography-objects.md)
</dt> </dl>

 

 
