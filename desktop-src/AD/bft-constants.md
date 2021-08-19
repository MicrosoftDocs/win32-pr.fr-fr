---
title: Constantes BFT (ntdsbcli. h)
description: Les constantes BFT sont utilisées comme indicateurs binaires pour identifier les différents types de fichiers dans une sauvegarde Active Directory Domain Services.
ms.assetid: 3658a657-d9e3-4fbf-9120-4b0205b81a36
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- BFT_LOG_DIRECTORY
- BFT_DATABASE_DIRECTORY
- BFT_DIRECTORY
- BFT_LOG
- BFT_LOG_DIR
- BFT_CHECKPOINT_DIR
- BFT_NTDS_DATABASE
- BFT_PATCH_FILE
- BFT_UNKNOWN
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b5e9275e01b8c33d308b55b2638d4eaf186b8f5265834acc27acd2f146f0d09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024048"
---
# <a name="bft-constants"></a>Constantes BFT

Les constantes BFT sont utilisées comme indicateurs binaires pour identifier les différents types de fichiers dans une sauvegarde Active Directory Domain Services.

<dl> <dt>

<span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**\_répertoire du journal BFT \_**
</dt> <dd> <dl> <dt>

0x20
</dt> <dt>



Le fichier appartient au répertoire des journaux.


</dt> </dl> </dd> <dt>

<span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**\_Répertoire de base de données BFT \_**
</dt> <dd> <dl> <dt>

0x40
</dt> <dt>



Le fichier appartient au répertoire de la base de données.


</dt> </dl> </dd> <dt>

<span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**\_répertoire BFT**
</dt> <dd> <dl> <dt>

0x80
</dt> <dt>



Le chemin d’accès spécifié est un répertoire et non un nom de fichier.


</dt> </dl> </dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>**\_Journal BFT**
</dt> <dd> <dl> <dt>

0x21
</dt> <dt>



Spécifie un fichier journal qui appartient au répertoire des journaux.


</dt> </dl> </dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**\_répertoire du journal BFT \_**
</dt> <dd> <dl> <dt>

0x22
</dt> <dt>



Le fichier est le chemin d’accès du répertoire des journaux.


</dt> </dl> </dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT \_ Répertoire de point de contrôle \_**
</dt> <dd> <dl> <dt>

0x23
</dt> <dt>



Le fichier est le chemin d’accès du répertoire de point de contrôle.


</dt> </dl> </dd> <dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_ \_ base de données BFT NTDS**
</dt> <dd> <dl> <dt>

0x44
</dt> <dt>



Le fichier est une base de données de service d’annuaire qui appartient au répertoire de base de données.


</dt> </dl> </dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**\_fichier correctif \_ BFT**
</dt> <dd> <dl> <dt>

0x25
</dt> <dt>



Le fichier est un fichier correctif qui appartient au répertoire des journaux.


</dt> </dl> </dd> <dt>

<span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**BFT \_ inconnu**
</dt> <dd> <dl> <dt>

0x0F
</dt> <dt>



Le fichier ne peut pas être reconnu. Le fichier ne coïncide pas avec les noms de fichiers et les types de fichiers connus.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                        |
| En-tête<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl> |



 

 





