---
title: Fonction type_UserMarshal
description: La \_ fonction de type UserMarshal est une fonction d’assistance pour les attributs \ Wire \_ Marshal \ et \ user \_ Marshal \.
ms.assetid: 3cbd78d1-a036-4d0d-bb1d-4c968acfdb36
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffea134b78ae8187fce3fab7876150c0a7a8cd7f892ebac602966712ec1b60e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016469"
---
# <a name="the-type_usermarshal-function"></a>Type \_ UserMarshal (fonction)

La fonction **<type> \_ UserMarshal** est une fonction d’assistance pour les attributs de marshaling de \[ [ \_ câble](/windows/desktop/Midl/wire-marshal) \] et d' \[ [utilisateur \_](/windows/desktop/Midl/user-marshal) \] . Les stubs appellent cette fonction pour marshaler des données côté client ou côté serveur. La fonction est définie comme suit :

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserMarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

Le <type> dans le nom de fonction correspond au type utilisateur spécifié dans la définition de type de marshaling de **\[ \_ \] câble** ou d' **\[ utilisateur \_ \]** . Ce type peut être non transmissible ou même, lorsqu’il est utilisé avec l’attribut **\[ User \_ Marshal \]** (un type inconnu pour le compilateur MIDL). Le nom du type de câble (le nom du type transmissible) n’est pas utilisé dans le prototype de la fonction. Notez, toutefois, que le type de câble définit la disposition filaire pour les données, comme spécifié par l’ETCD OSF.

Le paramètre *pFlags* est un pointeur vers un champ d’indicateur long non signé. Le mot supérieur de l’indicateur contient des indicateurs de représentation de données NDR tels que définis par l’ETCD OSF pour les représentations à virgule flottante, d’ordre d’octet et de caractère. Le mot inférieur contient un indicateur de contexte de marshaling tel que défini par le canal COM. La disposition exacte des indicateurs dans le champ est décrite dans [la fonction type d' \_ utilisateur](the-type-usersize-function.md).

Le paramètre *pbuffer* est le pointeur de la mémoire tampon en cours. Ce pointeur peut être ou ne pas être aligné sur l’entrée. Votre fonction **<type> \_ UserMarshal** doit aligner le pointeur de la mémoire tampon correctement, marshaler les données et retourner la nouvelle position de mémoire tampon, qui est l’adresse du premier octet après l’objet marshalé. Gardez à l’esprit que la spécification de type de câble détermine la disposition réelle des données dans la mémoire tampon.

Le paramètre *pMyObj* est un pointeur vers un objet de type utilisateur.

La valeur de retour est la nouvelle position de mémoire tampon, qui est l’adresse du premier octet après l’objet non marshalé.

Un dépassement de capacité de la mémoire tampon peut se produire lorsque vous calculez de manière incorrecte la taille des données et essayez de marshaler plus de données que prévu. Veillez à éviter cette situation. Vous pouvez le vérifier à l’aide du pointeur retourné par **<type> \_ UserMarshal** . Dans le cas contraire, vous risquez que le moteur de NDR génère une exception de dépassement de mémoire tampon plus tard.

Les exceptions doivent être interceptées et gérées localement, les exceptions ne doivent pas être autorisées à propigated la pile des appels.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Règles de marshaling pour le marshaling d’utilisateur \_ et le \_ marshaling de câble](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[Marshal de câble \_](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[Marshal d’utilisateur \_](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 