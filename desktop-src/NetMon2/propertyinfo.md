---
description: La structure de données PROPERTYINFO définit une propriété du protocole.
ms.assetid: 878777ab-141d-4cc5-b0c1-f2ac8f770bf0
title: PROPERTYINFO, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 8dc20b94fbf889b4c04712eadbee5d7d834d3cf260962fe01ef7837e5893c4a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128949"
---
# <a name="propertyinfo-structure"></a>PROPERTYINFO, structure

La structure de données **PROPERTYINFO** définit une propriété du protocole.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PROPERTYINFO {
  HPROPERTY hProperty;
  DWORD     Version;
  LPSTR     Label;
  LPSTR     Comment;
  BYTE      DataType;
  BYTE      DataQualifier;
  union {
    LPVOID  lpExtendedInfo;
    LPRANGE lpRange;
    LPSET   lpSet;
    DWORD   Bitmask;
    DWORD   Value;
  };
  WORD      FormatStringSize;
  LPVOID    InstanceData;
} PROPERTYINFO, *LPPROPERTYINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**hProperty**
</dt> <dd>

Définissez ce champ sur zéro. Lors de la sortie, Moniteur réseau retourne un handle vers la propriété après que la propriété a été ajoutée à la base de données de propriétés.

</dd> <dt>

**Version**
</dt> <dd>

Réservé. Doit être défini à zéro.

</dd> <dt>

**Étiquette**
</dt> <dd>

Nom de la propriété.

</dd> <dt>

**Commentaire**
</dt> <dd>

Description de la propriété. La description s’affiche dans la barre d’État Moniteur réseau.

</dd> <dt>

**DataType**
</dt> <dd>

