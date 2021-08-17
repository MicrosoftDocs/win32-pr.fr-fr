---
description: Fournit des fonctionnalités pour hacher une chaîne.
ms.assetid: 893639c2-57b9-48f6-bf60-a21c3368ffeb
title: Objet HashedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c61d52e7621acffb76df5bcb05693efb48c695c15e79d1f0a45523a0f0087c6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006447"
---
# <a name="hasheddata-object"></a>Objet HashedData

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe HashAlgorithm**](/previous-versions/windows/) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L’objet **HashedData** fournit les fonctionnalités de hachage d’une chaîne.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **HashedData** est utilisé pour effectuer les tâches suivantes :

-   Spécifiez la chaîne de contenu qui contient les données à hacher.
-   Applique un algorithme de hachage spécifié à la chaîne de contenu.

## <a name="members"></a>Membres

L’objet **HashedData** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **HashedData** a ces méthodes.



| Méthode                          | Description                                        |
|:--------------------------------|:---------------------------------------------------|
| [**Format**](hasheddata-hash.md) | Crée un hachage de la chaîne spécifiée.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **HashedData** a ces propriétés.



| Propriété                                             | Type d’accès           | Description                                                                                                                                                                          |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algorithm**](hasheddata-algorithm.md)<br/> | Lecture/écriture<br/> | Définit ou récupère le type d’algorithme de hachage utilisé.<br/>                                                                                                                     |
| [**Valeur**](hasheddata-value.md)<br/>         | Lecture seule<br/>  | Récupère les données hachées après des appels réussis à la méthode de [**hachage**](hasheddata-hash.md) . Le hachage est retourné au format hexadécimal. Il s’agit de la propriété par défaut.<br/> |



 

## <a name="remarks"></a>Remarques

Pour créer le hachage d’une grande quantité de données, appelez la méthode de [**hachage**](hasheddata-hash.md) pour chaque élément de données. Le hachage de chaque élément de données est concaténé à la propriété [**value**](hasheddata-value.md) jusqu’à ce que la propriété soit lue. Le contenu de la propriété **value** est réinitialisé lorsque la propriété est lue.

L’objet **HashedData** peut être créé et il est sécurisé pour les scripts. Le ProgID de l’objet **HashedData** est «CAPICOM. HashedData. 1».

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
