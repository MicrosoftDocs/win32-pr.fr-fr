---
title: wire_marshal (attribut)
description: L’attribut \ Wire \_ Marshal \ spécifie un type de données qui sera utilisé pour la transmission (type de câble) au lieu d’un type de données spécifique à l’application (type utilisateur).
ms.assetid: 51969f2c-7390-42c4-8aa6-ba12fdb22d23
keywords:
- wire_marshal MIDL de l’attribut
topic_type:
- apiref
api_name:
- wire_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17466648078162bc8244219f77e3ecc0dc4cb4d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093057"
---
# <a name="wire_marshal-attribute"></a>\_attribut Wire Marshal

L’attribut **\[ Wire \_ Marshal \]** spécifie un type de données qui sera utilisé pour la transmission ( *type de câble*) au lieu d’un type de données spécifique à l’application ( *type utilisateur*).

``` syntax
typedef [wire_marshal(wire_type)] type-specifier userm-type; 
unsigned long __RPC_USER  < userm-type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm-type > __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long  __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm-type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm-type > __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm-type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm-type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*type de câble* 
</dt> <dd>

Spécifie le type de données de transfert nommé qui est réellement transféré entre le client et le serveur. Le *type de câble* doit être un type de base MIDL, un type prédéfini ou un identificateur de type d’un type qui peut être transmis sur le réseau.

</dd> <dt>

*spécificateur de type* 
</dt> <dd>

Type pour lequel *User-type* deviendra un alias.

</dd> <dt>

*type d’utilisateur* 
</dt> <dd>

Spécifie l’identificateur du type de données utilisateur à marshaler. Il peut s’agir de n’importe quel type, comme indiqué par le *type-specifier*, à condition qu’il ait une taille bien définie. Le *type utilisateur* n’a pas besoin d’être transmissible, mais il doit être un type connu du compilateur MIDL.

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

Spécifie un pointeur vers un objet de *\_ type utilisateur.*

</dd> <dt>

*Buffer* 
</dt> <dd>

Spécifie le pointeur de la mémoire tampon actuelle.

</dd> </dl>

## <a name="remarks"></a>Notes

Chaque type de données spécifique à l’application, *utilisateur-type,* a une correspondance un-à-un avec un *type de câble* qui définit la représentation filaire du type. Vous devez fournir des routines pour dimensionner les données pour le marshaling, pour marshaler et démarshaler les données, ainsi que pour libérer de la mémoire. Notez que s’il existe des types incorporés dans vos données qui sont également définis avec un **\[ \_ marshaling \] de câble** ou un **\[** [**\_ Marshal d’utilisateur**](user-marshal.md) **\]** , vous devez également gérer la maintenance de ces types incorporés. Pour plus d’informations sur ces routines, consultez [l' \_ attribut Wire Marshal](/windows/desktop/Rpc/the-wire-marshal-attribute).

Votre implémentation doit suivre les règles de marshaling en fonction de la spécification OSF-DCE. Pour plus d’informations sur la syntaxe de transfert de rapport de non-remise [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm) , consultez. Il n’est pas recommandé d’utiliser le **\[ \_ marshaling \] de câble** si vous n’êtes pas familiarisé avec le protocole câble.

Le *type de câble* ne peut pas être un pointeur d’interface ou un pointeur complet. Le *type de câble* doit avoir une taille de mémoire bien définie. Pour plus d’informations sur la façon de marshaler un *type de câble* donné, consultez la page [règles de marshaling pour le marshaleur d’utilisateur \_ et le \_ marshaling de réseau](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) .

L' *utilisateur-type* ne doit pas être un pointeur d’interface, car ceux-ci peuvent être marshalés directement. Si le type d’utilisateur est un pointeur complet, vous devez gérer vous-même les alias.

Vous ne pouvez pas utiliser l’attribut **\[ Wire \_ \] Marshal** avec l' **\[** attribut [**allocate**](allocate.md) **\]** , directement ou indirectement, car le moteur de NDR ne contrôle pas l’allocation de mémoire pour le type transmis.

## <a name="examples"></a>Exemples

``` syntax
typedef unsigned long _FOUR_BYTE_DATA;

typedef struct _TWO_X_TWO_BYTE_DATA 
{
        unsigned short low;
        unsigned short high;
} TWO_X_TWO_BYTE_DATA;

typedef [wire_marshal(TWO_X_TWO_BYTE_DATA)] 
    _FOUR_BYTE_DATA FOUR_BYTE_DATA; 

//Marshaling functions:

// Calculate size that converted data will 
// require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as 
// TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top 
// node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul 
    );
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**lui**](allocate.md)
</dt> <dt>

[Représentation des données](/windows/desktop/Rpc/data-representation)
</dt> <dt>

[Types de base MIDL](midl-base-types.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> <dt>

[Attribut de \_ Marshal de câble](/windows/desktop/Rpc/the-wire-marshal-attribute)
</dt> <dt>

[**transmettre \_ en tant que**](transmit-as.md)
</dt> <dt>

[**non signé**](unsigned.md)
</dt> <dt>

[**Marshal d’utilisateur \_**](user-marshal.md)
</dt> </dl>

 

 