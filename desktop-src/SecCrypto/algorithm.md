---
description: Spécifie l’algorithme utilisé pour la signature, l’enveloppe et le chiffrement des opérations.
ms.assetid: 9a3071a3-e62d-43d3-acd7-0685592c78b4
title: Algorithme, objet (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f564efe9df3122951969a45443d58ace60e9db30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532201"
---
# <a name="algorithm-object"></a>Algorithme (objet)

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP. Utilisez plutôt la [**classe AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

L’objet **algorithme** spécifie l’algorithme utilisé pour la signature, l’enveloppe et le chiffrement des opérations.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **algorithme** est utilisé pour effectuer les tâches suivantes :

-   Définissez ou récupérez l’algorithme à utiliser.
-   Définissez ou récupérez la longueur de la clé.

> [!Note]  
> CAPICOM tente d’utiliser le fournisseur de services de chiffrement (CSP) par défaut du système. Si le fournisseur de services de chiffrement ne peut pas fournir l’algorithme ou la longueur de clé demandés, CAPICOM recherche un CSP disponible fourni par Microsoft qui peut gérer l’algorithme et la longueur de clé demandés, dans cet ordre de disponibilité : fournisseur de chiffrement amélioré Microsoft, fournisseur de chiffrement fort Microsoft, fournisseur de chiffrement de base Microsoft.

 

## <a name="members"></a>Membres

L’objet **algorithme** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **algorithme** a ces propriétés.



| Propriété                                            | Type d’accès           | Description                                                                                                                       |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**KeyLength**](algorithm-keylength.md)<br/> | Lecture/écriture<br/> | Définit ou récupère la longueur de la clé.<br/>                                                                               |
| [**Nom**](algorithm-name.md)<br/>           | Lecture/écriture<br/> | Définit ou récupère l’algorithme utilisé pour la signature, l’enveloppe et le chiffrement des opérations. Il s’agit de la propriété par défaut.<br/> |



 

## <a name="remarks"></a>Notes

Impossible de créer l’objet **algorithme** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| En-tête<br/>                | <dl> <dt>CAPICOM. h</dt> </dl>   |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> </dl>

 

 
