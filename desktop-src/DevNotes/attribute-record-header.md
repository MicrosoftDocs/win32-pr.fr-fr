---
description: Représente un enregistrement d’attribut.
ms.assetid: f9d9458c-b179-441c-9f62-ff0ac2f75329
title: Structure ATTRIBUTE_RECORD_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_RECORD_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: ae710ca04f11cb70c1bad9b5e6fec25f8fb5e94f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847014"
---
# <a name="attribute_record_header-structure"></a>\_Structure d' \_ en-tête d’enregistrement d’attribut

\[Cette structure est valide uniquement pour la version 3 des volumes NTFS ; elles peuvent être modifiées dans les versions ultérieures.\]

Représente un enregistrement d’attribut.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _ATTRIBUTE_RECORD_HEADER {
  ATTRIBUTE_TYPE_CODE TypeCode;
  ULONG               RecordLength;
  UCHAR               FormCode;
  UCHAR               NameLength;
  USHORT              NameOffset;
  USHORT              Flags;
  USHORT              Instance;
  union {
    struct {
      ULONG  ValueLength;
      USHORT ValueOffset;
      UCHAR  Reserved[2];
    } Resident;
    struct {
      VCN      LowestVcn;
      VCN      HighestVcn;
      USHORT   MappingPairsOffset;
      UCHAR    Reserved[6];
      LONGLONG AllocatedLength;
      LONGLONG FileSize;
      LONGLONG ValidDataLength;
      LONGLONG TotalAllocated;
    } Nonresident;
  } Form;
} ATTRIBUTE_RECORD_HEADER, *PATTRIBUTE_RECORD_HEADER;
```



## <a name="members"></a>Membres

<dl> <dt>

**TypeCode**
</dt> <dd>

Code du type d’attribut.



| Valeur                                                                                                                                                                                                                                           | Signification                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$Standard \_ INFORMATION**</dt> <dt>0x10</dt> </dl> | Les attributs de fichier (par exemple, lecture seule et Archive), les horodatages (tels que la création et la dernière modification de fichier) et le nombre de liens physiques.<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$Attribute \_ LISTE**</dt> <dt>0x20</dt> </dl>                   | Liste des attributs qui composent le fichier et la référence de fichier de l’enregistrement du fichier MFT dans lequel se trouve chaque attribut.<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$File \_ NOM**</dt> <dt>0x30</dt> </dl>                                  | Nom du fichier, en caractères Unicode.<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$Object \_ ID**</dt> <dt>0x40</dt> </dl>                                  | Identificateur d’objet de 64 octets assigné par le service de suivi des liens.<br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <dt>**$Volume \_ NOM**</dt> <dt>0x60</dt> </dl>                            | Étiquette de volume. Présent dans le fichier $Volume.<br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <dt>**$Volume \_ INFORMATIONS**</dt> <dt>0x70</dt> </dl>       | Informations sur le volume. Présent dans le fichier $Volume.<br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <dt>**$Data**</dt> <dt>0x80</dt> </dl>                                                  | Contenu du fichier.<br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <dt>**$Index \_**</dt> <dt>0X90</dt> racine </dl>                               | Utilisé pour implémenter l’allocation de noms de fichiers pour des répertoires volumineux.<br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <dt>**$Index \_ ALLOCATION**</dt> <dt>0xa0</dt> </dl>             | Utilisé pour implémenter l’allocation de noms de fichiers pour des répertoires volumineux.<br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <dt>**$Bitmap**</dt> <dt>0xB0</dt> </dl>                                            | Index bitmap pour un répertoire volumineux.<br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <dt>**$REPARSE \_ POINT**</dt> <dt>0xC0</dt> </dl>                      | Données du point d’analyse.<br/>                                                                                                          |



 

</dd> <dt>

**RecordLength**
</dt> <dd>

Taille de l’enregistrement d’attribut, en octets. Cette valeur reflète la taille requise pour la variante d’enregistrement et est toujours arrondie à la limite du mot quadruple le plus proche.

</dd> <dt>

**FormCode**
</dt> <dd>

Code du formulaire d’attribut.



| Valeur                                                                                                                                                                                                                            | Signification                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="RESIDENT_FORM"></span><span id="resident_form"></span><dl> <dt>**Résident \_ FORME**</dt> <dt>0x00</dt> </dl>          | La valeur est contenue dans l’enregistrement de fichier et suit immédiatement l’en-tête d’enregistrement d’attribut.<br/> |
| <span id="NONRESIDENT_FORM"></span><span id="nonresident_form"></span><dl> Pas de <dt>**résident \_ FORMAT**</dt> <dt>0x01</dt> </dl> | La valeur est contenue dans d’autres secteurs sur le disque.<br/>                                           |



 

</dd> <dt>

**NameLength**
</dt> <dd>

Taille du nom d’attribut facultatif, en caractères, ou 0 s’il n’y a aucun nom d’attribut. La longueur maximale du nom d’attribut est de 255 caractères.

</dd> <dt>

**NameOffset**
</dt> <dd>

Offset du nom d’attribut à partir du début de l’enregistrement d’attribut, en octets. Si le membre **NameLength** a la valeur 0, ce membre n’est pas défini.

</dd> <dt>

**Indicateurs**
</dt> <dd>

Indicateurs d’attribut.

<dl> <dt>

<span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**Attribut \_ \_ \_ Masque de compression des indicateurs** (0x00FF)
</dt> <dt>

<span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**Attribut \_ INDICATEUR \_ Sparse** (0x8000)
</dt> <dt>

<span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**Attribut \_ INDICATEUR \_ chiffré** (0x4000)
</dt> </dl> </dd> <dt>

**Instance**
</dt> <dd>

Instance unique de cet attribut dans l’enregistrement de fichier.

</dd> <dt>

**Forme**
</dt> <dd>

Si le membre **FormCode** est \_ un formulaire résident, l’Union est une structure **résidente** . Si **FormCode** n’est pas \_ une forme résidente, l’Union est une structure non **résidente** .

<dl> <dt>

**Ceux**
</dt> <dd> <dl> <dt>

**ValueLength**
</dt> <dd>

Taille de la valeur de l’attribut, en octets.

</dd> <dt>

**ValueOffset**
</dt> <dd>

Offset de la valeur à partir du début de l’enregistrement d’attribut, en octets.

</dd> <dt>

**Reserved**
</dt> <dd>

Réservé.

</dd> </dl> </dd> <dt>

**Pas de résident**
</dt> <dd> <dl> <dt>

**LowestVcn**
</dt> <dd>

Numéro de cluster virtuel le plus bas (VCN) couvert par cet enregistrement d’attribut.

</dd> <dt>

**HighestVcn**
</dt> <dd>

Le VCN le plus élevé couvert par cet enregistrement d’attribut.

</dd> <dt>

**MappingPairsOffset**
</dt> <dd>

Offset du tableau de paires de mappage à partir du début de l’enregistrement d’attribut, en octets. Pour plus d'informations, consultez la section Notes.

</dd> <dt>

**Reserved**
</dt> <dd>

Réservé.

</dd> <dt>

**AllocatedLength**
</dt> <dd>

Taille allouée du fichier, en octets. Cette valeur est un multiple pair de la taille du cluster. Ce membre n’est pas valide si le membre **LowestVcn** est différent de zéro.

</dd> <dt>

**FileSize**
</dt> <dd>

Taille de fichier (octet le plus élevé pouvant être lu plus 1), en octets. Ce membre n’est pas valide si **LowestVcn** est différent de zéro.

</dd> <dt>

**ValidDataLength**
</dt> <dd>

Longueur de données valide (plus grand octet initialisé plus 1), en octets. Cette valeur est arrondie à la limite de cluster la plus proche. Ce membre n’est pas valide si **LowestVcn** est différent de zéro.

</dd> <dt>

**TotalAllocated**
</dt> <dd>

Total alloué pour le fichier (la somme des clusters alloués).

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Notez qu’il n’y a aucun fichier d’en-tête associé pour cette structure.

Cette définition de structure est valide uniquement pour la version majeure de la version 3 et la version mineure 0 ou 1, comme indiqué par [**FSCTL \_ obtenir les \_ \_ \_ données du volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

Les enregistrements d’attributs sont toujours alignés sur une limite de mot quadruple.

Si l’attribut est non résident, l’en-tête d’enregistrement d’attribut contient une liste d’informations de récupération qui fournit un mappage entre VCN et le numéro de cluster logique (LCN) de l’attribut. Si les informations de récupération ne tiennent pas dans le segment de fichier de base, elles peuvent être stockées dans un segment d’enregistrement de fichier externe. S’il n’est toujours pas contenu dans un segment d’enregistrement de fichier externe, la liste d’attributs contient plusieurs entrées pour un attribut qui nécessite des informations de récupération supplémentaires.

Le tableau de paires de mappage est stocké sous forme compressée et suppose que les informations sont décompressées et mises en cache par le système. Il se compose d’une série de paires NextVcn/CurrentLcn. Par exemple, si un fichier a une seule exécution de 8 clusters à partir de LCN 128 et que le fichier commence à LowestVcn 0, le tableau de paires de mappage n’a qu’une seule entrée, qui est NextVcn = 8 et CurrentLcn = 128. Le tableau est un flux d’octets qui stocke les modifications apportées aux variables de travail lors du traitement séquentiel. Le flux d’octets doit être interprété comme un flux de triples terminé par zéro, comme suit :

nombre d’octets = *v* + (*l* \* 16)

où *v* est le nombre d’octets VCN de poids faible modifié et *l* est le nombre d’octets LCN de poids faible modifiés.

L’algorithme de décompression est le suivant :

1.  Initialisez NextVcn sur `Attribute->LowestVcn` et CurrentLcn sur 0.
2.  Initialisez le pointeur de flux d’octets vers `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset` .
3.  Définissez CurrentVcn sur NextVcn.
4.  Lit l’octet suivant à partir du flux. Si la valeur est 0, arrêter ; Sinon, extrayez *v* et *l* comme décrit précédemment.
5.  Interpréter les octets *v* suivants comme une quantité signée, en commençant par l’octet de poids faible. Décompressez-le de façon à ce qu’il soit étendu à 64 bits et ajoutez-le à NextVcn.
6.  Interpréter les octets *suivants comme* une quantité signée, en commençant par l’octet de poids faible. Décompressez-le de façon à ce qu’il soit étendu à 64 bits et ajoutez-le à CurrentLcn. Si cette valeur produit un CurrentLcn de 0, les VCNs de CurrentVcn à NextVcn – 1 ne sont pas alloués.
7.  Mettez à jour les informations de mappage mises en cache à partir de CurrentVcn, NextVcn et CurrentLcn.
8.  Passez à l’étape 3.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Table de fichiers maîtres](master-file-table.md)
</dt> </dl>

 

 
