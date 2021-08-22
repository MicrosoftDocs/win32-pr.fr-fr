---
description: Représente une entrée dans la liste d’attributs.
ms.assetid: daa0c97d-2ebe-4e14-b1f8-e4be3075b13e
title: Structure ATTRIBUTE_LIST_ENTRY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_LIST_ENTRY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0c0154de52dbefa6d29278ca05e924db6f6c1d84b124fe21b3092e728a0d07fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956138"
---
# <a name="attribute_list_entry-structure"></a>Structure d’entrée d’une liste d’attributs \_ \_

\[Cette structure est valide uniquement pour la version 3 des volumes NTFS ; elles peuvent être modifiées dans les versions ultérieures.\]

Représente une entrée dans la liste d’attributs.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _ATTRIBUTE_LIST_ENTRY {
  ATTRIBUTE_TYPE_CODE   AttributeTypeCode;
  USHORT                RecordLength;
  UCHAR                 AttributeNameLength;
  UCHAR                 AttributeNameOffset;
  VCN                   LowestVcn;
  MFT_SEGMENT_REFERENCE SegmentReference;
  USHORT                Reserved;
  WCHAR                 AttributeName[1];
} ATTRIBUTE_LIST_ENTRY, *PATTRIBUTE_LIST_ENTRY;
```



## <a name="members"></a>Membres

<dl> <dt>

**AttributeTypeCode**
</dt> <dd>

Code du type d’attribut.



| Valeur                                                                                                                                                                                                                                           | Signification                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$Standard \_ INFORMATION**</dt> <dt>0x10</dt> </dl> | Les attributs de fichier (par exemple, lecture seule et Archive), les horodatages (tels que la création et la dernière modification de fichier) et le nombre de liens physiques.<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$Attribute \_ LISTE**</dt> <dt>0x20</dt> </dl>                   | Liste des attributs qui composent le fichier et la référence de fichier de l’enregistrement du fichier MFT dans lequel se trouve chaque attribut.<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$File \_ NOM**</dt> <dt>0x30</dt> </dl>                                  | Nom du fichier, en caractères Unicode.<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$Object \_ ID**</dt> <dt>0x40</dt> </dl>                                  | Identificateur d’objet de 16 octets assigné par le service de suivi des liens.<br/>                                                              |
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

Taille de cette structure, plus la mémoire tampon de nom facultative, en octets.

</dd> <dt>

**AttributeNameLength**
</dt> <dd>

Taille du nom d’attribut facultatif, en caractères. Si un nom existe, cette valeur est différente de zéro et la structure est immédiatement suivie d’une chaîne Unicode du nombre spécifié de caractères.

</dd> <dt>

**AttributeNameOffset**
</dt> <dd>

Réservé.

</dd> <dt>

**LowestVcn**
</dt> <dd>

Numéro de cluster virtuel (VCN) le plus bas pour cet attribut. Ce membre est égal à zéro, sauf si l’attribut requiert plusieurs segments d’enregistrement de fichier et si cette entrée est une référence à un segment autre que le premier. Dans ce cas, cette valeur est le VCN le plus bas qui est décrit par le segment référencé.

</dd> <dt>

**SegmentReference**
</dt> <dd>

Segment de table de fichiers maîtres (MFT) dans lequel réside l’attribut. Consultez [**\_ \_ référence de segment MFT**](mft-segment-reference.md).

</dd> <dt>

**Reserved**
</dt> <dd>

Réservé.

</dd> <dt>

**AttributeName**
</dt> <dd>

Début du nom d’attribut facultatif.

</dd> </dl>

## <a name="remarks"></a>Remarques

La liste des attributs est une liste ordonnée de structures d' **\_ \_ entrée de liste d’attributs** alignés sur le mot quadruple. Cette liste est d’abord triée par le code de type d’attribut, puis par le nom d’attribut (le cas échéant). Deux attributs ne peuvent pas avoir le même code de type, le même nom et le VCN le plus bas. Par conséquent, il ne peut y avoir qu’un seul attribut pour chaque code de type sans nom.

Cette définition de structure est valide uniquement pour la version majeure de la version 3 et la version mineure 0 ou 1, comme indiqué par [**FSCTL \_ obtenir les \_ \_ \_ données du volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

Notez qu’il n’y a aucun fichier d’en-tête associé pour cette structure.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Table de fichiers maîtres](master-file-table.md)
</dt> </dl>

 

 
