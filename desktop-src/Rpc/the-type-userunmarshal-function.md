---
title: Fonction type_UserUnmarshal
description: La \_ fonction de type UserUnmarshal est une fonction d’assistance pour les attributs \ Wire \_ Marshal \ et \ user \_ Marshal \.
ms.assetid: ee7a0e96-11ec-4d15-9d4b-55cc175fdd55
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332edbc2391aadf297789cc0ae862454786bdd8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031815"
---
# <a name="the-type_userunmarshal-function"></a>Type \_ UserUnmarshal (fonction)

La fonction **<type> \_ UserUnmarshal** est une fonction d’assistance pour les attributs de marshaling de \[ [ \_ câble](/windows/desktop/Midl/wire-marshal) \] et d' \[ [utilisateur \_](/windows/desktop/Midl/user-marshal) \] . Les stubs appellent cette fonction pour démarshaler des données côté client ou côté serveur. La fonction est définie comme suit :

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserUnmarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

Le <type> dans le nom de fonction correspond au type utilisateur spécifié dans la définition de type de marshaling de **\[ \_ \] câble** ou d' **\[ utilisateur \_ \]** . Ce type peut être non transmissible ou même, lorsqu’il est utilisé avec l’attribut de **\[ \_ Marshal \] utilisateur** , inconnu du compilateur MIDL. Le nom du type de câble (le nom du type transmissible) n’est pas utilisé dans le prototype de la fonction. Notez, toutefois, que le type de câble définit la disposition filaire pour les données, comme spécifié par l’ETCD OSF.

Le paramètre *pFlags* est un pointeur vers un champ d’indicateur **long non signé** . Le mot supérieur de l’indicateur contient des indicateurs de représentation de données NDR tels que définis par l’ETCD OSF pour les représentations à virgule flottante, d’ordre d’octet et de caractère. Le mot inférieur contient un indicateur de contexte de marshaling tel que défini par le canal COM. La disposition exacte des indicateurs dans le champ est décrite dans [la fonction type d' \_ utilisateur](the-type-usersize-function.md).

Le paramètre *pbuffer* est le pointeur de la mémoire tampon en cours. Ce pointeur peut être ou ne pas être aligné sur l’entrée. Votre fonction **<type> \_ UserUnmarshal** doit aligner le pointeur de la mémoire tampon correctement, démarshaler les données et retourner la nouvelle position de mémoire tampon, qui est l’adresse du premier octet après l’objet non marshalé.

Le paramètre *pMyObj* est un pointeur vers un objet de type défini par l’utilisateur.

Dans un environnement hétérogène, le moteur de NDR effectue toute conversion de données nécessaire avant d’appeler la fonction **<type> \_ UserUnmarshal** . Notez que le moteur de NDR effectue cette conversion de données en fonction de la définition de type de câble fournie pour ce type de données utilisateur. L’indicateur indique la représentation des données de l’expéditeur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Règles de marshaling pour le marshaling d’utilisateur \_ et le \_ marshaling de câble](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[Marshal de câble \_](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[Marshal d’utilisateur \_](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 