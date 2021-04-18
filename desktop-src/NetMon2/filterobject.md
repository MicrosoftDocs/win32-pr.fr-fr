---
description: Définit un objet unique d’un filtre d’affichage.
ms.assetid: 865b55f3-9294-43c5-b4dc-eb5128ce3a38
title: FILTEROBJECT, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILTEROBJECT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7649ab294f2ecad90946926dcc68d6937b357666
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519254"
---
# <a name="filterobject-structure"></a>FILTEROBJECT, structure

La structure **FILTEROBJECT** définit un objet unique d’un filtre d’affichage. La fonction [**FilterAddObject**](filteraddobject.md) utilise **FILTEROBJECT** pour créer un filtre d’affichage.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _FILTEROBJECT {
  FILTERACTIONTYPE     Action;
  HPROPERTY            hProperty;
  union {
    VALUETYPE           Value;
    HPROTOCOL           hProtocol;
    LPVOID              lpArray;
    LPPROTOCOLTABLETYPE lpProtocolTable;
    LPADDRESS           lpAddress;
    ULPLARGEINT         lpLargeInt;
    ULPTIME             lpTime;
    LPOBJECT_IDENTIFIER lpOID;
  };
  union {
    WORD ByteCount;
    WORD ByteOffset;
  };
  struct _FILTEROBJECT  *pNext;
} FILTEROBJECT, *LPFILTEROBJECT;
```



## <a name="members"></a>Membres

<dl> <dt>

**Action**
</dt> <dd>

Indicateur qui spécifie l’action **FILTEROBJECT** . Un indicateur peut spécifier une propriété, une valeur ou un opérateur.

Le tableau suivant répertorie les indicateurs de propriété de membre d’action.



| Valeur                                                                                                                                                                                                | Signification                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="FILTERACTION_PROPERTY"></span><span id="filteraction_property"></span><dl> <dt>**FILTERACTION ( \_ propriété)**</dt> </dl>                | Contient cette propriété.<br/>                                     |
| <span id="FILTERACTION_PROPERTYEXIST"></span><span id="filteraction_propertyexist"></span><dl> <dt>**FILTERACTION \_ PROPERTYEXIST**</dt> </dl> | Indique qu’une propriété d’action de filtre est déjà définie.<br/> |



 

Le tableau suivant répertorie les indicateurs de valeur de membre d’action.



| Valeur                                                                                                                                                                                        | Signification                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="FILTERACTION_VALUE"></span><span id="filteraction_value"></span><dl> <dt>**valeur de FILTERACTION \_**</dt> </dl>                 | Contient cette valeur.<br/>                                             |
| <span id="FILTERACTION_STRING"></span><span id="filteraction_string"></span><dl> <dt>**chaîne de filtrage \_**</dt> </dl>              | Contient cette chaîne.<br/>                                            |
| <span id="FILTERACTION_ARRAY"></span><span id="filteraction_array"></span><dl> <dt>**Groupe de FILTERACTION \_**</dt> </dl>                 | Contient ce tableau.<br/>                                             |
| <span id="FILTERACTION_CONTAINSNC"></span><span id="filteraction_containsnc"></span><dl> <dt>**FILTERACTION \_ CONTAINSNC**</dt> </dl>  | Indique qu’une propriété contient une sous-chaîne non sensible à la casse.<br/> |
| <span id="FILTERACTION_CONTAINS"></span><span id="filteraction_contains"></span><dl> <dt>**l’action de filtrage \_ contient**</dt> </dl>        | Indique qu’une propriété contient une sous-chaîne respectant la casse.<br/>   |
| <span id="FILTERACTION_ADDRESS"></span><span id="filteraction_address"></span><dl> <dt>**adresse de filtrage \_**</dt> </dl>           | Contient l’adresse MAC.<br/>                                        |
| <span id="FILTERACTION_ADDRESSANY"></span><span id="filteraction_addressany"></span><dl> <dt>**FILTERACTION \_ ADDRESSANY**</dt> </dl>  | Correspond à n’importe quelle adresse MAC.<br/>                                         |
| <span id="FILTERACTION_FROM"></span><span id="filteraction_from"></span><dl> <dt>**ACTION \_ de filtrage à partir de**</dt> </dl>                    | Indique l’adresse **Mac de** l’ordinateur.<br/>                              |
| <span id="FILTERACTION_TO"></span><span id="filteraction_to"></span><dl> <dt>**ACTION \_ de filtrage vers**</dt> </dl>                          | Indique l’adresse **Mac** .<br/>                                |
| <span id="FILTERACTION_FROMTO"></span><span id="filteraction_fromto"></span><dl> <dt>**FILTERACTION \_ FROMTO**</dt> </dl>              | Indique un jumelage de **/à** des adresses Mac.<br/>                |
| <span id="FILTERACTION_LARGEINT"></span><span id="filteraction_largeint"></span><dl> <dt>**FILTERACTION \_ LARGEINT**</dt> </dl>        | Contient un entier long.<br/>                                        |
| <span id="FILTERACTION_TIME"></span><span id="filteraction_time"></span><dl> <dt>**heure de l’action de filtrage \_**</dt> </dl>                    | Contient une structure **SystemTime** .<br/>                             |
| <span id="FILTERACTION_ADDR_ETHER"></span><span id="filteraction_addr_ether"></span><dl> <dt>**ACTION de filtrage d' \_ adresse \_ éther**</dt> </dl> | Contient une adresse MAC Ethernet.<br/>                                |
| <span id="FILTERACTION_ADDR_TOKEN"></span><span id="filteraction_addr_token"></span><dl> <dt>**\_jeton d’adresse de FILTERACTION \_**</dt> </dl> | Contient une adresse MAC Token Ring.<br/>                               |
| <span id="FILTERACTION_ADDR_FDDI"></span><span id="filteraction_addr_fddi"></span><dl> <dt>**ACTION de filtrage d' \_ adresse \_ FDDI**</dt> </dl>    | Contient une adresse MAC FDDI.<br/>                                     |
| <span id="FILTERACTION_ADDR_IPX"></span><span id="filteraction_addr_ipx"></span><dl> <dt>**adresse de filtrage d’adresses \_ \_ IPX**</dt> </dl>       | Contient une adresse MAC IPX.<br/>                                     |
| <span id="FILTERACTION_ADDR_IP"></span><span id="filteraction_addr_ip"></span><dl> <dt>**adresse IP de l’adresse de filtrage \_ \_**</dt> </dl>          | Contient une adresse MAC IP.<br/>                                      |
| <span id="FILTERACTION_OID"></span><span id="filteraction_oid"></span><dl> <dt>**OID de filtrage \_**</dt> </dl>                       | Contient un identificateur d’objet (OID).<br/>                             |



 

Le tableau suivant répertorie les indicateurs d’opérateur de membre d’action.



| Valeur                                                                                                                                                                                                        | Signification                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILTERACTION_INVALID"></span><span id="filteraction_invalid"></span><dl> <dt>**ACTION de filtrage \_ non valide**</dt> </dl>                           | Indique une action de filtre non valide.<br/>                                                                                  |
| <span id="FILTERACTION_AND"></span><span id="filteraction_and"></span><dl> <dt>**FILTERACTION \_ et**</dt> </dl>                                       | Indique une instruction **and** logique.<br/>                                                                               |
| <span id="FILTERACTION_OR"></span><span id="filteraction_or"></span><dl> <dt>**FILTERACTION \_ ou**</dt> </dl>                                          | Indique une instruction **or** logique.<br/>                                                                                |
| <span id="FILTERACTION_XOR"></span><span id="filteraction_xor"></span><dl> <dt>**FILTERACTION \_ Xor**</dt> </dl>                                       | Indique une instruction **or** exclusive logique (XOR).<br/>                                                                |
| <span id="FILTERACTION_NOT"></span><span id="filteraction_not"></span><dl> <dt>**ACTION \_ non**</dt> </dl>                                       | Indique une instruction **not** logique.<br/>                                                                               |
| <span id="FILTERACTION_EQUALNC"></span><span id="filteraction_equalnc"></span><dl> <dt>**FILTERACTION \_ EQUALNC**</dt> </dl>                           | L’action de filtrage est égale et ne respecte pas la casse.<br/>                                                                         |
| <span id="FILTERACTION_EQUAL"></span><span id="filteraction_equal"></span><dl> <dt>**ACTION de filtrage \_ égale**</dt> </dl>                                 | L’action de filtrage est égale à et respecte la casse.<br/>                                                                           |
| <span id="FILTERACTION_NOTEQUALNC"></span><span id="filteraction_notequalnc"></span><dl> <dt>**FILTERACTION \_ NOTEQUALNC**</dt> </dl>                  | L’instruction not logique est égale à et **ne respecte pas** la casse.<br/>                                                             |
| <span id="FILTERACTION_NOTEQUAL"></span><span id="filteraction_notequal"></span><dl> <dt>**FILTERACTION \_ NOTEQUAL**</dt> </dl>                        | L’instruction **not** logique est EQUAL et respecte la casse.<br/>                                                            |
| <span id="FILTERACTION_GREATERNC"></span><span id="filteraction_greaternc"></span><dl> <dt>**FILTERACTION \_ GREATERNC**</dt> </dl>                     | L’action de filtrage est supérieure à (>) et ne respecte pas la casse.<br/>                                                           |
| <span id="FILTERACTION_GREATER"></span><span id="filteraction_greater"></span><dl> <dt>**ACTION de filtrage \_ supérieure**</dt> </dl>                           | L’action de filtrage est supérieure à (>) et respecte la casse.<br/>                                                             |
| <span id="FILTERACTION_LESSNC"></span><span id="filteraction_lessnc"></span><dl> <dt>**FILTERACTION \_ LESSNC**</dt> </dl>                              | L’action de filtrage est inférieure à (<) et ne respecte pas la casse.<br/>                                                              |
| <span id="FILTERACTION_LESS"></span><span id="filteraction_less"></span><dl> <dt>**ACTION de filtrage \_ moins**</dt> </dl>                                    | L’action de filtrage est inférieure à (<) et respecte la casse.<br/>                                                                |
| <span id="FILTERACTION_GREATEREQUALNC"></span><span id="filteraction_greaterequalnc"></span><dl> <dt>**FILTERACTION \_ GREATEREQUALNC**</dt> </dl>      | L’action de filtrage est supérieure ou égale à (>=) et ne respecte pas la casse.<br/>                                              |
| <span id="FILTERACTION_GREATEREQUAL"></span><span id="filteraction_greaterequal"></span><dl> <dt>**FILTERACTION \_ greaterequal à**</dt> </dl>            | L’action de filtrage est supérieure ou égale à (>=) et respecte la casse.<br/>                                                |
| <span id="FILTERACTION_LESSEQUALNC"></span><span id="filteraction_lessequalnc"></span><dl> <dt>**FILTERACTION \_ LESSEQUALNC**</dt> </dl>               | L’action de filtrage est inférieure ou égale à (<=) et ne respecte pas la casse.<br/>                                                 |
| <span id="FILTERACTION_LESSEQUAL"></span><span id="filteraction_lessequal"></span><dl> <dt>**FILTERACTION \_ LESSEQUAL**</dt> </dl>                     | L’action de filtrage est inférieure ou égale à (<=) et respecte la casse.<br/>                                                |
| <span id="FILTERACTION_PLUS"></span><span id="filteraction_plus"></span><dl> <dt>**ACTION de filtrage \_ plus**</dt> </dl>                                    | Ajoutez l’opérateur (+).<br/>                                                                                                    |
| <span id="FILTERACTION_MINUS"></span><span id="filteraction_minus"></span><dl> <dt>**ACTION de filtrage \_ moins**</dt> </dl>                                 | Opérateur de soustraction (-).<br/>                                                                                               |
| <span id="FILTERACTION_AREBITSON"></span><span id="filteraction_arebitson"></span><dl> <dt>**FILTERACTION \_ AREBITSON**</dt> </dl>                     | Indique une opération au niveau du bit.<br/>                                                                                       |
| <span id="FILTERACTION_AREBITSOFF"></span><span id="filteraction_arebitsoff"></span><dl> <dt>**FILTERACTION \_ AREBITSOFF**</dt> </dl>                  | Indique une opération non-au niveau du bit.<br/>                                                                                   |
| <span id="FILTERACTION_PROTOCOLSEXIST"></span><span id="filteraction_protocolsexist"></span><dl> <dt>**FILTERACTION \_ PROTOCOLSEXIST**</dt> </dl>      | Indique que les protocoles sélectionnés existent.<br/>                                                                         |
| <span id="FILTERACTION_PROTOCOLEXIST"></span><span id="filteraction_protocolexist"></span><dl> <dt>**FILTERACTION \_ PROTOCOLEXIST**</dt> </dl>         | Indique que le protocole sélectionné existe.<br/>                                                                         |
| <span id="FILTERACTION_ARRAYEQUAL"></span><span id="filteraction_arrayequal"></span><dl> <dt>**FILTERACTION \_ ARRAYEQUAL**</dt> </dl>                  | Indique que le contenu du tableau est égal. L’indicateur doit être utilisé avec une structure de **\_ tableau de FILTERACTION** .<br/>             |
| <span id="FILTERACTION_DEREFPROPERTY"></span><span id="filteraction_derefproperty"></span><dl> <dt>**FILTERACTION \_ DEREFPROPERTY**</dt> </dl>         | Décrit une correspondance de modèle à un offset (en octets) à partir du protocole.<br/>                                                |
| <span id="FILTERACTION_OID_CONTAINS"></span><span id="filteraction_oid_contains"></span><dl> <dt>**l' \_ OID de FILTERACTION \_ contient**</dt> </dl>           | Évalue une sous-chaîne dans un identificateur d’objet. L’action doit être utilisée avec la structure de l' **\_ OID de FILTERACTION** .<br/> |
| <span id="FILTERACTION_OID_BEGINS_WITH"></span><span id="filteraction_oid_begins_with"></span><dl> <dt>**l' \_ OID \_ de FILTERACTION commence \_ par**</dt> </dl> | Évalue une sous-chaîne qui commence un identificateur d’objet. L’indicateur doit être utilisé avec **l' \_ OID de FILTERACTION**.<br/>            |
| <span id="FILTERACTION_OID_ENDS_WITH"></span><span id="filteraction_oid_ends_with"></span><dl> <dt>**l' \_ OID \_ de filtrage se termine \_ par**</dt> </dl>       | Évalue une sous-chaîne qui termine un identificateur d’objet. L’indicateur doit être utilisé avec **l' \_ OID de FILTERACTION**.<br/>              |
| <span id="FILTERACTION_ADDR_VINES"></span><span id="filteraction_addr_vines"></span><dl> <dt>**ACTION de filtrage des \_ \_ vignes**</dt> </dl>                 | Contient une adresse MAC Vines.<br/>                                                                                        |
| <span id="FILTERACTION_EXPRESSION"></span><span id="filteraction_expression"></span><dl> <dt>**EXPRESSION de FILTERACTION \_**</dt> </dl>                  | Contient une expression d’action.<br/>                                                                                       |
| <span id="FILTERACTION_BOOL"></span><span id="filteraction_bool"></span><dl> <dt>**FILTERACTION (valeur \_ booléenne)**</dt> </dl>                                    | Contient un type de données **bool** .<br/>                                                                                       |
| <span id="FILTER_DIRECTION_NEXT"></span><span id="filter_direction_next"></span><dl> <dt>**DIRECTION du filtre \_ \_ suivant**</dt> </dl>                       | Contrôle la direction séquentielle (Frame suivant) dans un fichier de capture.<br/>                                                    |
| <span id="FILTER_DIRECTION_PREV"></span><span id="filter_direction_prev"></span><dl> <dt>**DIRECTION du filtre \_ \_ préc.**</dt> </dl>                       | Contrôle la direction séquentielle (Frame précédent) dans un fichier de capture.<br/>                                                |



 

</dd> <dt>

**hProperty**
</dt> <dd>

Handle d’une clé de propriété.

</dd> <dt>

**Valeur**
</dt> <dd>

Valeur d’un objet.

</dd> <dt>

**hProtocol**
</dt> <dd>

Handle permettant d’afficher le protocole de filtre.

</dd> <dt>

**lpArray**
</dt> <dd>

Pointeur vers un tableau.

</dd> <dt>

**lpProtocolTable**
</dt> <dd>

Pointeur vers une liste de protocoles conçue pour tester l’existence d’un protocole dans un frame.

</dd> <dt>

**lpAddress**
</dt> <dd>

Pointeur vers l’adresse du type de noyau. Par exemple, MAC ou IP.

</dd> <dt>

**lpLargeInt**
</dt> <dd>

Double **DWORD** utilisé dans une application Windows NT ou Windows 2000.

</dd> <dt>

**lpTime**
</dt> <dd>

Pointeur vers une structure **SystemTime** .

</dd> <dt>

**lpOID**
</dt> <dd>

Pointeur vers la structure de l' **\_ identificateur d’objet** (OID).

</dd> <dt>

**ByteCount**
</dt> <dd>

Nombre, en octets, dans le frame.

</dd> <dt>

**ByteOffset**
</dt> <dd>

Valeur d’octet de décalage de la structure FILTEROBJECT utilisée pour comparer des tableaux.

</dd> <dt>

**pNext**
</dt> <dd>

Réservé.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