Type de données de la propriété. Ce membre peut avoir l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                       | Signification                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_TYPE_VOID"></span><span id="prop_type_void"></span><dl> <dt>**PROP, \_ type \_ void**</dt> </dl>                                           | Le type de propriété est inconnu. Il n’existe pas de longueur ou de format implicite.<br/>                                                                                                                                                                                                                                  |
| <span id="PROP_TYPE_SUMMARY"></span><span id="prop_type_summary"></span><dl> <dt>**\_Résumé du type de prop \_**</dt> </dl>                                  | Résumé du type de propriété. Indique la première instance de propriété que l’analyseur attache à un frame. \_ \_ Le résumé du type prop peut servir d’espace réservé pour les groupes de propriétés. Cette valeur indique que la propriété n’est pas définie dans le protocole *RFC*.<br/> |
| <span id="PROP_TYPE_BYTE"></span><span id="prop_type_byte"></span><dl> <dt>**\_octet de type prop \_**</dt> </dl>                                           | Données numériques d’une taille d’un octet (entité 8 bits).<br/>                                                                                                                                                                                                                                             |
| <span id="PROP_TYPE_WORD"></span><span id="prop_type_word"></span><dl> <dt>**PROP, \_ type \_ Word**</dt> </dl>                                           | Données numériques d’une taille de deux octets (entité 16 bits).<br/>                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_DWORD"></span><span id="prop_type_dword"></span><dl> <dt>**TYPE de PROP \_ \_ DWORD**</dt> </dl>                                        | Données numériques d’une taille de 4 octets (entité 32 bits).<br/>                                                                                                                                                                                                                                          |
| <span id="PROP_TYPE_LARGEINT"></span><span id="prop_type_largeint"></span><dl> <dt>**PROP, \_ type \_ LARGEINT**</dt> </dl>                               | Données numériques d’une taille de huit octets (entité 64 bits).<br/>                                                                                                                                                                                                                                         |
| <span id="PROP_TYPE_ADDR"></span><span id="prop_type_addr"></span><dl> <dt>**\_ADR type \_ addr**</dt> </dl>                                           | Adresse MAC (entité de 6 octets).<br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_TIME"></span><span id="prop_type_time"></span><dl> <dt>**\_heure du type de prop \_**</dt> </dl>                                           | Structure **SystemTime** .<br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_STRING"></span><span id="prop_type_string"></span><dl> <dt>**\_chaîne de type prop \_**</dt> </dl>                                     | Données texte ASCII. Ce type de données ne se termine pas par un caractère NULL. <br/> Pour les données Unicode, lorsque les données de texte ASCII sont spécifiées, l' \_ Indicateur Unicode IFLAG doit également être défini lorsque la fonction d’instance de propriété Attach est appelée.<br/>                                                                          |
| <span id="PROP_TYPE_IP_ADDRESS"></span><span id="prop_type_ip_address"></span><dl> <dt>**\_ \_ adresse IP du type de prop \_**</dt> </dl>                        | Adresse IP. (entité de 4 octets).<br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_IPX_ADDRESS"></span><span id="prop_type_ipx_address"></span><dl> <dt>**\_ \_ adresse IPX du type prop \_**</dt> </dl>                     | Adresse IPX. (entité de 10 octets).<br/>                                                                                                                                                                                                                                                                   |
| <span id="PROP_TYPE_BYTESWAPPED_WORD"></span><span id="prop_type_byteswapped_word"></span><dl> <dt>**PROP, \_ type \_ BYTESWAPPED \_ mot**</dt> </dl>      | Obsolète. Pour les données de mot avec échange d’octets, définissez **DataType** sur Prop \_ type \_ Word et définissez l' \_ indicateur permuté IFLAG lors de l’appel d’une fonction d’instance de propriété **Attach** .<br/>                                                                                                                                |
| <span id="PROP_TYPE_BYTESWAPPED_DWORD"></span><span id="prop_type_byteswapped_dword"></span><dl> <dt>**PROP \_ type \_ BYTESWAPPED \_ DWORD**</dt> </dl>   | Obsolète. Pour les données DWORD échangées en octets, définissez **DataType** sur Prop \_ type \_ DWORD et définissez l' \_ indicateur permuté IFLAG lors de l’appel d’une fonction d’instance de propriété **Attach** .<br/>                                                                                                                              |
| <span id="PROP_TYPE_TYPED_STRING"></span><span id="prop_type_typed_string"></span><dl> <dt>**\_ \_ chaîne typée de type prop \_**</dt> </dl>                  | Obsolète. Pour les données de type chaîne de type variable, définissez **DataType** sur \_ type de \_ chaîne et définissez l' \_ Indicateur Unicode IFLAG lors de l’appel d’une fonction d’instance de propriété **Attach** .<br/>                                                                                                                           |
| <span id="PROP_TYPE_RAW_DATA"></span><span id="prop_type_raw_data"></span><dl> <dt>**\_ \_ données brutes de type prop \_**</dt> </dl>                              | Données brutes de longueur et de format inconnues.<br/>                                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_COMMENT"></span><span id="prop_type_comment"></span><dl> <dt>**Commentaire sur le \_ type prop \_**</dt> </dl>                                  | Identique au type PROP, \_ \_ void.<br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_SRCFRIENDLYNAME"></span><span id="prop_type_srcfriendlyname"></span><dl> <dt>**PROP, \_ type \_ SRCFRIENDLYNAME**</dt> </dl>          | Adresse du nom convivial de la source. Moniteur réseau ne fournit pas de prise en charge intégrée de la mise en forme pour ce type de données.<br/>                                                                                                                                                                                |
| <span id="PROP_TYPE_DSTFRIENDLYNAME"></span><span id="prop_type_dstfriendlyname"></span><dl> <dt>**PROP, \_ type \_ DSTFRIENDLYNAME**</dt> </dl>          | Adresse du nom convivial de destination. Moniteur réseau ne fournit pas de prise en charge intégrée de la mise en forme pour ce type de données.<br/>                                                                                                                                                                           |
| <span id="PROP_TYPE_TOKENRING_ADDRESS"></span><span id="prop_type_tokenring_address"></span><dl> <dt>**\_ \_ adresse TOKENRING de type prop \_**</dt> </dl>   | Adresse Token Ring. Moniteur réseau ne fournit pas de prise en charge intégrée de la mise en forme pour ce type de données.<br/>                                                                                                                                                                                             |
| <span id="PROP_TYPE_FDDI_ADDRESS"></span><span id="prop_type_fddi_address"></span><dl> <dt>**\_ \_ adresse FDDI du type de prop \_**</dt> </dl>                  | Adresse FDDI. Moniteur réseau ne fournit pas de prise en charge intégrée de la mise en forme pour ce type de données.<br/>                                                                                                                                                                                                   |
| <span id="PROP_TYPE_ETHERNET_ADDRESS"></span><span id="prop_type_ethernet_address"></span><dl> <dt>**\_ \_ adresse Ethernet du type prop \_**</dt> </dl>      | Adresse Ethernet. Moniteur réseau ne fournit pas de prise en charge intégrée de la mise en forme pour ce type de données.<br/>                                                                                                                                                                                               |
| <span id="PROP_TYPE_OBJECT_IDENTIFIER"></span><span id="prop_type_object_identifier"></span><dl> <dt>**\_identificateur d' \_ objet du type prop \_**</dt> </dl>   | Identificateur d’objet SNMP encodé BER.<br/>                                                                                                                                                                                                                                                              |
| <span id="PROP_TYPE_VINES_IP_ADDRESS"></span><span id="prop_type_vines_ip_address"></span><dl> <dt>**\_ \_ \_ adresse IP du type de props \_**</dt> </dl>     | Adresse IP Vines (entité de 6 octets).<br/>                                                                                                                                                                                                                                                                |
| <span id="PROP_TYPE_VAR_LEN_SMALL_INT"></span><span id="prop_type_var_len_small_int"></span><dl> <dt>**PROP \_ type \_ var \_ Len \_ petit \_ int**</dt> </dl> | Valeur numérique sans longueur prédéfinie, mais inférieure à 8 octets. La longueur des données attachées détermine la longueur de la valeur.<br/>                                                                                                                                                |



 

