---
title: Classe Win32_TSVmMetadataAssociation
description: Représente une association entre un Bureau à distance ordinateur virtuel et ses propriétés de métadonnées.
ms.assetid: 374b1a29-78de-45fd-97b3-c5a5b724e66b
ms.tgt_platform: multiple
keywords:
- Win32_TSVmMetadataAssociation de la classe Services Bureau à distance
- Win32_TSVmMetadataAssociation de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataAssociation
- Win32_TSVmMetadataAssociation.TSVm
- Win32_TSVmMetadataAssociation.MetadataItem
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebe3389bb03c9e3f33a2cc3e33450318b68171f7ac35fffeaaa3976cb5ae3a33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419999"
---
# <a name="win32_tsvmmetadataassociation-class"></a>\_Classe TSVmMetadataAssociation Win32

Représente une association entre un Bureau à distance ordinateur virtuel et ses propriétés de métadonnées.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, Association, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataAssociation
{
  Win32_TSVm             REF TSVm;
  Win32_TSVmMetadataItem REF MetadataItem;
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ TSVmMetadataAssociation** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **Win32 \_ TSVmMetadataAssociation** a ces propriétés.

<dl> <dt>

**MetadataItem**
</dt> <dd> <dl> <dt>

Type de données : **[ **Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Instance de la classe [**\_ TSVmMetadataItem Win32**](win32-tsvmmetadataitem.md) qui représente les métadonnées de l’ordinateur virtuel.

</dd> <dt>

**TSVm**
</dt> <dd> <dl> <dt>

Type de données : **[ **Win32 \_ TSVm**](win32-tsvm.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Instance de la classe [**\_ TSVm Win32**](win32-tsvm.md) qui représente l’ordinateur virtuel.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                             |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

