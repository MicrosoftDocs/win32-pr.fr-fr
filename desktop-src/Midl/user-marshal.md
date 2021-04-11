---
title: attribut user_marshal
description: L' \_ attribut ACF de Marshal d’utilisateur associe un type local nommé dans le langage cible (type utilisateur) à un type de transfert (type filaire) qui est transféré entre le client et le serveur.
ms.assetid: a2407aa3-574d-4690-8cdf-cb1c01ca8c49
keywords:
- user_marshal MIDL de l’attribut
topic_type:
- apiref
api_name:
- user_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5326c9390362193a1be9dc06ee3a57f174474cc2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314796"
---
# <a name="user_marshal-attribute"></a>\_attribut de Marshal utilisateur

L’attribut ACF de **\_ Marshal d’utilisateur** associe un type local nommé dans le langage cible (*type utilisateur*) à un type de transfert (*type filaire*) qui est transféré entre le client et le serveur.

``` syntax
typedef [user_marshal(userm_type)] wire-type; 
unsigned long __RPC_USER  < userm_type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm_type >  __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long __RPC_FAR *pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm_type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm_type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm_type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type d’utilisateur* 
</dt> <dd>

Spécifie l’identificateur du type de données utilisateur à marshaler. Le *type utilisateur* n’a pas besoin d’être transmissible et n’a pas besoin d’être un type connu du compilateur MIDL.

</dd> <dt>

*type de câble* 
</dt> <dd>

Spécifie le type de données de transfert nommé qui est réellement transféré entre le client et le serveur. Le type de câble doit être un type de base MIDL, un type prédéfini ou un identificateur de type d’un type qui peut être transmis sur le réseau.

</dd> <dt>

*pFlags* 
</dt> <dd>

Spécifie un pointeur vers un champ d’indicateur ( [**unsigned**](unsigned.md) [**long**](long.md)). Le mot de poids fort spécifie les indicateurs de représentation des données de rapport de non-remise tels qu’ils sont définis par DCE pour la représentation à virgule flottante, Big-endian et caractère. Le mot de poids faible spécifie un indicateur de contexte de marshaling. La disposition exacte des indicateurs est décrite dans [la fonction type d' \_ utilisateur](/windows/desktop/Rpc/the-type-usersize-function).

</dd> <dt>

*StartingSize* 
</dt> <dd>

Spécifie la taille de la mémoire tampon actuelle (décalage) avant le dimensionnement de l’objet.

</dd> <dt>

*pUser \_ typeObject* 
</dt> <dd>

Spécifie un pointeur vers un objet de *\_ type utilisateur*.

</dd> <dt>

*Buffer* 
</dt> <dd>

Spécifie le pointeur de la mémoire tampon actuelle.

</dd> </dl>

## <a name="remarks"></a>Notes

Chaque type local nommé, *utilisateur-type*, a une correspondance un-à-un avec un *type de câble* qui définit la représentation filaire du type. Vous devez fournir des routines pour dimensionner les données pour le marshaling, pour marshaler et démarshaler les données, ainsi que pour libérer de la mémoire. Pour plus d’informations sur ces routines, consultez [l' \_ attribut User Marshal](/windows/desktop/Rpc/the-user-marshal-attribute). Notez que s’il existe des types incorporés dans vos données qui sont également définis avec le **\_ Marshal utilisateur** ou \[ le [**\[ \_ Marshal \] de câble**](wire-marshal.md), vous devez également gérer la maintenance de ces types incorporés.

Le *type de câble* ne peut pas être un pointeur d’interface ou un pointeur complet. Le *type de câble* doit avoir une taille de mémoire bien définie. Pour plus d’informations sur la façon de marshaler un *type de câble* donné, consultez la page [règles de marshaling pour le marshaleur d’utilisateur \_ et le \_ marshaling de réseau](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) .

Le *type utilisateur* ne doit pas être un pointeur d’interface, car ceux-ci peuvent être marshalés directement. Si le type d’utilisateur est un pointeur complet, vous devez gérer vous-même les alias.

## <a name="examples"></a>Exemples

``` syntax
// Marshal a long as a structure containing two shorts.

typedef unsigned long FOUR_BYTE_DATA;
typedef struct _TWO_X_TWO_BYTE_DATA 
{ 
    unsigned short low; 
    unsigned short high; 
} TWO_X_TWO_BYTE_DATA;
```

``` syntax
// ACFL file

typedef [user_marshal(FOUR_BYTE_DATA)] TWO_X_TWO_BYTE_DATA;

// Marshaling functions:

// Calculate size that converted data will require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**représenter \_ comme**](represent-as.md)
</dt> <dt>

[**non signé**](unsigned.md)
</dt> <dt>

[Attribut de \_ Marshal d’utilisateur](/windows/desktop/Rpc/the-user-marshal-attribute)
</dt> <dt>

[**Marshal de câble \_**](wire-marshal.md)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 