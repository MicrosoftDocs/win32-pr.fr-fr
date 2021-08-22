---
description: Représente le segment d’enregistrement de fichier. Il s’agit de l’en-tête pour chaque segment d’enregistrement de fichier dans la table de fichiers maîtres (MFT).
ms.assetid: 4548ad49-1924-4888-8966-c45f8e453c6f
title: Structure FILE_RECORD_SEGMENT_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_RECORD_SEGMENT_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0c9d7a3653ad965141e691546866f599d8615f5f12feb92fa25c861d7c429b74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260599"
---
# <a name="file_record_segment_header-structure"></a>\_Structure d' \_ \_ en-tête de segment d’enregistrement de fichier

\[Cette structure est valide uniquement pour la version 3 des volumes NTFS ; elles peuvent être modifiées dans les versions ultérieures.\]

Représente le segment d’enregistrement de fichier. Il s’agit de l’en-tête pour chaque segment d’enregistrement de fichier dans la table de fichiers maîtres (MFT).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _FILE_RECORD_SEGMENT_HEADER {
  MULTI_SECTOR_HEADER   MultiSectorHeader;
  ULONGLONG             Reserved1;
  USHORT                SequenceNumber;
  USHORT                Reserved2;
  USHORT                FirstAttributeOffset;
  USHORT                Flags;
  ULONG                 Reserved3[2];
  FILE_REFERENCE        BaseFileRecordSegment;
  USHORT                Reserved4;
  UPDATE_SEQUENCE_ARRAY UpdateSequenceArray;
} FILE_RECORD_SEGMENT_HEADER, *PFILE_RECORD_SEGMENT_HEADER;
```



## <a name="members"></a>Membres

<dl> <dt>

**MultiSectorHeader**
</dt> <dd>

En-tête multisecteur défini par le gestionnaire de cache. La structure d' [**\_ \_ en-tête multisecteur**](multi-sector-header.md) contient toujours la signature « fichier » et une description de l’emplacement et de la taille du tableau de séquences de mise à jour.

</dd> <dt>

**Reserved1**
</dt> <dd>

Réservé.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Numéro séquentiel. Cette valeur est incrémentée chaque fois qu’un segment d’enregistrement de fichier est libéré ; elle est égale à 0 si le segment n’est pas utilisé. Le **champ de** champ d’une référence de fichier doit correspondre au contenu de ce champ ; Si elles ne correspondent pas, la référence de fichier est incorrecte et probablement obsolète.

</dd> <dt>

**Réservé 2**
</dt> <dd>

Réservé.

</dd> <dt>

**FirstAttributeOffset**
</dt> <dd>

Décalage du premier enregistrement d’attribut, en octets.

</dd> <dt>

**Indicateurs**
</dt> <dd>

Indicateurs de fichier.

<dl> <dt>

<span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**Fichier \_ \_Segment \_ d’enregistrement en cours d' \_ utilisation** (0x0001)
</dt> <dt>

<span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**Fichier \_ INDEX de nom de fichier \_ \_ \_ présent** (0x0002)
</dt> </dl> </dd> <dt>

**Reserved3**
</dt> <dd>

Réservé.

</dd> <dt>

**BaseFileRecordSegment**
</dt> <dd>

Référence de fichier au segment d’enregistrement de fichier de base pour ce fichier. S’il s’agit de l’enregistrement de fichier de base, la valeur est 0. Consultez [**\_ \_ référence de segment MFT**](mft-segment-reference.md).

</dd> <dt>

**Reserved4**
</dt> <dd>

Réservé.

</dd> <dt>

**UpdateSequenceArray**
</dt> <dd>

Tableau de séquence de mise à jour pour protéger les transferts multisecteur du segment d’enregistrement de fichier.

</dd> </dl>

## <a name="remarks"></a>Remarques

Notez qu’il n’y a aucun fichier d’en-tête associé pour cette structure.

Cette définition de structure est valide uniquement pour la version majeure de la version 3 et la version mineure 0 ou 1, comme indiqué par [**FSCTL \_ obtenir les \_ \_ \_ données du volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Table de fichiers maîtres](master-file-table.md)
</dt> </dl>

 

 
