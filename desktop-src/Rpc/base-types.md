---
title: Types de base
description: Pour éviter les problèmes que les types de données dépendants de l’implémentation peuvent provoquer sur différentes architectures d’ordinateur, MIDL définit ses propres types de données de base.
ms.assetid: 0b2778c7-8cee-415f-bb5e-01f6c9eedc70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ee57261aac1de6ea4bb15c9a4550721dd10282
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416615"
---
# <a name="base-types"></a>Types de base

Pour éviter les problèmes que les types de données dépendants de l’implémentation peuvent provoquer sur différentes architectures d’ordinateur, MIDL définit ses propres types de données de base.



| Type de base                         | Description                                                                                                                                                         |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**expression**](/windows/desktop/Midl/boolean)       | Élément de données qui peut avoir la valeur **true** ou **false**.                                                                                                          |
| [**poids**](/windows/desktop/Midl/byte)             | Un élément de données 8 bits est garanti comme étant transmis sans aucune modification.                                                                                                 |
| [**char**](/windows/desktop/Midl/char-idl)         | Élément de données de caractères non signés 8 bits.                                                                                                                              |
| [**Cliquer**](/windows/desktop/Midl/double)         | Nombre à virgule flottante 64 bits.                                                                                                                                     |
| [**dissocié**](/windows/desktop/Midl/float)           | Nombre à virgule flottante 32 bits.                                                                                                                                     |
| [**handle \_ t**](/windows/desktop/Midl/handle-t)    | Handle primitif qui peut être utilisé pour la liaison RPC ou la sérialisation de données.                                                                                            |
| [**hyper**](/windows/desktop/Midl/hyper)           | Un entier 64 bits qui peut être déclaré comme étant [**signé**](/windows/desktop/Midl/signed) ou [**non signé**](/windows/desktop/Midl/unsigned) peut également être appelé **\_ Int64**.                  |
| [**int**](/windows/desktop/Midl/int)               | Entier 32 bits qui peut être déclaré comme étant **signé** ou **non signé**.                                                                                         |
| [**\_\_int3264**](/windows/desktop/Midl/--int3264) | Mot clé qui spécifie un type intégral qui a des propriétés 32 bits ou 64 bits.                                                                              |
| [**long**](/windows/desktop/Midl/long)             | Modificateur pour **int** qui indique un entier 32 bits. Peut être déclarée comme **étant signed ou** **unsigned**.                                                       |
| [**Résumé**](/windows/desktop/Midl/short)           | Entier 16 bits qui peut être déclaré comme étant **signé** ou **non signé**.                                                                                         |
| [**Small**](/windows/desktop/Midl/small)           | Modificateur pour **int** qui indique un entier 8 bits. Peut être déclarée comme **étant signed ou** **unsigned**.                                                       |
| [**WCHAR \_ t**](/windows/desktop/Midl/wchar-t)      | Type à caractères larges pris en charge en tant qu’extension Microsoft d’IDL. Par conséquent, ce type n’est pas disponible si vous compilez à l’aide du commutateur [ / **OSF**](/windows/desktop/Midl/-osf) . |



 

Le fichier d’en-tête Rpcndr. h fournit des définitions pour la plupart de ces types de données de base. Le mot clé **int** est reconnu et est transmissible sur les plateformes 32 bits. Sur les plateformes 16 bits, le type de données **int** requiert un modificateur, tel que **short** ou **long**, pour spécifier sa longueur.

Bien **que \* \* void** soit reconnu comme un type pointeur générique par la norme C ANSI, MIDL restreint son utilisation. Chaque pointeur utilisé dans une opération distante ou de sérialisation doit pointer vers des types de base ou des types construits à partir de types de base. (Il existe une exception : les handles de contexte sont définis comme des types **void** . Pour plus d’informations, consultez [Handles de contexte](context-handles.md).)

 

 