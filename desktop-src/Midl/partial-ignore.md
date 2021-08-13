---
title: attribut partial_ignore
description: L’attribut ACF \ partial \_ ignore \ définit une version spécialisée de \ pointeurs uniques \ qui fournissent une sémantique de sortie facultative.
ms.assetid: 8a8f88b0-4a12-496d-bf77-ee57241b577b
keywords:
- partial_ignore MIDL de l’attribut
topic_type:
- apiref
api_name:
- partial_ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac751e5b3bdb4a93c003e170333af8956048c9793630419fff0857d61f8c1f2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641972"
---
# <a name="partial_ignore-attribute"></a>\_attribut ignore partiel

L’attribut CCP **\[ Partial \_ ignore \]** définit une version spécialisée de pointeurs **\[ uniques \]** qui fournit une sémantique de sortie facultative.

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ partial_ignore [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="remarks"></a>Remarques

Lors de la création d’une fonction, il est courant de permettre aux utilisateurs de spécifier un pointeur non **null** vers des données de retour facultatives, souvent appelées pointeur facultatif-out. La mémoire vers laquelle pointe l’utilisateur n’est généralement pas obligatoirement initialisée. Cette technique représente un problème lorsque la fonction est utilisée sur RPC.

Si le pointeur facultatif-out est valide, mais qu’il pointe vers des données non initialisées, RPC tente de marshaler ces données et de les envoyer au serveur, ce qui peut entraîner l’échec du marshaling et l’abandon de l’appel. Même si le marshaling s’effectue correctement, un nombre potentiellement important de données inutiles sont envoyées au serveur.

Ces problèmes sont résolus en marquant le pointeur **\[ sur in, out, unique et \_ Partial \] ignore**. Les quatre attributs doivent être présents. Lorsqu’un pointeur **\[ \_ ignore \] partiellement** est marshalé côté client, les seules données envoyées au serveur sont un indicateur qui indique si le pointeur est **null**. Si le pointeur n’est pas **null**, la routine côté serveur reçoit un pointeur valide vers un bloc de mémoire qui a été initialisé avec des zéros. Si le pointeur a la **valeur null**, la routine côté serveur reçoit un pointeur **null** .

Dans ce cas, la taille maximale du pointeur doit être bien définie au moment de la compilation ou en fonction des paramètres d’entrée, car le serveur doit allouer de l’espace pour l’emplacement de la mémoire vers lequel pointe. Par exemple, un pointeur de **\[ chaîne \]** simple n’a pas une taille bien définie, car la chaîne se termine implicitement par un caractère null. Dans ce cas, la spécification de la taille maximale de la chaîne par l’ajout d’une **\[ taille \_ est \]** que l’attribut permet d’obtenir la taille requise bien définie.

## <a name="examples"></a>Exemples

``` syntax
/* The MoveLeft function will move one position to the left and optionally return the previous position */
void MoveLeft([in, out, unique, partial_ignore] long *pPrevPosition);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**unique**](unique.md)
</dt> </dl>

 

 




