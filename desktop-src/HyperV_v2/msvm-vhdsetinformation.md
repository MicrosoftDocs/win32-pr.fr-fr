---
description: Fournit des informations sur un fichier de définition de disque dur virtuel.
ms.assetid: a975c131-d3f3-4be3-bc69-e277e3ce4d28
title: Classe Msvm_VHDSetInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSetInformation
- Msvm_VHDSetInformation.Path
- Msvm_VHDSetInformation.SnapshotIdList
- Msvm_VHDSetInformation.AllPaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8cef737c02629ac0a1a026a459adf6eb7060e0dbdf8c0f9ecb20c66fce1259e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789429"
---
# <a name="msvm_vhdsetinformation-class"></a>MSVM \_ VHDSetInformation, classe

Fournit des informations sur un fichier de définition de disque dur virtuel.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[AMENDMENT]
class Msvm_VHDSetInformation
{
  string Path;
  string SnapshotIdList[];
  string AllPaths[];
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ VHDSetInformation** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ VHDSetInformation** possède les propriétés suivantes.

<dl> <dt>

**AllPaths**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Liste de tous les fichiers contenus dans le fichier de définition de disque dur virtuel, y compris les fichiers non référencés et les parents du disque dur virtuel racine. Tous les fichiers répertoriés après le disque dur virtuel racine ne sont pas gérés par ce fichier de définition de VHD. Ce champ peut être vide si ces informations ne sont pas spécifiquement demandées.

</dd> <dt>

**Chemin d’accès**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chemin d’accès du fichier de définition de disque dur virtuel.

</dd> <dt>

**SnapshotIdList**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Liste de GUID représentant tous les instantanés contenus dans ce fichier de définition de disque dur virtuel.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




