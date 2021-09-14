---
description: Représente un attribut authentifié unique.
ms.assetid: 71c4543b-683f-4ffa-8301-c40c46c490b3
title: Attribute (objet)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34c0800874dc9380b8c9034df2867fc3d1fb578d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127222260"
---
# <a name="attribute-object"></a>Attribute (objet)

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP. Utilisez plutôt la [**classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography**](/previous-versions/windows/) .\]

L’objet d' **attribut** représente un attribut authentifié unique.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **attribut** est utilisé pour effectuer les tâches suivantes :

-   Définissez ou récupérez le nom CAPICOM de l’attribut.
-   Définissez ou récupérez la valeur de l’attribut, par exemple la durée de signature, le nom du document signé ou une description du document signé.

## <a name="members"></a>Membres

L’objet **attribut** a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **attribut** a ces propriétés.



| Propriété                                    | Type d’accès           | Description                                                                                   |
|:--------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [**Nom**](attribute-name.md)<br/>   | Lecture/écriture<br/> | Définit ou récupère le nom CAPICOM de l’attribut. Il s’agit de la propriété par défaut.<br/> |
| [**Valeur**](attribute-value.md)<br/> | Lecture/écriture<br/> | Définit ou récupère la valeur de l’attribut.<br/>                                      |



 

## <a name="remarks"></a>Notes

L’objet d' **attribut** peut être créé et il est sécurisé pour les scripts. Le ProgID de l’objet **attribut** est CAPICOM. Attribut. 1.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> </dl>

 

 