</dd> <dt>

**DataQualifier**
</dt> <dd>

Qualificateur de données d’une propriété. Ce membre fournit des informations précises sur le type de données.

**DataQualifier** peut avoir l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                  | Signification                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_QUAL_NONE"></span><span id="prop_qual_none"></span><dl> <dt>**PROP \_ Qualys \_ None**</dt> </dl>                                      | Le type de données de la propriété est la seule spécification de la propriété. <br/> Lorsque cette valeur est définie, le membre Union de la structure a la valeur **null**, puis est ignoré.<br/>                                                                                                                                        |
| <span id="PROP_QUAL_RANGE"></span><span id="prop_qual_range"></span><dl> <dt>**plage de compétences PROP \_ \_**</dt> </dl>                                   | La valeur numérique doit être comprise dans une plage donnée. Définissez la plage dans le membre **lpRange** .<br/>                                                                                                                                                                                                                |
| <span id="PROP_QUAL_SET"></span><span id="prop_qual_set"></span><dl> <dt>**ensemble de compétences PROP \_ \_**</dt> </dl>                                         | La valeur d’une propriété est comparée à un ensemble de valeurs spécifiées dans le membre **lpSet** de l’Union de la structure. La valeur d’une propriété peut être un **octet**, un **mot**, un **DWORD**, un **LARGEINT** ou une **heure**.<br/>                                                                                                |
| <span id="PROP_QUAL_BITFIELD"></span><span id="prop_qual_bitfield"></span><dl> <dt>**\_champ de \_ binaire prop Qualys**</dt> </dl>                          | Obsolète.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="PROP_QUAL_LABELED_SET"></span><span id="prop_qual_labeled_set"></span><dl> <dt>**PROP \_ prop \_ étiquetée \_ Set**</dt> </dl>                | La valeur d’une propriété est comparée à une valeur d’un ensemble de paires d’étiquettes de valeur. Les paires d’étiquettes de valeur sont spécifiées dans le membre **lpSet** de l’Union de la structure. <br/> Au moment de l’affichage, si la valeur de la propriété correspond à une valeur dans le jeu, une valeur et l’étiquette associée sont affichées.<br/> |
| <span id="PROP_QUAL_LABELED_BITFIELD"></span><span id="prop_qual_labeled_bitfield"></span><dl> <dt>**PROP \_ , \_ étiquette de champ de \_ champ**</dt> </dl> | Obsolète. Utilisez les indicateurs de compétences PROP à la \_ \_ place.<br/>                                                                                                                                                                                                                                                                             |
| <span id="PROP_QUAL_CONST"></span><span id="prop_qual_const"></span><dl> <dt>**PROP \_ Qualys \_ const**</dt> </dl>                                   | La valeur d’une propriété est comparée à une constante spécifiée dans le membre **value** de l’Union. <br/> Au moment de l’affichage, si les valeurs de propriété et la constante ne correspondent pas, un message d’erreur mis en forme s’affiche avec la valeur définie sur normal.<br/>                                                             |
| <span id="PROP_QUAL_FLAGS"></span><span id="prop_qual_flags"></span><dl> <dt>**indicateurs de compétences PROP \_ \_**</dt> </dl>                                   | La valeur de la propriété est comparée aux BITs spécifiques identifiés dans le membre **lpSet** de l’Union.<br/>                                                                                                                                                                                                              |
| <span id="PROP_QUAL_ARRAY"></span><span id="prop_qual_array"></span><dl> <dt>**Tableau de compétences PROP \_ \_**</dt> </dl>                                   | La valeur d’une propriété spécifie un tableau de valeurs. La longueur des données attachées détermine la longueur d’un tableau. <br/> Lorsque la \_ valeur du tableau prop Qualys \_ est définie, le membre Union de la structure de données **PROPERTYINFO** a la valeur **null** et est ignoré.<br/>                                                    |



 

