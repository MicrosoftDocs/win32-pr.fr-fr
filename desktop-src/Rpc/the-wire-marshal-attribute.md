---
title: Attribut wire_marshal
description: L’attribut \ Wire \_ Marshal \ est un attribut de type IDL similaire à la syntaxe à envoyer \_ en tant que \, mais offrant un moyen plus efficace de marshaler les données sur un réseau.
ms.assetid: b764ca2b-7bbc-4266-836c-0d70033e9c62
keywords:
- Appel de procédure distante RPC, attributs, wire_marshal
- wire_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424fb73597482030adb2e7147d0ba8c05b034475
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382351"
---
# <a name="the-wire_marshal-attribute"></a>Attribut de \_ Marshal de câble

L' \[ attribut [Wire \_ Marshal](/windows/desktop/Midl/wire-marshal) \] est un attribut de type IDL similaire à la syntaxe à \[ [transmettre \_ en tant que](/windows/desktop/Midl/transmit-as) \] , mais il offre un moyen plus efficace de marshaler les données sur un réseau.

Vous utilisez l' \[ attribut **Wire \_ Marshal** \] pour spécifier un type de données qui sera transmis à la place du type de données spécifique à l’application. Chaque type spécifique à l’application a un type pouvant être transmis correspondant qui définit la représentation filaire (la représentation utilisée sur le réseau). Le type spécifique à l’application n’a pas besoin d’être transmissible, mais il doit être un type reconnu par MIDL. Pour marshaler un type inconnu en MIDL, utilisez le \[ [ \_ Marshal d’utilisateur](/windows/desktop/Midl/user-marshal)d’attribut ACF \] .

Votre type spécifique à votre application peut être un type simple, composite ou pointeur. La restriction principale est que l’instance de type doit avoir une taille de mémoire fixe et bien définie. Si la taille de votre instance de type doit être modifiée, utilisez un champ de pointeur plutôt qu’un tableau conforme. Vous pouvez également définir un pointeur vers le type modifiable.

Vous devez fournir les routines pour le dimensionnement, le marshaling et le démarshaling des données, ainsi que la libération de la mémoire associée. Le tableau suivant décrit les quatre noms de routines fournis par l’utilisateur. <type>Est le type utilisateur spécifié dans la définition de type de \[ **\_ Marshal de câble** \] .



| Routine                                                            | Description                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<type>\_Utilisateurs](the-type-usersize-function.md)           | Dimensionne la mémoire tampon de données RPC avant le marshaling côté client ou côté serveur. |
| [<type>\_UserMarshal](the-type-usermarshal-function.md)     | Marshale les données côté client ou côté serveur.                           |
| [<type>\_UserUnmarshal](the-type-userunmarshal-function.md) | Démarshale les données côté client ou côté serveur.                         |
| [<type>\_UserFree](the-type-userfree-function.md)           | Libère les données côté serveur.                                        |



 

Ces routines fournies par le programmeur sont fournies par le client ou l’application serveur en fonction des attributs directionnels.

Si le paramètre est \[ uniquement [dans](/windows/desktop/Midl/in) \] , le client transmet au serveur. Le client a besoin des fonctions **<type> \_ Users** et **<type> \_ UserMarshal** . Le serveur a besoin des fonctions **<type> \_ UserUnmarshal** et **<type> \_ UserFree** .

Pour un \[ paramètre en [sortie](/windows/desktop/Midl/out-idl) \] seule, le serveur transmet au client. Le serveur a besoin des fonctions **<type> \_ Users** et **<type> \_ UserMarshal** , tandis que le client a besoin de la fonction **<type> \_ UserMarshal** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attribut de \_ Marshal d’utilisateur](the-user-marshal-attribute.md)
</dt> <dt>

[Règles de marshaling pour le marshaling d’utilisateur \_ et le \_ marshaling de câble](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[Marshal de câble \_](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[Marshal d’utilisateur \_](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 