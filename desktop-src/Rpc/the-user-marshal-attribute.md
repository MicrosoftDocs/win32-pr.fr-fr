---
title: Attribut user_marshal
description: L’attribut \ user \_ Marshal \ est un attribut de type ACF similaire à la syntaxe pour que \ représente \_ comme \.
ms.assetid: 5a381b44-e271-4713-954f-a55840a92bb7
keywords:
- Appel de procédure distante RPC, attributs, user_marshal
- user_marshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b769e6a7e176d5aeba68afd322cdd6f24d76c6b5
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883746"
---
# <a name="the-user_marshal-attribute"></a>Attribut de \_ Marshal d’utilisateur

L' \[ attribut [User \_ Marshal](/windows/desktop/Midl/user-marshal) \] est un attribut de type ACF similaire à la syntaxe à \[ [représenter \_ comme](/windows/desktop/Midl/represent-as) \] . Comme avec l’attribut IDL, le \[ [ \_ Marshal de câble](/windows/desktop/Midl/wire-marshal) \] , il offre un moyen plus efficace de marshaler les données sur un réseau. En tant qu’attribut ACF, le **\[ \_ Marshal \] d’utilisateur** vous permet de marshaler des types de données personnalisés qui sont inconnus de MIDL. Chaque type spécifique à l’application a un type pouvant être transmis correspondant qui définit la représentation filaire.

Votre type spécifique à votre application peut être un type simple, composite ou pointeur. La restriction principale est que l’instance de type doit avoir une taille de mémoire fixe et bien définie. Si la taille de votre instance de type doit être modifiée, utilisez un champ de pointeur plutôt qu’un tableau conforme. Vous pouvez également définir un pointeur vers le type modifiable.

Comme avec l’attribut **\[ Wire \_ Marshal \]** , vous fournissez des routines pour le dimensionnement, le marshaling, le démarshaling et les passes de libération. Le tableau suivant décrit les quatre noms de routines fournis par l’utilisateur. Le &lt; type &gt; est le *type* utilisateur spécifié dans la définition de type de **\[ \_ Marshal \] utilisateur** .



| Routine                                                            | Description                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------|
| [&lt;type d' &gt; \_ utilisateur](the-type-usersize-function.md)           | Dimensionne la mémoire tampon de données RPC avant le marshaling côté client ou côté serveur. |
| [&lt;tapez &gt; \_ UserMarshal](the-type-usermarshal-function.md)     | Marshale les données côté client ou côté serveur.                           |
| [&lt;tapez &gt; \_ UserUnmarshal](the-type-userunmarshal-function.md) | Démarshale les données côté client ou côté serveur.                         |
| [&lt;tapez &gt; \_ UserFree](the-type-userfree-function.md)           | Libère les données côté serveur.                                        |



 

Ces routines fournies par l’utilisateur sont fournies par le client ou l’application serveur, en fonction des attributs directionnels.

Si le paramètre est \[ uniquement [dans](/windows/desktop/Midl/in) \] , le client transmet au serveur. Le client a besoin du **&lt; type &gt; \_ Users** et des fonctions **&lt; &gt; \_ UserMarshal** . Le serveur a besoin du **&lt; type &gt; \_ UserUnmarshal** et des fonctions **&lt; &gt; \_ UserFree de type** .

Pour un \[ paramètre en [sortie](/windows/desktop/Midl/out-idl) \] seule, le serveur transmet au client. Le serveur a besoin des fonctions **&lt; type &gt; \_ Users** et **&lt; &gt; \_ UserMarshal** , tandis que le client a besoin du **&lt; type &gt; \_ UserMarshal** function.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attribut de \_ Marshal de câble](the-wire-marshal-attribute.md)
</dt> <dt>

[Règles de marshaling pour le marshaling d’utilisateur et le \_ marshaling de câble](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[Marshal d’utilisateur \_](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[Marshal de câble \_](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 