</dd> <dt>

**lpExtendedInfo**
</dt> <dd>

Réservé (membre de l’Union).

</dd> <dt>

**lpRange**
</dt> <dd>

Pointeur vers une structure de [plage](range.md) qui définit une plage de valeurs. Ce membre doit être défini si le membre **DataQualifier** de cette structure a la valeur prop \_ Qualys \_ Range (membre de Union).

</dd> <dt>

**lpSet**
</dt> <dd>

Pointeur vers une structure de [jeu](set.md) qui spécifie un ensemble de valeurs ou d’étiquettes. Ce membre doit être défini si le membre **DataQualifier** de la structure a la valeur prop \_ Qualys \_ Set, prop \_ Qualys \_ étiquetée \_ set ou prop \_ Qualys \_ Flags (member of Union).

</dd> <dt>

**Binaire**
</dt> <dd>

Obsolète (membre de l’Union).

</dd> <dt>

**Valeur**
</dt> <dd>

Valeur constante utilisée lorsque **DataQualifier** a la valeur prop \_ Qualys \_ const (membre de Union).

</dd> <dt>

**FormatStringSize**
</dt> <dd>

Taille maximale utilisée uniquement pour la description de la propriété.

</dd> <dt>

**InstanceData**
</dt> <dd>

Spécifiez la fonction de format appelée pour mettre en forme les données affichées pour la propriété. Pour utiliser le formateur générique, spécifiez la fonction **FormatPropertyInstance** .

</dd> </dl>

## <a name="remarks"></a>Remarques

La structure **PROPERTYINFO** est utilisée dans les appels à la fonction [AddProperty](/previous-versions/bb251873(v=msdn.10)) . La fonction **AddProperty** ajoute une définition de propriété unique à la [*base de données des propriétés de*](p.md)l’analyseur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[AddProperty](/previous-versions/bb251873(v=msdn.10))
</dt> <dt>

[VONT](range.md)
</dt> <dt>

[SET](set.md)
</dt> </dl>

 

